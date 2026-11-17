# Mini Duck Browser

A small, dependency-free Android WebView browser. DuckDuckGo is its default search engine.

## Build in Android Studio
1. Unzip this project.
2. In Android Studio, select **Open** and choose the `MiniDuckBrowser` folder.
3. Allow Android Studio to install Android SDK 35 / Android Gradle Plugin dependencies.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. Install `app/build/outputs/apk/debug/app-debug.apk` on your Android phone.

## Build online with GitHub Actions
1. Create a GitHub repository and upload the project files (including `.github/workflows/build-apk.yml`).
2. Go to **Actions > Build Android APK > Run workflow**.
3. Open the successful run's **Artifacts** section and download `MiniDuckBrowser-debug-apk`.
4. Extract the ZIP containing `app-debug.apk` and install it on Android.

## Notes
- Minimum Android version: 6.0 (API 23). Actual page compatibility depends on Android System WebView.
- Regular VPN apps, when enabled on the phone, normally route this app's network connections too.
- Supports JavaScript, cookies, local storage, downloads, and basic file upload.
- Does not include a custom VPN, ad blocking, account system, telemetry, or proxy.
- HTTP is allowed, but bad HTTPS certificates are NOT bypassed. This app cannot circumvent network restrictions, DRM, or WebView limitations.
- Some downloads or sites requiring multiple browser windows may not work fully.
- This build intentionally uses target SDK 28 for broad WebView and public-download compatibility; Android may show compatibility warnings on recent devices. For Play Store publication, modernize the target SDK and storage handling.
