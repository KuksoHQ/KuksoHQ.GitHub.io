---
sidebar_position: 1
sidebar_label: "JavaDocs"
---

# JavaDoc Standard

JavaDocs are published only for KuksoLib because KuksoLib is the developer integration surface for Kukso Java projects.

Customer-facing products are documented with curated Docusaurus pages instead of generated JavaDocs:

- KuksoDialogs
- KuksoWorlds
- KuksoItems
- KuksoEcon
- KuksoWarps

## Canonical URLs

Minecraft KuksoLib:

- Latest: `/api/minecraft/lib/latest/`
- Versioned: `/api/minecraft/lib/vX.Y.Z/`

Hytale KuksoLib:

- Latest: `/api/hytale/lib/latest/`
- Versioned: `/api/hytale/lib/vX.Y.Z/`

## Publishing Rules

Generated JavaDoc HTML is not committed to the `kuksohq.github.io` source branch.

Library release workflows publish JavaDocs to the deployed GitHub Pages branch:

- `kukso-minecraft-lib-vX.Y.Z` publishes Minecraft KuksoLib JavaDocs.
- `kukso-hytale-lib-vX.Y.Z` publishes Hytale KuksoLib JavaDocs.

Hytale JavaDoc publishing requires a GitHub self-hosted runner labeled `hytale` with a local Hytale installation. The runner must expose `HYTALE_HOME`, and the expected server jar path is:

```text
$HYTALE_HOME/install/<patchline>/package/game/<game_build>/Server/HytaleServer.jar
```

Hytale server jars must not be committed, uploaded as secrets, or stored in package repositories.
