# Moonglade.ActivityLog

## Summary

| Metric | Value |
|--------|-------|
| Total Issues | 17 |
| Mandatory Blockers | 1 |
| Potential Issues | 10 |

## Component Information

| Property | Value |
|----------|-------|
| Language | C# |
| Frameworks | net10.0 |
| Build tools | MSBuild |

## Cloud Readiness Issues

| Issue Name | Criticality | Story Points | Occurrences |
|------------|-------------|--------------|-------------|
| Local or network IO operations detected | Potential | 3 | [30](#Local_or_network_IO_operations_detected) |
| Local application configuration detected | Potential | 1 | [17](#Local_application_configuration_detected) |
| Hardcoded URLs detected | Potential | 1 | [13](#Hardcoded_URLs_detected) |
| Access to external resources via HTTP is detected | Potential | 3 | [8](#Access_to_external_resources_via_HTTP_is_detected) |
| Local OS environment access detected | Potential | 1 | [4](#Local_OS_environment_access_detected) |
| Connection string is detected | Potential | 3 | [2](#Connection_string_is_detected) |
| Environment variables dependency detected | Potential | 3 | [1](#Environment_variables_dependency_detected) |
| Hardcoded sensitive data detected | Optional | 3 | [5](#Hardcoded_sensitive_data_detected) |
| Synchronous API usage detected | Optional | 1 | [4](#Synchronous_API_usage_detected) |
| Static content detected | Optional | 3 | [1](#Static_content_detected) |
| MD5/SHA1 usage detected | Optional | 1 | [1](#MD5_SHA1_usage_detected) |

### Issue Details

<details id="Local_or_network_IO_operations_detected">
<summary><b>Local or network IO operations detected</b> — affected files</summary>

- `Moonglade.Data\Exporting\ExportPageDataCommand.cs (line 12)`
- `Moonglade.Data\Exporting\ExportPostDataCommand.cs (line 40)`
- `Moonglade.Data\Exporting\ZippedJsonExporter.cs (line 21)`
- `Moonglade.Data\Exporting\ZippedJsonExporter.cs (line 51)`
- `Moonglade.Data\Exporting\ZippedJsonExporter.cs (line 27)`
- `Moonglade.Data\Exporting\ZippedJsonExporter.cs (line 33)`
- `Moonglade.Data\Exporting\ZippedJsonExporter.cs (line 48)`
- `Moonglade.Data\Exporting\ZippedJsonExporter.cs (line 46)`
- `Moonglade.Data\Exporting\ZippedJsonExporter.cs (line 30)`
- `Moonglade.ImageStorage\Providers\FileSystemImageStorage.cs (line 137)`
- `Moonglade.ImageStorage\Providers\FileSystemImageStorage.cs (line 157)`
- `Moonglade.ImageStorage\Providers\FileSystemImageStorage.cs (line 225)`
- `Moonglade.ImageStorage\Providers\FileSystemImageStorage.cs (line 92)`
- `Moonglade.ImageStorage\Providers\FileSystemImageStorage.cs (line 223)`
- `Moonglade.ImageStorage\Providers\FileSystemImageStorage.cs (line 55)`
- `Moonglade.ImageStorage\Providers\FileSystemImageStorage.cs (line 90)`
- `Moonglade.Setup\IconGenerator.cs (line 48)`
- `Moonglade.Setup\IconGenerator.cs (line 60)`
- `Moonglade.Setup\IconGenerator.cs (line 20)`
- `Moonglade.Setup\IconGenerator.cs (line 38)`
- `Moonglade.Setup\IconGenerator.cs (line 18)`
- `Moonglade.Setup\ScriptHashGenerator.cs (line 48)`
- `Moonglade.Setup\ScriptHashGenerator.cs (line 18)`
- `Moonglade.Setup\SiteIconBuilder.cs (line 116)`
- `Moonglade.Setup\SiteIconBuilder.cs (line 108)`
- `Moonglade.Setup\SiteIconBuilder.cs (line 106)`
- `Moonglade.Setup\SiteIconBuilder.cs (line 66)`
- `Moonglade.Setup\SiteIconBuilder.cs (line 104)`
- `Moonglade.Setup\SiteIconBuilder.cs (line 83)`
- `Moonglade.Setup\SiteIconBuilder.cs (line 72)`

</details>

<details id="Local_application_configuration_detected">
<summary><b>Local application configuration detected</b> — affected files</summary>

- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`

</details>

<details id="Hardcoded_URLs_detected">
<summary><b>Hardcoded URLs detected</b> — affected files</summary>

- `Moonglade.Data\Seed.cs (line 90)`
- `Moonglade.Data\Seed.cs (line 28)`
- `Moonglade.Syndication\GetOpmlQuery.cs (line 11)`
- `Moonglade.Syndication\GetOpmlQuery.cs (line 10)`
- `Moonglade.Web\Configuration\ConfigureExceptionHandler.cs (line 30)`
- `Moonglade.Web\Extensions\ServiceCollectionExtensions.cs (line 232)`
- `Moonglade.Web\Handlers\OpenSearchMapHandler.cs (line 6)`
- `Moonglade.Web\Handlers\SiteMapMapHandler.cs (line 38)`
- `Moonglade.Web\Handlers\WriteFoafCommand.cs (line 29)`
- `Moonglade.Web\Handlers\WriteFoafCommand.cs (line 28)`
- `Moonglade.Web\Handlers\WriteFoafCommand.cs (line 161)`
- `Moonglade.Webmention\WebmentionSender.cs (line 119)`
- `Moonglade.Webmention\WebmentionSender.cs (line 120)`

</details>

<details id="Access_to_external_resources_via_HTTP_is_detected">
<summary><b>Access to external resources via HTTP is detected</b> — affected files</summary>

- `Moonglade.BackgroundServices\GitHubReleaseClient.cs (line 4)`
- `Moonglade.Email.Client\MoongladeEmailClient.cs (line 18)`
- `Moonglade.Email.Client\MoongladeEmailClient.cs (line 28)`
- `Moonglade.Moderation\RemoteModerationService.cs (line 14)`
- `Moonglade.Webmention\MentionSourceInspector.cs (line 10)`
- `Moonglade.Webmention\WebmentionRequestor.cs (line 11)`
- `Moonglade.Webmention\WebmentionRequestor.cs (line 9)`
- `Moonglade.Webmention\WebmentionSender.cs (line 8)`

</details>

<details id="Local_OS_environment_access_detected">
<summary><b>Local OS environment access detected</b> — affected files</summary>

- `Moonglade.ImageStorage\Providers\FileSystemImageStorage.cs (line 34)`
- `Moonglade.Web\Extensions\WebApplicationBuilderExtension.cs (line 38)`
- `Moonglade.Web\Extensions\WebApplicationBuilderExtension.cs (line 40)`
- `Moonglade.Web\Extensions\WebApplicationBuilderExtension.cs (line 41)`

</details>

<details id="Connection_string_is_detected">
<summary><b>Connection string is detected</b> — affected files</summary>

- `Moonglade.Web\appsettings.json`
- `Moonglade.Web\appsettings.json`

</details>

<details id="Environment_variables_dependency_detected">
<summary><b>Environment variables dependency detected</b> — affected files</summary>

- `Moonglade.Web\Properties\launchSettings.json`

</details>

<details id="Hardcoded_sensitive_data_detected">
<summary><b>Hardcoded sensitive data detected</b> — affected files</summary>

- `Moonglade.Web\Controllers\SettingsController.cs (line 202)`
- `Moonglade.Web\Controllers\SettingsController.cs (line 213)`
- `Moonglade.Web\Controllers\SettingsController.cs (line 229)`
- `Moonglade.Web\Controllers\SettingsController.cs (line 218)`
- `Moonglade.Web\Pages\SignIn.cshtml.cs (line 29)`

</details>

<details id="Synchronous_API_usage_detected">
<summary><b>Synchronous API usage detected</b> — affected files</summary>

- `Moonglade.Setup\IconGenerator.cs (line 48)`
- `Moonglade.Setup\IconGenerator.cs (line 60)`
- `Moonglade.Setup\ScriptHashGenerator.cs (line 18)`
- `Moonglade.Setup\SiteIconBuilder.cs (line 83)`

</details>

<details id="Static_content_detected">
<summary><b>Static content detected</b> — affected files</summary>

- `Moonglade.Web\Moonglade.Web.csproj`

</details>

<details id="MD5_SHA1_usage_detected">
<summary><b>MD5/SHA1 usage detected</b> — affected files</summary>

- `Moonglade.Web\Handlers\WriteFoafCommand.cs (line 174)`

</details>

## Security Issues

> **Note:** These issues were generated by AI and may contain inaccuracies or incomplete information. Please review carefully.

| Issue Name | Criticality | Story Points | Files |
|------------|-------------|--------------|-------|
| CWE-434: Unrestricted Upload of File with Dangerous Type | Mandatory | 8 | [1](#CWE-434_Unrestricted_Upload_of_File_with_Dangerous_Type) |
| CWE-821: Incorrect Synchronization | Potential | 8 | [1](#CWE-821_Incorrect_Synchronization) |
| CWE-1057: Data Access Operations Outside of Expected Data Manager Component | Potential | 5 | [1](#CWE-1057_Data_Access_Operations_Outside_of_Expected_Data_Manager_Component) |
| CWE-321: Use of Hard-coded Cryptographic Key | Potential | 5 | [1](#CWE-321_Use_of_Hard-coded_Cryptographic_Key) |
| CWE-259: Use of Hard-coded Password | Optional | 5 | [1](#CWE-259_Use_of_Hard-coded_Password) |
| CWE-798: Use of Hard-coded Credentials | Optional | 5 | [1](#CWE-798_Use_of_Hard-coded_Credentials) |

### Security Issue Details

<details id="CWE-434_Unrestricted_Upload_of_File_with_Dangerous_Type">
<summary><b>CWE-434: Unrestricted Upload of File with Dangerous Type</b> — affected files</summary>

- `Moonglade.Web/Controllers/ImageController.cs`

</details>

<details id="CWE-821_Incorrect_Synchronization">
<summary><b>CWE-821: Incorrect Synchronization</b> — affected files</summary>

- `Moonglade.Features/Post/AddRequestCountCommand.cs`

</details>

<details id="CWE-1057_Data_Access_Operations_Outside_of_Expected_Data_Manager_Component">
<summary><b>CWE-1057: Data Access Operations Outside of Expected Data Manager Component</b> — affected files</summary>

- `Moonglade.Web/Handlers/SiteMapMapHandler.cs`

</details>

<details id="CWE-321_Use_of_Hard-coded_Cryptographic_Key">
<summary><b>CWE-321: Use of Hard-coded Cryptographic Key</b> — affected files</summary>

- `Moonglade.Web/appsettings.json`

</details>

<details id="CWE-259_Use_of_Hard-coded_Password">
<summary><b>CWE-259: Use of Hard-coded Password</b> — affected files</summary>

- `Moonglade.Web/appsettings.json`

</details>

<details id="CWE-798_Use_of_Hard-coded_Credentials">
<summary><b>CWE-798: Use of Hard-coded Credentials</b> — affected files</summary>

- `Moonglade.Web/appsettings.json`

</details>

---

## Codebase Insights

> **Note:** These documents are generated by AI and may contain inaccuracies or incomplete information. Please review carefully.

> **Codebase Insights aren't available yet.**
>
> These documents are generated when assessment runs with **Full analysis** coverage. Re-run the assessment and set `analysisCoverage: full` to enable them.

[Share feedback](https://aka.ms/ghcp-appmod/feedback)
