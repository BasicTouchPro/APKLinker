<div align="center">

<img src="/apklinker-logo.png" alt="APKLinker app icon" width="160" />

# APKLinker

### Extract. Upload. Share.

A lightweight Android utility by **Basic Touch Pro** for inspecting installed apps, extracting APK packages, uploading files to Gofile, and sharing download links with QR codes.

[![Download APK](https://img.shields.io/badge/⬇%20Download-Latest%20APK-1688F0?style=for-the-badge&logo=android&logoColor=white)](https://github.com/BasicTouchPro/APKLinker/releases/download/v1.0.0/APKLinker-v1.0.0-release.apk)

[![All Releases](https://img.shields.io/badge/All-Releases-24292F?style=for-the-badge&logo=github&logoColor=white)](https://github.com/BasicTouchPro/APKLinker/releases)

[![Android](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)](#)
[![Kotlin](https://img.shields.io/badge/Language-Kotlin-7F52FF?logo=kotlin&logoColor=white)](#)
[![Jetpack Compose](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4?logo=jetpackcompose&logoColor=white)](#)

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

## Download & Install

Use the **Download Latest APK** button at the top of this page to download the newest published version directly. For this button to keep working after every release, attach the APK with the exact asset filename `APKLinker.apk` each time.

1. Tap **Download Latest APK**.
2. Open the downloaded `APKLinker.apk` file.
3. If Android asks, allow installation from that source.
4. Review the requested permissions and install.

Only install APKs from this repository's official Releases. Android may display a warning when installing apps outside Google Play.


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

## 🌐 Developer & Social Media

<div align="center">

<a href="https://www.youtube.com/@BasicTouchPro">
  <img src="https://img.shields.io/badge/YouTube-BasicTouchPro-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube" />
</a>
<a href="https://www.facebook.com/BasicTouchPro">
  <img src="https://img.shields.io/badge/Facebook-BasicTouchPro-0866FF?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook" />
</a>
<a href="https://t.me/BasicTouchPro">
  <img src="https://img.shields.io/badge/Telegram-BasicTouchPro-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram" />
</a>
<a href="https://github.com/BasicTouchPro">
  <img src="https://img.shields.io/badge/GitHub-BasicTouchPro-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
</a>

</div>

## Support

- **Bug reports:** [Open an issue](../../issues/new)
- **Feature requests:** [Open an issue](../../issues/new)
- **Releases:** [View releases](../../releases)

When reporting a bug, include your APKLinker version, Android version, device model, and steps to reproduce the issue. Never include API tokens, passwords, or private files in an issue.

## License

No open-source license has been specified yet. Unless a license file is added to this repository, all rights are reserved by the copyright holder. Do not assume that the source code or app may be reused, modified, or redistributed.

