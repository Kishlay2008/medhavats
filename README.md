# SmartBook — GitHub Pages version

## Deploy the static demo
1. Create a GitHub repository (for example, `smartbook`).
2. Upload the contents of this folder to the repository root. `index.html` must be in the root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/(root)`, then Save.
5. Wait for GitHub Pages to publish the site. The URL will be shown in Settings → Pages.

## Pages
- `index.html` — landing page
- `book.html` — booking demo
- `admin.html` — merchant dashboard demo
- `manage.html` — customer portal demo

## Important limitations
GitHub Pages only serves static files. It does not run Express/Node.js API routes, Firebase Functions, or keep API secrets safe. The booking form currently stores demo bookings in the visitor's browser (`localStorage`), and the AI panel displays a demo response; it does not send real WhatsApp messages, accept payments, or call Gemini.

The optional backend source and `package.json` are in `backend/` for separate deployment to Firebase Functions or another server platform. Before using it in production, configure Firebase and a server-side `GEMINI_API_KEY` secret, and implement real database, payment, and messaging integrations. Do not put Gemini secret keys in frontend files.

`js/firebase-config.js` contains placeholder Firebase values and is not used by the static demo until you configure and initialize Firebase.
