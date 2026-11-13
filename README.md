# Mac Touch Panel — Updates

This public repository hosts release downloads and the update feed for **Mac Touch Panel**, a macOS touchscreen shortcut/control panel.

## Update feed

The installed app reads the file `appcast.json` on the `main` branch. The public URL will be:

`https://raw.githubusercontent.com/DMSILucas/mac-touch-panel-updates/main/appcast.json`

The feed is published **only after** a real, downloadable GitHub Release asset is available, so users are never directed to a missing installer.

## Release workflow

1. Build and test Mac Touch Panel on macOS and create the DMG using `Build Mac App.command`.
2. Create a GitHub Release named `vX.Y.Z` and attach the matching `MacTouchPanel-X.Y.Z.dmg`.
3. Publish the release.
4. Update `appcast.json` with the version, release notes, and **actual HTTPS download URL** of the DMG.
5. Open Mac Touch Panel → **Check for Updates…** to verify it.

Expected feed format:

```json
{
  "version": "1.3.1",
  "downloadURL": "https://github.com/DMSILucas/mac-touch-panel-updates/releases/download/v1.3.1/MacTouchPanel-1.3.1.dmg",
  "releaseNotes": "Release notes go here."
}
```

**Note:** The JSON above is an example. It is not an active release feed. The URL only works once that exact release asset is published.

## Privacy and distribution

Do not commit personal `configuration.json` backups, access tokens, passwords, private documents, or YouTube sign-in data. Public GitHub Releases are accessible to everyone. Locally signed builds are not Apple-notarized and may show macOS security prompts when installed on another Mac.
