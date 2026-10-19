# WordCraft on iPad (no Mac needed)

WordCraft runs on iPad as a home-screen web app: it opens full screen with its own icon, works
offline after the first visit, and opens and saves .docx files through the Files app.
GitHub builds it for you, so all you need is a Windows PC (or the iPad itself) and a free
GitHub account.

## One-time setup (about 10 minutes, plus the build)

1. **Fork the repo:** open https://github.com/storytold/wordcraft, click **Fork** › **Create fork**.
2. **Add the iPad files** to your fork (if they aren't there already): in your fork click
   **Add file › Upload files**, drag in the contents of `wordcraft-ipad-files.zip` (the
   `apps`, `.github` folders, `ATTRIBUTION.md` and this `IPAD.md`), and click **Commit changes**.
3. **Turn on Pages:** **Settings › Pages › Build and deployment › Source: GitHub Actions**.
4. **Build:** **Actions** tab › if asked, click *I understand my workflows, enable them* ›
   **iPad web app** › **Run workflow**. The first build takes roughly 20–40 minutes.
5. When it turns green, the address is shown on the run's **deploy** step:
   `https://<your-github-name>.github.io/wordcraft/`

## Install on the iPad

1. Open that address in **Safari** (WordCraft takes a few seconds to load the first time).
2. Tap **Share** (square with an arrow) › **Add to Home Screen** › **Add**.
3. Start WordCraft from its home-screen icon from then on.

## Using it on iPad

- **Open:** File › Open, then pick a .docx from the Files app (iCloud Drive, On My iPad, Google
  Drive, OneDrive…).
- **Save:** Safari has no "save in place", so Save downloads the .docx; Safari asks where to put it
  (or it goes to *Downloads* in the Files app).
- **Keyboard:** a hardware keyboard (Magic Keyboard / Smart Keyboard) is strongly recommended;
  Word's shortcuts work, with ⌘ on Apple keyboards.
- **Updates:** every new run of the workflow updates the app; close and reopen it to pick it up.
  To pull in upstream fixes, on your fork's page click **Sync fork**, then run the workflow again.
- Your documents stay on the iPad; nothing is uploaded to a server.

## A native App Store–style app?

That needs Apple's Xcode, which only runs on macOS, plus a paid Apple Developer account to install
it on an iPad. Without a Mac, the home-screen web app above is the practical route.
