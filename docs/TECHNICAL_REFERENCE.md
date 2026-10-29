# Mindful Journal

**An iOS-inspired personal journaling experience built with Flutter.**

Mindful Journal is a cross-platform personal project focused on reflection, expressive writing, mood awareness, and a calm, customizable interface. It includes writing and reading flows, rich media, local storage, and responsive layouts for different screen sizes.

**Built with:** Flutter · Dart · Local JSON persistence · `shared_preferences` · `path_provider`

## App preview

<!-- Replace these placeholders with screenshots captured from the actual app. -->

### Home and writing
<img src="docs/screenshots/home.png" width="48%" alt="Mindful Journal home screen"> <img src="docs/screenshots/editor.png" width="48%" alt="Mindful Journal editor screen">

### Calendar and insights
<img src="docs/screenshots/calendar.png" width="48%" alt="Journal calendar and writing history"> <img src="docs/screenshots/insights.png" width="48%" alt="Journal insights and mood summaries">

### Personalization
![Mindful Journal appearance and profile options](docs/screenshots/personalization.png)

*The screenshots above are file paths to fill with authentic app images; they are not included in this README package.*

## Features

### Journaling and reflection
- Five labeled mood choices and preselected editor mood.
- Create, view, edit, and confirm deletion of journal entries.
- Date selection, title/body validation, word counts, and unsaved-change protection.
- Timeline grouped by month, backdated writing, writing streaks, and calendar history.
- Search, favorites, mood/media/tag filters, and highlighted matches.

### Creative writing tools
- Formatted text, text colors and highlights, undo/redo, and focus mode.
- Up to four saved photos and two editable drawings per entry.
- Pen, marker, highlighter, pencil, eraser, drawing undo/redo, and zoom previews.
- Animated checklists, tasks, and secondary insights.

### Personalization and layouts
- Editable profile name, tagline, and photo.
- Eight accent themes and a custom color picker with System / Light / Dark modes.
- Home, Journal, Calendar, Profile, and a separate creation menu.
- Phone, tablet, landscape, and desktop-oriented responsive interfaces.
- Keyboard shortcuts: `Cmd/Ctrl+N` for new entry; `Cmd/Ctrl+S` to save; `Esc` to close with change protection.

## Data storage and privacy

Entries, favorites, tags, tasks, media, checklist state, and preferences are stored **locally on the device**. The application uses `shared_preferences` for profile/appearance preferences and an app-specific documents directory for JSON data and media. Changes are serialized to disk, and important editing flows wait for saves to complete.

There is **no claim of account-based cloud sync** or online backup. See [Local persistence report](docs/LOCAL_PERSISTENCE_REPORT.md).

## Run locally

```bash
flutter pub get
flutter run
flutter analyze
flutter test
```

The supplied documentation reports validation with **Flutter 3.47.7 / Dart 3.13.5**. Confirm the version in your current environment before publishing refreshed build claims.

## Platforms and validation

- Android release APK has been built, according to the project report.
- Flutter project includes platform runners and responsive widget checks.
- Actual Android install, force-stop, and reopen acceptance testing was identified as still pending in the supplied README.
- Inclusion of a platform runner does **not** mean a release was tested or published for that platform.

## Project structure

```text
lib/
  app/            # application root, state, startup hydration, themes
  core/           # shared functions and design tokens
  models/         # journal and mood data
  screens/        # major application screens
  widgets/        # reusable UI components
assets/images/    # approved app artwork
test/             # behavior and responsive-layout tests
docs/             # detailed engineering and validation reports
```

## Detailed documentation

- [Architecture](docs/ARCHITECTURE.md)
- [Design system](docs/DESIGN_SYSTEM.md)
- [Local persistence](docs/LOCAL_PERSISTENCE_REPORT.md)
- [Release guide](docs/RELEASE_GUIDE.md)
- [Product experience](docs/PRODUCT_EXPERIENCE_REPORT.md)
- [Settings, tasks, and views](docs/SETTINGS_TASKS_VIEWS_REPORT.md)
- [Production roadmap](docs/PRODUCTION_ROADMAP.md)
- [Full original technical notes](docs/ORIGINAL_README_NOTES.md)

## Project status

**Portfolio and learning project.** It demonstrates Flutter UI engineering, local persistence, responsive layouts, and app testing. It is not described as a commercially published App Store product.
