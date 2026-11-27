# AURA

Full-screen Spotify vinyl player + built-in NEET study tracker.

## Files
- index.html — the whole app
- manifest.webmanifest — installable app (Add to Home Screen)
- icons/ — icon.svg, icon-192.png, icon-512.png, icon-maskable-512.png, apple-touch-icon.png

## Deploy (GitHub Pages)
Put all of these in the repo root, keeping the `icons/` folder, then enable Pages.
Your Spotify redirect URI stays the same as before if the URL doesn't change.

## Playback
AURA plays the music itself in the browser (Spotify's Web Playback SDK, Premium required) — the Spotify app doesn't need to be open. You sign in once; AURA reads your playlists from that login. Pressing play with nothing loaded starts the last playlist you played (or your first playlist, or Liked Songs).

## Spatial layout (floating 3D panels)
Settings → Layout → Preset → **Spatial**, the cube button in the top bar, or press V.
- Glowing panels float on a 3D ring: Player, Lyrics, Study (exam countdown, timer, chapters), Up next, Clock & weather.
- The camera flies between them with motion blur. Tap a panel, tap the chips, swipe, or press [ and ] to fly somewhere; otherwise it tours on its own and flies to the Player when the song changes.
- Lyrics appear as floating cards that change style every line (pay pill, message bubbles, island pill, voice note, gradient card), or pick one style.
- Settings → Spatial view: lyric card style, auto tour on/off, time on lyrics, drift & mouse parallax, and which panels to show.
- Layout mode (E) is for the flat layouts; switch Spatial off to drag widgets.

## Kinetic layout (lock-screen lyrics)
Settings → Layout → Preset → **Kinetic**, or Settings → Lyrics → Lyrics view → Kinetic (the lyrics button / Y also cycles to it). A lock-screen style clock on top, and each lyric line pops in a few big words at a time, one by one as they're sung — small italic, huge bold and highlighted-label words mixed, with emoji stickers (❤️ 🚗 💃 🔥 …). Tune words per card, size, emoji, clock and the song name in Settings → Lyrics. Needs synced lyrics.

## Study tracker (button next to Library, or press T)
- Today: days left to exam (edit the date), live study timer, mock test countdowns, backup/restore
- Chapters: add by subject, tick off, optionally note a topic left
- Widgets: Settings → Elements on screen → Study timer / Exam countdown / Chapter progress / Studied today, then Layout mode to place them (double-tap a widget to open the tracker)
- Calendar: monthly view of minutes studied, streak, add/delete entries per day

Study data is stored in the browser (localStorage). Use Backup to move it between devices.
