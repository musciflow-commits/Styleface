# StyleFace Android Starter

A native Android starter app for a face-shape hairstyle recommendation product with a freemium UI.

## Included
- Kotlin + Jetpack Compose UI
- User-selectable face shape, hair texture, length, maintenance and facial hair
- Local recommendation rules
- Android photo picker (no storage permission needed)
- Basic illustrative hair overlay on the selected photo
- Premium-locked sample styles and a local demo-unlock dialog
- Barber guidance

## Important limitations
- Face shape is selected by the user. This starter does **not** perform automatic face detection.
- The photo overlay is illustrative, not realistic AI hair replacement or segmentation.
- Premium unlock is a local demo flag. It does **not** take payment or create a subscription.
- No photo upload, account, analytics, backend, or billing integration is included.

## Open and run
1. Install Android Studio (current stable) and a compatible JDK (17).
2. Extract this ZIP.
3. In Android Studio, choose **Open** and select the `StyleFaceAndroid` folder.
4. Allow Gradle sync to finish; install the Android SDK platform requested by the project if prompted.
5. Run the `app` configuration on an Android emulator or connected Android phone.

## Suggested next production steps
1. Add face landmarks / face-shape estimation with clear user consent and a manual correction option.
2. Replace the illustrative overlay with a hair segmentation + virtual try-on model or an image-generation backend.
3. Add secure account and saved-look storage only if needed.
4. Integrate Google Play Billing for real subscriptions, server-side entitlement validation, restore purchases, and a privacy policy.
5. Add automated tests, accessibility checks, crash reporting with consent, and store listing assets.

## Design intent
StyleFace should present recommendations as suggestions rather than absolute rules. Face shape is only one factor; hairline, density, curl pattern, lifestyle, and personal taste matter too.


## Build an APK in GitHub Actions (without installing Android Studio locally)
1. Create a GitHub repository and upload the contents of this project folder.
2. Push the files to the `main` branch, or open the repository's **Actions** tab.
3. Select **Build StyleFace APK** and choose **Run workflow** if it has not run automatically.
4. When the workflow finishes, open its run and download the `StyleFace-debug-apk` artifact.
5. Extract the artifact ZIP to get `app-debug.apk`. On your Android phone, install it after allowing installation from that source if Android asks.

This produces a **debug APK** for testing, not a Play Store release APK. A signed release build and real billing integration are separate steps.
