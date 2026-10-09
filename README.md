# Privacy Site Deployment Guide

This directory contains the static site for 易识 / WrenRec: privacy policy, open-source licenses, and support page. It is deployed via GitHub Pages and referenced by the in-app "Open-Source Licenses" link and the App Store Connect listing.

## Deployment Steps

1. The site lives in the public repo **`Kn0688/wrenrec-privacy`** (already created). The three HTML files sit at the repository root: `index.html` / `licenses.html` / `support.html`.
2. GitHub Pages is enabled: Settings → Pages → Source = `main` branch, `/ (root)`.
3. After pushing changes, Pages rebuilds in about a minute. Live URLs:
   - Privacy policy: `https://kn0688.github.io/wrenrec-privacy/` (use this as the "Privacy Policy URL" in App Store Connect)
   - Open-source licenses: `https://kn0688.github.io/wrenrec-privacy/licenses.html` (the app's AboutView already points here)
   - Support: `https://kn0688.github.io/wrenrec-privacy/support.html` (use this as the "Support URL" in App Store Connect)
4. After any update, verify all three pages load correctly (ideally from mobile Safari with any proxy/VPN disabled).

## Related Code Locations

- In-app licenses link: `licensesURL` in `SenseTranscription/Views/AboutView.swift` (points to the licenses.html URL above; update it if the repo is ever renamed)
- Contact email (single source of truth): `SenseTranscription/Utils/AppContact.swift` — keep the email in support.html in sync with it
- License inventory source document: `开源许可清单.md` in the app repository root — review it and update licenses.html whenever dependencies are upgraded

## Notes

- GitHub Pages availability in mainland China is inconsistent. If users report the pages unreachable after launch, consider migrating to a domestic host with ICP registration.
- Site content (effective dates, license lists) ships with each push — just commit and push to update.
