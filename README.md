# aminta's MiSTer cores — database for downloader / update_all

Custom database for the [MiSTer Downloader](https://github.com/MiSTer-devel/Downloader_MiSTer)
with the cores by aminta. With it, `update` and `update_all` install and keep them up to date.

| Core | Menu | Files | Project |
|---|---|---|---|
| **Programma101** — Olivetti Programma 101 (1965), considered by many the first personal computer | Computer | `_Computer/Programma101_<date>.rbf` | [P101_MiSTer](https://github.com/aminta/P101_MiSTer) |
| **PLATO** — PLATO terminal for CYBER1 (hybrid core: FPGA video + PTerm engine on the ARM) | Other | `_Other/PLATO_<date>.rbf`, `PLATO/`, `Scripts/plato_install.sh` | [PLATO_MiSTer](https://github.com/aminta/PLATO_MiSTer) |

## How to add it to your MiSTer

**Drop-in:** download
[downloader_aminta_MiSTer_aminta_db.zip](https://raw.githubusercontent.com/aminta/MiSTer_aminta_db/db/downloader_aminta_MiSTer_aminta_db.zip),
extract the `.ini` file and copy it to the root of the SD card, next to `downloader.ini`.
Then run *update* or *update_all*.

**Or by hand:** add these lines at the bottom of `downloader.ini`:

```ini
[aminta/MiSTer_aminta_db]
db_url = https://raw.githubusercontent.com/aminta/MiSTer_aminta_db/db/db.json.zip
```

## Notes

- **Programma101**: create `games/Programma101/` for your card files (`.p1c`); no programs are
  included (see the project README). User files (cards, `Paper.txt`) are never touched.
- **PLATO**: after the first install run **Scripts → plato_install** once (it starts `platod`
  when the core is loaded). Your `PLATO/platod.ini` is never overwritten.

Database built with [theypsilon's DB template](https://github.com/theypsilon/DB-Template_MiSTer).
