# John's Health System - Progressive Web App

Your complete personal health dashboard for tracking fitness, nutrition, weight, and progress.

## Features

### Daily Tracking
- **Morning Check-in**: Weight, yesterday's Fitbit data (steps, calories, sleep)
- **Daily Habits**: Meditation (5min), Plank (60s), Dead hang (30s)
- **Meal Logging**: Breakfast, lunch, dinner, snack, and other with separate calorie/protein tracking
- **Alcohol Tracking**: Pint equivalents with weekly budget (15 pints/week)

### Weekly Tracking
- **Saturday Strength**: Bicep curls (19-week auto-progression), push-ups, chin-ups
- **Sunday Body Fat**: Weekly body fat percentage assessment

### Progress & Motivation
- **Streaks**: Real streak tracking for all habits (resets when broken)
- **Consistency Metrics**: 30-day and 90-day rolling averages (forgiving)
- **100+ Achievements**: Milestone celebrations across all categories
- **Personal Bests**: Automatic tracking of your best performances

### Targets
- **Food**: 1,700-2,000 kcal/day (green zone)
- **Protein**: 110-150g/day (green zone), 90-109g (yellow zone)
- **Alcohol**: 429 kcal/day average (15 pint-equivalents/week)

## Installation

### Step 1: Convert SVG Icons to PNG

The app includes two SVG icon files (`icon-192.svg` and `icon-512.svg`). You need to convert these to PNG format:

**Option A: Online Converter**
1. Go to https://cloudconvert.com/svg-to-png
2. Upload `icon-192.svg`, convert to PNG at 192x192
3. Upload `icon-512.svg`, convert to PNG at 512x512
4. Download both PNG files

**Option B: Using a Graphics Tool**
1. Open each SVG in a graphics editor (Photoshop, GIMP, Inkscape, etc.)
2. Export as PNG at the correct size (192x192 or 512x512)
3. Save as `icon-192.png` and `icon-512.png`

### Step 2: Upload to GitHub

1. Create a new repository on GitHub (can be private)
2. Upload these files:
   - `health-dashboard.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png` (converted from SVG)
   - `icon-512.png` (converted from SVG)

3. Enable GitHub Pages:
   - Go to repository Settings
   - Scroll to "Pages" section
   - Select "main" branch as source
   - Save

4. Wait a few minutes for GitHub Pages to deploy

### Step 3: Install on Mobile

1. Open the GitHub Pages URL in Chrome on your phone
   - URL will be: `https://[your-username].github.io/[repository-name]/health-dashboard.html`

2. Look for the "Add to Home Screen" prompt
   - Or tap the menu (⋮) → "Add to Home Screen"

3. The app will install as a standalone application
   - No browser chrome/URL bar
   - Appears in your app drawer
   - Works offline after first load

## Usage

### Daily Routine

**Morning** (after waking):
1. Open app
2. Log weight
3. Enter yesterday's Fitbit data (steps, calories burned)
4. Enter last night's sleep hours
5. Complete meditation → Plank → Dead hang
6. Check off each habit as completed

**Throughout the day**:
- Log meals as you eat them (or at end of day)
- Log alcohol if consumed
- Check dashboard for progress

**Saturday**:
- Complete strength session (biceps, push-ups, chin-ups)
- App suggests current week's bicep target
- Auto-progresses after 2 consecutive successful weeks

**Sunday**:
- Send body fat % photo (to Claude for assessment)
- Log the percentage in the app

### Navigation

- **Dashboard**: Overview, current streaks, this week summary
- **Log**: Input all daily data (check-in, meals, alcohol, strength)
- **Streaks**: View all streaks, consistency metrics, achievements
- **Settings**: Backup/restore, data management

### Backup

**IMPORTANT**: Back up your data regularly!

1. Go to Settings tab
2. Tap "Export Backup"
3. Save the JSON file to Google Drive or email it to yourself
4. Do this **weekly** (app will remind you after 7 days)

To restore:
1. Settings → Import Backup
2. Select your backup JSON file
3. Confirm restoration

## Data Storage

