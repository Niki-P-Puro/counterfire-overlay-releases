## Counterfire 3.3.4

Minimap panning now uses a bounded preprocessed render cache and fast drag-only resampling, then restores full Lanczos quality when released. Sustained local benchmarks measured about 61 FPS on cached maps and 58 FPS with a 4096 x 4096 source.

Counterfire is an external manual-input tool. It does not access Broken Arrow
files, process memory, network traffic, or screen pixels.
