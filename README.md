# Potter Service Game Hub v0.2

This repository supplies dynamic content to Potter Service Game Launcher.

## Important change in v0.2

Every game and every server can have its own custom HTML page.

`servers/Alfheim/page.html` is the first example. The launcher will render this
page inside its embedded browser rather than creating a generic C# server card.

### Server page bridge

Custom pages can request native launcher actions with:

- `pslauncher://join-server`
- `pslauncher://refresh-status`

The launcher will intercept those actions. Connection information remains in
`server.json`, not in the HTML design.

The launcher can inject live status into a page by calling:

`window.PotterLauncher.setServerStatus({ online, players, maxPlayers })`

## Adding future servers

Create:

servers/YourServer/
  server.json
  page.html
  assets/

Then add that server to the `servers` array in `manifest.json`.

## Adding future games

Create:

games/YourGame/
  game.json
  page.html
  assets/

Then add that game to the `games` array in `manifest.json`.

Do not commit passwords, API keys, Git credentials, or other secrets.
