# 5G CA Combo Diff

A single-file web tool for comparing carrier aggregation combo lists between firmware versions. Drop two CSV exports and instantly see what changed.

Live here: https://h3nnes.github.io/5g-combo-diff/

<img width="2638" height="1446" alt="image" src="https://github.com/user-attachments/assets/a70589ba-9c39-454b-a410-f01c31e5ce7c" />

## Features

- **Side-by-side diff view** with field-level change highlighting
- **EN-DC and NR-CA** combo support
- **Fuzzy modification detection** — catches changes even when MIMO values alter the combo name
- **Git-diff-style context** — unchanged combos shown as dimmed context around changes, with fold separators
- **Column-aligned layout** — bands, BWs, and MIMO in fixed-width columns for easy scanning
- **Hover tooltips** — BCS, modulation, and SCS details on hover
- **Search and filter** — by type (EN-DC/NR-CA), status (+/−/~/=), or free text
- **No dependencies, no build step** — just open `index.html` in a browser

## Usage

1. Open `index.html` in any modern browser
2. Drop old firmware CSV(s) on the left zone, new on the right
3. The tool auto-detects EN-DC vs NR-CA from the CSV headers

Supports the semicolon-separated CSV format exported by [UECapabilityParser](https://github.com/handymenny/uecapabilityparser).

## Contributing

Contributions are welcome. The codebase is a single HTML file with four modular sections:

| Module | Purpose |
|--------|---------|
| `ComboParser` | CSV detection and parsing |
| `ComboDiffer` | Fingerprint matching, fuzzy pairing, field-level diffing |
| `ComboRenderer` | Column-aligned rendering, tooltips, highlights |
| `AppController` | State management, filtering, pagination |

## Transparency

Non-biological intelligence was used to support the development of this webapp.

## License

[MIT](https://opensource.org/licenses/MIT)
