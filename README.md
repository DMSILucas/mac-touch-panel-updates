# Mac Touch Panel — Updates

This public repository hosts the GitHub Releases and update feed for **Mac Touch Panel**, a macOS touchscreen shortcut/control panel.

## Live update feed

**Status: Active** — latest published release: **v1.3.1**.

Feed URL for **Mac Touch Panel → Updater Settings…**:

```text
https://raw.githubusercontent.com/DMSILucas/mac-touch-panel-updates/main/appcast.json
```

Published releases: https://github.com/DMSILucas/mac-touch-panel-updates/releases

The installed app reads the JSON feed, compares the available version with the installed version, displays release notes when an update is newer, and opens its DMG download URL in the default browser. It does **not** install updates without user action.

## How to publish future releases

1. Build and test the new version on macOS with `Build Mac App.command`.
2. Create a GitHub Release tagged `vX.Y.Z` and attach the matching `MacTouchPanel-X.Y.Z.dmg`.
3. Publish the release and confirm its asset appears on GitHub.
4. Update `appcast.json` using the real release asset's `browser_download_url`, version, notes, and publication date.
5. Test **Check for Updates…** on the installed app.

Only publish a feed entry after the matching DMG is uploaded successfully. Keep this repository public so the app can read its feed without GitHub authentication.

## Privacy and distribution

Do not commit personal `configuration.json` backups, credentials, private documents, or browser sign-in data. Public GitHub Releases can be downloaded by anyone. Locally signed builds are not Apple-notarized and may show macOS security prompts on other Macs.
