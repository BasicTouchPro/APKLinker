<div align="center">

<img src="assets/apklinker-logo.png" alt="APKLinker app icon" width="160" />

# APKLinker

### Extract. Upload. Share.

A lightweight Android utility by **Basic Touch Pro** for inspecting installed apps, extracting APK packages, uploading files to Gofile, and sharing download links with QR codes.

[![Android](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)](#)
[![Kotlin](https://img.shields.io/badge/Language-Kotlin-7F52FF?logo=kotlin&logoColor=white)](#)
[![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4?logo=jetpackcompose&logoColor=white)](#)
[![Developer](https://img.shields.io/badge/Developer-Basic%20Touch%20Pro-1688F0)](https://www.youtube.com/@BasicTouchPro)

**[Download latest APK](../../releases/latest)** · **[All Releases](../../releases)** · **[Report an Issue](../../issues)**

</div>

---

## About

APKLinker helps Android users inspect applications on their device, extract APK files where Android permits, and share those files through Gofile.

1. Find an installed app or select an APK file.
2. Review its available information.
3. Extract or prepare the APK package.
4. Upload it to Gofile.
5. Copy or share the resulting download page and its QR code.

> **Project status:** Check the [Releases](../../releases) page for the latest build. Features and device compatibility may vary by release.

## Features

- **Installed Apps** — Browse user-installed applications.
- **System Apps** — Browse preinstalled/system applications where Android package visibility permits.
- **APK Files** — Select APK-related files using Android's Storage Access Framework.
- **App Information** — View available app name, package name, version, and file size.
- **Package Name Copy** — Copy an application's package identifier.
- **APK Extraction** — Export available APK files without modifying their contents or signatures.
- **Split APK Support** — Prepare base and split APK files together in a compatible archive when an app uses split packages.
- **Gofile Upload** — Upload supported files using the Gofile API.
- **Shareable Result** — Copy/share the returned download page and generate a QR code from that URL.
- **Light and Dark Themes** — Choose the appearance from the navigation drawer.
- **App Search** — Search installed apps, system apps, and accessible APK files.
- **Basic Touch Pro Social Links** — Find the project's social profiles in the app.

Feature availability depends on the installed build, Android version, file access permissions, Gofile service limits, and API availability.

## Screenshots

Screenshots will be added here as the app UI is finalized.

## Download

Get the latest available APK from GitHub Releases:

- **Latest release:** [Download APK](../../releases/latest)
- **All versions:** [View release history](../../releases)

### Install

1. Open the latest release.
2. Download the APK asset attached to that release.
3. Open the downloaded APK on your Android device.
4. If Android asks, allow installation from that source.
5. Review the requested permissions and install.

Only install APKs from this repository's official Releases page. Android may display a warning when installing apps outside Google Play.

## How to Use

1. Open APKLinker.
2. Choose **Installed Apps**, **System Apps**, or **APK Files**.
3. Search for and select an app or file.
4. Review the available information.
5. Tap **Extract APK** or the relevant upload action.
6. Wait for the upload to finish.
7. Copy or share the Gofile download page, or share its QR code.

## Technology

The Android project is intended to use:

- Kotlin
- Jetpack Compose
- Material 3
- MVVM architecture
- Kotlin Coroutines
- Android PackageManager
- Storage Access Framework (SAF)
- WorkManager where background upload execution is supported
- Android DataStore for theme preferences
- Android Keystore-backed protection for locally stored sensitive values where applicable
- Gofile API for file uploads
- QR code generation for sharing the returned download page

The exact dependencies and minimum Android version should be confirmed in the source code for each release.

## Important Notes

### APK and split APK files

Some Android applications consist of multiple APK components (for example, a base APK and configuration splits). Exporting only the base APK may not be sufficient to reinstall such an app. APKLinker may package the available components together; installation can require a compatible split-APK installer.

APKLinker does not remove or bypass application licensing, signature verification, DRM, or other platform protections.

### Permission and file access

Android restricts access to installed-package information and shared storage. APKLinker requests only the access needed for its supported features. Available results can differ across Android versions and device manufacturers.

### Gofile and upload availability

Uploads depend on Gofile's current API, account/guest limits, file-size restrictions, availability, and terms. Gofile may change its API or service policies. A generated sharing page is controlled by Gofile, not by this repository.

### API credentials and security

**Never commit API tokens, passwords, signing keys, keystores, or private configuration files to this public repository.**

Client-side encryption and code obfuscation cannot make a secret embedded in an Android APK impossible to extract. If a private Gofile account token is used directly by the app, it may be recoverable through reverse engineering. Prefer a documented guest-upload flow or a secure server-side design when protecting a private account credential is required.

If a credential has been exposed, revoke or rotate it through the provider.

## Privacy

APKLinker processes app/file information to provide its extraction and upload features. When a user initiates an upload, the selected file is sent to Gofile (or the configured upload service) and may become accessible through the generated sharing page according to that provider's settings and policies.

Do not upload or share applications unless you own them or have permission to redistribute them. Review the in-app Privacy Policy and the provider's current terms before using the app.

## Legal and Responsible Use

APKLinker is a file utility. Users are responsible for ensuring that they have the rights and authorization to extract, upload, and redistribute any APK or other file they share. Do not use the app to distribute malware, modified apps without authorization, copyrighted software unlawfully, or files that violate applicable laws or service terms.

## Developer & Social Media

Follow **Basic Touch Pro**:

| Platform | Link |
|---|---|
| YouTube | [@BasicTouchPro](https://www.youtube.com/@BasicTouchPro) |
| Facebook | [BasicTouchPro](https://www.facebook.com/BasicTouchPro) |
| Telegram | [@BasicTouchPro](https://t.me/BasicTouchPro) |
| GitHub | [BasicTouchPro](https://github.com/BasicTouchPro) |

## Support

- **Bug reports:** [Open an issue](../../issues/new)
- **Feature requests:** [Open an issue](../../issues/new)
- **Releases:** [View releases](../../releases)

When reporting a bug, include your APKLinker version, Android version, device model, and steps to reproduce the issue. Never include API tokens, passwords, or private files in an issue.

## License

No open-source license has been specified yet. Unless a license file is added to this repository, all rights are reserved by the copyright holder. Do not assume that the source code or app may be reused, modified, or redistributed.

---

<div align="center">

**Made by Basic Touch Pro**

[YouTube](https://www.youtube.com/@BasicTouchPro) ·
[Facebook](https://www.facebook.com/BasicTouchPro) ·
[Telegram](https://t.me/BasicTouchPro) ·
[GitHub](https://github.com/BasicTouchPro)

</div>
