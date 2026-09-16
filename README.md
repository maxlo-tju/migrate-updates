# Maxlo Migrate — builds

Notarized builds of **Maxlo Migrate**, the tool for pre-populating drives before
they ship to a client.

Downloads are on the [Releases](../../releases) page. Source lives in a private
repository.

## Install

Download the `.dmg`, open it, drag **Maxlo Migrate** to Applications.

Builds are signed with a Developer ID, notarized and stapled, so they open
without a Gatekeeper prompt.

## Before the first run

1. Grant **Full Disk Access** to Maxlo Migrate in System Settings › Privacy &
   Security. Without it macOS returns nothing for `/Volumes` and no source
   volumes are found.
2. Expect **one administrator prompt** the first time a privileged step runs.

## Flags

| Flag | What it does |
|---|---|
| `--demo` | Fabricated state for looking around. Every action is disabled; nothing touches a disk. |
| `--selftest` | Transfer engine. |
| `--selftest-helper` | Privileged helper transport. |
| `--selftest-gates` | Ship-blocking checks. |
| `--selftest-apfs` | `diskutil` wrappers, against a throwaway disk image. |
| `--selftest-e2e` | Full flow end to end. |

No self test touches a physical disk.
