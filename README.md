# aios-god-mode-template

God Mode template for **Synkra AIOS** -- the complete agent creation and framework management skill.

## What This Repo Contains

This repository holds the official God Mode template used by Synkra AIOS. It provides a full set of skills, rules, and configuration files that enable advanced agent orchestration, framework governance, and development workflow automation.

God Mode unlocks the complete AIOS capability set, including:

- All agent personas and their command sets
- Framework management skills (story lifecycle, QA gates, spec pipeline)
- Pre-configured Claude Code rules for tool selection and workflow execution
- Default permission settings for safe CLI operation

## Installation

### Automatic (recommended)

The template is fetched and applied automatically when you scaffold a new project:

```bash
npx create-aios my-project
```

No manual steps required. The CLI downloads the latest template version and copies all files into the correct locations.

### Manual

If you need to install the template manually:

1. Download or clone this repository:

   ```bash
   git clone https://github.com/gutomec/aios-god-mode-template.git
   ```

2. Copy the template files into your AIOS project:

   ```bash
   cp -r aios-god-mode-template/template/skills/   your-project/.claude/skills/
   cp -r aios-god-mode-template/template/rules/    your-project/.claude/rules/
   cp -r aios-god-mode-template/template/config/   your-project/.claude/
   ```

3. Verify the installation:

   ```bash
   cd your-project
   npx aios doctor
   ```

## File Structure

```
aios-god-mode-template/
├── template.json              # Template manifest (name, version, file mappings)
├── README.md
├── LICENSE
└── template/
    ├── skills/                # God Mode skill definitions
    ├── rules/                 # Claude Code rules (tool examples, workflows)
    └── config/                # Default settings (permissions, schema)
```

## Version

| Field           | Value |
|-----------------|-------|
| Template        | 3.0.0 |
| AIOS min version | 1.0.0 |

## Compatibility

- **Node.js:** 18 or later
- **Synkra AIOS:** 1.0.0 or later
- **Claude Code:** Latest stable

## License

[MIT](LICENSE)
