# RPG Project — SFML game and web prototype

A collaborative C++/SFML game prototype with a separate web interface, Python/MongoDB backend experiment, and Windows C++ HTTP client. End-to-end integration has not been verified.

## Repository layout

| Directory | Contents |
| --- | --- |
| `game/src/` | C++ game, animation, player control, enemies, health, backgrounds, fonts, and audio |
| `game/assets/` | Original graphics, maps, fonts, and music |
| `game/Makefile` | macOS-oriented build recipe |
| `frontend/` | HTML/CSS/JavaScript website |
| `backend/` | Flask/PyMongo backend prototype |
| `windows-client/` | Visual Studio solution and C++ HTTP client |
| `third_party/` | Original cURL/MinGW distribution and notices |
| `archive/game-prototypes/` | Historical game source drafts |

## Game features

Sprite animation, movement, map transitions, enemies, collision detection, health display, coin collection and scoring, and music/sound playback.

## Build and run

Install a compatible SFML 2.x development package, Clang, Make, and libcurl. The inherited Makefile is macOS-oriented; include and library paths may need configuration. From the root run `make -C game`. The executable expects `game/` as its working directory for relative asset paths.

The Windows solution is under `windows-client/`. Visual Studio needs an MSVC-compatible cURL library; the bundled MinGW distribution is not a verified MSVC dependency. Configure linker settings as required.

For backend development, install `backend/requirements.txt` and configure `MONGODB_URI` in the environment. Never commit credentials. Authentication, password handling, form handling, and frontend/backend integration require review before deployment. The original backend remains a prototype.

## Cleanup and verification

Original game assets, third-party files and historical source drafts are preserved, excluding OS metadata and generated project outputs. Relative game asset paths and build paths were updated. No gameplay logic was intentionally changed. Compilation and execution have not been independently verified. Verify asset redistribution permissions before reuse.
