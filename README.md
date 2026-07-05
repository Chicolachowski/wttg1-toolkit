# WTTG 1 Toolkit

A single-file multi-page helper hub for Welcome to the Game 1.

## Included subpages

- Dashboard
- Run Timer / Timeline
- Claffis Helper
- Key Compiler
- A.N.N Notes Tracker
- Win Log / Streak Tracker
- Soundboard / Cue Trainer
- Session Checklist

## Latest update

- Added configurable Troll Mode frequency controls in Soundboard.
- Added Troll Mode random spread, cue pool and instant-start option.
- Added Quick loss button in Win Log.
- Added Run Timer with timestamped timeline events.

## Key Compiler behavior

You can paste fragments like `1 - yx6B` into any Part field. The toolkit reads the number, puts the code into the correct slot, and compiles the final Red Room address as:

`http://<key1><key2><key3><key4><key5><key6><key7><key8>.ann`

The input fields no longer re-render on every typed character, so typing and pasting should feel normal.

## Soundboard note

The soundboard uses synthetic browser-generated practice sounds, not original game audio. It is meant for recognition training and fake-cue drills.

Troll Mode can be configured with a frequency slider, random spread, cue pool and an optional instant cue when enabled.

## How to run

Open `index.html` in your browser.

## Notes

Everything is stored in `localStorage`, so your notes, wins, timer, key slots and selections stay saved in the same browser.
The app uses hash routes like `#run`, `#claffis`, `#keys`, `#links`, `#wins`, `#soundboard`, and `#checklist`, so it can be moved to React Router later without changing the concept.
