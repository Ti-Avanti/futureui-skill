# futureui-skill

AI skill pack **`futureui-ui`** for **FutureUI 1.0.0** — a config-driven Minecraft GUI menu and universal shop plugin.

Turn natural language into loadable menu configs (Canvas / Dialog YAML, actions, language files, pixel assets) with Claude Code, Codex, MiMoCode, or any assistant that reads `SKILL.md`.

## Install

1. Download [v1.0.0](https://github.com/Ti-Avanti/futureui-skill/releases/tag/v1.0.0) or clone this repository
2. Copy the `futureui-ui/` folder into your AI assistant's skills directory
   - e.g. `.mimocode/skills/futureui-ui/` or `.agents/skills/futureui-ui/`
3. Ask your assistant to build a menu

## Contents

| Path | Purpose |
| --- | --- |
| `futureui-ui/SKILL.md` | Skill entry (read by AI assistants) |
| `futureui-ui/references/` | Layout, actions, commerce, variables, validation docs |
| `futureui-ui/assets/templates/starter/` | 15+ example menus, themes, shops, languages |
| `futureui-ui/scripts/check_config.py` | Offline config validator (Python 3.10+, PyYAML) |
| Release asset `futureui-skill.zip` | Packed skill for one-shot download; not stored in the repository tree |

## Validate configs

```bash
python -B futureui-ui/scripts/check_config.py --root /path/to/menus --base /path/to/plugins/FutureUI
python -B futureui-ui/scripts/check_config.py --root futureui-ui/assets/templates/starter
```

## Plugin baseline

This release targets FutureUI `1.0.0`. It includes references for FotiaCosmetic, FotiaChat, FotiaCrates and FotiaTags integrations, horizontal viewport examples, pixel layout guidance and matching validation rules. Third-party menu data and actions require the corresponding plugin adapter; static validation does not certify live transactions or client rendering.

## Environment

- Server: Paper (api-version 1.21.8+), dependency: packetevents
- Skill: any AI assistant that reads `SKILL.md`
- Validator: Python 3.10+ and PyYAML
