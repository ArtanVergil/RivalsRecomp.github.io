# Rivals Recomp

A fan-made native PC port of **Sonic Rivals 2**, built by recompiling the original PSP game code into Windows code. **Not an emulator.**

> **Status:** Alpha 0.2: playable, unfinished, may have bugs.
>
> **[⬇️ Download Alpha 0.2](https://github.com/ArtanVergil/ArtanVergil.github.io/releases/tag/v0.2-alpha)**

## 🎮 About

**Rivals Recomp** brings *Sonic Rivals 2*, originally released for the PlayStation Portable (PSP), to Windows.

Instead of emulating the PSP, the game's own code is translated ahead of time into native Windows x64 code, with new Windows graphics (Direct3D 11), audio (XAudio2) and input. The goal is to keep the original experience while taking advantage of modern PCs.

**No game files are included.** You build the game from your own copy of Sonic Rivals 2.

## ✨ Features (Alpha 0.2)

- 🖥️ Native rendering at your screen resolution: 720p, 1080p, 1440p, 4K
- 🎨 Texture filtering and xBR texture upscaling for sharper graphics
- 🚀 Main menu at a full 60 FPS; levels at a steady 30 FPS (like the original game)
- 🎵 Original music and sound
- 💾 Separate save files with card collection tracking
- ⌨️ Keyboard controls you can change in the launcher
- 🚪 Hold **Escape** for 3 seconds to quit
- 🧰 Launcher with picture, controls, saves and game-file settings

## 📸 Screenshots & Gameplay

Screenshots and gameplay footage coming soon.

<!-- Add screenshots here:
![Gameplay](screenshots/gameplay.png)
-->

## 📥 Installation

### Requirements

- Windows 10 or 11 (64-bit)
- Your own copy of **Sonic Rivals 2 (Europe, ULES00940)** as an `.iso` file
- [Python 3](https://www.python.org/downloads/windows/) (tick **"Add python.exe to PATH"** when installing)
- [Git](https://git-scm.com/download/win)
- [FFmpeg](https://www.gyan.dev/ffmpeg/builds/) for the music: download `ffmpeg-release-essentials.zip` and copy `bin\ffmpeg.exe` next to `BUILD.cmd`
- Internet connection for the first build (it downloads the compiler)

### Getting Started

1. Download **RivalsRecomp-Alpha-0.2-source.zip** from the [release page](https://github.com/ArtanVergil/ArtanVergil.github.io/releases/tag/v0.2-alpha).
2. Unzip it, for example to `D:\Games\RivalsRecomp`.
3. Double-click **BUILD.cmd**.
4. Drag your Sonic Rivals 2 `.iso` into the window and press **Enter**.
5. Wait until it says **Done!** (the first build can take 10–20 minutes).
6. Double-click **RivalsRecompLauncher.exe** and click **PLAY GAME**.

Your ISO is only read, never changed.

### Default controls

| Action | Key |
|---|---|
| Move | Arrow keys |
| Jump | Z |
| Attack | X |
| Item | A |
| Special | S |
| Shoulder buttons | Q / W |
| Pause / Start | Enter |
| Select | Right Shift |
| Quit game | Hold Escape 3 seconds |

## 🛠️ Building from Source

The release zip *is* the source. `BUILD.cmd` runs the whole pipeline:

1. Downloads the pinned build tools ([psprecomp](https://github.com/sp00nznet/psprecomp) and Zig 0.14.1)
2. Reads your ISO, checks the game code (BOOT.BIN) against the expected version, and translates it to C
3. Prepares the music from your ISO with FFmpeg
4. Compiles everything into `RivalsRecomp.exe` and builds the launcher

Technical details are in `native/README.md` and `native/PROGRESS.md` inside the zip.

## 🗺️ Roadmap

- [x] Native recompilation of the game code (no emulator)
- [x] Direct3D 11 renderer with native high resolutions
- [x] Audio and music
- [x] Launcher with settings, controls and save files
- [x] Fix crash after a rival wins
- [ ] 60 FPS gameplay in levels
- [ ] Gamepad / controller support
- [ ] Test every stage and game mode
- [ ] Mod support
- [ ] Easier one-click setup

*The roadmap may change as development continues.*

## 🐛 Known Issues

- Levels run at 30 FPS (the original game's own speed).
- 2×2 anti-aliasing can be slow on built-in (integrated) graphics; keep it off there.
- Not every stage and mode has been tested yet.
- Only the European ISO (ULES00940) is supported.
- Keyboard only for now.

## 💬 Bug Reports & Feedback

Found a bug or have feedback?

- Open an issue in this repository.
- Describe the problem and how to make it happen again.
- Include your Windows version and the file `logs\launcher-game.log`.
- Check existing issues before posting a new one.

Feedback from the Sonic community is welcome!

## ⚖️ Disclaimer

Rivals Recomp is an unofficial, fan-made project and is not affiliated with, endorsed by, or sponsored by SEGA or Sonic Team.

*Sonic Rivals 2*, Sonic, and all associated trademarks and original game assets belong to their respective rights holders.

This project does not distribute any game data, game code or assets. You must supply your own legally obtained copy of the game. Please do not share ISOs or the built `RivalsRecomp.exe`, because it contains translated game code.

## 📜 License

The Rivals Recomp source code in the release is under the **MIT License** (see `LICENSE` in the zip). Third-party tools keep their own licenses (see `LICENSES/THIRD_PARTY.md`). This license does not cover Sonic Rivals 2 or any SEGA material.

---

**Rivals Recomp** 💙

*A fan project dedicated to bringing Sonic Rivals 2 to PC.*
