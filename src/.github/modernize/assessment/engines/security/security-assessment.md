# Security Assessment Report

**Generated:** 06/22/2026 10:38:43

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 6 |
| CVE Vulnerabilities | 0 |
| CWE Vulnerabilities | 6 |
| Total Rules Assessed | 59 |
| Rules Passed | 53 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 1 |
| optional | 2 |
| potential | 3 |

## CVE Findings (Dependency Vulnerabilities)

No CVE vulnerabilities found at or above the high severity threshold.

## CWE Findings (Code-Level Vulnerabilities)

### CWE-1057: Data Access Operations Outside of Expected Data Manager Component
- **Category:** Code Quality
- **Severity:** potential
- **Story Points:** 5
- **Files:** `Moonglade.Web/Handlers/SiteMapMapHandler.cs`

In SiteMapMapHandler.cs (lines 16, 30), the Web layer handler directly injects and uses BlogDbContext to perform database queries for posts and pages instead of going through the CQRS command/query pattern (LiteBus mediators) used throughout the rest of the application. This bypasses the established data manager abstraction, creating an inconsistency in data access patterns.

### CWE-821: Incorrect Synchronization
- **Category:** Concurrency & Synchronization
- **Severity:** potential
- **Story Points:** 8
- **Files:** `Moonglade.Features/Post/AddRequestCountCommand.cs`

In AddRequestCountCommandHandler (lines 57-60), after releasing the SemaphoreSlim lock via postLock.Release(), the code checks postLock.CurrentCount == 1 before removing the entry from the static ConcurrentDictionary _locks. There is a TOCTOU race condition: between Release() and the count check, another thread can call GetOrAdd() to retrieve the same semaphore and call WaitAsync() (reducing CurrentCount to 0). If a third thread then arrives after the first thread removes the entry, it creates a new SemaphoreSlim, allowing two threads to concurrently update the same PostId's request count despite the intended exclusive-access design.

### CWE-259: Use of Hard-coded Password
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** `Moonglade.Web/appsettings.json`

In appsettings.json (line 3), the default database connection string contains a hard-coded SQL Server password: '******'. This credential is committed to source control and could be used to authenticate to the SQL Server database if the same credentials are used in a deployed environment.

### CWE-321: Use of Hard-coded Cryptographic Key
- **Category:** Credentials & Secrets
- **Severity:** potential
- **Story Points:** 5
- **Files:** `Moonglade.Web/appsettings.json`

In appsettings.json (line 17), a cryptographic key is hard-coded for the captcha feature: 'SharedKey': 'ShMV26g193e7Lg0nBxmgFRXBMmHDGWhknWul4yXnVbE='. This base64-encoded key is committed to source control and used for HMAC signing of captcha tokens. Anyone with access to the repository can use this key to forge captcha tokens.

### CWE-798: Use of Hard-coded Credentials
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** `Moonglade.Web/appsettings.json`

In appsettings.json (line 3), the default ConnectionStrings section contains hard-coded SQL Server credentials including username ('User Id=sa') and password ('******') committed to the repository. Additionally, the CaptchaSettings section (line 17) contains a hard-coded cryptographic SharedKey. These hard-coded credentials in the default configuration file pose a security risk if deployed without modification.

### CWE-434: Unrestricted Upload of File with Dangerous Type
- **Category:** File & Path Security
- **Severity:** mandatory
- **Story Points:** 8
- **Files:** `Moonglade.Web/Controllers/ImageController.cs`

In ImageController.cs (line 80), the upload handler accepts '.svg' as a valid file extension alongside image types. SVG files can contain embedded JavaScript (<script> tags, event handlers, external resource references) and are served with 'image/svg+xml' content type (ImageInfo.cs:10-11), which browsers render as HTML. No sanitization or content inspection of SVG file content is performed before storage or retrieval. This allows a malicious authenticated user to upload a crafted SVG that executes scripts in the context of the blog's origin when another user views the image URL.

