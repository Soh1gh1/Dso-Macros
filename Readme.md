# BasaMacro — User Guide

BasaMacro is an application for automating repetitive actions in Drakensang Online.
It includes Zoom, Swaps, Autoport, Autoclicker, Automount, and Sell & Melt.

> Use the application responsibly. Automation may violate the rules of a
> third-party game or server. The account owner is solely responsible for how
> the application is used.

## 1. System Requirements

- Windows 10 or Windows 11, 64-bit.
- An installed Drakensang Online client.
- An internet connection for license verification.

BasaMacro and the game must run with the same privilege level. If Drakensang
Online is running as administrator, BasaMacro must also be run as administrator.
Administrator privileges are not required under normal circumstances.

## 2. Installation and Launch

1. Create a separate folder, for example `C:\BasaMacro`.
2. Copy `BasaMacro.exe` into that folder.
3. Double-click `BasaMacro.exe` to launch it.

## 3. License Activation

1. Launch BasaMacro while connected to the internet.
2. Paste the key you received into the **License key** field.
3. Click the activation button and wait for the Profile page to open.

After the first successful activation, the license is bound to that computer.
Do not share the key, `device_identity.dat`, or the entire data folder with
another person. To transfer the license to another computer, contact the
administrator and request a device binding reset.

The license is checked every time the application starts and, during extended
use, approximately once every 120 minutes in the background. Verification
should not interrupt the current action or freeze the interface. If a temporary
network error occurs, the application retries for a limited period.

On the **Profile** page, you can:

- view the license type and its activation and expiration dates;
- see the remaining time;
- show or hide the key;
- copy the key by clicking it;
- refresh the information using the **Refresh** button.

After a manual refresh, a 60-second cooldown prevents accidental request spam
to the server.

## 4. Initial Setup

Recommended order:

1. Open **Coordinates** and select a preset matching the game's resolution, or
   create your own.
2. Check all required coordinates and fill in any missing ones.
3. Configure the required modules and hotkeys.
4. Open **Settings** and, if necessary, assign Pause and module toggle hotkeys.
5. Click **SAVE** if there are unsaved changes.
6. Enable the hotkey system by clicking **START MACRO**.

The bottom button changes its function depending on the current state:

- **START MACRO** — starts the hotkey system;
- **SAVE** — saves all changes across all pages;
- **SAVE & RESTART** — saves an interface scale change and restarts the application;
- **SAVED** — briefly confirms a successful save;
- **STOP MACRO** — stops the hotkey system.

The **CANCEL** button restores all settings to their state before the first
unsaved change. The application asks for confirmation before discarding changes.

If required information is missing, BasaMacro will not start the affected
module. It will open the page containing the problem and highlight the empty
fields in red.

## 5. Recording Hotkeys

1. Click a hotkey field.
2. Press one key or the required combination, for example `Ctrl+F`.
3. The field automatically finishes recording.

Additional actions:

- press `Esc` while recording to restore the previous value;
- press `Backspace` or `Delete` to clear the field;
- Ctrl, Shift, Alt, Tab, Numpad keys, and side mouse buttons are supported.

The same control hotkey cannot be assigned to multiple actions. If a duplicate
is entered, the field briefly turns red. The only exceptions are the **Skill
key**, **Main Skillbar**, and **Macro Skillbar** fields in Skill-Swap, where
duplicates are allowed.

After **START MACRO**, regular hotkeys and module toggles work only while the
Drakensang Online window is active. The main Pause/Resume hotkey and emergency
`Esc` remain globally available.

## 6. Coordinates

Coordinates stores a separate set of coordinates for every preset. The built-in
presets are:

- 1920x1080;
- 2560x1440;
- 3840x2160.

If none of the built-in presets matches your game interface, create a **Custom
preset**. Each custom preset has its own name and an independent set of
coordinates.

- Left-clicking a coordinate field starts point capture.
- Right-clicking clears the coordinate.
- Coordinate fields remain locked until a preset is selected.
- After START MACRO, you can still view Coordinates, but you cannot change the
  active preset or create a new one.

For stable operation, do not change the game's resolution, window mode, UI
scale, or panel layout after recording coordinates. If any of these settings
change, check or record the affected points again.

## 7. Zoom

1. Enter the game world with your character.
2. Open **Zoom**.
3. Select the game process. If it is not listed, click **Refresh**.
4. Set a value from 10 to 50.
5. Enable **Camera lock**.

The slider changes the value in real time. Zoom returns to its default value of
25 every time BasaMacro starts. The increase, decrease, reset, maximum, and
Lock/Unlock hotkeys work only after START MACRO. Changes to hotkey values must
be saved.

If a message says that no pointer was found:

- make sure the character is already in the game world rather than the login menu;
- select the correct process and click Refresh;
- an updated pointer table may be required after a game client update.

## 8. Swaps and Skill-Swaps

- **Add Swap** creates a sequence that replaces items by Bag/Slot.
- **Add Skill-Swap** adds Skill key, Main Skillbar, and Macro Skillbar actions
  to the sequence.
- **Add step** adds another step with a bag and slot number.
- The Enabled/Disabled switch temporarily disables a specific tab.

Inventory key is shared by all modules that open the inventory. When several
consecutive steps use the same bag, BasaMacro does not press that bag again.
A Skill-Swap without Steps can perform only the sequence of switching to the
macro skillbar, pressing the skill key, and returning to the main skillbar.

