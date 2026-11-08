# raspberry_pi_baseline

Raspberry Pi OS settings for wired, swap-free nodes:

- Wi-Fi and Bluetooth turned off in the firmware (`dtoverlay=disable-wifi` and `disable-bt`).
- No swap, through Pi OS's own swap manager (`rpi-swap`).
- The journal kept on disk across reboots, capped in size. Pi OS keeps it in RAM only.
- EEPROM firmware kept current: updates are staged and applied at the next boot.

The role never reboots. When a change needs one, it creates `/run/reboot-required`.

Tested on Raspberry Pi OS trixie (Debian 13).

## Variables

| Variable | Default |
| --- | --- |
| `raspberry_pi_baseline_journal_max_size` | `200M` |

## Usage

```yaml
- hosts: raspberry_pi
  become: true
  roles:
    - raspberry_pi_baseline
```

## Development

Tests run with Molecule in a Debian trixie container running systemd, set up with Pi OS's default `config.txt`.
They check the real `config.txt`, the swap setting, and that journald keeps a capped journal on disk despite Pi OS's
RAM-only default. A container has no Pi firmware, so the EEPROM
tasks are only checked to be skipped there; their effect is checked on real Pis.

```sh
pip install -r requirements-test.txt
molecule test
```

Commits follow Conventional Commits. Releases are versioned and tagged automatically from `main`.
