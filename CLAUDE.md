# AdBreak

## Project
AdBreak removes ads, tracking, and bloat from an LG OLED TV and builds custom tools around it.

- TV: LG OLED77C8PUA (2018 C8), webOS 4.4.3, software version 05.50.70
- Firmware is frozen on purpose (rootable with faultmanager). Never update it.
- Dev machine: M1 MacBook Pro
- Full plan: see the AdBreak project plan doc (phases 0 to 4)
- Current phase: 0 (Baseline)

## Who I am working with
Nolan is a recent CS-adjacent grad learning to code for real, not just vibe code. This project is for learning and for a portfolio.

- Explain what each change does and why before making it.
- Keep changes small. One concept at a time.
- When a task has a small, self-contained piece (a function, a test, a config line), stop and ask Nolan to write it first. Then review his version.
- Use plain, simple language. No em dashes.
- After each change, summarize what changed in 2 to 3 bullets.

## Safety rules for the TV
- Never run a command that touches the TV (network calls to its IP, SSH, luna-send, file transfers) without explaining it first and getting approval.
- Explore read-only before changing anything. Save snapshots of the TV's state to `snapshots/`.
- Never delete files on the TV. Disable instead, and write an undo step for every change in `undo/`.
- One change at a time. Reboot and test after each.
- Never install or suggest the LG Developer Mode app while the TV is rooted.
- Never flash firmware, modify partitions, or touch the bootloader.
- Use SSH with keys. Never enable Telnet.

## Repo conventions
- Log every work session in `LOG.md`: date, what was tried, what broke, what was learned.
- Never commit secrets: TV pairing keys, SSH keys, tokens, or `.env` files.
- Commit messages: short and in present tense (for example, "Add TV power command").
- Commit after each working step, not in big batches.
