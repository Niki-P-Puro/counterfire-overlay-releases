## Counterfire 3.3.2

Fixes the post-update python313.dll failure when upgrading from older versions by resetting inherited PyInstaller runtime state inside both the updater handoff and the installer before silent relaunch.

Counterfire is an external manual-input tool. It does not access Broken Arrow
files, process memory, network traffic, or screen pixels.
