# Voron VS.594 – Enderwire Configuration

Configuration repository for **Voron VS.594**, an **Enderwire conversion** running Klipper.

This repository stores the printer configuration, macros, and service configuration used by the machine.

---

## Printer Details

| Component | Description               |
| --------- | ------------------------- |
| Printer   | Enderwire                 |
| Firmware  | Klipper                   |
| Host      | Raspberry Pi (MainsailOS) |
| UI        | Mainsail / KlipperScreen  |

---

## Repository Layout

```
printer.cfg                Main Klipper entrypoint

hardware/                  Board, steppers, heaters, sensors
features/                  Optional printer features
tuning/                    Input shaper / accelerometer tuning

macros/                    Organized macro files
  print/
  filament/
  calibration/
  system/
  environment/

services/                  Host-side service configs
archive/                   Old configs retained for reference
artifacts/                 Runtime files ignored by git
```

---

## Configuration Backup

The printer includes a helper macro to commit and push configuration updates to GitHub.

Run:

```
BACKUP_CFG
```

This executes:

```
services/autocommit.sh
```

which performs a git commit and push.

---

## Notes

* Runtime files are excluded via `.gitignore`
* Backup configs and logs are not tracked
* Repository is structured for easy migration between similar printers

---

## License

MIT License

---

## Author

Jason S
