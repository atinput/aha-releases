# Aha desktop releases

This repository hosts official Aha desktop installers, signed update bundles, and the Aha Web Clipper Chrome extension.
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

## Chrome extension — Aha Web Clipper

[Download Aha Web Clipper v0.3.0](https://github.com/atinput/aha-releases/releases/download/v0.1.8/Aha-Web-Clipper-0.3.0.zip)
to save web pages, selected passages, and PDF documents into Aha.

1. Download and extract the ZIP. Keep the extracted folder somewhere permanent.
2. In Chrome 123 or newer, open `chrome://extensions` and enable **Developer mode**.
3. Click **Load unpacked** and select the extracted `Aha-Web-Clipper` folder containing `manifest.json`.
4. Open your Aha workspace in Chrome, then choose **Settings → Chrome extension → Connect Chrome extension**. Click **Connect Chrome extension** on the setup page.
5. Pin **Aha Web Clipper** in Chrome's extensions menu. Open a page, click the clipper, and save it to Aha.

Aha must be running and reachable from Chrome. You can also connect from the
clipper's **Connection → Connect to Aha** menu by entering your Aha web server URL.
The default is `http://localhost:3000`; use your actual server address if different.
Remote servers require HTTPS. The extension does not start an Aha server.

This is a manual installation, not a Chrome Web Store listing. For later updates,
replace the files in the same extracted folder, click **Reload** on
`chrome://extensions`, and refresh open pages. The ZIP includes installation notes
and the bundled reader's license.

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
