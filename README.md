# Vault Rush

First-person parkour game.

- `VaultRushDEV.html` - the whole game in one file. Double-click it to play in any modern browser.
- `main.js`, `package.json` - wrap the game in an Electron window so it can be built into a Windows `.exe`.

## Controls

Default keys (all rebindable in Options):

| Action | Key |
|---|---|
| Move | W / A / S / D |
| Look | Mouse |
| Jump (hold to vault over tall obstacles) | Space |
| Sprint | Shift |
| Slide (hold) | C or Ctrl |
| End run / reset (hold) | R |
| Screenshot | T |

## Level editor

`editor/index.html` is a standalone 3D level and obstacle editor (open it in a browser; it loads three.js from a CDN).
Export a level, then in the game press `6` on the main menu and use the IMPORT LEVEL button to play it.

## Build the exe

**Automatically (GitHub Actions):** every push to `main` builds `Vault-Rush.exe`.
Open the repo's **Actions** tab, pick the latest run, and download the **Vault-Rush-windows** artifact.
Push a tag like `v1.0.0` and the exe is also attached to a GitHub Release.

**On your own machine** (needs Node.js 18+):

```
npm install
npm start        # run the game in an Electron window
npm run dist     # builds dist/Vault-Rush.exe (portable, no installer)
```

F11 toggles fullscreen in the exe.

Note: Wavedash leaderboards and achievements only work when the game runs on Wavedash, not in the exe.
