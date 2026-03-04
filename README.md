# Modes Picker v1.0.2 for Picked Crews

## 1. Roll Phase:
1. Download the [Script](https://github.com/Frittutisna/Picked-Crews/blob/main/Script.py)
2. Find the [Spreadsheet](https://docs.google.com/spreadsheets/d/1VxqdLA3T_coSpoFXhSnaNgAk3BZ2XQ7drvNgcUf6OXQ/edit?gid=269142575#gid=269142575), then click `File > Download > Microsoft Excel (.xlsx)` in the top-left
3. Gather both in the same folder, then open said folder in CMD/VSCode. Make sure said folder only contains the Script and the Spreadsheet
4. Run the Script. By default, it rolls 50 modes with no minimum Sports Modes. To change this, do one of the following (the latter takes precedence):
    * Edit `DEFAULT_MODES` and/or `DEFAULT_SPORTS` in the `# Configurations` section of the Script
    * Add the flag(s) `--modes [1+]` and/or `--sports [1-4]` when running the Script (e.g., `python Script.py --modes 120 --sports 1` if you want to roll 120 modes with 1 guaranteed Sports Mode)
5. Find `Rolls.txt` and copy-paste it in `#tour-information`

## 2. Protect Phase:
Each team picks one mode to pick and protect for themselves. This mode cannot be banned by the other team

## 3. Ban Phase:
Each team bans unprotected modes for the other team so that the number of players in the banned modes equal the number of team members

## 4. Pick Phase:
Each team picks unprotected, available modes for themselves so that the number of players in the picked modes equal the number of team members

## 5. Roll Phase:
Round 1 will be played using Team A's picks, while Round 2 uses Team B's picks and Round 3 takes from the rest. To do so, before starting Round 1:
1. In the same folder as the Script, Spreadsheet, and `Rolls.txt`, write `Setup.txt`. Use `Example-Setup.txt` as reference:
    * `Size` sets the number of team members
    * `Protected` lists the IDs (first number in each row of `Rolls.txt`) of protected modes
    * `Banned` lists the IDs of banned modes, bracketed by bans from Team A and B respectively
    * `Picked` lists the IDs of picked modes, bracketed by picks from Team A and B respectively
2. Open said folder in CMD/VSCode, then run the Script again without flags
3. Find `Results.txt` and copy-paste it in `#tour-information`