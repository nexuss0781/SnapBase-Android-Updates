# SnapBase Android updates

This public repository contains only SnapBase's Android update feed and APK releases. The application source remains in the private [Snap-Base repository](https://github.com/nexuss0781/Snap-Base).

- Latest version feed: [`latest.json`](latest.json)
- APK downloads: [SnapBase releases](https://github.com/nexuss0781/SnapBase-Android-Updates/releases)

SnapBase checks the feed when it opens and from the **Updates** control in the app. The feed always provides a full APK URL and SHA-256 checksum. Newer clients may also use an optional `deltas` array containing BSDIFF40 patches. Each entry identifies the exact base `versionCode` and APK `fromSha256`, along with `patchUrl` and `patchSha256`. The client uses a patch only if the installed APK matches both base fields, verifies the downloaded patch, reconstructs and verifies the complete target APK, and otherwise falls back to the full APK. The full APK remains available for older clients and as a recovery path.

Delta patch creation and signed release builds happen outside GitHub Actions so the update-compatible signing key is never stored in GitHub. Publish the signed full APK and its optional patch assets before updating `latest.json`; Android still requires the user to approve installation in the system installer.
