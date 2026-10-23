# Neon Runner 3D — Android APK project

This project is prepared for building a test APK in the cloud, so you can work from an Android phone without installing Android Studio.

## Build the APK using GitHub Actions (phone-only workflow)

1. Sign in to GitHub and create a **new private repository** (recommended while learning).
2. Upload the contents of this ZIP to the repository. Make sure `.github/workflows/build-apk.yml` is included. If GitHub's mobile upload screen hides dot-folders, create `.github/workflows` in the GitHub web editor and add `build-apk.yml` from this ZIP.
3. Open the repository's **Actions** tab and enable Actions if asked.
4. Choose **Build Android APK** → **Run workflow**. You can also push a commit to the `main` branch to trigger a build.
5. Wait for the workflow to finish successfully.
6. Open that completed workflow run and scroll to **Artifacts**. Download `Neon-Runner-3D-APK`.
7. Extract the downloaded ZIP on your phone. Tap `app-debug.apk` and follow Android's install prompts. Only install APKs you built or trust.

## Project files

- `www/index.html` — the game (canvas runner, obstacles, pause/resume/restart, colour selection, touch controls).
- `package.json` — JavaScript dependencies.
- `capacitor.config.ts` — Android app name and package ID.
- `.github/workflows/build-apk.yml` — cloud build workflow.

## Notes

- The workflow creates an **unsigned-for-store debug/test APK** (debug-signed for local installation). It is for testing, not a Google Play release.
- Keep the repository private if you don't want to publish your source code.
- Save a copy of your project. If you later publish, create a release-signed APK or Android App Bundle and keep your signing key safe.
- The character is a stylized original drawing inspired by the game concept, not a 3D model extracted from a video.
