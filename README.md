# WTTG 1 Toolkit

A local multi-page helper hub for Welcome to the Game 1.

## Included subpages

- Dashboard
- Run Timer / Timeline
- Claffis Helper + Practice Mode
- Key Compiler
- A.N.N Notes Tracker
- Win Log / Streak Tracker
- Soundboard / Cue Trainer
- Session Checklist
- Threat Guide
- Sites Database / Page Lookup
- Resources / Learning Hub
- Settings / Data Management

## Latest update

- Set the app font to Inter and added a reliable Google Fonts import so local and Vercel builds should match more closely.
- Removed the global Panic Button and its floating emergency panel.
- Fixed Sites Database ordering: the default list now follows the walkthrough order from top to bottom instead of sorting alphabetically.
- Made each Sites Database card show the open time explicitly, with source section and key status.
- Improved Claffis Practice Mode: Start Practice is now next to the Claffis map, sequence playback highlights notes on the map, and the player clicks the same notes back in order.
- Added synthetic Claffis note placeholder audio files in `assets/audio/claffis/` for every hotspot ID.
- Cleaned up the Threat Guide bottom layout and softened oversized shadows so short pages no longer look like a broken dark overlay at the bottom.

## Claffis Practice audio

Practice Mode uses one placeholder WAV per Claffis hotspot:

- `assets/audio/claffis/T1.wav`, `T2.wav`, `T3.wav`
- `assets/audio/claffis/M1.wav`, `M2.wav`, `M3.wav`, `M4.wav`, `M5.wav`
- `assets/audio/claffis/B1.wav`, `B2.wav`, `B3.wav`, `B4.wav`

You can replace these files later with your own local samples as long as the filenames stay the same. If audio fails, the app falls back to synthetic Web Audio tones.

## Sites Database behavior

The database keeps the walkthrough-style order:

1. Dead Link Sites
2. Possible Key Spawn Sites
3. Always Key Sites
4. Deep Wiki URL Sites
5. Ceased Sites

Sites that also contain Secret N Keys are tagged without moving them out of their original position.

## Key Compiler behavior

You can paste fragments like `1 - yx6B` into any Part field. The toolkit reads the number, puts the code into the correct slot, and compiles the final Red Room address as:

`http://<key1><key2><key3><key4><key5><key6><key7><key8>.ann`

The input fields do not re-render on every typed character, so typing and pasting should feel normal.

## Soundboard note

The soundboard uses synthetic browser-generated practice sounds, not original game audio. It is meant for recognition training and fake-cue drills.

Troll Mode can be configured with a frequency slider, random spread, cue pool and an optional instant cue when enabled.

## LocalStorage keys

- `wttg1-toolkit-claffis-v1`
- `wttg1-toolkit-claffis-practice-v1`
- `wttg1-toolkit-run-timer-v1`
- `wttg1-toolkit-keys-v2`
- `wttg1-toolkit-links-v1`
- `wttg1-toolkit-wins-v1`
- `wttg1-toolkit-soundboard-v1`
- `wttg1-toolkit-checklist-v1`
- `wttg1-toolkit-resources-v1`
- `wttg1-toolkit-sites-v1`
- `wttg1-toolkit-strategy-v1`
- `wttg1-toolkit-settings-v1`

## How to run

Open `index.html` in your browser, or deploy the folder as a static site on Vercel.

## Notes

Everything is stored in `localStorage`, so your notes, wins, timer, key slots, site notes, favorites and selections stay saved in the same browser.
The app uses hash routes like `#run`, `#claffis`, `#keys`, `#links`, `#wins`, `#soundboard`, `#checklist`, `#threats`, `#sites`, `#resources`, and `#settings`, so it can be moved to React Router later without changing the concept.

## UI cleanup patch
- Removed the sidebar note about future React Router pages.
- Reworked the global background so short pages no longer show a weird bottom overlay/banding effect.
- Kept the Inter font setup and previous toolkit fixes.
