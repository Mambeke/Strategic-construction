# Strategic Construction Group website

This is a static, pre-rendered website for Cloudflare Pages. No framework or runtime dependencies are required. Run `python3 build_site.py` to regenerate pages after editing `build_site.py` or the project data. `styles.css` and `app.js` are shared across pages.

## Publishing verified projects
Edit `data/projects.json`. The build publishes only records with `"verified": true`. Before setting that field, replace every associated image with authorised photographs of that actual project and verify its title, category, location, description, status and scope. Each stage accepts multiple image filenames. Place those images in `assets/`, rebuild, and deploy. Existing unverified records remain excluded. There is no admin upload interface.

## Before accepting enquiries and final launch
- Add verified contact details, business hours, social URLs and WhatsApp number to `build_site.py`.
- Connect the contact and quote forms to a secure backend, with spam protection and a verified recipient. Currently the forms validate and download a local brief; they do not send data.
- Have the legal pages reviewed and approved by a qualified professional.
- Replace conceptual construction imagery with authorised company photographs where appropriate.
- Update the canonical base URL in `build_site.py` if a custom domain is connected, then rebuild.
- Rebuild and redeploy after changes. Cloudflare Pages is a direct-upload project, not connected to GitHub automatic deployment.
