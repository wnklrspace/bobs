# Bobs

Bobs is the multimedia system for my apartment.

This repo does two jobs:

1. **Code.** It holds the software that runs the system.
2. **Planning hub.** It's where the system is planned, documented and extended one module at a time.

> Status: planning. Nothing is installed yet.

## Idea

Bobs is not one big application. It's a set of **modules**. Each module covers one part of the apartment's multimedia setup, such as audio in the living room, a screen, lighting scenes or a control panel. A module can be built, replaced or dropped without touching the others.

The core stays small. It's whatever the modules need in common, such as configuration, a way to talk to each other and a shared control surface.

## Repository layout

```
bobs/
├── README.md          # this file
├── docs/
│   ├── apartment.md   # rooms, power, network, where things go
│   ├── decisions/     # one file per architectural decision
│   └── roadmap.md     # what's planned, in what order
├── core/              # shared code used by all modules
└── modules/
    └── <module-name>/
        ├── README.md  # what it does, hardware, status
        └── ...        # the module's code and config
```

Create folders when the first content for them exists, not in advance.

## Modules

| Module | Purpose | Status |
| ------ | ------- | ------ |
| _tbd_  |         | idea   |

Status values are `idea`, `planned`, `in progress`, `running` and `retired`.

### Adding a module

1. Create `modules/<module-name>/README.md` with these sections:
   - **Purpose:** what the module does and in which room
   - **Hardware:** devices, cables and where they sit
   - **Software:** what runs and where
   - **Interfaces:** what it exposes to or needs from other modules or the core
   - **Status and open questions**
2. Add a row to the table above.
3. If the module forces a decision that affects other modules, record it in `docs/decisions/`.

## Planning

- **Apartment facts** go in `docs/apartment.md`: rooms, sockets, network and constraints.
- **Ideas and order of work** go in `docs/roadmap.md`.
- **Decisions** go in `docs/decisions/NNNN-title.md`, one short file per decision, covering context, decision and consequences.

## Branches

- `develop` is the default branch, where work happens.
- `main` holds stable states of the system.
