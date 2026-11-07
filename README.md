# Aha desktop releases

This repository hosts official Aha desktop installers and signed update bundles.
Application development and source control are maintained separately.

## Downloads

Use the assets on the [Releases page](https://github.com/atinput/aha-releases/releases).
Pilot installers are available for macOS on Apple Silicon.
Use the latest release marked **Latest**; earlier pilot releases are superseded.

The organization feed was introduced in `0.1.5`. Install the latest DMG manually
once when upgrading from `0.1.4` or earlier to switch from the retired personal feed. Subsequent
builds check at launch and offer **Update now** or
**Later** before opening the workspace. Finish your work, quit normally and reopen
to install an available update. **Settings → Appearance → Aha updates** also
provides a manual version check. These releases remain a Mac pilot; clean-Mac
rollout checks and Apple Developer ID notarization are pending.

## Update feed

The updater endpoint is:

```text
https://github.com/atinput/aha-releases/releases/latest/download/latest.json
```

Each release contains a versioned update archive and its signature. The app
verifies updates with its embedded public key. Signing private keys and user
workspace data are never published here.

This is a release distribution repository. Its automatically generated source
archives contain only this repository's documentation.
