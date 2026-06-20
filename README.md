<div align="center">

<img src="https://avatars.githubusercontent.com/u/193316573?s=200&v=4" width="120" height="120" style="border-radius: 50%;" />

# getAOSP

### Custom ROM development for devices nobody else wants to touch.

![Android](https://img.shields.io/badge/Android-16-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Build](https://img.shields.io/badge/Builds-Unofficial-7C3AED?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-22C55E?style=for-the-badge)
![License](https://img.shields.io/badge/License-GPLv2-blue?style=for-the-badge)

</div>

<br>

Most of what's here exists because something was officially declared dead, broken, or "not happening." We tend to disagree with that conclusion. This page is the index for everything currently being built, ported, or kept alive.

<br>

## 📦 Repositories

Active ROM projects and where to find them.

| Project | Device | Android | Type | Thread |
|---|---|---|---|---|
| **LineageOS 23.2** | POCO F7 Ultra (`miro`) | 16 (QPR2) | Unofficial · Vanilla | [XDA Thread](#) |
| **Lunaris AOSP** | POCO F7 Ultra (`miro`) | 16 (QPR2) | Unofficial · GMS | [XDA Thread](#) |

<sub>Swap the `#` links above for your actual XDA thread URLs once posted.</sub>

<br>

## 🔧 Under the Hood

Most `miro` development was stalled by broken Xiaomi source releases — half-finished blobs, missing hardware baseline data, and trees that didn't build clean out of the box. The breakthrough behind both ROMs above came from reconstructing a working hardware baseline from scratch, bypassing the broken upstream pieces entirely.

That fix is what unblocked everything else. Once the baseline was solid, porting additional ROMs on top of it — rather than fighting the same broken source twice — became realistic instead of theoretical.

<br>

## 🛠️ Tech Stack

<div align="center">

![](https://skillicons.dev/icons?i=androidstudio,linux,git,github,bash,python,cpp,kotlin)

</div>

**Core skills applied across these projects:**

- AOSP & LineageOS build system (`repo`, `soong`, manifest management)
- Kernel bring-up and device tree maintenance
- Vendor blob extraction, patching, and hardware baseline reconstruction
- Custom recovery porting (Lineage Recovery / TWRP)
- GPL compliance — full kernel source publishing for every release
- Cross-ROM feature porting (CAF patches, PixelProps, GMS integration via Project Clover, etc.)
- Community support & triage on XDA-Developers

<br>

## 🧵 Threads

Where releases, changelogs, and bug reports actually live:

- [`miro`] LineageOS 23.2 — XDA thread (link pending)
- [`miro`] Lunaris AOSP — XDA thread (link pending)

<sub>Bug reports without logs get politely ignored. Bug reports with logs get fixed.</sub>

<br>

## ✨ Extras

- 🚲 Currently aiming to out-pedal every merge conflict.
- ☕ If a build helped you, a "Thanks" on the XDA thread does more than you'd think.
- 🤝 PRs and device tree contributions are always welcome — open an issue first for anything non-trivial.

<br>

<div align="center">
<sub>Built by <b>getAOSP</b> · No GApps were harmed in the making of the Vanilla build.</sub>
</div>
