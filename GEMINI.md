# SFXMint

The `sfxmint` MCP server finds free CC0 sound effects for apps, games and videos (https://sfxmint.com). No API key is needed to search; downloading files takes the user's free SFXMint API key (3 sounds a day, the website and the API together).

- One named event (button click, coin pickup, game over): `get_role_sound`.
- Several events for one app or game: `get_sound_set`.
- A described sound or a gap: `search_sounds`. When nothing matches every word, it returns the closest sounds and says what is missing; judge them and let the user listen.
- One sound by id: `get_sound`.
- Choosing for several events: `create_listen_page` gives the user a page to play the candidates and keep one each; when they are done, `get_picks` returns their picks and notes. If they say "you decide", skip it.

Download the chosen files into the project and keep a `SOUNDS.md` listing each file with its `page_url`, the CC0 license and that the sounds are AI-generated (a game on Steam or itch.io discloses that). The server's own instructions cover download allowances and generating a missing sound.
