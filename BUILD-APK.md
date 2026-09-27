# Build Vid2Cam APK online — no Android Studio required

1. Create a new GitHub repository (a private repository is fine).
2. Upload the contents of this folder to the repository. Make sure `.github/workflows/build-apk.yml` is uploaded too.
3. Open the repository's **Actions** tab.
4. Open **Build Vid2Cam APK**.
5. Click **Run workflow** (or push to `main`/`master` to trigger it automatically).
6. Wait for the green check mark.
7. Open the completed workflow run and download the **vid2cam-debug-apk** artifact.
8. Unzip the downloaded artifact and install `app-debug.apk` on the Android phone.

The workflow uses the Gradle wrapper already included in the project, Java 17, and GitHub's hosted Ubuntu runner.
