# jiracorp.co.in (redirect)

JIRACORP is now **Asvan Labs**. This repo only keeps the old address working: every page on
jiracorp.co.in sends the visitor to https://asvanlabs.com/ (meta refresh plus a canonical link, since
GitHub Pages cannot send an HTTP 301). The company site lives in `tdb-project/asvanlabs-site`; this
repo's history up to 2026-11-11 is the original JIRACORP page.

- `index.html` and `404.html` are the same redirect page, so any old path lands on asvanlabs.com.
- `.well-known/security.txt` points reporters to `hello@asvanlabs.com`. **Renew `Expires` before 2027-11-11.**
- `.nojekyll` keeps `.well-known/` served.

## DNS (GoDaddy, `ns31/32.domaincontrol.com`)

- `@` A: GitHub Pages `185.199.108–111.153`; `www` CNAME `tdb-project.github.io`.
- `tdb` A records serve The Data-Bridge landing page (separate repo); leave them alone.
- MX and other TXT records are Google Workspace mail (`hello@jiracorp.co.in` still receives mail); leave them alone.

If a true 301 is ever needed (for example Google Search Console's change of address), switch the apex to
GoDaddy domain forwarding to `https://asvanlabs.com` and remove the A records; `tdb` is unaffected.
