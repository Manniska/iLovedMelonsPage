# ilovedmelons — Twitch landing page

This is a small, static landing page for the Twitch streamer `ilovedmelons`.

What it includes
- Responsive Twitch embed (iframe created dynamically so the `parent` query param matches the current host).
- About, Schedule, Clips and Support sections.
- Accessible improvements (skip link, focus states, aria labels).

Local development
1. Serve the files over HTTP so the Twitch embed will work correctly.

Using Python (works on Windows PowerShell):
```powershell
# From the project folder
python -m http.server 8000
# Then open http://localhost:8000 in your browser
```

Notes about the Twitch embed
- Twitch requires the `parent` query parameter to match the hostname where the embed is served.
- The page sets the iframe `parent` to the current `location.hostname`. When testing via a file:// URL the hostname is empty; the page will fall back to `localhost` but you should use a local HTTP server for reliable results.

Next improvements you can ask for
- Add streamer avatar and branding images.
- Add social icons for other platforms and real links.
- Connect to Twitch APIs to show live status, follower count, or recent streams.
