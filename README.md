# DougDoug Food Challenge Tracker - OBS Overlay

![Made by @sixtyvari0us](https://img.shields.io/badge/made%20by-%40sixtyvari0us-blue)

## Features

- **Real-time Tracking**: Live calorie and fat tracking displayed on stream
- **Restaurant Database**: Pre-loaded database with 300+ items from popular chains
- **Multiplayer Mode**: Track multiple players/competitors simultaneously
- **Manual Entry**: Add custom items not in the database
- **Smart Search**: Quick search and filter by restaurant
- **History Tracking**: View and manage recent entries

## Supported Restaurants

The database includes items from:
- McDonald's
- Taco Bell
- Burger King
- Wendy's
- KFC
- Chick-fil-A
- In-N-Out
- Subway
- Dunkin'
- Jollibee
- El Pollo Loco
- Del Taco
- The Habit Burger Grill
- Fatburger
- Dave's Hot Chicken
- Jack in the Box
- Carl's Jr.
- Popeyes
- Original Tommy's
- Wienerschnitzel
- Arby's
- Domino's

## Installation

1. **Download the overlay file**
   - Click the green "Code" button on GitHub
   - Select "Download ZIP"
   - Extract the ZIP file

## Setup in OBS

1. In OBS, click **+** in Sources
2. Select **Browser Source**
3. Name it whatever
4. Check **Local file**
5. Browse to `dd-challenge-overlay.html`
6. Set Width: `1920px` (or adjust to your preference)
7. Set Height: `1080px` (or adjust to your preference)
8. Click **OK**

### Crop Out Admin Panel

**Important**: You need to crop out the admin panel on the right side before using the overlay on stream.

1. In OBS, select the Browser Source
2. Hold **Alt** and drag with **Left Mouse Button** from the right edge
3. Crop until only the left overlay (HUD) is visible
4. The admin panel should be completely hidden from the stream view

### Chroma Key Setup (For Transparent Background)

1. In the Browser Source properties, check **Shutdown source when not visible**
2. Add a **Chroma Key** filter

## Usage

### Basic Usage

1. **Open the overlay** in your browser or OBS preview
2. **Add items** using one of two methods:
   - **Manual Entry**: Enter restaurant, item name, calories, and fat manually
   - **Database Search**: Search the pre-loaded database and click to add

3. **View stats** on the left side of the overlay:
   - Total calories consumed
   - Total fat consumed
   - List of restaurants visited (in order)

### Manual Entry

1. In the **Manual Entry** section:
   - Enter the restaurant name (autocomplete available)
   - Enter the item name
   - Enter calories
   - Enter fat (optional)
   - Click **ADD ITEM**

2. The item will appear in the history and stats will update automatically.

### Database Search

1. In the **Menu Database Search** section:
   - Optionally filter by restaurant using the top field
   - Type to search for items
   - Click any item in the results to add it instantly

2. Items are added with pre-loaded calorie and fat values.

### Multiplayer Mode

1. **Enable Multiplayer**:
   - Check the **Multiplayer** toggle in the top right

2. **Add Players**:
   - Enter a player name in the "New Player Name" field
   - Click **Add**
   - Repeat for all players

3. **Select Active Player**:
   - Click on a player button at the top to make them active
   - All items added will be attributed to the active player

4. **View Player Stats**:
   - Each player's stats appear on the right side of the overlay
   - Stats show calories and fat per player

5. **Manage Players**:
   - Rename players by editing their name in the "Manage Players" section
   - Delete players with the **X** button

### History Management

- **View History**: All added items appear in the "Recent History" section
- **Delete Items**: Click the **X** button next to any item to remove it
- **Reset All**: Click **Reset All** to clear all data (requires confirmation)

### Display Options

- **Show/Hide Fat**: Toggle the "Show Fat" checkbox to show or hide fat tracking
- **Multiplayer Toggle**: Enable/disable multiplayer mode

## Customization

### Adding Custom Items to Database

Edit the `menuDB` array in the JavaScript section:

```javascript
{ chain: "Your Restaurant", item: "Item Name", cals: 500, fat: 25 },
```

## Tips & Tricks

- **Quick Entry**: Use the database search for fastest entry - just type and click
- **Restaurant Autocomplete**: Start typing a restaurant name and select from suggestions
- **Multiplayer Efficiency**: Set up all players before starting the challenge
- **History Cleanup**: Regularly delete items if you make mistakes to keep stats accurate
- **Crop First**: Always crop out the admin panel before going live
- **Chroma Key**: Use the green background (#00b140) for easy chroma key removal in OBS

## Credits

- Made by [@sixtyvari0us](https://twitter.com/sixtyvari0us)
- Designed for DougDoug food challenge streams

