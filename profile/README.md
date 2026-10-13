# Oxygen Not Included simulation SDK

*Oxygen Not Included: now with actual reasons for the oxygen to be not included.*

> [!WARNING]
> **Early alpha release (`v0.1.0-alpha.2`).** Expect bugs, missing features and changes between
> releases, including to the API. It replaces one game file,
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

## Releases

Current: [Alpha 2 (`v0.1.0-alpha.2`)](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/releases/tag/v0.1.0-alpha.2)

Each link opens that repository's releases, newest first:

- [oni-sim-replacement releases](https://github.com/Salacious-Oni-Dev/oni-sim-replacement/releases): the replacement `SimDLL.dll`
- [oni-framework-api releases](https://github.com/Salacious-Oni-Dev/oni-framework-api/releases): the `OniFramework.Library` and `OniFramework` mods
- [oni-flagship-mods releases](https://github.com/Salacious-Oni-Dev/oni-flagship-mods/releases): the gameplay mods
- [oni-sdk-docs releases](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/releases): the release notes, guides and preview films
- [oni-sim-visualizer releases](https://github.com/Salacious-Oni-Dev/oni-sim-visualizer/releases): the simulation visualizer
- [oni-sim-vanilla releases](https://github.com/Salacious-Oni-Dev/oni-sim-vanilla/releases): the plain vanilla-behaving `SimDLL.dll`
- [oni-dev-environment releases](https://github.com/Salacious-Oni-Dev/oni-dev-environment/releases): the development copy of the game (unchanged since `v0.1.0-alpha.1`)

Browse the project online: the [Project Navigator](https://salacious-oni-dev.github.io/oni-sdk-docs/navigator/navigator.html) lists every simulation system, the machines whose recipes hide physics, and which elements exist.

## Alpha 2 (current release)

Alpha 2 (`v0.1.0-alpha.2`) adds liquid depth pressure, several diseases per cell, an odour field,
smoke, fire and the buildings that use it, and rooms whose air condenses and exchanges heat, and a
new mod, Mod 5: Stationeers' IC10 programmable chips, reading and driving the game's own buildings.
Each repository's `CHANGELOG.md` lists the release in full.

[Release notes](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/releases/tag/v0.1.0-alpha.2) ·
[What is in Alpha 2, and its known limitations](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/blob/main/NEXT-ALPHA.md#alpha-2)

## Where to start

- **To play the mods:** follow [Installing and removing](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/blob/main/guides/installing.md).
  It says which release files to download (the `OniFramework.Library` and `OniFramework` mods and the gameplay mods), what
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
| [oni-framework-api](https://github.com/Salacious-Oni-Dev/oni-framework-api) | the managed API mods call, as two mods: `OniFramework.Library`, which needs no SDK simulation library, and `OniFramework`, the simulation half |
| [oni-flagship-mods](https://github.com/Salacious-Oni-Dev/oni-flagship-mods) | Mod 1, Physical Thermodynamics + Fluid Dynamics; Mod 2, Matter / Environmental Physics; and Mod 5, Automation / IC10 |
| [oni-sim-visualizer](https://github.com/Salacious-Oni-Dev/oni-sim-visualizer) | a standalone viewer for the simulation's state, from a recording or a running game |
| [oni-dev-environment](https://github.com/Salacious-Oni-Dev/oni-dev-environment) | a debuggable development copy of the game, with its own data and the game's debug tools working again |
| [oni-sim-vanilla](https://github.com/Salacious-Oni-Dev/oni-sim-vanilla) | a plain `SimDLL.dll` that behaves like the game's own, with no extensions and every part documented; frozen, and not used by the SDK |

Mods built on the SDK need one of two framework mods, both in the
[oni-framework-api](https://github.com/Salacious-Oni-Dev/oni-framework-api) release: a mod that uses
the replacement simulation library needs `OniFramework` together with `OniFramework.Library`, which
it is built on; a mod that does not needs only `OniFramework.Library` 1.2 or later, and runs on the
game's own `SimDLL.dll`.

Mods that stand on their own, including a frame-rate and load-time mod and a garbage-collector
runtime with shorter freezes, are in [Salacious-Oni-Mods](https://github.com/Salacious-Oni-Mods).

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

Releases follow a regular cadence, currently a trial of about ten days between releases. Alpha 2
adds liquids with real depth pressure, several diseases sharing a cell, an odour field, and smoke
and fire that conserve what burns, and the first release of programmable automation built on
Stationeers' IC10. Built in development and shown as a preview: a first trade route between
planets and a chlor-alkali cell. Further out are a Mars planet with its own atmosphere and day and
night, and planetary logistics between colonies.
[What comes next](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/blob/main/NEXT-ALPHA.md) has
the detail.

Bug reports and ideas are welcome in the issues of the repository they concern.

---

Oxygen Not Included is developed and published by Klei Entertainment. This project is not
affiliated with or endorsed by Klei.
How this project follows Klei's modding guidelines, rule by rule: [COMPLIANCE](https://github.com/Salacious-Oni-Dev/oni-sdk-docs/blob/main/COMPLIANCE.md).

Development of this project uses AI coding assistants. All changes are reviewed, tested and
released by the maintainer.
