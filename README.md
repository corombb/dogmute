# Muzzle Mic

A Vencord / Vesktop theme that replaces the microphone mute button with a dog. Muting puts a muzzle on it. Unmuting takes it off.

<p>
  <img src="assets/dog-unmuted.svg" width="64" alt="Unmuted: dog with its snout free">
  <img src="assets/dog-muted.svg" width="64" alt="Muted: dog wearing a basket muzzle">
</p>

The muzzle flies in and off with the same timing and easing as Discord's own mic animation. The dog uses Discord's icon colors: grey normally, red when muted.

## Install

**Online theme (updates automatically)**

1. In Discord, open **Settings → Vencord → Themes → Online Themes**.
2. Paste the raw link to the theme file:
   `https://raw.githubusercontent.com/<your-user>/<your-repo>/main/MuzzleMic.theme.css`
3. Make sure the theme is enabled.

**Local file**

1. Open **Settings → Vencord → Themes → Local Themes** and click **Open Themes Folder**.
2. Drop `MuzzleMic.theme.css` into that folder.
3. Tick **Muzzle Mic** in the list.

## Settings

Edit the `:root` block at the top of the file (or override it in QuickCSS):

| Variable | Default | What it does |
|---|---|---|
| `--muzzle-mic-speed` | `1` | `2` plays at half speed, `0.5` at double speed. |
| `--muzzle-mic-from-x` / `--muzzle-mic-from-y` | `45%` / `-40%` | Where the muzzle flies in from. `60%` / `0%` = from the front, `0%` / `-60%` = from above, `0%` / `0%` = fade only. |

## Notes

- The theme finds the mic button by its English label, "Mute". For a client in another language, replace `aria-label="Mute"` in the file with your client's label for that button. To find it, right-click the mic button, choose **Inspect**, and look for `aria-label`.
- Discord's own mic drawing is hidden but keeps running underneath, so the button works exactly as before.
- Both the system reduced-motion setting and Discord's **Reduced Motion** option switch the animation off.
