# Potter Service Game Launcher — Content Repository

Remote content/configuration for the Potter Service Game Launcher.

## Structure
- `manifest.json` — master launcher index
- `games/` — supported games, pages and assets
- `servers/` — server definitions, pages and assets
- `news/` — launcher announcements

## Adding a server
Create a folder under `servers/`, add `server.json`, `page.html`, and assets, then add it to `manifest.json`.

## Included starter server
Alfheim is configured for Valheim. Its connection and query ports are stored in `server.json`, but `showAddress` is false so the future launcher will not display them. The server password is not stored.

The HTML uses `data-launch-action="join-server"` so the future desktop app can intercept the button and launch the configured game/server.

Do not commit passwords, API keys, private tokens, or Git credentials.

Sponsored by Potter Service — https://potterservice.com
