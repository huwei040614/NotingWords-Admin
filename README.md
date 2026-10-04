# NotingWords Admin

Deployment-only repository for the compiled Phase 19 content console.

- Production target: https://admin.notingwords.xyz/
- Admin route: /#/admin (existing HashRouter)
- Hosting: GitHub Actions + GitHub Pages; deploy only site/.
- Backend: existing Tencent CloudBase Auth/API/Worker. Server roles remain authoritative.
- Build source: d78d52425bf3d687213237949a4042ff0aba7dc6, branch phase19/curated-admin-console.
- Original build command: npm run build:admin; Vite base ./ (valid at both project and domain roots).
- Legacy deployment commit: bd3945c569606529a810e594862d4f021acf00de. Every compiled file was SHA-256 checked against the live legacy site before copying. index.html is an exact copy of admin.html.
- Fallback: https://huwei040614.github.io/NotingWord-Releases/admin/#/admin. The Releases repository and version 1.5.0 / 10500 remain unchanged.
- Custom domain is managed only by GitHub Pages settings. Actions ignores CNAME; no duplicate CNAME configuration.

No private app source, secrets, user data, environment files or Android signing material belongs in this repository. Public browser configuration is intentionally delivered to the browser. Secret scan passed before first push. Domain/HTTPS and the human Manual Admin Gate have passed. Phase19 remains PASS / FROZEN; Phase20 is NOT STARTED.

## Historical deployment notes

The earlier pending/freeze states below describe historical deployments and are superseded by the final acceptance above.

Phase 19 Manual Gate repair: immutable article return, revision draft hydration, persistent detail routes and save-protected navigation. Targeted tests (19), TypeScript, Admin and production Web builds passed. This follow-up adds Source and Category cancellation and excludes withdrawn articles from pending counts. Technical production Admin verification is in progress in an isolated authenticated BrowserAct session.

Follow-up: category HTML validation is compatible with modern Chrome Unicode Sets, and Admin uses the existing icon to avoid a favicon 404. Targeted tests (20), SQL gate, TypeScript, Admin and production Web builds passed. Final production browser retest is pending this deployment.

Import UX: source-aware progressive disclosure, collapsed permissions by default, Registry-derived LINK_ONLY declarations and explicit per-article FULLTEXT confirmation when source-wide coverage is incomplete. Backend rights guards are unchanged. Targeted tests (17), TypeScript and Admin production build passed; focused production browser verification follows deployment. Manual Admin Gate remains pending user confirmation; Phase19 is not frozen and Phase20 has not started.

AI Settings: server-authorized encrypted provider profiles, editable versioned Editorial Prompt Center, isolated cache/provenance and preview-only playground. Targeted frontend (45) and backend (27) tests, TypeScript and Admin production build passed; focused production verification follows deployment. Manual Admin Gate remains pending user confirmation; Phase19 is not frozen and Phase20 has not started.

AI Settings current product decision: administrator-managed cloud configuration only; no system default or hidden credential. First-use UNCONFIGURED wizard; successful test before explicit activation; atomic updates/replacement; deletion stops Editorial AI without fallback. Reader configuration is independent and unchanged. Prompt v1/history, encrypted private storage, SSRF/Admin guards, cache and provenance are retained. Focused frontend 40 and backend/Worker 29 tests, TypeScript and Admin build passed. Production browser verification continues, with user-only secret input. Manual Admin Gate remains PENDING USER CONFIRMATION; Frozen NO; Phase20 started NO.

## Source discovery post-freeze operational patch — 2026-10-05

Source readiness, RSS/Atom cadence and blockers, independent access/discovery status, observed period job status and audit-reason explanations. Existing server gates and Worker code remain unchanged; NASA alone is explicitly configured for daily RSS, metadata/link candidates and human review only. Frontend targeted 34 and SQL scheduler/worker 8 tests, TypeScript and Admin production build passed. Production UI verification follows deployment. Phase19 remains PASS / FROZEN; version 1.5.0 / 10500; Phase20 NOT STARTED.
