# GPT Batsho — Cloud Android Build

This is the first Android wrapper for GPT Batsho. It packages the existing GPT Batsho web interface into an Android APK using Android WebView and is designed to build in GitHub Actions, so Android Studio is not required on the phone.

## Cloud build
1. Create a GitHub repository named `GPT-Batsho`.
2. Upload this entire project, preserving `.github/workflows/build-apk.yml`.
3. Push to the `main` branch.
4. Open the repository's **Actions** tab.
5. Open **Build GPT Batsho APK** and wait for the workflow to finish.
6. Download the **GPT-Batsho-debug-apk** artifact.
7. Extract the APK and install it on Android.

The workflow uses Gradle on a GitHub-hosted runner. It does not require Android Studio on the phone.

## Current scope
- Packages GPT Batsho v10 UI and live-market WebSocket connector.
- Internet permission is enabled.
- Notification permission is requested on Android 13+.
- This is a debug/testing APK. Release signing and a backend for secure market credentials/trial enforcement come later.
