# Potter Service Game Hub v0.3

## New architecture

### Custom Home
`home/page.html` controls the launcher's Home design. You can change its HTML/CSS/assets in Git without rebuilding the launcher.

### Favorites
The next launcher stores each user's hearts/favorites locally on their own computer. Games and individual servers can be favorited. Favorites are not stored in this public repo.

### Servers grouped by game
The Servers screen first reads game categories:

servers/
  Valheim/
    category.json
    assets/logo.png
    Alfheim/
      server.json
      page.html
      assets/

Click the Valheim logo -> list all published Valheim servers -> click a server -> load its custom HTML page.

To add another Valheim server, create another sibling folder under `servers/Valheim/` and add it to `category.json`.

### Active / deactivated
`enabled` controls whether an item is published/listed.
`active` in `server.json` controls whether joining is currently allowed.
Set `active: false` to keep a server visible but disable joining and show its `inactiveMessage`.
A category also has `enabled`, allowing the entire game-server category to be hidden.

### Programs
`programs/` is now a full launcher section for things such as Steam download links, Discord, Potter Service utilities, installers, and future tools.

Never commit passwords, API keys, private tokens, or other secrets.