- All data stored locally in your browser's localStorage
- No cloud sync
- No data leaves your device
- Manual backup/restore only

## Targets & Zones

### Food Calories
- **Green (1,700-2,000 kcal)**: Optimal for goals
- **Yellow (2,000-2,200 kcal)**: Maintenance territory
- **Red (2,200+ kcal)**: Surplus

### Protein
- **Green (110-150g)**: Optimal for muscle preservation
- **Yellow (90-109g)**: Acceptable occasionally
- **Red (<90g)**: Too low, undermining goals

### Alcohol
- **Weekly budget**: 15 pint-equivalents (~429 kcal/day average)
- 1 pint beer = 1.0 equivalent = 200 kcal
- 1 glass wine (175ml) = 0.8 equivalent = 160 kcal
- 1 shot spirits = 0.5 equivalent = 100 kcal

## Bicep Curl Progression

19-week auto-progression (all with 15kg dumbbells):

- Week 1-2: 2×4 reps
- Week 3-4: 2×5 reps
- Week 5-6: 2×6 reps
- Week 7-8: 2×7 reps
- Week 9-10: 2×8 reps
- Week 11-12: 2×9 reps
- Week 13-14: 2×10 reps
- Week 15-16: 3×8 reps
- Week 17-18: 3×10 reps
- Week 19+: 3×12 reps (maintenance)

App auto-progresses after hitting target 2 Saturdays in a row.

## Rest Periods

- **Between sets (same exercise)**: 60-90 seconds
- **Between different exercises**: 1-2 minutes
- **Plank → Dead hang**: 30-60 seconds

## Achievements

Over 100 achievements across categories:

- **Streak milestones**: 1, 3, 7, 14, 21, 30, 50, 75, 100, 150, 200, 300, 365, 500, 1000 days
- **Weight loss**: -1kg, -2kg, -5kg, -7kg, -10kg
- **Body fat**: -1%, -2%, -5%, reached 20%, 18%, 16%, 15%
- **Strength**: First chin-up, 5 reps, 10 reps, 15 reps, 20 reps
- **Perfect performance**: Perfect days, perfect weeks
- **Consistency**: 80%+ compliance, 90%+ compliance
- **Surprise achievements**: Hidden until unlocked

## Troubleshooting

**App won't install:**
- Make sure you're using Chrome on Android or Safari on iOS
- Try opening in incognito mode first, then regular browser
- Clear browser cache and try again

**Data lost:**
- Import your backup JSON file from Settings
- If no backup exists, data cannot be recovered
- This is why weekly backups are critical!

**Icons not showing:**
- Make sure you converted SVG to PNG and uploaded both files
- Check that filenames are exactly `icon-192.png` and `icon-512.png`
- Redeploy GitHub Pages after adding icons

**Service worker issues:**
- Clear browser cache
- Uninstall and reinstall the app
- Check browser console for errors

## Tips

1. **Be consistent with morning routine** - make it automatic
2. **Log meals as you eat** - easier than trying to remember
3. **Don't obsess over daily weight fluctuations** - watch weekly trends
4. **Celebrate streak milestones** - they're achievements!
5. **Back up weekly** - seriously, do this
6. **Perfect is the enemy of good** - 90% compliance beats 100% attempts
7. **Use quick picks for meals** - 500 cal / 50g protein for smoothies, etc.

## Philosophy

This system is designed around YOUR behavior patterns:

- **Forgiving, not punitive**: Streaks reset honestly, but consistency metrics are forgiving
- **Celebration over criticism**: Positive reinforcement, achievements, milestones
- **Low friction**: Quick logging, smart defaults, minimal decisions
- **ADHD-friendly**: Clear hierarchy, visual feedback, progress always visible
- **Long-term sustainable**: You'll still be using this in December 2026

The goal isn't perfection - it's sustainable progress that becomes part of your life.

## Support

This is your personal system. Modify it as needed:
- Change targets by editing the code
- Add new habits
- Adjust progression schedules
- Customize achievements

The code is yours to own and adapt.

---

**Version**: 1.0  
**Created**: December 2024  
**Built for**: John - Great Beyond Brewing Co.
