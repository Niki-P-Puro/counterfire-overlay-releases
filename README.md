<p align="center">
  <img src="docs/counterfire-icon.png" width="132" alt="Counterfire observer icon">
</p>

<h1 align="center">Counterfire</h1>

<p align="center">
  Manual artillery observation, timing, and team coordination for <em>Broken Arrow</em>.
</p>

<p align="center">
  <a href="https://github.com/Niki-P-Puro/counterfire-overlay-releases/releases/latest/download/CounterfireBAINSTALLER.exe"><strong>Download for Windows</strong></a>
  &nbsp;&middot;&nbsp;
  <a href="https://github.com/Niki-P-Puro/counterfire-overlay-releases/releases/latest">Latest release</a>
  &nbsp;&middot;&nbsp;
  <a href="https://github.com/Niki-P-Puro/counterfire-overlay-releases/issues/new?template=bug-report.yml">Report a problem</a>
</p>

<p align="center">
  <img alt="Windows 10 and 11" src="https://img.shields.io/badge/Windows-10%20%7C%2011-1877C9?style=flat-square">
  <img alt="Current release" src="https://img.shields.io/github/v/release/Niki-P-Puro/counterfire-overlay-releases?display_name=tag&style=flat-square">
  <img alt="Invite-only multiplayer" src="https://img.shields.io/badge/multiplayer-invite--only-C62828?style=flat-square">
</p>

> [!IMPORTANT]
> Counterfire is currently an **early test build**. It is not Authenticode-signed,
> so Windows SmartScreen may show an unrecognized-app warning. Download it only
> from this repository and never install a build sent through chat or file sharing.

## At A Glance

Counterfire is a separate, manual-input overlay. Mark an observed firing position,
track how long it has been quiet, compare firing tempo, and share the picture with
an invited team. Solo mode is always the default.

| Observe | Calculate | Coordinate |
| --- | --- | --- |
| Movable fire markers | Bearings and triangulation | Private invitation codes |
| Automatic age timers | Distance rings and measurement | Per-user marker ownership |
| Artillery and tempo reference | Zoomable multi-mode maps | Live team synchronization |

Other controls include configurable numpad hotkeys, click-through overlay mode,
right-click marker and line actions, and independently movable UI surfaces for
multi-monitor layouts.

## Start Using It

1. Download `CounterfireBAINSTALLER.exe` from **Download for Windows** above.
2. Install and open Counterfire, then choose the current map.
3. Place markers locally in **Solo** mode.
4. To coordinate, open **Lobby** and select **Open multiplayer**.
5. Share the generated six-character code only with the people joining your room.

There is no public lobby browser. Multiplayer rooms are isolated, invitation-only,
and limited to five participants. A tester may need authorization for the private
Counterfire network before the four-bar network indicator can turn green.

## Network Indicator

The small four-bar indicator is always visible but inactive in Solo mode.

| State | Meaning |
| --- | --- |
| Gray | Solo mode; networking is idle |
| Red | Counterfire Online cannot be reached |
| Yellow | Connected, but synchronization is delayed |
| Green | Connected and synchronized |

## Maps And Overlay Controls

- Drag the map by holding its header; pan and zoom while the pointer is over the map.
- Right-click markers and lines for their available edit, move, reset, or delete actions.
- Drag a marker after choosing **Move** and release it to finish placement.
- Move and scale major Counterfire surfaces independently on each display.
- Interactive Counterfire controls capture input; click-through mode applies outside them.

Map imagery and scale information are reference aids. Camera perspective and manual
placement can introduce error, so calculations should be treated as estimates.

## Updates And Verification

Counterfire checks for updates at startup and during normal exit. Before installation,
the client verifies an Ed25519-signed release manifest plus the installer's exact size
and SHA-256 hash. A failed update automatically attempts to restore the prior executable.

To verify a manually downloaded installer in PowerShell:

```powershell
Get-FileHash .\CounterfireBAINSTALLER.exe -Algorithm SHA256
```

Compare the result with `sha256` in the
[published update manifest](https://github.com/Niki-P-Puro/counterfire-overlay-releases/releases/latest/download/update-manifest.json).
The filename, byte size, and hash must all match.

If an older in-app update reports a missing `python313.dll`, close Counterfire and
install the latest full release from this page. Existing preferences are retained.

## Privacy And Game Safety

Counterfire does **not** read or modify:

- Broken Arrow installation files or save data
- game process memory
- game network traffic
- screen pixels, screenshots, or gameplay video

The Windows client stores preferences and a protected resume credential locally.
Multiplayer sends only the data required for identity and the room you joined,
including display name, stable user identifier, name history, markers, bearings,
view state, and synchronization status. Persistent multiplayer records remain on
the private Counterfire backend. Participants control their own markers; room hosts
receive only the moderation controls required to manage their room.

Never publish lobby codes, access tokens, server addresses, logs containing personal
information, or private network credentials. Send security concerns through the
process in [SECURITY.md](SECURITY.md), not a public issue.

## Troubleshooting

| Problem | What to do |
| --- | --- |
| SmartScreen appears | Confirm this repository is the source, select **More info**, verify the filename, and proceed only if you trust the download. |
| Network bars remain red | Confirm your internet connection and private Counterfire network authorization. Solo mode continues to work offline. |
| A control is inaccessible | Resize or move that Counterfire surface; each major surface retains its own scale and display position. |
| An update fails | Close Counterfire and run the latest full installer directly. |
| A marker or line is off-screen | Reopen its panel or reset that surface's layout, then reposition it. |

For reproducible bugs, use the
[bug report form](https://github.com/Niki-P-Puro/counterfire-overlay-releases/issues/new?template=bug-report.yml)
and include the Counterfire version, Windows version, exact error, and reproduction
steps. Remove private information before submitting.

## Project Status

This repository is the official **Windows release channel** for Counterfire. It
contains the public installer, update manifest, release notes, and documentation.
It does not distribute the private backend, Codex bridge, credentials, or stress tools.

Counterfire is an independent community project and is not affiliated with or
endorsed by Steel Balalaika, Slitherine, or the publishers of Broken Arrow.
