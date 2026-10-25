# CoP-Gunslinger-Burer-Nerf

Gunslinger Mod - Burer Gameplay Nerf / Balance Tweak

This repository contains a modified gameplay script for the S.T.A.L.K.E.R.: Call of Pripyat - Gunslinger Mod that rebalances the Burer mutant. The official "Weakened Burers" option included in the mod launcher only reduces the mutant's base health pool while keeping its highly aggressive, scripted telekinetic mechanics active.
This script addresses common community frustration by fundamentally reworking the Burer's scripted behaviors, disabling its permanent bullet-blocking shield, and removing weapon-disarm mechanics.

Prerequisites

• Official "Weakened Burers" Option: You must have the official "Weakened Burers" (weakened_burer) option checked and enabled inside the game's launcher (CheckUpdates.exe). This script builds upon that layout to ensure compatibility and dynamic execution.
• Backup Recommendation: It is highly recommended to create a backup copy of your existing gamedata folder or related game scripts before applying these changes.

Installation / Override Method

Since the Gunslinger launcher utilizes an integrity check tracking file sizes and CRC32 checksums of .db archives, this tweak uses the standard Gamedata Override approach to bypass static system file validation safely.
1. Navigate to your main Gunslinger Mod installation folder.
2. Locate the fsgame.ltx file, open it with a text editor, and ensure the $game_data$ flag is enabled by setting it to true| true:text
$game_data$ = true| true| $fs_root$| gamedata\
Use code with caution.
3. Inside the main directory, create a new folder named gamedata (if you do not have one already), then create a subfolder named scripts.
	• Target Path: .../Gunslinger/gamedata/scripts/
4. Place the modified gunsl_burer.script file into that folder.
5. Launch the game normally via the standard executable or launcher. The X-Ray engine will dynamically read the modified script from the external directory with high priority, leaving the original .db archives unmodified and avoiding file verification crashes.
