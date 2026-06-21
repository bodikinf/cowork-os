# cowork-os (plugin)

The installable plugin version of [**cowork-os**](https://github.com/yempik-ai/cowork-os), an operating system for Claude Cowork. Install it once and Claude gets the cowork-os operating rules plus a set of slash commands, with no setup.

Built by [Yempik](https://yempik.com) for Claude Cowork. MIT.

## Install

**Claude Cowork:** browse and install from [claude.com/plugins](https://claude.com/plugins) once published, or add this repo as a marketplace.

**Claude Code:**
```bash
# Add the marketplace
/plugin marketplace add yempik-ai/cowork-os
# Install the plugin
/plugin install cowork-os@cowork-os
```

## What you get

A always-on **core skill** (`cowork-os-core`) that makes Claude check sources first, separate facts from assumptions and recommendations, never invent data, keep a business tone, and maintain the workspace's living memory.

Plus six slash commands:

| Command | What it does |
|---|---|
| `/cowork-os:install` | Guided setup. Interviews you (about 5 min) and generates a full, pre-configured workspace: folders, copy, project instructions, and recurring routines. |
| `/cowork-os:memory-update` | Runs the Memory Update protocol so decisions, questions, assumptions and risks are written to the right files. |
| `/cowork-os:linkedin-editor` | The 8-step LinkedIn editor: turns any source into ready-to-publish, founder-voice posts optimized for reach and leads. |
| `/cowork-os:mission` | Mission mode: pursue an ambitious outcome (a dream client, a partnership) with route maps, an evidence log, and stop conditions. |
| `/cowork-os:weekly-pulse` | A short Monday marketing brief: what happened, what it means, the week's priorities. |
| `/cowork-os:process-inbox` | Reads unsorted material you dropped in `_inbox/` and routes each fact to the most specific workspace file. |

## Plugin vs full kit

This plugin is the **runnable core**: the operating rules and the commands. The [full repository](https://github.com/yempik-ai/cowork-os) also ships the complete folder structure, every module template, and a sanitized real workspace (`examples/yempik/`) as a quality bar. Use the plugin to drive the work; copy the template repo when you want the full file scaffold.

## Customize it

These are generic starting points. They get much more useful when you adapt them to your company: your terminology, your offers, your tone. Edit the command and skill markdown files, or run `/cowork-os:install` and let Claude generate a workspace filled with your real answers.
