# NotingWords Admin

Deployment-only repository for the compiled Phase 19 content console.

- Production target: https://admin.notingwords.xyz/
- Admin route: /#/admin (existing HashRouter)
- Hosting: GitHub Actions + GitHub Pages; deploy only site/.
- Backend: existing Tencent CloudBase Auth/API/Worker. Server roles remain authoritative.
- Build source: 867de504d348798d9c96e605f4b303f88fff2002, branch phase19/curated-admin-console.
- Original build command: npm run build:admin; Vite base ./ (valid at both project and domain roots).
- Legacy deployment commit: bd3945c569606529a810e594862d4f021acf00de. Every compiled file was SHA-256 checked against the live legacy site before copying. index.html is an exact copy of admin.html.
- Fallback: https://huwei040614.github.io/NotingWord-Releases/admin/#/admin. The Releases repository and version 1.5.0 / 10500 remain unchanged.
- Custom domain is managed only by GitHub Pages settings. Actions ignores CNAME; no duplicate CNAME configuration.

No private app source, secrets, user data, environment files or Android signing material belongs in this repository. Public browser configuration is intentionally delivered to the browser. Secret scan passed before first push. Domain/HTTPS smoke and the human Manual Admin Gate are separate; the human gate remains PENDING.

Phase 19 Manual Gate repair: immutable article return, revision draft hydration, persistent detail routes and save-protected navigation. Targeted tests (17), TypeScript, Admin and production Web builds passed. Technical production Admin browser verification remains BLOCKED until the existing authenticated Chrome session is available to the browser tool; no production test data was created by this repair.
