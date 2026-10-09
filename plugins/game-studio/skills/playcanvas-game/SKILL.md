---
name: playcanvas-game
description: Build or extend browser games with PlayCanvas Engine, @playcanvas/react, or @playcanvas/web-components. Use when the user chooses PlayCanvas or the project already uses it.
---

# PlayCanvas Game

Read `package.json`, imports, and markup to identify the active PlayCanvas surface. Preserve it. For a new app, choose direct Engine for imperative control, React for a React-owned app, or Web Components for a markup-led app.

This skill covers Engine games. Follow the project's workflow for Editor-hosted scenes; lens packaging, preview, and submission need separate guidance.

## Surface rules

- Direct Engine: keep the `Application` or `AppBase` bootstrap; the app owns assets, updates, resize, and teardown.
- React: let `@playcanvas/react` components and hooks own the scene; use Engine scripts or app events for per-frame work.
- Web Components: use `<pc-app>`, `<pc-asset>`, and `<pc-entity>` for scene structure, with Engine scripts for behavior.

## Game workflow

- Define the core loop, action map, pause and reset states, and saveable state boundary before wiring scene events.
- Check installed package declarations and matching official examples for version-sensitive APIs. Use PlayCanvas components and loaders.
- Configure input devices and resizing in direct Engine apps; use the owning lifecycle in React and Web Components.
- Load GLB through the chosen surface: container assets and render entities in direct Engine, asset hooks or components in React, and asset and model elements in Web Components. Inspect scale and facing; configure decoders only when assets require them.
- Use DOM or React for text-heavy and accessibility-sensitive controls, or Engine screen and element components for canvas UI. Gate game input while menus are active.

## Verify

Build and play the app in a browser. Check first load, player actions, pause and reset, asset appearance, HUD readability, and resize. Inspect screenshots before making visual claims.

## References

Use `../web-game-foundations/SKILL.md` for game architecture, `../web-3d-asset-pipeline/SKILL.md` for assets, `../game-ui-frontend/SKILL.md` for HUD, and `../game-playtest/SKILL.md` for QA. Check https://developer.playcanvas.com/, https://playcanvas.com/examples/, and https://github.com/playcanvas/skills for Engine-specific workflows.
