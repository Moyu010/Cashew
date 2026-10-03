# Local Android build

This fork is based on upstream commit `9cfbe50` (Cashew 5.4.3+416).
The Android package is `com.budget.tracker_app.local` and the launcher
name is Cashew Local, so it can coexist with the official application.
The two applications keep separate databases.

Premium prompts and store billing are disabled. Backup sync defaults
to off. Google account and cloud features have not been configured for
this package; use the app without signing in.

The existing Gradle integration requires an older Flutter SDK. This
build uses Flutter 3.19.6, Java 17 and the Android SDK. Build with:

```sh
cd budget
flutter build apk --release --no-tree-shake-icons
```

The release build uses the local Android debug signing key for personal
sideloading. Keep that key to install later updates over this build.
It is not intended for publishing to an app store.

The APK is generated at `budget/build/app/outputs/flutter-apk/app-release.apk`.
