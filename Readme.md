# Drakensang Macro

Automation macro for **Drakensang Online** built on **AutoHotkey v1**.

> Disclaimer: This project automates in-game input. Use at your own risk and in accordance with the game’s Terms of Service. The author assumes no responsibility for any consequences.

---

## Features

- **Automount Script**
  - Uses a fast-mount cloak (e.g., DTU/Gwenfara) and the Collector’s Bag to mount quickly.
  - Automatically opens inventory if needed and performs the required equip/unequip steps.

- **Swap Script (SWAP 1–8)**
  - Up to **10 steps** per swap.
  - Each step swaps an item from a chosen **Bag (I–VIII)** and **Slot (1–28)**.

- **Skill swap Script (SKILL 1–4)**
  - Performs a swap sequence, uses a configured skill, then swaps back to the original setup.
  - Optional skillbar switching for macro vs. main gameplay bars.

- **Safety & usability**
  - Works only when the active window is **Drakensang Online**.
  - Temporarily blocks physical mouse input during macro execution to prevent misclicks.
  - **Emergency unlock:** press **Esc** to force-disable mouse blocking.

---

## Instructions

### Main Menu

- **Automount Hotkey**
  - Binds the hotkey that runs the **Automount** routine (only while Drakensang Online is the active window).

- **Toggle Pause ON/OFF**
  - Pause/resume the macro system.
  - While paused:
    - macro hotkeys do not execute actions
    - the main automount hotkey is disabled to prevent accidental triggers

- **Swaps ON/OFF**
  - Enables or disables **Swap** and **Skill Swap** hotkeys globally.

![Main GUI](screenshot1.png)

---

## Swaps Settings

### SWAP 1–8

- **Hotkey**
  - Hotkey that triggers this swap profile.

- **Steps (1..10)**
  - Number of steps executed when the hotkey is pressed.

- **Steps 1–10 (Bag / Slot)**
  - For each step, select:
    - **Bag**: inventory bag index (**1–8**)
    - **Slot**: inventory slot index (**1–28**)

Notes:
- If the game UI feels inconsistent, increase timing values in **TIMINGS**.

![Swap Settings](screenshot2.png)

---

### SKILL 1–4

- **Hotkey**
  - Hotkey that triggers this skill-swap profile.

- **Steps (1..10)**
  - Number of swap steps executed before (and after) using the skill.

- **Steps 1–10 (Bag / Slot)**
  - For each step, select:
    - **Bag**: inventory bag index (**1–8**)
    - **Slot**: inventory slot index (**1–28**)

- **Skill key**
  - Key used to cast the skill.

- **Macro Skillbar (optional)**
  - Key that switches to a dedicated macro skillbar (if you use one).

- **Main Skillbar (optional)**
  - Key that switches back to your main gameplay skillbar after the macro.

How it runs:
1. Ensure inventory is open (opens it if needed)
2. Execute swap steps (equip macro setup)
3. Close inventory
4. (Optional) switch to macro skillbar
5. Cast skill
6. (Optional) switch back to main skillbar
7. Open inventory and swap back (restore original setup)

![Skill Swap Settings](screenshot3.png)

---

### Timings

These values control macro stability. If you experience missed clicks, wrong slots, or UI lag, increase delays.

- **DelayAfterInventory**
  - Delay after opening/closing inventory before continuing.
  - Recommended starting point: **20 ms**.

- **DelayBetweenClicks**
  - Delay between click actions while swapping.
  - Recommended starting point: **20 ms**.

- **DelayAfterSwap**
  - Delay after finishing the swap sequence (useful to let UI settle).
  - Recommended starting point: **20 ms**.

- **DelayBeforeSkill**
  - Delay between finishing the last swap and casting the skill.
  - Recommended starting point: **20 ms**.

- **DelayAfterSkill**
  - Delay after casting the skill before starting the “swap back” phase.
  - Recommended starting point: **20 ms**.

![Timings](screenshot4.png)

---

## Automount Settings

### Hotkeys

- **Inventory Key**
  - Your in-game keybind for opening inventory.
  - Default in many setups: **I** (depends on your game settings).

- **Collector’s Bag Key**
  - Your in-game keybind for opening the Collector’s Bag.
  - Set this according to your in-game configuration.

- **DTU / Gwenfara Cloak (Bag + Slot)**
  - Choose where your fast-mount cloak is located:
    - **Bag**: 1–8
    - **Slot**: 1–28

### Timings

- **DelayAfterActivate**
  - Delay after activating the game window and/or after the macro finishes.
  - Recommended: **20 ms** (increase if your focus switches slowly).

- **DelayAfterInventory**
  - Delay after opening inventory.
  - Recommended: **20 ms**.

- **DelayBetweenClicks**
  - Delay between macro clicks.
  - Recommended: **20 ms**.

- **DoubleClickGap**
  - Gap between clicks for double-click actions (equip/unequip).
  - Recommended: **20 ms** (increase if double-clicks are not recognized).

![Automount Settings](screenshot5.png)

## Coordinates settings

![Coordinates Settings](screenshot6.png)

### (1920x1080) 1080P PRESET ↓

![Coordinates Settings](screenshot7.png)

## Notes & Best Practices

- Calibrate your coordinates and inventory anchors carefully (UI scale and resolution matter).
- Start with **20 ms** delays and increase gradually if your PC or the game UI lags.
- Avoid moving the mouse during macro execution. If something goes wrong, press **Esc**.

---

## Troubleshooting

- **Nothing happens when I press hotkeys**
  - Ensure Drakensang Online is the active window.
  - Check that swaps are enabled (Swaps ON/OFF).
  - Verify your hotkeys are not used by other applications.

- **Clicks go to wrong places**
  - Re-check your coordinates and UI scale.
  - Increase delays in Timings.

- **Mouse is blocked**
  - Press **Esc** to force-disable mouse blocking (failsafe).
