# Moonglade.ActivityLog

## Summary

| Metric | Value |
|--------|-------|
| Total Issues | 22 |
| Mandatory Blockers | 2 |
| Potential Issues | 14 |

## Component Information

| Property | Value |
|----------|-------|
| Language | C# |
| Frameworks | net10.0 |
| Build tools | MSBuild |

## Cloud Readiness Issues

| Issue Name | Criticality | Story Points | Occurrences |
|------------|-------------|--------------|-------------|
| Hardcoded local or network paths detected | Mandatory | 1 | [3](#Hardcoded_local_or_network_paths_detected) |
| Hardcoded URLs detected | Potential | 1 | [336](#Hardcoded_URLs_detected) |
| Local or network IO operations detected | Potential | 3 | [48](#Local_or_network_IO_operations_detected) |
| Access to external resources via HTTP is detected | Potential | 3 | [29](#Access_to_external_resources_via_HTTP_is_detected) |
| Local application configuration detected | Potential | 1 | [17](#Local_application_configuration_detected) |
| Local OS environment access detected | Potential | 1 | [4](#Local_OS_environment_access_detected) |
| Connection string is detected | Potential | 3 | [2](#Connection_string_is_detected) |
| Certificate management dependency detected | Potential | 5 | [1](#Certificate_management_dependency_detected) |
| Environment variables dependency detected | Potential | 3 | [1](#Environment_variables_dependency_detected) |
| Hardcoded sensitive data detected | Optional | 3 | [14](#Hardcoded_sensitive_data_detected) |
| Synchronous API usage detected | Optional | 1 | [5](#Synchronous_API_usage_detected) |
| Static content detected | Optional | 3 | [1](#Static_content_detected) |
| MD5/SHA1 usage detected | Optional | 1 | [1](#MD5_SHA1_usage_detected) |

### Issue Details

<details id="Hardcoded_local_or_network_paths_detected">
<summary><b>Hardcoded local or network paths detected</b> — affected files</summary>

- `Tests\Moonglade.Web.Tests\AssetsControllerTests.cs (line 34)`
- `Tests\Moonglade.Web.Tests\AssetsControllerTests.cs (line 31)`
- `Tests\Moonglade.Web.Tests\ImageControllerTests.cs (line 164)`

</details>

<details id="Hardcoded_URLs_detected">
<summary><b>Hardcoded URLs detected</b> — affected files</summary>

- `Tests\Moonglade.BackgroundServices.Tests\GitHubReleaseClientTests.cs (line 56)`
- `Tests\Moonglade.BackgroundServices.Tests\GitHubReleaseClientTests.cs (line 44)`
- `Tests\Moonglade.BackgroundServices.Tests\GitHubReleaseClientTests.cs (line 32)`
- `Tests\Moonglade.BackgroundServices.Tests\GitHubReleaseClientTests.cs (line 15)`
- `Moonglade.Data\Seed.cs (line 90)`
- `Moonglade.Data\Seed.cs (line 28)`
- `Tests\Moonglade.Email.Client.Tests\CommentReplyNotificationHandlerTests.cs (line 72)`
- `Tests\Moonglade.Email.Client.Tests\CommentReplyNotificationHandlerTests.cs (line 23)`
- `Tests\Moonglade.Email.Client.Tests\CommentReplyNotificationHandlerTests.cs (line 39)`
- `Tests\Moonglade.Email.Client.Tests\CommentReplyNotificationHandlerTests.cs (line 55)`
- `Tests\Moonglade.Email.Client.Tests\MentionNotificationHandlerTests.cs (line 31)`
- `Tests\Moonglade.Email.Client.Tests\MentionNotificationHandlerTests.cs (line 19)`
- `Tests\Moonglade.Email.Client.Tests\MoongladeEmailClientTests.cs (line 32)`
- `Tests\Moonglade.Email.Client.Tests\MoongladeEmailClientTests.cs (line 73)`
- `Tests\Moonglade.Email.Client.Tests\MoongladeEmailClientTests.cs (line 90)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 25)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 245)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 120)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 150)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 184)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 221)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 80)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 81)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 115)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 145)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 179)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 209)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 28)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 51)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 73)`
- `Tests\Moonglade.Moderation.Tests\MoongladeModeratorServiceTests.cs (line 682)`
- `Tests\Moonglade.Moderation.Tests\MoongladeModeratorServiceTests.cs (line 98)`
- `Tests\Moonglade.Moderation.Tests\MoongladeModeratorServiceTests.cs (line 637)`
- `Tests\Moonglade.Moderation.Tests\RemoteModerationServiceTests.cs (line 21)`
- `Moonglade.Syndication\GetOpmlQuery.cs (line 11)`
- `Moonglade.Syndication\GetOpmlQuery.cs (line 10)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 63)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 68)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 174)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 203)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 29)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 41)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 10)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 15)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 144)`
- `Tests\Moonglade.Syndication.Tests\FeedGeneratorTests.cs (line 158)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 81)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 150)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 80)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 149)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 11)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 12)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 13)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 14)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 111)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 112)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 113)`
- `Tests\Moonglade.Syndication.Tests\GetOpmlQueryTests.cs (line 114)`
- `Tests\Moonglade.Syndication.Tests\SyndicationQueryHandlerTests.cs (line 65)`
- `Tests\Moonglade.Syndication.Tests\SyndicationQueryHandlerTests.cs (line 34)`
- `Tests\Moonglade.Syndication.Tests\SyndicationQueryHandlerTests.cs (line 101)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 10)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 11)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 9)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 402)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 437)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 107)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 100)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 26)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 56)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 634)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 70)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 85)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 41)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 86)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 27)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 42)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 71)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 433)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 398)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 311)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 639)`
- `Tests\Moonglade.Utils.Tests\ContentProcessorTests.cs (line 642)`
- `Tests\Moonglade.Utils.Tests\ScriptTagValidatorTests.cs (line 323)`
- `Tests\Moonglade.Utils.Tests\ScriptTagValidatorTests.cs (line 336)`
- `Tests\Moonglade.Utils.Tests\ScriptTagValidatorTests.cs (line 79)`
- `Tests\Moonglade.Utils.Tests\ScriptTagValidatorTests.cs (line 92)`
- `Tests\Moonglade.Utils.Tests\ScriptTagValidatorTests.cs (line 152)`
- `Tests\Moonglade.Utils.Tests\ScriptTagValidatorTests.cs (line 370)`
- `Tests\Moonglade.Utils.Tests\ScriptTagValidatorTests.cs (line 349)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 69)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 145)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 68)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 70)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 144)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 143)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 384)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 31)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 11)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 245)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 245)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 247)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 247)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 13)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 244)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 244)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 346)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 346)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 324)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 325)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 325)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 327)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 342)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 343)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 345)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 394)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 395)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 324)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 326)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 326)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 327)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 342)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 344)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 343)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 344)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 345)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 25)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 26)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 27)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 28)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 29)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 53)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 10)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 52)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 42)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 41)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 43)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 12)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 246)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 246)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 14)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 139)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 105)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 104)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 138)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 444)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 445)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 443)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 305)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 320)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 153)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 378)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 420)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 299)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 427)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 126)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 97)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 419)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 290)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 375)`
- `Tests\Moonglade.Utils.Tests\UrlHelperTests.cs (line 317)`
- `Moonglade.Web\Configuration\ConfigureExceptionHandler.cs (line 30)`
- `Moonglade.Web\Extensions\ServiceCollectionExtensions.cs (line 232)`
- `Moonglade.Web\Handlers\OpenSearchMapHandler.cs (line 6)`
- `Moonglade.Web\Handlers\SiteMapMapHandler.cs (line 38)`
- `Moonglade.Web\Handlers\WriteFoafCommand.cs (line 29)`
- `Moonglade.Web\Handlers\WriteFoafCommand.cs (line 28)`
- `Moonglade.Web\Handlers\WriteFoafCommand.cs (line 161)`
- `Tests\Moonglade.Web.Tests\AuthControllerTests.cs (line 22)`
- `Tests\Moonglade.Web.Tests\ImageControllerTests.cs (line 65)`
- `Tests\Moonglade.Web.Tests\ImageControllerTests.cs (line 57)`
- `Tests\Moonglade.Web.Tests\MentionControllerTests.cs (line 206)`
- `Tests\Moonglade.Web.Tests\MentionControllerTests.cs (line 57)`
- `Tests\Moonglade.Web.Tests\MentionControllerTests.cs (line 58)`
- `Tests\Moonglade.Web.Tests\MentionControllerTests.cs (line 36)`
- `Tests\Moonglade.Web.Tests\MentionControllerTests.cs (line 36)`
- `Tests\Moonglade.Web.Tests\MentionControllerTests.cs (line 52)`
- `Tests\Moonglade.Web.Tests\MentionControllerTests.cs (line 52)`
- `Tests\Moonglade.Web.Tests\MentionControllerTests.cs (line 79)`
- `Tests\Moonglade.Web.Tests\MentionControllerTests.cs (line 79)`
- `Tests\Moonglade.Web.Tests\OpenSearchMapHandlerTests.cs (line 73)`
- `Tests\Moonglade.Web.Tests\OpenSearchMapHandlerTests.cs (line 78)`
- `Tests\Moonglade.Web.Tests\OpenSearchMapHandlerTests.cs (line 44)`
- `Tests\Moonglade.Web.Tests\OpenSearchMapHandlerTests.cs (line 62)`
- `Tests\Moonglade.Web.Tests\PostManagementCommandTests.cs (line 178)`
- `Tests\Moonglade.Web.Tests\SaveAssetToCdnHandlerTests.cs (line 78)`
- `Tests\Moonglade.Web.Tests\SaveAssetToCdnHandlerTests.cs (line 108)`
- `Moonglade.Webmention\WebmentionSender.cs (line 119)`
- `Moonglade.Webmention\WebmentionSender.cs (line 120)`
- `Tests\Moonglade.Webmention.Tests\DeleteMentionsCommandTests.cs (line 23)`
- `Tests\Moonglade.Webmention.Tests\DeleteMentionsCommandTests.cs (line 48)`
- `Tests\Moonglade.Webmention.Tests\DeleteMentionsCommandTests.cs (line 73)`
- `Tests\Moonglade.Webmention.Tests\DeleteMentionsCommandTests.cs (line 100)`
- `Tests\Moonglade.Webmention.Tests\DeleteMentionsCommandTests.cs (line 101)`
- `Tests\Moonglade.Webmention.Tests\DeleteMentionsCommandTests.cs (line 99)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 44)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 35)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 62)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 53)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 26)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 70)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 279)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 170)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 194)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 304)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 121)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 145)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 168)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 192)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 216)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 235)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 260)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 277)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 302)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 326)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 68)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 96)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 122)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 146)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 193)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 217)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 236)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 261)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 278)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 303)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 327)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 69)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 97)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 169)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 328)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 328)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 143)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 143)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 461)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 459)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 460)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 462)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 463)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 363)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 364)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 335)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 263)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 122)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 122)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 83)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 83)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 96)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 96)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 109)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 109)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 70)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 70)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 135)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 135)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 151)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 151)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 166)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 166)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 190)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 190)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 352)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 352)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 214)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 214)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 273)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 273)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 317)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 317)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 435)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 435)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 57)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 44)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 389)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 488)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 170)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 171)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 194)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 195)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 321)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 322)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 439)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 440)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 218)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 219)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 277)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 278)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 394)`
- `Tests\Moonglade.Webmention.Tests\ReceiveWebmentionCommandHandlerTests.cs (line 493)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 86)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 268)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 291)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 314)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 105)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 106)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 135)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 136)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 151)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 152)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 171)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 172)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 204)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 205)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 241)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 242)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 261)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 262)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 284)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 285)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 307)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 308)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 341)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 342)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 44)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 58)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 59)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 81)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 30)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 31)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 252)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 275)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 95)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 162)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 182)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 219)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 70)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 321)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 186)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 69)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSourceRateLimiterTests.cs (line 34)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSourceRateLimiterTests.cs (line 20)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSourceRateLimiterTests.cs (line 33)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSourceRateLimiterTests.cs (line 35)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSourceRateLimiterTests.cs (line 18)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSourceRateLimiterTests.cs (line 48)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSourceRateLimiterTests.cs (line 19)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSourceRateLimiterTests.cs (line 49)`

</details>

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
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 98)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 21)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 60)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 114)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 29)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 55)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 14)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 27)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 42)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 53)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 66)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 80)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 91)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 127)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 125)`
- `Tests\Moonglade.ImageStorage.Tests\Providers\FileSystemImageStorageTests.cs (line 9)`
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
- `Tests\Moonglade.Web.Tests\SearchPageTests.cs (line 266)`
- `Tests\Moonglade.Web.Tests\SearchPageTests.cs (line 262)`

</details>

<details id="Access_to_external_resources_via_HTTP_is_detected">
<summary><b>Access to external resources via HTTP is detected</b> — affected files</summary>

- `Moonglade.BackgroundServices\GitHubReleaseClient.cs (line 4)`
- `Tests\Moonglade.BackgroundServices.Tests\GitHubReleaseClientTests.cs (line 42)`
- `Tests\Moonglade.BackgroundServices.Tests\GitHubReleaseClientTests.cs (line 27)`
- `Tests\Moonglade.BackgroundServices.Tests\GitHubReleaseClientTests.cs (line 10)`
- `Moonglade.Email.Client\MoongladeEmailClient.cs (line 18)`
- `Moonglade.Email.Client\MoongladeEmailClient.cs (line 28)`
- `Tests\Moonglade.Email.Client.Tests\MoongladeEmailClientTests.cs (line 30)`
- `Tests\Moonglade.Email.Client.Tests\MoongladeEmailClientTests.cs (line 48)`
- `Tests\Moonglade.Email.Client.Tests\MoongladeEmailClientTests.cs (line 51)`
- `Tests\Moonglade.Email.Client.Tests\MoongladeEmailClientTests.cs (line 191)`
- `Tests\Moonglade.Email.Client.Tests\MoongladeEmailClientTests.cs (line 219)`
- `Tests\Moonglade.Email.Client.Tests\MoongladeEmailClientTests.cs (line 233)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 120)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 150)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 184)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 221)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 80)`
- `Tests\Moonglade.IndexNow.Client.Tests\IndexNowClientTests.cs (line 81)`
- `Moonglade.Moderation\RemoteModerationService.cs (line 14)`
- `Tests\Moonglade.Moderation.Tests\RemoteModerationServiceTests.cs (line 19)`
- `Tests\Moonglade.Moderation.Tests\RemoteModerationServiceTests.cs (line 12)`
- `Moonglade.Webmention\MentionSourceInspector.cs (line 10)`
- `Moonglade.Webmention\WebmentionRequestor.cs (line 11)`
- `Moonglade.Webmention\WebmentionRequestor.cs (line 9)`
- `Moonglade.Webmention\WebmentionSender.cs (line 8)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 17)`
- `Tests\Moonglade.Webmention.Tests\MentionSourceInspectorTests.cs (line 11)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 19)`
- `Tests\Moonglade.Webmention.Tests\WebmentionSenderTests.cs (line 12)`

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

<details id="Certificate_management_dependency_detected">
<summary><b>Certificate management dependency detected</b> — affected files</summary>

- `Tests\Moonglade.Auth.Tests\Moonglade.Auth.Tests.csproj`

</details>

<details id="Environment_variables_dependency_detected">
<summary><b>Environment variables dependency detected</b> — affected files</summary>

- `Moonglade.Web\Properties\launchSettings.json`

</details>

<details id="Hardcoded_sensitive_data_detected">
<summary><b>Hardcoded sensitive data detected</b> — affected files</summary>

- `Tests\Moonglade.Auth.Tests\UpdateLocalAccountPasswordRequestTests.cs (line 58)`
- `Tests\Moonglade.Auth.Tests\UpdateLocalAccountPasswordRequestTests.cs (line 78)`
- `Tests\Moonglade.Auth.Tests\UpdateLocalAccountPasswordRequestTests.cs (line 20)`
- `Tests\Moonglade.Auth.Tests\UpdateLocalAccountPasswordRequestTests.cs (line 21)`
- `Tests\Moonglade.Auth.Tests\UpdateLocalAccountPasswordRequestTests.cs (line 39)`
- `Tests\Moonglade.Auth.Tests\UpdateLocalAccountPasswordRequestTests.cs (line 40)`
- `Tests\Moonglade.Auth.Tests\ValidateLoginCommandTests.cs (line 24)`
- `Tests\Moonglade.Auth.Tests\ValidateLoginCommandTests.cs (line 46)`
- `Tests\Moonglade.Auth.Tests\ValidateLoginCommandTests.cs (line 80)`
- `Moonglade.Web\Controllers\SettingsController.cs (line 202)`
- `Moonglade.Web\Controllers\SettingsController.cs (line 213)`
- `Moonglade.Web\Controllers\SettingsController.cs (line 229)`
- `Moonglade.Web\Controllers\SettingsController.cs (line 218)`
- `Moonglade.Web\Pages\SignIn.cshtml.cs (line 29)`

</details>

<details id="Synchronous_API_usage_detected">
<summary><b>Synchronous API usage detected</b> — affected files</summary>

- `Tests\Moonglade.ImageStorage.Tests\Providers\AzureBlobImageStorageTests.cs (line 359)`
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
| CVE-2025-6965: SQLitePCLRaw.lib.e_sqlite3 has a vulnerable dependency on SQLite | Mandatory | 1 | [1](#CVE-2025-6965_SQLitePCLRaw_lib_e_sqlite3_has_a_vulnerable_dependency_on_SQLite) |
| CWE-667: Improper Locking | Potential | 8 | [1](#CWE-667_Improper_Locking) |
| CWE-682: Incorrect Calculation | Potential | 5 | [1](#CWE-682_Incorrect_Calculation) |
| CWE-543: Use of Singleton Pattern Without Synchronization in a Multithreaded Context | Potential | 5 | [1](#CWE-543_Use_of_Singleton_Pattern_Without_Synchronization_in_a_Multithreaded_Context) |
| CWE-321: Use of Hard-coded Cryptographic Key | Potential | 5 | [1](#CWE-321_Use_of_Hard-coded_Cryptographic_Key) |
| CWE-772: Missing Release of Resource after Effective Lifetime | Potential | 3 | [1](#CWE-772_Missing_Release_of_Resource_after_Effective_Lifetime) |
| CWE-778: Insufficient Logging | Potential | 3 | [1](#CWE-778_Insufficient_Logging) |
| CWE-259: Use of Hard-coded Password | Optional | 5 | [1](#CWE-259_Use_of_Hard-coded_Password) |
| CWE-798: Use of Hard-coded Credentials | Optional | 5 | [1](#CWE-798_Use_of_Hard-coded_Credentials) |

### Security Issue Details

<details id="CVE-2025-6965_SQLitePCLRaw_lib_e_sqlite3_has_a_vulnerable_dependency_on_SQLite">
<summary><b>CVE-2025-6965: SQLitePCLRaw.lib.e_sqlite3 has a vulnerable dependency on SQLite</b> — affected files</summary>

- `Tests/Moonglade.Features.Tests/Moonglade.Features.Tests.csproj:17`

</details>

<details id="CWE-667_Improper_Locking">
<summary><b>CWE-667: Improper Locking</b> — affected files</summary>

- `Moonglade.BackgroundServices/ScheduledPublishWakeUp.cs`

</details>

<details id="CWE-682_Incorrect_Calculation">
<summary><b>CWE-682: Incorrect Calculation</b> — affected files</summary>

- `Moonglade.Web/Handlers/WriteFoafCommand.cs`

</details>

<details id="CWE-543_Use_of_Singleton_Pattern_Without_Synchronization_in_a_Multithreaded_Context">
<summary><b>CWE-543: Use of Singleton Pattern Without Synchronization in a Multithreaded Context</b> — affected files</summary>

- `Moonglade.Web/Handlers/WriteFoafCommand.cs`

</details>

<details id="CWE-321_Use_of_Hard-coded_Cryptographic_Key">
<summary><b>CWE-321: Use of Hard-coded Cryptographic Key</b> — affected files</summary>

- `Moonglade.Web/appsettings.json`

</details>

<details id="CWE-772_Missing_Release_of_Resource_after_Effective_Lifetime">
<summary><b>CWE-772: Missing Release of Resource after Effective Lifetime</b> — affected files</summary>

- `Moonglade.Web/Handlers/WriteFoafCommand.cs`

</details>

<details id="CWE-778_Insufficient_Logging">
<summary><b>CWE-778: Insufficient Logging</b> — affected files</summary>

- `Moonglade.Web/Controllers/AuthController.cs`

</details>

<details id="CWE-259_Use_of_Hard-coded_Password">
<summary><b>CWE-259: Use of Hard-coded Password</b> — affected files</summary>

- `Moonglade.Configuration/LocalAccountSettings.cs`

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