## 9. Autoport

Create one or more Port presets. For each one, specify:

- a name and hotkey;
- Travel map: Bag and Slot;
- Region, Map, and Difficulty;
- the required Difficulty and Confirm button switches.

Inventory key is shared with the other modules. Return button, Enter map, and
Confirm button are shared between Port tabs within the same coordinate preset,
but they are not carried over between different coordinate presets.

When Difficulty or Confirm button is disabled, the corresponding step is
skipped. Confirm button may remain without a coordinate when that step is not
used.

## 10. Autoclicker

1. Set the **Trigger hotkey**.
2. Set the speed under **Clicks per second**.
3. Save the settings and click START MACRO.
4. Hold the Trigger together with the left, right, or middle mouse button.

A regular click without the Trigger does not start autoclicking. If you first
hold the Trigger and a mouse button, then release the Trigger, autoclicking
continues until the mouse button is released.

## 11. Automount

Under General, set the hotkey, shared Inventory key, Pet bag key, list of Mount
coordinates, and, if needed, the Bag/Slot for the Fast-mount cloak.

- You can add multiple mount points.
- Disabled points are ignored.
- If several enabled points contain coordinates, Automount randomly selects one
  each time it runs.
- At least one point must always remain Enabled.
- If the Automount hotkey is empty, missing mount coordinates are not treated
  as an error.

## 12. Sell & Melt

The General page contains the Sell hotkey, Melt hotkey, Inventory key, Skill
page key, required coordinates, Smeltery, and bags 1–9.

Under **Item Colors**:

- enable the item colors that may be processed;
- add your own colors with **Add custom color**;
- Clear removes the colors from a row after confirmation;
- a disabled row is ignored completely.

The last active bag cannot be disabled. If the required coordinates, bags, or
colors are not configured, the module must not start an action.

## 13. Timings

Each module has its own Timings page. Values are specified in milliseconds, and
the initial delay value is 50 ms.

If the game or its interface does not respond quickly enough, gradually
increase the relevant timing. Do not change every slider at once, as that makes
it harder to determine which stage needs an additional delay.

## 14. Pause, Stop, and Emergency Abort

- **Pause / Resume** temporarily pauses execution without disabling the entire runtime.
- **STOP MACRO** unregisters the hotkeys and stops the runtime.
- `Esc` immediately aborts the current action and unlocks the mouse.

If you click the window's close button while the runtime is active, BasaMacro
hides in the system tray. Double-click the tray icon to restore the window. To
close it completely, select **Exit** from the tray context menu or click STOP
MACRO first.

## 15. Import and Export

Settings can export all macro settings to an INI file and import them into
another installation.

The export intentionally excludes:

- the license key;
- the device identity;
- the interface scale.

An import is applied immediately, but you should review it before clicking START
MACRO. Store backups only in a trusted location and do not edit the INI manually
unless you understand its parameter structure.

## 16. Interface Scale

Available scales are 0.5x, 0.75x, 1x, 1.25x, and 1.5x. A new value is applied
after **SAVE & RESTART**. If the selected scale does not fit on the current
screen, BasaMacro automatically uses the largest smaller scale that fits. When
possible, the application keeps 1x or the previously saved valid option.

## 17. Updating the Application

1. Click STOP MACRO.
2. Close BasaMacro completely through the system tray.
3. Replace the old `BasaMacro.exe` with the new one.
4. Launch the new version and check its version number on the Profile page.

Settings are stored separately from the EXE, so a normal update should not
delete them.

## 18. Data Storage Locations

```text
%LOCALAPPDATA%\BasaMacro\settings.ini
%LOCALAPPDATA%\BasaMacro\device_identity.dat
%LOCALAPPDATA%\BasaMacro\logs\app.log
```

- `settings.ini` contains settings, coordinates, and the saved license key;
- `device_identity.dat` contains the Windows-protected identity of this device;
- `logs\app.log` is the diagnostic log.

Do not share `settings.ini` or `device_identity.dat` with other people. Do not
delete `device_identity.dat` unless you are prepared to request another license
binding reset.

## 19. Common Problems

### A hotkey does not work

- Make sure START MACRO has been clicked.
- Bring the Drakensang Online window into the foreground.
- Check whether Pause is enabled or the required module is disabled.
- Check for fields and tabs highlighted in red.
- Run BasaMacro with the same privilege level as the game.

### An action clicks the wrong location

- Check the active coordinate preset.
- Check the game's resolution, window mode, and UI scale.
- Record the affected points again in a custom preset.

### The license cannot be verified

- Check the internet connection and the system date and time.
- Restart the application and try again.
- If the key is shown as invalid, expired, revoked, or bound to another device,
  contact the license administrator.

### The application disappeared after clicking the close button

If the runtime was active, the application did not close; it was hidden in the
system tray. Double-click its icon near the clock.

### The application crashes or freezes

1. Remember which action was running immediately before the problem.
2. Close BasaMacro completely and launch it again.
3. Reproduce the problem once.
4. Send the following file to the administrator:
   `%LOCALAPPDATA%\BasaMacro\logs\app.log`.

Do not publish the log, settings.ini, or your license key publicly.

## 20. Important Security Rules

- Download BasaMacro only from a source you trust.
- Do not share your license key or local application files.
- Do not download third-party cracks, DLLs, pointer tables, or modified EXE files.
- Do not completely disable Windows Security to run the application.
- Send diagnostic files only to an administrator you trust.

