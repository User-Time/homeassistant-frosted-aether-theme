# Frosted Aether Theme for Home Assistant ✨

[![HACS](https://img.shields.io/badge/HACS-Custom%20Repository-41BDF5?logo=home-assistant&logoColor=white)](https://my.home-assistant.io/redirect/hacs_repository/?owner=User-Time&repository=homeassistant-frosted-aether-theme&category=theme)
[![Last Commit](https://img.shields.io/github/last-commit/User-Time/homeassistant-frosted-aether-theme?label=Last%20commit)](https://github.com/User-Time/homeassistant-frosted-aether-theme/commits/main)
[![GitHub Stars](https://img.shields.io/github/stars/User-Time/homeassistant-frosted-aether-theme?style=social)](https://github.com/User-Time/homeassistant-frosted-aether-theme/stargazers)
[![License](https://img.shields.io/github/license/User-Time/homeassistant-frosted-aether-theme)](LICENSE)

A dark, frosted-glass Home Assistant theme inspired by the visual language of [Palace of the gods](https://potg.org/): deep navy surfaces, cyan-to-violet accents, soft glow, layered transparency, and restrained glass effects.

## ✨ Features

- **Frosted Aether aesthetic** — deep blue-black backgrounds with translucent glass surfaces.
- **Cyan + violet accents** — based around `#46b5ff` and `#7f6cff`.
- **Comprehensive HA theming** — cards, header, sidebar, dialogs, inputs, switches, sliders, badges, charts, Energy, maps, code editor, and entity state colors.
- **Home Assistant 2026-ready palette** — includes the newer `ha-color-*` theme tokens together with compatibility variables used by older Material/Paper components.
- **card-mod enhancements** — glass blur, soft glow, hover lift, translucent header/sidebar, dialog styling, chips, badges, rows, and more.
- **Dark-first design** — intentionally tuned as a dark theme to preserve the Aether visual style.

## 🚀 Quick Installation Guide

### Option 1: HACS

**Prerequisites**

- Install [HACS](https://hacs.xyz/).
- Install [`card-mod`](https://github.com/thomasloven/lovelace-card-mod) through HACS for the full frosted-glass effect.

Then open the repository in HACS:

[![Open your Home Assistant instance and add this repository](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=User-Time&repository=homeassistant-frosted-aether-theme&category=theme)

Restart Home Assistant after installation, then open your profile and select **Frosted Aether** from the theme dropdown.

### Option 2: Manual installation

Copy:

```text
themes/Frosted Aether.yaml
```

to:

```text
/config/themes/Frosted Aether.yaml
```

Make sure your `configuration.yaml` contains:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

Then restart Home Assistant or run the `frontend.reload_themes` action and select **Frosted Aether** in your profile.

---

> **card-mod is strongly recommended.** The native Home Assistant variables still provide the Aether color system without it, but blur, glow, hover, and some shell styling depend on `card-mod`.

## 🎨 Design Language

| Token | Value | Use |
| --- | --- | --- |
| Background | `#0a1220` | Main deep navy background |
| Secondary background | `#0b101e` | Layered dark surface |
| Primary | `#46b5ff` | Cyan-blue active/accent color |
| Accent | `#7f6cff` | Violet secondary accent |
| Primary text | `#f5f8ff` | Main text |
| Secondary text | `#aebbd0` | Muted labels and metadata |

The theme uses subtle radial gradients and low-opacity glow instead of heavy neon effects, keeping the dashboard readable while preserving depth.

## 🧩 Coverage

Frosted Aether currently styles or provides tokens for:

- Home Assistant app shell, header and sidebar
- Lovelace cards and sections
- More-info dialogs and popups
- Inputs, dropdowns, buttons, checkboxes and radio controls
- Switches, sliders and progress bars
- Entity state colors for lights, climate, locks, alarms, weather, vacuum, sensors and more
- Energy dashboard colors
- History and chart palettes
- Badges, chips and Assist UI
- Markdown, tables and CodeMirror
- Dark map filtering
- `card-mod` card, root, row, badge, dialog, config and panel hooks

## ⚙️ Compatibility & Notes

- Designed primarily for current Home Assistant 2026.x frontend builds.
- The theme also includes legacy Material/Paper variables to improve compatibility with older and custom cards.
- Heavy use of `backdrop-filter` can reduce performance on older tablets or low-power wall panels.
- Custom cards can override Home Assistant theme variables internally; those may need per-card `card_mod` rules.
- Browser rendering of blur and transparency can differ slightly between Chromium, WebView, Safari, and Firefox.

## 🐞 Issues / Feedback

If you find a component that still falls back to Home Assistant's default colors, or a custom card that conflicts with the glass layer, please open an [issue](https://github.com/User-Time/homeassistant-frosted-aether-theme/issues).

When reporting visual issues, include:

- Home Assistant version
- Browser / Companion App platform
- The affected card or integration
- A screenshot if possible

## ❤️ Credits

- Visual direction inspired by [Palace of the gods](https://potg.org/).
- Repository layout and HACS packaging conventions informed by the Home Assistant theme ecosystem, including [Frosted Glass Theme](https://github.com/wessamlauf/homeassistant-frosted-glass-themes).
- [`card-mod`](https://github.com/thomasloven/lovelace-card-mod) provides the advanced theme-level CSS hooks used for the glass effects.

## 📄 License

Released under the [MIT License](LICENSE).
