# Imgur Android App

Android Imgur client built in Java as the **final assignment (“Eindopdracht”)** for a Mobile Development Android course.  
The app demonstrates consuming a REST API, working with lists and detail views, and following common Android architecture patterns.

> **Note:** This is a student project and not an official Imgur application.

---

## Table of Contents

- [Features](#features)
- [Screenshots](#screenshots)
- [Architecture & Tech Stack](#architecture--tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [1. Prerequisites](#1-prerequisites)
  - [2. Clone the Repository](#2-clone-the-repository)
  - [3. Open in Android Studio](#3-open-in-android-studio)
  - [4. Configure Imgur API](#4-configure-imgur-api)
  - [5. Run the App](#5-run-the-app)
- [Building an APK](#building-an-apk)
- [Releases](#releases)
- [Known Limitations](#known-limitations)
- [Future Improvements](#future-improvements)
- [Credits](#credits)
- [License](#license)

---

## Features

> The exact feature set depends on the current state of the code in `app/src/main`, but the app is designed around these core ideas:

- 📷 **Browse Imgur content**
  - Load images from the Imgur API.
  - View image details like title, description, and other metadata.
- 🧭 **Simple navigation**
  - Separate screens / activities or fragments for lists and detail views.
  - Use of Android navigation patterns (toolbar, back navigation, etc.).
- 📱 **Responsive layout**
  - Optimized for phones.
  - Uses standard Android UI components and layouts.
- 🌐 **Networked data**
  - Fetch data from a REST API endpoint (Imgur).
  - Basic error handling for failed requests (no connection, timeouts, etc.).

You can explore the exact functionality by checking the activities, fragments, and adapters in `app/src/main/java`.

---

## Screenshots

Add some screenshots of the app here (optional but recommended):

```text
app/
└── src/
    └── main/
        └── res/
            └── drawable-*/      # Put your screenshots/UI images here if you like

Example section once you add images:

## Screenshots

| Home / Feed | Detail View |
| ----------- | ----------- |
| ![Home](./docs/screenshot_home.png) | ![Detail](./docs/screenshot_detail.png) |


---

Architecture & Tech Stack

Language: Java

Platform: Native Android

Gradle: Android Gradle project with app module

Minimum / Target SDK: Defined in app/build.gradle (check there for exact values)

Networking / Images: Standard Android HTTP & image loading libraries (check build.gradle and imports in the code for the exact libraries)


Typical concepts demonstrated:

Activities & possibly Fragments

RecyclerView / List-based UI

View binding / findViewById

Working with background threads / async calls for network access

Handling configuration changes via the Android framework



---

Project Structure

The project follows the standard Android app layout:

Imgur-App-Android/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/           # Application source code (activities, adapters, models, API layer)
│   │   │   ├── res/            # Layouts, drawables, strings, styles, etc.
│   │   │   └── AndroidManifest.xml
│   │   └── test/               # (Optional) Unit tests
│   ├── build.gradle            # Module-level Gradle config
├── build.gradle                # Project-level Gradle config
├── gradle/                     # Gradle wrapper files
└── settings.gradle             # Module inclusion

Look into app/src/main/java for:

Activities / Fragments – entry point(s) to the UI.

Adapters – connecting lists (RecyclerView) to data.

Models – classes that represent Imgur API responses.

Networking layer – classes that handle HTTP calls / API communication.



---

Getting Started

1. Prerequisites

Android Studio (Arctic Fox or newer recommended)

Android SDK installed (matching the SDK versions in app/build.gradle)

A working Internet connection

An Imgur API Client ID (for real API calls)


> You can create an Imgur application via the Imgur API docs and obtain a Client ID and Client Secret.




---

2. Clone the Repository

git clone https://github.com/ferrannl/Imgur-App-Android.git
cd Imgur-App-Android


---

3. Open in Android Studio

1. Start Android Studio.


2. Choose “Open an existing project”.


3. Select the cloned Imgur-App-Android folder.


4. Let Gradle sync and finish indexing.




---

4. Configure Imgur API

The app expects valid Imgur API credentials to make requests.

1. Create an Imgur application and obtain a Client ID (and optionally Client Secret).


2. Search the codebase for something like CLIENT_ID, CLIENT_SECRET, IMGUR_CLIENT_ID, or similar constant in java/ or build.gradle.


3. Fill in your keys in the appropriate place:

Either in a Constants-like class, or

As Gradle properties / BuildConfig fields (check comments and TODOs in the code).




> If you’re not sure where to put them, simply search the project for "imgur" to find the relevant classes and configuration points.




---

5. Run the App

1. Connect an Android device via USB with USB debugging enabled, or start an Emulator.


2. In Android Studio, select the app run configuration.


3. Click Run ▶.


4. The app will be built and deployed to your device/emulator.




---

Building an APK

If you prefer to build an APK directly:

Via Android Studio

1. In the menu, go to Build → Build Bundle(s) / APK(s) → Build APK(s).


2. When it finishes, click the notification and open the output folder.


3. You’ll find an app-debug.apk (or release variant if you created one).



Via Gradle (command line)

From the project root:

./gradlew assembleDebug

The resulting APK will typically be located at:

app/build/outputs/apk/debug/app-debug.apk

Transfer that APK to your device and install it (you may need to allow installation from unknown sources).


---

Releases

The repository includes GitHub Releases which may contain ready-built APKs of specific versions.

Go to the Releases section on GitHub.

Download the latest APK (e.g. Imgur App) and install it on your Android device.



---

Known Limitations

This is a course assignment, not a production app.

Error handling, offline support, and UI polish may be limited compared to a full commercial application.

Some parts of the Imgur API may be only partially implemented or hard-coded.


Check open issues and comments in the code for any TODOs or known problems.


---

Future Improvements

Ideas if you want to extend the project:

✅ Improve error handling and user feedback for network errors.

✅ Add pagination and infinite scrolling for long lists.

✅ Add user authentication (OAuth2) for posting, voting, and favorites.

✅ Introduce a proper repository pattern with ViewModel + LiveData / Flow.

✅ Add unit tests and UI tests.

✅ Dark mode and additional theming options.



---

Credits

Author(s):

@ferrannl

And any collaborators listed under the repository’s contributors.


API: Imgur API



---

License

No explicit license file is currently included in this repository.

That means, by default, all rights are reserved to the author(s) unless a license is added later.
If you intend to reuse or redistribute the code, please contact the repository owner first or add an appropriate open-source license.


---
