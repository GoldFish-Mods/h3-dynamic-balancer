### H3 Dynamic Balancer
(aka h3Balancer)

**Mod Version:** **0.1.4a** *(early testing stage!)*  
**Authors:** GoldFish, daemon_n

A mod that dynamically adjusts the pacing and progression of AI players.

Based on the overall army strength of the human player compared to enemy forces, the algorithm automatically buffs or nerfs the AI, adapting your opponents to match your pacing.

#### Changelog:

**0.1.3a**
- Added mod configuration files: `h3Balancer_preset.ini`, `h3Balancer.ini`
- Added in-game chat commands to control the mod
- Updated the balance control algorithm
- Various fixes and minor improvements
- fix for a critical issue in the code (0.1.4a)

**0.2a** (Build ID: 9.9.2.211)

- Added compatibility with the **HumanAI** mod and other third-party modifications.
- Improved balancer compatibility with the HumanAI handicap.
- Fixed compatibility with WoG options.
- Various logging improvements.

#### What this mod helps with:
- Smoothing out balance issues in modpacks with altered creatures, magic, and hero skills/specialties.
- Leveling the playing field on maps where terrain layout or economic imbalance gives the AI an overwhelming advantage as early as the first month.

#### How it works:
1. Every day, the script compares the human player's total army strength against each individual AI player using a hidden battle simulation and mathematical formulas, estimating the power ratio with up to 70–80% accuracy.
2. When a power gap is detected, the script adjusts the AI's progression rate (resources, creature growth, and daily regenerating points). If the AI is stronger than the human player, it receives penalties to slow down its expansion; if it falls behind, it receives bonuses.
3. The script only affects AI players and never alters the human player.

> **Important Note:** Army strength evaluation takes place under standard conditions on neutral terrain using the engine's built-in quick combat (auto-combat) algorithms.

#### Recommendations:
To get the most out of this mod, we recommend playing on difficulties above 130% alongside the **Human AI** mod. This allows the AI to match your tempo and become a worthy opponent without steamrolling you throughout the game.

This mod also gives you a fighting chance to rebuild your army after losing a major battle, offering a second chance at a comeback. However, the ultimate outcome still depends on the tactical situation on the adventure map.

---

#### Compatibility:

- Recommended ERA build version: 2.2+
- ERA 3.9+, Era Erm Framework
- Added compatibility with **HumanAI** (as of version 0.2a).
- **Warning!** This mod has not yet been tested with other third-party modifications (such as ACM, Difficulty Mod, etc.).

Any discovered compatibility issues will be addressed in upcoming updates whenever possible.

#### Current Version Notes (0.2a):

- Currently, only **part of the planned functionality** is implemented. Right now, the mod regulates game pacing strictly through resources. While it has yet to reach its full potential, it already functions as a solid progression balancer between you and the AI.
- In the current version, pacing is balanced linearly — the script continuously tweaks the AI players' resource income. This creates fairly strict control boundaries and currently lacks a natural element of randomness in how opponents develop over the course of a match.
- Since this is an early release, it requires further testing and fine-tuning. If needed, you can manually adjust the balance offset in `\Mods\H3 Dynamic Balancer\h3Balancer_preset.ini` by changing the `adjustmentAmount` parameter within the range of `[-100 (human advantage) ... 100 (AI advantage)]`. *(If you want to tweak this value mid-game, simply edit the parameter and type `bal conf` into the in-game chat to reload the configuration files).*

Additional mod settings with detailed descriptions for each are also available in the `h3Balancer_preset.ini` file.

#### Feedback:

You can share your ideas or report bugs in the mod's thread on the [ERA Discord server](https://discord.com/channels/665742159307341827/689568017285120228).

**Have fun!** ;)
