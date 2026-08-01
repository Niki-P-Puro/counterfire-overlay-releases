## Counterfire 3.3.1

Fixes the post-update python313.dll launch failure by clearing inherited PyInstaller runtime state, waiting for installation to finish, restarting one clean Counterfire process, and removing a duplicate interactive launch entry.

Counterfire is an external manual-input tool. It does not access Broken Arrow
files, process memory, network traffic, or screen pixels.
