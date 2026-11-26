# Publishing a new FeatherLite version

This repository only holds the README and this file. The program itself is published as a **release**
(the exe is attached to the release, not stored in the repository).

1. On your PC, change `VERSION = "x.y"` in `featherlite_app.py` to the new number. It must be higher than
   the last release.
2. Run **make_release.bat**. It builds `dist\FeatherLite.exe` and `dist\FeatherLite.exe.sha256`.
3. On GitHub open **Releases > Draft a new release**.
4. Click **Choose a tag**, type `v` + the version (for example `v3.7`), then **Create new tag**.
5. Give it a title such as `FeatherLite 3.7` and write what's new in the description - users see this text
   when they update.
6. Drag in **both** files: `FeatherLite.exe` and `FeatherLite.exe.sha256`.
7. Leave **Set as a pre-release** and **Draft** unticked, then click **Publish release**.

Rules the updater relies on:
- The tag number must be higher than what people have installed.
- The exe must be named exactly `FeatherLite.exe`, with `FeatherLite.exe.sha256` next to it.
- The repository must stay public.
- Turn on two-factor authentication for the GitHub account - anyone who can publish a release can
  push an update to everyone.

Keep your own copy of the source:
- The source code (`featherlite_app.py`, `make_release.bat`, `build_exe.bat`, the icon) is NOT on GitHub.
  Back the whole folder up somewhere safe (cloud drive or external disk). If you lose it, you can't build
  new versions.
