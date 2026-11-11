# Percentage calculator (Android app)

A phone-sized percentage calculator. The app lives in `www/index.html`;
Capacitor wraps it as an Android app and GitHub builds the APK for you.

## Get the APK

1. Create a new repository on GitHub and upload everything in this folder
   (keep the `.github` folder). Push to the `main` branch.
2. Open the repository's **Actions** tab. The **Build Android APK** workflow
   starts by itself. You can also start it with **Run workflow**.
3. When it turns green (about 5 minutes), open the run and download
   **percentage-calculator-apk** from the Artifacts section.
4. Unzip it and copy `app-debug.apk` to your phone. Open it and allow
   "Install unknown apps" when Android asks.

## Change the calculator

Edit `www/index.html` and push. The workflow builds a new APK each time.

## Notes

- This is a debug-signed APK. It installs fine on your own phone. Publishing
  to the Play Store needs a signed release build, which is a separate step.
- The fonts load from Google Fonts. With no internet the app falls back to
  the phone's system font and still works.
- The Android project is created fresh on every build, so `android/` is not
  stored in the repository. To build on your own computer instead:
  `npm install`, `npx cap add android`, `npx cap sync android`, then open the
  `android` folder in Android Studio.
