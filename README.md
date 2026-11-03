# Skyes Apart website

A plain HTML site (no build step). Everything that goes live is in the `public/` folder, and `public/index.html` is the home page.

## Cloudflare settings

Pushing to the `main` branch on GitHub deploys the site automatically.

If the project is a **Pages** project (Settings > Build):

| Setting | Value |
| --- | --- |
| Framework preset | None |
| Build command | *(leave empty)* |
| Build output directory | `public` |
| Root directory | *(leave empty)* |

If the project is a **Worker** (the build settings show a deploy command like `npx wrangler deploy`), leave the build command empty and the deploy command as `npx wrangler deploy`. The `wrangler.jsonc` file tells it to publish the `public/` folder.

## Editing in VS Code

One-time setup:

1. Install [VS Code](https://code.visualstudio.com/) and [Git](https://git-scm.com/downloads).
2. In VS Code, open the Command Palette (Ctrl+Shift+P, or Cmd+Shift+P on Mac), run **Git: Clone**, and paste `https://github.com/StripesMusic/skyes-apart-website`. Sign in to GitHub when asked, pick a folder, then click **Open**.
3. When VS Code suggests the recommended **Live Server** extension, click **Install**.

Every time you edit:

1. Open `public/index.html` and make your changes.
2. Click **Go Live** in the bottom-right status bar to preview the site in your browser. It refreshes every time you save.
3. When you're happy, open the **Source Control** tab (the branch icon on the left), type a short message, click **Commit**, then **Sync Changes**. Cloudflare redeploys within a minute or two.

Put images in `public/` too (for example `public/background.jpg`) and refer to them by name, like `url('background.jpg')`.
