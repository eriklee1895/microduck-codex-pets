# microduck-codex-pets

An unofficial community archive of themed MicroDuck pets for Codex.

The archive currently includes a cartoon `MicroDuck` pet and its first themed variant, `MicroDuck Night Shift`, based on the real [Pollen Robotics MicroDuck](https://github.com/pollen-robotics/microduck). More themes can be added under `pets/` without changing the install contract.

> This project is not affiliated with or endorsed by Pollen Robotics. `MicroDuck` is referenced here as the name of the open-source robot project.

## Meet the Flock

### MicroDuck

- Style: compact 3D-toy cartoon
- Identity detail: thin, flat, nearly closed mechanical bill matching the physical reference
- Animation: Codex v2 atlas with standard activity states and 16 look directions
- Package: `pets/microduck/pet.json` + `pets/microduck/spritesheet.webp`

### MicroDuck Night Shift

- Style: flatter vector chibi cartoon
- Personality: sleepy, focused, and slightly awkward
- Identity detail: oversized hooded head, half-lidded camera eye, cyan status panel, and thin flat mechanical bill
- Package: `pets/microduck-nightshift/pet.json` + `pets/microduck-nightshift/spritesheet.webp`

## Install

Choose one:

### Install with Codex (Recommended)

Give Codex this prompt:

```text
Install or update the MicroDuck Codex pets from:

https://github.com/eriklee1895/microduck-codex-pets

Use the packages under pets/ and keep other pets untouched.
Tell me to refresh the Pets list when finished.
```

### Manual install

Copy the package into the local Codex pet directory:

```bash
for PET_SOURCE in pets/*; do
  [ -f "$PET_SOURCE/pet.json" ] || continue
  PET_ID="$(basename "$PET_SOURCE")"
  PET_DIR="${CODEX_HOME:-$HOME/.codex}/pets/$PET_ID"
  mkdir -p "$PET_DIR"
  cp "$PET_SOURCE/pet.json" "$PET_SOURCE/spritesheet.webp" "$PET_DIR/"
done
```

Then open Codex settings → Pets and refresh the list.

## Preview

<p align="center">
  <img src="previews/microduck/demo.gif"
       alt="MicroDuck Codex pet demo"
       width="260">
</p>

The demo loops through idle, waddling, waving, and review so the pet's behavior is visible without opening the spritesheet.

| Idle | Waddling | Waving | Review |
| --- | --- | --- | --- |
| <img src="previews/microduck/idle.gif" alt="Idle animation" width="150"> | <img src="previews/microduck/running-right.gif" alt="Waddling animation" width="150"> | <img src="previews/microduck/waving.gif" alt="Waving animation" width="150"> | <img src="previews/microduck/review.gif" alt="Review animation" width="150"> |

- [Canonical character](previews/microduck/canonical-base-green.png)
- [Animation contact sheet](previews/microduck/contact-sheet-extended.png)
- [16 look directions](previews/microduck/look-directions.png)
- [Neutral 192×208 frame](previews/microduck/neutral-192x208.png)

### MicroDuck Night Shift

<p align="center">
  <img src="previews/microduck-nightshift/demo.gif"
       alt="MicroDuck Night Shift pet demo"
       width="260">
</p>

| Idle | Waddling | Waving | Review |
| --- | --- | --- | --- |
| <img src="previews/microduck-nightshift/idle.gif" alt="Night Shift idle animation" width="150"> | <img src="previews/microduck-nightshift/running-right.gif" alt="Night Shift waddling animation" width="150"> | <img src="previews/microduck-nightshift/waving.gif" alt="Night Shift waving animation" width="150"> | <img src="previews/microduck-nightshift/review.gif" alt="Night Shift review animation" width="150"> |

- [Canonical character](previews/microduck-nightshift/canonical-base-green.png)
- [Animation contact sheet](previews/microduck-nightshift/contact-sheet-extended.png)
- [16 look directions](previews/microduck-nightshift/look-directions.png)
- [Neutral 192×208 frame](previews/microduck-nightshift/neutral-192x208.png)

## Repository layout

```text
microduck-codex-pets/
├── pets/
│   ├── catalog.json
│   ├── microduck/
│   │   ├── pet.json
│   │   └── spritesheet.webp
│   └── microduck-nightshift/
│       ├── pet.json
│       └── spritesheet.webp
├── previews/
├── docs/
└── NOTICE.md
```

Each future theme should get its own directory, for example `pets/microduck-space/`, with a self-contained `pet.json` and `spritesheet.webp`.

Reusable creation prompts, mouth-design decisions, and motion mechanics are kept in [`docs/microduck/`](docs/microduck/) so future themes can build on the same design knowledge.

## Licensing

No license file is included yet. Until the artwork license is chosen, please do not assume that the generated artwork may be reused outside this archive. Attribution and source notes are in [`NOTICE.md`](NOTICE.md).
