# 360VFX Updates

Auto-update manifest for the 360VFX 2.0 After Effects extension.

The panel fetches `version.json` from the `main` branch and shows an update banner if the version is newer than the installed one.

## Releasing a new version

1. Bump `APP_VERSION` in the extension's `js/main.js`.
2. Build the macOS / Windows installers and upload the zip somewhere reachable (this repo's Releases tab works).
3. Edit `version.json`:
   ```json
   {
     "version": "2.1.0",
     "downloadUrl": "https://github.com/360medaedits/360vfx-updates/releases/download/v2.1.0/360VFX-2.1.0.zip",
     "notes": "What's new in this release"
   }
   ```
4. Commit and push. Within 6 hours every running panel sees the update banner.
