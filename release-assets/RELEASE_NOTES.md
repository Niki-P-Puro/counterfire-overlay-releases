## Counterfire 3.2.4

Fixes Windows update error 5 caused by a lingering one-file launcher process. The updater now waits for every Counterfire process using the installed executable, handles stale locks with a bounded fallback, and includes the dedicated lobby host in replacement lock handling.

Counterfire is an external manual-input tool. It does not access Broken Arrow
files, process memory, network traffic, or screen pixels.
