# Publishing a new "Did you know?" tip

1. Add the mp4 to `videos/` (e.g. `videos/draft-recipes.mp4`).
2. Add an entry to `manifest.json`:
   ```json
   {
     "videos": [
       {
         "url": "https://www.forkenspoon.com/how-to/videos/draft-recipes.mp4",
         "title": "Draft recipes before publishing"
       }
     ]
   }
   ```
   `url` must be the full `https://www.forkenspoon.com/...` address, not a relative path — the app fetches this file directly, not from a page that could resolve a relative URL. `title` is optional and never shown on top of the video itself (the clip's own baked-in art/text covers that); it's just a label for this page and for accessibility.
3. Commit and push. GitHub Pages redeploys automatically; both this page and the app pick up the change on their next fetch (the app fetches manifest.json fresh every time onboarding shows).
