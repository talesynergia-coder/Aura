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

## Birthday 🎂
Spotify doesn't share your birthday with apps, so AURA asks once (a small card after you connect Spotify, or Settings → Birthday) and keeps it on your device. On the day you get a full-screen celebration — confetti, balloons, a cake to blow out, "Happy birthday" in your greeting, a one-tap birthday mix — and confetti bursts on every song change while music plays. Settings → Birthday has toggles, "Show my age" and a Preview button.

## Study tracker (button next to Library, or press T)
- Today: days left to exam (edit the date), live study timer, mock test countdowns, backup/restore
- Chapters: add by subject, tick off, optionally note a topic left
- Widgets: Settings → Elements on screen → Study timer / Exam countdown / Chapter progress / Studied today, then Layout mode to place them (double-tap a widget to open the tracker)
- Calendar: monthly view of minutes studied, streak, add/delete entries per day

Study data is stored in the browser (localStorage). Use Backup to move it between devices.

## More layouts

Pick any from **Settings → Preset** (each is its own full layout, not a Spatial variant):

- **Bento board / Coverflow** – the Spatial panels, laid out all at once or gliding past.
- **Cinema crawl** – lyrics scroll away into space like a film opening; the current line is bright.
- **LED marquee** – a dot-matrix sign: scrolling title, big lyric line, progress strip. Colour in *Settings → Full-screen scenes*.
- **Terminal** – now-playing, lyrics typed as a live log, and your queue, in a terminal window.
- **Cassette** – spinning reels whose tape moves with the song, handwritten label, current lyric underneath.

Scenes and Spatial view never run together; switching one turns the other off.
- **Retro radio** – wooden tuner, the needle sweeps the dial as the song plays, lyric glows on the speaker cloth.
- **Departures board** – split-flap letters flip to spell the song, artist, gate/time, lyric and next track.
- **Receipt** – a thermal printer prints each lyric line like a till receipt, ending with a total and barcode.
- **Polaroid** – the cover "develops" on every new track with the lyric handwritten underneath.
- **Rainy window** – a night city behind fogged glass. A finger writes each lyric line into the fog, raindrops run down and wipe trails, and the glass slowly fogs back over the words.
