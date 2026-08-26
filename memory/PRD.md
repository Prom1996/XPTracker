# Apex Ledger — Product Requirements

## Problem statement
Build a modern, dark-first expense tracker for iOS and Android with fast expense entry, transaction management, persistent local storage, summary metrics, and spending analytics.

## Architecture
- Expo SDK 54 / React Native frontend with Expo Router entrypoint.
- Local device persistence through the provided AsyncStorage-backed storage helper.
- No backend required for the selected local-first product direction.
- Native Feather icons, Haptics, SafeAreaView, ScrollView, and responsive React Native layouts.

## User personas
- Individuals who want a lightweight personal spending log.
- Mobile-first users who need to record expenses quickly and review patterns.

## Core requirements (static)
- Expense fields: amount, category, date, notes.
- Categories: Food, Transportation, Utilities, Entertainment, Housing, Miscellaneous.
- Validation, add, edit, delete, and category filtering.
- Persistent local storage across refresh/relaunch.
- Total spent, current-month spend, and highest spending category.
- Category breakdown and seven-day spending trend visualization.
- Dark-first, bold, legible, touch-friendly mobile UI.

## Implemented (2026-08-26)
- Built Apex Ledger dashboard with obsidian/emerald visual system and bottom navigation.
- Added validated add/edit expense form with category chips, date input, notes, haptics, and reliable awaited persistence.
- Added transaction history, category filter chips, edit/delete confirmation flow, empty states, summary metrics, category ring, and seven-day bar trend.
- Added stable control test IDs and preserved the icon-font splash prewarming logic.
- Verified rendering, validation, persistence, filtering, summaries, charts, edit, and delete in mobile preview.
- Added native date picker integration for expense dates and from/to range filters, CSV generation, and native share-sheet export.
- Verified new controls, export invocation, and responsive layout in preview; actual picker selection/share sheet require an iOS or Android runtime.

## Prioritized backlog
- P0: None for the requested local-first MVP.
- P1: Validate native picker selection and share sheet on physical iOS/Android devices; add date-range filter alongside category filters and export/share CSV are implemented.
- P2: Add recurring expenses, budgets, monthly comparison analytics, and optional cloud sync.

## Next tasks
1. Add a native date picker for easier date entry.
2. Add budget targets and progress alerts.
3. Add optional authenticated cloud backup if multi-device access is needed.