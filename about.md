# Versus first installer

Version 1.1.0, displayed as **Versus Installer**, with the existing Versus logo.

Build: `python scripts/build_allplatform.py --ndk <NDK> --installer` (also run by
`deploy-05xx.ps1`). Output: `bootstrap-dist/tipp7.versus-Installer.geode`
(Windows x64 + Android32 + Android64). The deploy script also publishes it to
`https://54.180.43.196/updates/bootstrap/tipp7.versus.geode`.

Install this `.geode` in Geode, then open Versus. The updater downloads the
current full package from the Versus server, verifies its size and SHA-256,
installs it and restarts Geometry Dash. Membership is decided by the server.

The installer uses `tipp7.versus`, the same ID/save folder as the complete mod,
so it replaces it. Installing it manually also repairs a mobile install that is
stuck on an older updater ("Previous update has not completed"): the installer
reconciles the leftover update journal at launch and installs the latest full
version. No match logic, cosmetics or sounds are bundled.
