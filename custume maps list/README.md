# Repository custom maps

This folder contains map JSON files that players can load from the **REPOSITORY MAPS** button on the main menu.

## Add a map

1. Create or edit a map in the game and choose **EXPORT .JSON**.
2. Put the exported `.json` file in this folder.
3. Add its filename to `index.json`, with a display name, note count, and difficulty:

   ```json
   {
     "maps": [
       {
         "file": "steins_gate_simplified.json",
         "name": "Steins Gate (Simplified)",
         "notes": 106,
         "difficulty": "Normal"
       }
     ]
   }
   ```

4. Publish both files to the repository. The website reads the list and each map directly from this folder.

Keep `index.json` valid JSON, separate map objects with commas, and list each map filename once. The game shows each map's name, note count, and difficulty. Players can search by name and sort the map list by name, difficulty, or note count; the list scrolls independently when it is long. The search has an on-screen keyboard, the sort choices can be opened and selected with a controller, and the list can be expanded with zoom controls. The expanded list scrolls horizontally and zoom changes both card size and grid density: 100% shows three columns of five maps, 20% shows eight columns of up to 20 maps, and 300% shows three maps per column. Press B or Escape to close an open keyboard, sort menu, or expanded list. Saved custom maps have the same search and sort controls, and show **Not rated** when no difficulty is stored. Selecting a repository map provides Play, Preview, and Download JSON actions. Map files exported by the game include their audio (and optional video), so they can be played without extra assets.

Run the site through a web server or GitHub Pages; browser security prevents loading the map files when `index.html` is opened directly as a `file://` URL.
