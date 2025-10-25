# musicbu — Random MP3 to GitHub Pages

This repo publishes a single **stable MP3 URL** to GitHub Pages and **rotates tracks randomly** from `playlist.txt`.
Paste the final URL into IMVU (or anywhere) and the audio will change every rotation while the URL stays the same.

## Final MP3 URL (after the first successful run)
```
https://<your-username>.github.io/musicbu/f/xz8cvuf.mp3
```

## Files
- `playlist.txt` — one track per line. You can append duration using `|` with formats like `41m43s`, `1h41m27s`, `90s`, `2h`.
- `.github/workflows/random-mp3.yml` — GitHub Actions workflow that picks a random track, downloads it, and deploys Pages.

## How to use
1. Upload all files in this folder to your GitHub repo named **musicbu** (public).
2. Go to **Settings → Pages → Build and deployment** and set **Source = GitHub Actions**.
3. Open the **Actions** tab, run the workflow manually the first time (`Run workflow`) or wait for the schedule.
4. Use the final URL above. It will remain constant while tracks rotate.

### Rotate frequency
- The default schedule is **every 20 minutes**. Change the cron in the workflow if you prefer.
- You can also run it manually at any time from the **Actions** tab.

### Update playlist
- Edit `playlist.txt` and commit. The next run will use the updated list.

### Notes
- Only *direct* MP3 links (e.g., Pomf2/Catbox) will work.
- The workflow retries downloads and fails cleanly if a link is dead.
