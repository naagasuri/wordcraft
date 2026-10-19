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
- **Full screen:** opened from the home-screen icon, WordCraft fills the whole screen with no
  Safari bars, like an installed app (the clock and battery stay visible at the top). In a normal
  Safari tab a small hint offers this once.
- **Updates (automatic):** every 6 hours the fork merges new commits from storytold/wordcraft and,
  if there were any, rebuilds the app. The iPad picks up the new version the next time you open
  WordCraft (fully close it and reopen if you want it straight away). Actions › **iPad web app** ›
  **Run workflow** syncs and rebuilds immediately.
- Your documents stay on the iPad; nothing is uploaded to a server.

## If an automatic update fails

The run shows a red ✗ on the **Actions** tab, and GitHub emails you. Usually it is one of these:

- **"workflow" in the message:** the original project changed its own GitHub workflow files, which
  GitHub's built-in token isn't allowed to merge. Press **Sync fork › Update branch** on the
  repository page once, or, to make it automatic for good, create a token: GitHub › your photo ›
  **Settings › Developer settings › Personal access tokens › Fine-grained tokens › Generate new
  token**, repository access *Only select repositories › wordcraft*, permissions **Contents: Read
  and write** and **Workflows: Read and write**. Then in the fork: **Settings › Secrets and
  variables › Actions › New repository secret**, name `SYNC_TOKEN`, paste the token.
- **"conflict":** an edit you made clashes with an upstream change; press **Sync fork** and choose
  how to resolve it.

## A native App Store–style app?

That needs Apple's Xcode, which only runs on macOS, plus a paid Apple Developer account to install
it on an iPad. Without a Mac, the home-screen web app above is the practical route.
