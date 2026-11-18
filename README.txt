a6400 Field Settings — standalone web app (PWA)
================================================
Files: index.html, data.json, manifest.json, sw.js, icon-*.png  (keep them together in one folder)

Free hosting (pick one, ~5 minutes):
 A) Netlify Drop: open app.netlify.com/drop in a browser, drag this whole folder onto the page.
    You get a link like https://something.netlify.app (sign up free to keep it permanently).
 B) GitHub Pages: create a repository, upload all files, Settings > Pages > Deploy from branch (main, /root).
    Link: https://<your-username>.github.io/<repo>/
 C) Cloudflare Pages: Workers & Pages > Create > Pages > Upload assets > drag the folder.

On the iPhone: open the link in Safari > Share > Add to Home Screen.
Open it once with internet; after that it works offline (settings, recipes, matrices).

Updating: replace data.json / index.html, and change VERSION in sw.js (e.g. v2) so phones fetch the new files.
Note: it must be served over https (all three hosts do this). Opening index.html straight from Files will not load data.json.
