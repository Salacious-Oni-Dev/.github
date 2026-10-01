# Oxygen Not Included simulation SDK

> [!WARNING]
> **Early alpha release (`v0.1.0-alpha.1`).** This is the first public release: expect bugs,
> missing features and changes between releases, including to the API. It replaces one game file,
> supports one game build (744825), and runs on Windows only. Keep backups of saves you care
> about, and report problems in the issues of the repository they concern.

An open replacement for Oxygen Not Included's native simulation library, a managed API that
lets mods use what it adds, and gameplay mods built on that API as working examples. Heat that
is moved instead of deleted, rooms whose air is a real mixture of gases, pipes with real
pressure, gas dissolved in liquids, and phase change that costs and releases real latent heat.

<p>
<a href="https://github.com/Salacious-Oni-Dev/oni-flagship-mods#showcase-videos"><img src="https://github.com/Salacious-Oni-Dev/oni-flagship-mods/raw/main/media/airloop.gif" width="24%" alt="A nitrogen-oxygen air loop"></a>
<a href="https://github.com/Salacious-Oni-Dev/oni-flagship-mods#showcase-videos"><img src="https://github.com/Salacious-Oni-Dev/oni-flagship-mods/raw/main/media/phaseloop.gif" width="24%" alt="A condensation cooling loop"></a>
<a href="https://github.com/Salacious-Oni-Dev/oni-flagship-mods#showcase-videos"><img src="https://github.com/Salacious-Oni-Dev/oni-flagship-mods/raw/main/media/bubblephysics.gif" width="24%" alt="Bubbles rising through water"></a>
<a href="https://github.com/Salacious-Oni-Dev/oni-sim-visualizer#showcase-videos"><img src="https://github.com/Salacious-Oni-Dev/oni-sim-visualizer/raw/main/media/simviz-interactive.gif" width="24%" alt="The simulation visualizer"></a>
</p>

## Where to start

- **To play the mods:** follow [Installing and removing](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/blob/main/guides/installing.md).
  It says which release files to download (the `OniFramework` mod and the gameplay mods), what
  they change, and how to remove them.
- **To write a mod:** start with [Getting started](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/blob/main/guides/getting-started.md)
  and [Writing a mod](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/blob/main/guides/mod-authors.md).
- **To see it running:** the [showcase videos](https://github.com/Salacious-Oni-Dev/oni-flagship-mods#showcase-videos)
  show each system in a test scenario.

## Repositories

| repository | what it is |
|---|---|
| [oni-sdk-docs](https://github.com/Salacious-Oni-Dev/oni-sdk-docs) | the guides: what the SDK is, how its parts fit together, installing and removing it, compatibility, and writing a mod |
| [oni-sim-replacement](https://github.com/Salacious-Oni-Dev/oni-sim-replacement) | the replacement `SimDLL.dll`, with an extension surface for mods |
| [oni-framework-api](https://github.com/Salacious-Oni-Dev/oni-framework-api) | `OniFramework`, the managed API mods call, installed as its own mod |
| [oni-flagship-mods](https://github.com/Salacious-Oni-Dev/oni-flagship-mods) | Mod 1, Physical Thermodynamics + Fluid Dynamics, and Mod 2, Matter / Environmental Physics |
| [oni-sim-visualizer](https://github.com/Salacious-Oni-Dev/oni-sim-visualizer) | a standalone viewer for the simulation's state, from a recording or a running game |
| [oni-dev-environment](https://github.com/Salacious-Oni-Dev/oni-dev-environment) | a debuggable development copy of the game, with its own data and the game's debug tools working again |

## Replacing a game file

The SDK replaces one file of the game, `SimDLL.dll`. That is a lot to ask, so:

- the full source of the replacement is in [oni-sim-replacement](https://github.com/Salacious-Oni-Dev/oni-sim-replacement),
  and you can build it yourself;
- every release publishes the file's SHA-256, and the framework checks it and the game build
  before putting the file in place;
- the game's own file is kept, and put back when you remove the SDK.

The [installing guide](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/blob/main/guides/installing.md)
covers exactly what is replaced and how to get back to the unmodified game.

## What comes next

Releases come about every four weeks. Candidates for the next alpha are several diseases sharing
a cell, an odour field for gameplay mods, and liquids with real depth pressure. Further out are
a Mars planet with its own atmosphere and day and night, planetary logistics between colonies,
and programmable automation built on Stationeers' IC10. [What comes next](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/blob/main/NEXT-ALPHA.md)
has the detail.

Bug reports and ideas are welcome in the issues of the repository they concern.

---

Oxygen Not Included is developed and published by Klei Entertainment. This project is not
affiliated with or endorsed by Klei.

Development of this project uses AI coding assistants. All changes are reviewed and released by
the maintainer.
