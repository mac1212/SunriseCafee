# MyApp

Basic Android (Kotlin) starter project — Hello World with a button.

## Structure
- `app/src/main/kotlin/.../MainActivity.kt` — main screen logic
- `app/src/main/res/layout/activity_main.xml` — screen layout
- `app/src/main/res/values/` — strings, colors, themes
- `app/src/main/AndroidManifest.xml` — app config
- `app/build.gradle` — app-level dependencies
- `build.gradle` — project-level plugins

## First-time setup (on your machine)

1. Create `local.properties` in the project root with your SDK path:
   ```
   sdk.dir=C:/ANDROID_HOME
   ```
   (use your actual ANDROID_HOME path, forward slashes)

2. Generate the Gradle wrapper jar (one-time, needs internet + a JDK):
   ```
   gradle wrapper --gradle-version 8.6
   ```
   (only needed if `gradlew.bat`/`gradlew` aren't already present with a working `gradle-wrapper.jar`)

3. Build and install to a connected phone (USB debugging on):
   ```
   gradlew.bat installDebug
   ```

4. Launch on phone:
   ```
   adb shell am start -n com.example.myapp/.MainActivity
   ```

## Notes
- Package name / applicationId: `com.example.myapp`
- Uses ViewBinding — reference views via `binding.viewId` in MainActivity.kt
- To add a new screen: create a new Activity class + matching layout XML, then register it in AndroidManifest.xml
