# GitHub Pages MP3 Auto-Fetch (Template)

This repo auto-fetches an MP3 from a source URL and publishes it to GitHub Pages at:

```
https://<your-username>.github.io/<your-repo>/f/xz8cvuf.mp3
```

## How to use

1. Create a new GitHub repository (public or private).
2. Upload **all files** from this template (including the `.github` folder) to your repo (unzip first; drag-and-drop is fine).
3. Go to **Settings → Pages → Build and deployment → Source = GitHub Actions**.
4. Edit `source_url.txt` and paste **one line**: the direct MP3 URL (e.g. Pomf2 link).
5. Commit. The workflow runs and deploys your site.
6. Your final link will be:

```
https://<your-username>.github.io/<your-repo>/f/xz8cvuf.mp3
```

To change the track later, just edit `source_url.txt` with a new MP3 URL and commit.
