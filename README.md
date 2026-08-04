# Rural APS — deploy build (GitHub repo -> Cloudflare Pages)

Single source: this repo is served by GitHub Pages (preview at
yherhr.github.io/RAPS/) AND deployed to production by Cloudflare Pages
(ruralaps.com.au). One push updates both.

Build notes: relative links (work at domain root and under the /RAPS/
subpath); canonicals point to https://www.ruralaps.com.au/ so search
consolidates to the real domain; sitemap.xml/robots.txt/_redirects are
production files (harmless on GitHub Pages); .nojekyll included.

## Updating the site
1. Replace repo files with this build's contents — ADD/OVERWRITE, do not
   delete images/ first (images added directly to the repo, e.g.
   Mathew-133.jpg, live only there).
2. Push to main. GitHub Pages and Cloudflare Pages both redeploy.

## After the domain goes live on Cloudflare
- Optionally turn OFF GitHub Pages (repo Settings -> Pages -> Source: None).
  The repo keeps working as the Cloudflare deploy source; the github.io
  preview simply stops being served.
- Submit sitemap.xml in Google Search Console; set up GA4.

## Go-live checklist
- [ ] images/Mathew-133.jpg present in the repo (referenced by the home About block)
- [ ] Test the enquiry form (delivers to ruralaps@hotmail.com; check junk on first test)
- [ ] Verify Facebook link works: https://www.facebook.com/share/1F1fu1cJkC/
- [ ] Logo/photos reviewed; captions confirmed by Mathew
