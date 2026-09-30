# Fuel Assist Demo: Android APK

This folder turns the Highway Fuel Assist demo into an Android app (APK). GitHub builds it for you for free, so you do not need Android Studio.

## Build the APK (once, about 10 minutes)

1. Create a free account at https://github.com and sign in.
2. Click **+** (top right), then **New repository**. Name it `fuel-assist-demo`, choose **Public** (or Private), and click **Create repository**.
3. On the new page, click **uploading an existing file**.
4. Unzip this package on your computer. Open the unzipped folder, select **everything inside it** (including the hidden `.github` folder) and drag it onto the GitHub page.
   - On Mac, press Cmd+Shift+. in Finder to show hidden folders. On Windows, turn on View > Hidden items.
   - If `.github` will not upload, see "If the build does not start" below.
5. Click **Commit changes**.
6. Click the **Actions** tab. A build called "Build Android APK" starts. Wait until it shows a green tick (about 5 to 8 minutes).
7. Go to the repository's main page and click **Releases** on the right. Open the newest release and download **FuelAssistDemo.apk**.

## Install on an Android phone

1. Open the Releases page on the phone (or send the APK to the phone by WhatsApp, email, Google Drive or USB).
2. Tap **FuelAssistDemo.apk**.
3. If the phone asks, allow **Install unknown apps** for your browser or file app, then go back.
4. Tap **Install**, then **Open**. The app appears as **Fuel Assist Demo**.
5. If Play Protect warns that the app is unknown, tap **More details**, then **Install anyway**. This happens because the demo is not from the Play Store.

Share the Releases link with users so they can install it the same way.

## If the build does not start

GitHub's upload page sometimes skips the `.github` folder. Then:
1. In the repository, click **Add file**, then **Create new file**.
2. Type the name `.github/workflows/build-apk.yml` (the slashes create the folders).
3. Paste the contents of `build-apk.yml` from this package and click **Commit changes**.
4. The build starts. Continue from step 6 above.

To rebuild at any time: **Actions**, then **Build Android APK**, then **Run workflow**.

## Update the app

Replace `www/index.html` with a new version (Add file > Upload files) and commit. GitHub builds a new APK automatically. Install it over the old one on the phone.

## Notes

- This is a debug build. It installs on phones directly but cannot go on the Play Store. The Play Store needs a signed release build and a Google Play developer account ($25 one-time fee).
- iPhones cannot install APK files. For iPhone users, share the web version (Add to Home Screen in Safari).
- The app works offline. Fonts load from the internet when available.
