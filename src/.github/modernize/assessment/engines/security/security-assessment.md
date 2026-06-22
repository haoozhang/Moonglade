# Security Assessment Report

**Generated:** 06/22/2026 07:38:11

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 9 |
| CVE Vulnerabilities | 1 |
| CWE Vulnerabilities | 8 |
| Total Rules Assessed | 59 |
| Rules Passed | 51 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 1 |
| optional | 2 |
| potential | 6 |

## CVE Findings (Dependency Vulnerabilities)

### CVE-2025-6965: SQLitePCLRaw.lib.e_sqlite3 has a vulnerable dependency on SQLite
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** Tests/Moonglade.Features.Tests/Moonglade.Features.Tests.csproj:17

[CVE-2025-6965](https://github.com/advisories/GHSA-2m69-gcr7-jv3q): SQLitePCLRaw.lib.e_sqlite3 has a vulnerable dependency on SQLite

Severity: HIGH (CVSS 9.8)

There exists a vulnerability in SQLite versions before 3.50.2 where the number of aggregate terms could exceed the number of columns available. This could lead to a memory corruption issue.

Affected dependencies:
  - SQLitePCLRaw.lib.e_sqlite3:2.1.11 (transitive, pulled by Microsoft.EntityFrameworkCore.Sqlite at Tests/Moonglade.Features.Tests/Moonglade.Features.Tests.csproj:17)

Recommended fix:
  - Upgrade SQLitePCLRaw.lib.e_sqlite3 to a version above 2.1.11 once a patched version is available, or upgrade Microsoft.EntityFrameworkCore.Sqlite to a version that depends on a patched SQLitePCLRaw.

## CWE Findings (Code-Level Vulnerabilities)

### CWE-682: Incorrect Calculation
- **Category:** Code Quality
- **Severity:** potential
- **Story Points:** 5
- **Files:** Moonglade.Web/Handlers/WriteFoafCommand.cs

In WriteFoafCommandHandler.HandleAsync() at line 60, Math.Abs(friend.Url.GetHashCode()) is used to generate a stable friend ID. However, GetHashCode() can return int.MinValue (-2147483648), and Math.Abs(int.MinValue) overflows in C# (returns int.MinValue unchanged, a negative number), producing an incorrect negative-valued ID string '#friend_-2147483648'. This logic error can cause duplicate or malformed FOAF friend IDs.

### CWE-772: Missing Release of Resource after Effective Lifetime
- **Category:** Code Quality
- **Severity:** potential
- **Story Points:** 3
- **Files:** Moonglade.Web/Handlers/WriteFoafCommand.cs

In WriteFoafCommandHandler.HandleAsync() at line 35, a StringWriter is created without a 'using' statement or explicit Dispose() call. The XmlWriter wrapping it is closed via writer.Close() on line 72, but the StringWriter itself (which implements IDisposable) is never explicitly disposed, leaving its resources unreleased until garbage collection.

### CWE-543: Use of Singleton Pattern Without Synchronization in a Multithreaded Context
- **Category:** Concurrency & Synchronization
- **Severity:** potential
- **Story Points:** 5
- **Files:** Moonglade.Web/Handlers/WriteFoafCommand.cs

In WriteFoafCommandHandler (lines 25-27), the static field '_xmlNamespaces' is lazily initialized using the '??=' operator without any synchronization: 'private static Dictionary<string,string> _xmlNamespaces; ... _xmlNamespaces ??= new()'. In a multithreaded ASP.NET Core environment, multiple concurrent requests can simultaneously observe '_xmlNamespaces' as null and each create a new Dictionary instance, violating the singleton guarantee and potentially causing race conditions.

### CWE-667: Improper Locking
- **Category:** Concurrency & Synchronization
- **Severity:** potential
- **Story Points:** 8
- **Files:** Moonglade.BackgroundServices/ScheduledPublishWakeUp.cs

In ScheduledPublishWakeUp (lines 9 and 18), 'lock(this)' is used in both GetWakeToken() and WakeUp() methods. Locking on 'this' (the instance reference) is an improper locking pattern: external code that holds a reference to the same ScheduledPublishWakeUp instance could acquire the same lock, potentially causing deadlocks or unintended blocking. The recommended approach is to use a private dedicated lock object.

### CWE-259: Use of Hard-coded Password
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** Moonglade.Configuration/LocalAccountSettings.cs

In LocalAccountSettings.DefaultValue (line 14), the default admin account is initialized with a hard-coded password hash 'bXHAa7tEsZmCh1pYcHPotNlP0gaYfzIkxKuHoJnHMt0=' with a source code comment explicitly revealing the plaintext password '// admin123'. This hard-coded default credential is committed to source control, making it discoverable by anyone with access to the repository.

### CWE-321: Use of Hard-coded Cryptographic Key
- **Category:** Credentials & Secrets
- **Severity:** potential
- **Story Points:** 5
- **Files:** Moonglade.Web/appsettings.json

In appsettings.json at line 17, the CaptchaSettings SharedKey is hard-coded to 'ShMV26g193e7Lg0nBxmgFRXBMmHDGWhknWul4yXnVbE='. This cryptographic key used for CAPTCHA validation is committed to source control, allowing anyone with repository access to potentially bypass CAPTCHA verification.

### CWE-778: Insufficient Logging
- **Category:** Credentials & Secrets
- **Severity:** potential
- **Story Points:** 3
- **Files:** Moonglade.Web/Controllers/AuthController.cs

The AuthController SignOut endpoint completes the user session without logging the sign-out event. While sign-in events are logged elsewhere in the authentication flow, the lack of a sign-out audit log means that session termination events are not tracked, making it difficult to detect and investigate suspicious session activity or unauthorized access patterns.

### CWE-798: Use of Hard-coded Credentials
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** Moonglade.Web/appsettings.json

In appsettings.json at line 3, the database connection string contains hard-coded SQL Server credentials: 'User Id=sa;******'. The SA (system administrator) account credentials are committed directly in source control, exposing full database access to anyone with repository access.

