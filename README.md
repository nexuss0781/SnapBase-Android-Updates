# SnapBase Android updates

This public repository contains only SnapBase's Android update feed and APK releases. The application source remains in the private [Snap-Base repository](https://github.com/nexuss0781/Snap-Base).

- Latest version feed: [`latest.json`](latest.json)
- APK downloads: [SnapBase releases](https://github.com/nexuss0781/SnapBase-Android-Updates/releases)

SnapBase checks the feed when it opens and from the **Updates** control in the app. Before installation, the app verifies the published SHA-256 checksum and then hands the APK to Android's system installer. Android requires the user to approve sideload installation.
