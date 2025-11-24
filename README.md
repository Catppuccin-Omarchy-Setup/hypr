# Hyprland Config (But Spicier)

Yes, this is an even more opinionated Hyprland setup than Omarchy. I need this setup to function properly and to not loose my sanity over the keybinds. Similar to windows or End_4's config.
Feel free to try it out!

## Installation
1. Copy all files to your hypr folder:
    ```bash
    ~/.config/hypr
    ```
2. Update your keyboard layout in [`input.conf`](./input.conf)
3. Create a `monitors.conf` file and add your monitor config (see: https://wiki.hypr.land/Configuring/Monitors/ for details)
4. Install the Bibata cursor:
    ```bash
    yay bibata-cursor-theme-bin 
    ```

## Changed Keybinds
- `SUPER`: open Walker (should be the default honestly)
- `SUPER`+`V`: Walker clipboard history instead of Omarchy’s old picker (similar to windows)
- `SUPER`+`SPACE`: Omarchy menu cause this is so much easier
- Core window shenanigans: `SUPER`+`Q` to kill, `SUPER`+`F` for force-fullscreen, `SUPER`+`D` to maximize, `SUPER`+`Y` to toggle floating.
- Workspace ergonomics: `SUPER`+`SHIFT`+number sends the focused window to that workspace, `SUPER`+`SHIFT`+`S` punts it into the scratchpad.
- App shortcuts tuned for my flow:
  - `SUPER`+`T` opens `$TERMINAL` in the cwd of the active Omarchy pane.
  - `SUPER`+`E` launches Nautilus, `SUPER`+`W` opens Firefox, `SUPER`+`N` jumps to my editor helper, `SUPER`+`C` pulls up Cursor.
  - `SUPER`+`O` = 1Password, `SUPER`+`SHIFT`+`O` = Obsidian, `SUPER`+`M` launches the Omarchy activity TUI, `SUPER`+`SHIFT`+`D` boots lazydocker.
  - `SUPER`+`A` ChatGPT, `SUPER`+`SHIFT`+`A` Grok, `SUPER`+`SHIFT`+`G` is a sticky WhatsApp webapp. (I honestly dont use these)

## Visual Changes
- Waybar gets a mild blur via `layerrule = blur,waybar` so panels blend into the wallpaper.
- Gesture tweaking: 3-finger swipe/pinch for move/fullscreen, 4-finger gestures for workspace sweeps, floating toggles, and scratchpad entry with tuned swipe distances and locks.
- `general` section tightens gaps (4/5 px) with a dramatic `gaps_workspaces = 50`, enables border snapping, and keeps `allow_tearing = true` for immediate rulesets.
- Rounded windows (`rounding = 8`) plus gentle dimming of inactive/special surfaces for better focus.
- Animations lean into more expressive bezier curves for windows, layers, fades, and workspace transitions, so everything feels lively but not floaty.
- Cursor polish: `hyprctl setcursor Bibata-Modern-Classic 22` on startup plus `cursor.hotspot_padding = 1` for precise clicks.

## Everything Else
- Base config still sources the Omarchy defaults (`~/.local/share/omarchy/default/...`) but overlays custom files (`monitors.conf`, `bindings.conf`, `looknfeel.conf`, etc.) so upgrades don’t wreck tweaks.
- Special workspace `scratchpad` automatically corrals 1Password thanks to a window rule and autostarts the app for instant vault access.
- `envs.conf` remains intentionally empty—use it to inject per-session variables whenever needed.

## Credits
- Hyprlock visuals/ideas borrowed from end_4’s legendary dotfiles. Huge thanks to [end_4](https://github.com/end-4/dots-hyprland) for the inspiration and assets. 

