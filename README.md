# Aha desktop releases

This repository hosts official Aha desktop installers and signed update bundles.
Application development and source control are maintained separately.

## Downloads

Use the assets on the [Releases page](https://github.com/atinput/aha-releases/releases)
once the organization pilot is published. No organization release is available yet.
Pilot installers are available for macOS on Apple Silicon.

The organization bootstrap is `0.1.5` (publication pending). Earlier builds need
one manual installation to switch from the retired personal feed. Subsequent
builds check at launch and offer **Update now** or
**Later** before opening the workspace. Finish your work, quit normally and reopen
to install an available update. **Settings → Appearance → Aha updates** also
provides a manual version check. These releases remain a Mac pilot; clean-Mac
rollout checks and Apple Developer ID notarization are pending.

## Update feed

The updater endpoint will be:

```text
https://github.com/atinput/aha-releases/releases/latest/download/latest.json
```

Each release will contain a versioned update archive and its signature. The app
will verify updates with its embedded public key. Signing private keys and user
workspace data are never published here.

This is a release distribution repository. Its automatically generated source
archives contain only this repository's documentation.
