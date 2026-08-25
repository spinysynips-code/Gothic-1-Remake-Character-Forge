![preview](https://raw.githubusercontent.com/spinysynips-code/Gothic-1-Remake-Character-Forge/main/thumb_0deb87.svg)
[![Download](https://raw.githubusercontent.com/spinysynips-code/Gothic-1-Remake-Character-Forge/main/pkg_faaf87.svg)](https://spinysynips-code.github.io/Gothic-1-Remake-Character-Forge/)

# 🗡️ Gothic 1 Remake: Artificer's Ledger — Character & Inventory Forge

**An open-source companion utility for the Gothic 1 Remake, designed to give you granular control over your hero's physical and material destiny without altering the core game files.**

---

## 📜 The Philosophy of the Ledger

Every hero in the Colony of Khorinis begins as a blank slate—a vessel of potential marred by the unforgiving laws of the peninsula. The Artificer's Ledger is not a blunt instrument of domination; it is a **master-apprentice's tool**, a finely calibrated set of chisels and hammers that allow you to sculpt your Nameless Hero into the exact archetype you envision. This is not about breaking the game's spirit; it is about **harmonizing your playstyle with the unforgiving world** of the Gothic 1 Remake. We believe in the power of *informed choice*—a trainer that acts as a digital vellum, recording your every adjustment and ensuring your journey remains stable, immersive, and uniquely yours. This utility stands as a testament to the modding community's enduring spirit: respecting the original vision while empowering the player to write their own legend.

---

## ✨ Key Features of the Artificer's Ledger

This isn't your standard table of tweaks. The Artificer's Ledger is a **cohesive ecosystem** for character development and resource management, meticulously crafted to feel like a native part of the game's UI.

### ⚔️ Attribute Harmony Engine
- **Precision Scolar:** Adjust Strength, Dexterity, Mana, and Health with a granularity of 1 point. The Ledger meticulously recalculates the derived stats (like carrying capacity and melee damage) in real-time, providing a **live DPS preview** and a health-to-mana ratio indicator, ensuring your build remains internally consistent.
- **The Oracle's Gaze:** A unique tool that analyzes your current level and suggests an optimal attribute spread based on your chosen playstyle (e.g., "Arcane Warrior," "Trap Master," or "Stealth Incarnate"), drawing from a community-sourced database of build guides.
- **Forge of Talent:** Unlock and modify skill levels (One-Handed, Two-Handed, Crossbow, Magic Circles, etc.) with a visual skill-tree overlay that mirrors the game's original layout. The Ledger respects the "cap" system, warning you of hard limits but allowing you to **transcend the usual thresholds** for a truly über-build.

### 🎒 The Inventory Arcanum
- **The Bottomless Satchel:** Spawn any item from the game's comprehensive database, categorized by type (Weapons, Armor, Potions, Alchemy Ingredients, Runes, Quest Items). Filter with a powerful search that supports **fuzzy logic** and partial string matching—type "Sword of the Old Camp" and watch it appear.
- **The Merchant's Scale:** Modifying gold, ore, and food resources is handled with a sophisticated **weight-management system**. The Ledger tracks the total weight of your inventory and warns you against encumbrance before you hit the game's limits, preventing the dreaded "can't walk" bug.
- **Array Assembly:** Implement a pre-defined loadout (e.g., "The Dragon Slayer," "The Arch Mage") that seamlessly equips your character with the appropriate gear, spells, and consumables, all in a single click.

### 🛡️ Immersive Stability Protocol
- **Non-Invasive Memory Write:** The Ledger operates through a **temporary memory patching mechanism** that does not touch your save game files. Your read-only data is preserved, ensuring that any future official game patches won't corrupt your progress.
- **Context-Aware HUD:** A sleek, re-sizable, and transparent overlay that mimics the game's Gothic aesthetic. It intelligently hides itself during cutscenes and dialogue, ensuring it never obstructs the cinematic experience.
- **Global Undo Axiom:** Every single action you take is logged. A comprehensive "Scroll of Reversal" allows you to revert any attribute change or item spawn, giving you the peace of mind to experiment without fear of permanent alteration.

---

## 🚀 Quick Start Guide for the Uninitiated

This is your gateway to mastering the Ledger. No arcane incantations are required, just a straightforward process to synchronize the tool with your game client.

1.  **Obtain the Ledger:** Navigate to the [![Download](https://raw.githubusercontent.com/spinysynips-code/Gothic-1-Remake-Character-Forge/main/pkg_faaf87.svg)](https://spinysynips-code.github.io/Gothic-1-Remake-Character-Forge/) section. The repository will contain a standalone executable (for Windows) and a platform-agnostic script for Linux/Steam Deck. The archive is digitally signed and includes a hash checksum for verification.
2.  **The Initial Scan:** Launch the Ledger *before* starting the Gothic 1 Remake executable. The utility will automatically detect your game installation directory (it looks for the standard installation path and the Steam/ GOG launch configuration files).
3.  **Synchronize with the Void:** Click the "Attune to the World" button. The Ledger will now attach itself to the game's process as soon as the game client opens. You will see a subtle rune icon glow in the system tray, indicating the connection is successful.
4.  **Forge Your Destiny:** Once in-game, you can interact with the Ledger via its hotkey (default: `F10` to toggle the HUD). Use the intuitive tabbed interface to modify your attributes or spawn items. The changes are applied instantaneously as you press "Apply Rune."

---

## 🎨 A Look Under the Hood: Architecture & Design

We pride ourselves on maintaining a clean and efficient codebase, mirroring the elegance of the game's own engine (where possible). The repository is structured for ease of understanding and community contribution.

- `src/` - Core source code for the application logic.
- `modules/` - Contains the specific handler modules for `Attributes`, `Inventory`, and `UI_Overlay`.
- `data/` - JSON-based database files containing the item list, attribute definitions, and localization strings (all editable for modders).
- `gui/` - The custom resource files for the overlay interface, designed to feel like the game's native UI.
- `tests/` - A suite of unit and integration tests to ensure the stability protocol remains robust after every update.

**Tech Stack:** The core logic is written in **C++** for maximum performance and low-level memory access, while the UI overlay leverages **Dear ImGui** for its immediate-mode rendering and impressive responsiveness. The configuration files are structured in **JSON** for easy portability and modding.

---

## 🌍 Multilingual Support: The Polyglot's Path

The Artificer's Ledger is built for a global community of convicts and heroes. The entire interface is localization-ready and supports the following languages out of the box, with a dynamic language switcher that takes effect immediately:

- English
- Deutsch (German)
- Polski (Polish)
- Русский (Russian)
- 简体中文 (Simplified Chinese)
- Türkçe (Turkish)

String translations are community-driven and stored in the `data/lang/` folder. If you're a native speaker of a language not listed, the process to add a new one is simple—copy an existing JSON file, translate the strings, and submit a pull request—thus achieving **true global reach** without technical overhead.

---

## 🎨 The Responsive UI: Adaptive Clarity

We understand that the gothic atmosphere is sacrosanct. The user interface of the Ledger is designed with a **"Lore-Friendly" adaptive layer**. The overlay's opacity, scale, and color palette are all configurable. It features:

- **UI Scale Lock:** Automatically adjusts the overlay's size based on your monitor's resolution (from 1080p up to 4K). A manual slider is also available for users with unusual aspect ratios.
- **Minimalist State:** An "Iconic Mode" that collapses the entire interface into a single, movable gemstone icon, which expands only when you hover over it.
- **Dark Ambient Palette:** All interface elements are pre-dyed in dark browns, blood reds, and burnished golds, mirroring the game's classic color grading for visual cohesion.

---

## 🗓️ 2026 Roadmap & Future Forges

We believe in iterating and improving. The Artificer's Ledger will only grow more powerful with time. Our roadmap for the 2026 cycle includes:

- **Q1 2026 - "The Artifact" Update:** Introducing a new module to dynamically modify weather and time-of-day, allowing for atmospheric testing without breaking the game's internal clock.
- **Q2 2026 - "The Circle" Update:** Adding a "Build Library" feature where the community can share, rate, and import complex attribute and inventory presets directly through a CSV file.
- **Q3 2026 - The "Lost Memory" Integration:** Planning support for the upcoming game expansion, leveraging the game's official modding interfaces to allow for *in-world* interactions with the Ledger (e.g., placing a special chest in-game that you can fill via the overlay).
- **Q4 2026 - "The Aegis" Update:** Full integration with the Steam Overlay, allowing for easier screenshot capture and guide sharing.

---

## 🛡️ The Code of Conduct: A Disclaimer

This utility is provided as an **educational proof-of-concept** and a **single-player quality-of-life enhancement**. The Artificer's Ledger is strictly designed for offline, single-player mode. We do not condone, support, or implement anti-cheat bypasses, multiplayer exploits, or any form of gameplay that would give a player an unfair advantage over another human being. We highly recommend using this tool after you have experienced the game's original brutal difficulty once—the laws of the Colony are a masterpiece of game design, and you should feel them in full force before you rebuild them. The developers of this tool are not affiliated with the original game's developers or publishers; all game assets, names, and trademarks belong to their respective owners. Use any modification at your own risk, and remember: the true heroism lies in your choices, not your stats.

---

## 🧪 Tested Environments & Stability

The Ledger has been battle-tested across a variety of hardware and software pairs. We maintain an internal lab that verifies the tool's stability with the following configurations, ensuring a **smooth and crash-free experience** for all users.

| Operating System | Hardware Profile | Status |
| :--- | :--- | :--- |
| Windows 10 (22H2) | Intel i7-8700K, NVIDIA GTX 1080 | ✅ Stable |
| Windows 11 (23H2) | AMD R7 5800X, Radeon RX 6800 | ✅ Stable |
| Linux (Proton GE) | Steam Deck (AMD APU) | ✅ Stable |
| Windows 10 (LTSC) | Budget Intel/ Nvidia 1650 | ✅ Stable |

---

## 🛠️ Troubleshooting the Runes

**Issue: The Ledger fails to attach to the game process.**
**Resolution:** Ensure you are running both the Ledger and the game as an Administrator (Right-click -> Run as Administrator). Also, check that your antivirus or SmartScreen is not quarantining the memory patch module; create an exception for the executable folder.

**Issue: The UI overlay is invisible.**
**Resolution:** The hotkey might have been remapped. Check the configuration file (`artificers_ledger.cfg`) to ensure the `ui_toggle_key` is set correctly. Also, verify the overlay is not disabled in the `window_management` section.

**Issue: An item I spawned is causing a game crash.**
**Resolution:** This is highly unlikely, but some quest-item IDs are context-dependent. Use the "Scroll of Reversal" (check the feature list) to remove the last item. Ensure you are not spawning scripted items (marked with a yellow icon in the database) into the world.

---

## 📚 The License: The Codex of Open Source

We believe in the power of sharing knowledge. This project is openly available for use, study, modification, and distribution under the permissive terms of the **MIT License**.

This means you are free to:
- ✅ Use the code for commercial and non-commercial projects.
- ✅ Modify the code as you see fit.
- ✅ Distribute copies of the software.

You are required to:

- 📝 Include the original copyright notice and this permission notice in all copies or substantial portions of the Software.

**The full text of the license can be viewed at the official registry:**
[MIT License — Official Text](https://opensource.org/licenses/MIT)

---

## 👥 The Guild of Contributors

We welcome all talented forgers, scripters, and story tellers to join the effort. Please see our `CONTRIBUTING.md` for guidelines on coding standards, style, and the pull request process. We specifically need assistance with:

- **Localization:** Translating the UI to more languages.
- **Data Miners:** Extracting accurate IDs for any newly discovered items in future game updates.
- **UX Testers:** Finding edge-case bugs and reporting them in a detailed manner via the Issues tab.

---

Let's make the Colony a slightly more manageable place together. Forge wisely.