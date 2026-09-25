# Rewise firmware updates

`manifest.json` lists the latest firmware for each Rewise device. The Rewise app reads
it every few hours. Each image is attached to a GitHub release and signed with the Rewise
firmware key (ECDSA P-256 over SHA-256). The app checks the size, SHA-256 and signature
before sending an image to a device, and the device checks the signature again before it
installs. Unsigned or modified images are rejected.

Published with `Scripts/publish-firmware.py` from the Rewise project.
