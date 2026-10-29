<div align="center">

# Mindful Journal

**A thoughtful space to write, reflect, and revisit your days.**

A Flutter-powered personal journaling application with mood check-ins, rich writing tools, creative expression, and a customizable experience across screen sizes.

**Flutter · Dart · Local-first storage · Responsive UI**

[Explore Features](#features) · [App Preview](#app-preview) · [Run Locally](#run-locally) · [Technical Notes](#technical-notes)

</div>

---

## Overview

Mindful Journal brings reflection, writing, and reading into one cohesive experience. Its iOS-inspired interface pairs an indigo visual identity with a distraction-conscious editor, mood tracking, calendar history, and personal insights.

The application is designed around **local-first journaling**: entries, media, preferences, and related information are saved on the device rather than requiring a hosted account or backend service.

## App preview

> **Screenshots are pending upload.** The images below are intended to be genuine captures of the running app, not promotional mockups. Add files with the exact names shown in the [screenshot checklist](#screenshot-checklist) to render them here.

### Home and writing experience

| Home | Journal editor |
|:---:|:---:|
| ![Mindful Journal home screen](docs/screenshots/home.png) | ![Mindful Journal editor](docs/screenshots/journal-editor.png) |

### Reflection and personal history

| Mood check-in | Calendar |
|:---:|:---:|
| ![Mood check-in](docs/screenshots/mood-check-in.png) | ![Journal calendar](docs/screenshots/calendar.png) |

### Personalization and creative tools

| Profile and themes | Drawing canvas |
|:---:|:---:|
| ![Profile and appearance settings](docs/screenshots/profile-themes.png) | ![Drawing canvas](docs/screenshots/drawing-canvas.png) |

## Features

### Write and organize
- Create, read, edit, and delete entries with confirmation before deletion.
- Use date selection, required-field validation, word count, and unsaved-change protection.
- Navigate a chronological journal timeline grouped by month.
- Search locally and filter entries by mood, media, tags, and favorites.
- Organize writing with collections, templates, and checklists.

### Reflect and understand patterns
- Choose from five labeled moods during check-in.
- View writing streaks and related calendar history, including backdated entries.
- See local insights such as entry count, average mood, total words, and most common mood.

### Make entries your own
- Format text with styles, colors, and highlights; use undo/redo and Focus mode.
- Attach up to four photos and two editable drawings to an entry, with zoom previews.
- Draw using Pen, Marker, Highlighter, Pencil, and Eraser, with undo/redo and clear actions.
- Personalize your profile, choose from eight accent themes or a custom color, and use System, Light, or Dark appearance.

### Designed across devices
- Responsive layouts for phones, tablets, and desktop-sized screens.
- Dedicated Home, Journal, Calendar, and Profile areas.
- Keyboard shortcuts: `Cmd/Ctrl + N` to create from Home, `Cmd/Ctrl + S` to save in the editor, and `Escape` to close with unsaved-change protection.
- Accessible controls and labeled mood choices.

## Technology

| Area | Implementation |
|---|---|
| Application | Flutter, Dart |
| Preferences | `shared_preferences` |
| Local data and media | JSON records and app-owned files under the application documents directory via `path_provider` |
| Media processing | Image validation and normalization before local storage |
| Supported codebases | Android, iOS, macOS, and web project files; platform validation differs |
| Verification | Flutter analysis, tests, and responsive widget checks |

## Technical notes

### Local persistence

At startup, the app loads saved entries, tasks, checklists, favorites, tags, collections, profile details, and preferences. Changes queue serialized writes; journal-editor saves and quick check-ins wait for completion. An intentionally emptied journal remains empty after reopening rather than being repopulated with sample entries.

For implementation details, see [Local Persistence Report](docs/LOCAL_PERSISTENCE_REPORT.md).

### Project structure

```text
lib/
├── app/           # Root state, startup hydration, themes
├── core/          # Design tokens and shared utilities
├── models/        # Journal-entry and mood models
├── screens/       # Main screens, editor and reading flows
└── widgets/       # Reusable controls and UI components

test/              # Behavior and responsive-layout tests
assets/images/     # App artwork
scripts/ or tools/ # Optional local tooling (see repository)
docs/              # Technical reports and guides
```

### Current platform and release status

- An Android release APK build has been reported successful. **Physical-device installation and reopen testing still require confirmation** from the release checklist.
- Responsive widget tests cover phone, tablet, desktop, landscape, and enlarged text scenarios.
- The repository includes platform runners, but their presence alone is **not** evidence of release readiness on every platform.
- Production distribution, store publication, and device acceptance are not claimed.

See [Release Guide](docs/RELEASE_GUIDE.md), [Architecture](docs/ARCHITECTURE.md), and [Production Roadmap](docs/PRODUCTION_ROADMAP.md).

## Run locally

Install a compatible Flutter SDK and follow the repository's dependency configuration.

```bash
flutter pub get
flutter run
```

Run checks:

```bash
flutter analyze
flutter test
```

The supplied project notes report verification with **Flutter 3.47.7 / Dart 3.13.5**. Results may differ across SDK versions and target platforms.

## Screenshot checklist

Upload **real screenshots**, preferably captured from a simulator or device. Create a `docs/screenshots/` directory and use these exact filenames:

| Filename | Capture |
|---|---|
| `home.png` | Main Home screen with greeting and journal overview |
| `journal-editor.png` | Writing editor with a sample entry |
| `mood-check-in.png` | Five-choice mood selector |
| `calendar.png` | Calendar with fictional journal history |
| `profile-themes.png` | Profile and theme/personalization interface |
| `drawing-canvas.png` | Working drawing editor or canvas |

**Image guidance:** Use sample journal entries with invented names and text; never share personal journal content. Consistent portrait crops work best for mobile screenshots. The README image links render automatically once the files are committed at the referenced paths.

## Documentation

- [Local persistence implementation](docs/LOCAL_PERSISTENCE_REPORT.md)
- [Architecture](docs/ARCHITECTURE.md)
- [Design system](docs/DESIGN_SYSTEM.md)
- [Product experience](docs/PRODUCT_EXPERIENCE_REPORT.md)
- [Settings and layout refinements](docs/SETTINGS_TASKS_VIEWS_REPORT.md)
- [Release guide](docs/RELEASE_GUIDE.md)
- [Production roadmap](docs/PRODUCTION_ROADMAP.md)

Some older project reports describe earlier implementation stages; consult the latest persistence and release documentation for current behavior. Verify linked filenames against the actual repository before publishing.

## Project ownership

**Created and developed by Fiel Mark E. Oronos.**

This repository presents Mindful Journal as a software project and portfolio case study. It does not claim an app-store release or a commercial production deployment.

---

<div align="center">

**Made with Flutter · Designed for mindful everyday writing**

[GitHub Profile](https://github.com/oronex-dev) · [Portfolio](https://oronex-dev.github.io/portfolio-fiel-mark/) · [Contact](mailto:oronosfielmark@gmail.com)

</div>
