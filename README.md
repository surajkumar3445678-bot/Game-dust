# Ultimate Game Booster — Non-Root Edition

A Kotlin + Jetpack Compose Android application designed to work without Magisk, `su`, or root permission.

## Included
- Neon blue/purple gaming dashboard.
- Installed launchable app discovery, search, favourites, and launch.
- Per-app Android App Info shortcut for user-managed app storage/cache settings.
- Real device readings: Android memory, internal storage, battery percentage, battery temperature, and CPU0 frequency when the device exposes it.
- Safe local cache cleanup for this booster app only.
- Shortcuts to Android battery, network, display, storage, and app settings.
- Manual in-app Game Mode and Balanced/Gaming/Battery preference profiles.
- GitHub Actions workflow to build a debug APK.

## Important non-root limits
Android does not let ordinary apps silently force-stop other apps, clear another app's private cache, change CPU/GPU governors or frequencies, unlock FPS, or guarantee a network speed increase. The app therefore does not fake these features. CPU frequency is read-only and may be unavailable. Battery temperature is not CPU/GPU temperature.

## Build
Requires JDK 17, Android SDK platform 35, and Gradle 8.9.

```bash
gradle :app:assembleDebug
```

APK:
`app/build/outputs/apk/debug/app-debug.apk`

## Permissions and privacy
The app does not request root access, accessibility access, VPN access, or overlay access. It queries launchable apps for the game library. It does not upload device data.
