# AdBreak

AdBreak removes ads, tracking, and bloat from an LG OLED TV, then builds custom tools on top of it.

## Hardware

| Item | Details |
| --- | --- |
| TV | LG OLED77C8PUA (2018 C8) |
| OS | webOS 4.4.3 |
| Firmware | 05.50.70 (frozen on purpose, never updated) |
| Dev machine | M1 MacBook Pro |

The firmware stays frozen because this version can be rooted with the faultmanager exploit.

## Approach

The TV is a real device I use every day, so every change is careful and can be undone:

- **Read-only first.** I explore and save snapshots of the TV's state before changing anything.
- **Disable, never delete.** Every change has a matching undo step in `undo/`.
- **One change at a time.** Reboot and test after each one.
- **No risky low-level changes.** No firmware flashing, partition edits, or bootloader changes.
- **Secure access only.** SSH with keys. Telnet stays off.

## Project phases

| Phase | Name | Status |
| --- | --- | --- |
| 0 | Baseline | In progress |
| 1 to 4 | See project plan | Not started |

## Repo layout

| Path | Purpose |
| --- | --- |
| `LOG.md` | Work log for every session: what I tried, what broke, what I learned |
| `snapshots/` | Saved snapshots of the TV's state |
| `undo/` | Undo steps for every change made to the TV |

## Disclaimer

This is a personal learning project. Rooting a TV can void its warranty or break it. Do this on your own hardware at your own risk.
