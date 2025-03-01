# Candy Blast

A single-file HTML puzzle game inspired by Candy Crush Saga, featuring infinite levels, special candies, and customizable settings. Created by Ygstudio97.

## Features

- **Gameplay**: Match 3 to 10 adjacent candies of the same color to clear them and meet level targets.
- **Infinite Levels**: Start at Level 1 and progress endlessly, with grid size increasing from 5x5 to 10x10 (at Level 41+).
- **Special Candies**:
  - **Striped**: 5% spawn chance, awards +15 points when cleared.
  - **Wrapped**: 5% spawn chance, awards +15 points when cleared.
- **Points System**:
  - Clear candies: `group size * (level + 5)` points.
  - Level up: +5 bonus points.
  - Special candies: +15 bonus points each.
- **Skip Feature**: Deduct 10 points to skip to the next level (requires at least 10 points; otherwise, shows "Minimum credit needed: 10" alert).
- **Customization**:
  - Adjust candy colors via color pickers in the settings screen.
  - Upload a custom background image.
  - Changes apply only when clicking "Apply Settings."
- **Watermark**: "Created by Ygstudio97" displayed in the bottom-right corner.
- **Screens**:
  - **Home**: Start Game, Settings, Exit buttons.
  - **Game**: Play area with Skip and Restart buttons.
  - **Settings**: Customize colors, upload background, view stats, and "How to Play."
  - **How to Play**: Instructions overlay.

## How to Play

1. **Setup**: Save the code as `index.html` and open it in a modern browser (e.g., Chrome, Firefox).
2. **Start**: Click "Start Game" on the home screen.
3. **Gameplay**:
   - Click groups of 3–10 adjacent same-color candies to clear them.
   - Clear the target number of candies (e.g., 20 at Level 1, increases by 5 per level) to advance.
   - Earn points:
     - Base: `group size * (level + 5)`.
     - Striped/Wrapped: +15 points.
     - Level Up: +5 points.
   - Use "Skip" (-10 points) to advance if you have at least 10 points.
4. **Settings**:
   - Click "Settings" from the home screen.
   - Adjust candy colors with color pickers.
   - Upload a background image.
   - Click "Apply Settings" to save changes.
   - View stats (last levels completed, wins, total points) or "How to Play."
5. **Restart**: Click "Restart" in the game screen to return to the home screen.
6. **Exit**: Click "Exit" (works in some browsers if opened as a popup).

## How to Test

1. **Initial Setup**:
   - Open `index.html` in a browser.
   - Verify the watermark "Created by Ygstudio97" in the bottom-right corner.

2. **Home Screen**:
   - Click "Start Game" → Game screen appears.
   - Click "Settings" → Settings screen appears.
   - Click "Exit" → Browser window closes (if permitted).

3. **Game Screen**:
   - Check header: "Level: 1 | Points: 0 | Goal: Clear 20 candies."
   - Clear 3 candies at Level 1 → Points increase to 18 (`3 * (1 + 5)`).
   - Clear a striped/wrapped candy → Points increase by +15.
   - Clear target (20 candies) → Level up to 2, Points increase by +5.
   - **Skip Test**:
     - With < 10 points: Click "Skip" → Alert: "Minimum credit needed: 10."
     - With ≥ 10 points: Click "Skip" → 10 points deducted, level advances.
   - Click "Restart" → Returns to home screen.

4. **Settings Screen**:
   - Adjust color pickers → Colors update in `pendingColors`.
   - Upload an image → Image loads into `pendingBgImage`.
   - Click "Apply Settings" → Colors and background update (refreshes game if active).
   - Click "How to Play" → Instructions appear.
   - Click "Back" → Returns to home screen.

5. **How to Play Screen**:
   - Verify instructions match gameplay.
   - Click "Close" → Instructions disappear.

## Technical Details

- **File**: Single HTML file with embedded CSS and JavaScript.
- **Dependencies**: None (uses Web Audio API for sounds).
- **Browser Support**: Tested in Chrome and Firefox.

## Credits

- **Created by**: Ygstudio97
