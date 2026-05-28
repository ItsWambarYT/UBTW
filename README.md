# UBTW

Un-Block The World — web proxy for the school Chromebook. Two engines live in this repo: `nodeunblocker.com` (recommended) and `Riptide` (backup).

## Use it

1. On github.com, open this repo → **Code → Codespaces → Create codespace on main**. A VS Code editor opens in the browser.
2. In the terminal at the bottom of the Codespace, run:
   ```bash
   cd nodeunblocker.com
   npm install
   npm start
   ```
3. A popup appears for port **8080** — click **Open in Browser**.
4. **Critical, don't skip:** open the **Ports** tab at the bottom, right-click port `8080` → **Port Visibility → Public**. Without this the URL shows a GitHub login wall and the school Chromebook can't reach it.
5. Copy the forwarded URL (looks like `https://<something>-8080.app.github.dev`). Open it in any browser, type a blocked URL in the box, go.

To stop the proxy: `Ctrl+C` in the terminal.
To shut the whole Codespace and free your monthly hours: go to [github.com/codespaces](https://github.com/codespaces) → click `…` next to the Codespace → **Stop**.

## Riptide (backup)

If a site doesn't render right under nodeunblocker, try Riptide instead:

```bash
cd Riptide
npm install
npm start
```

Same port-forward + Public-visibility step. Riptide runs a quick webpack build on first launch — give it 5–10 seconds to bind before you click the popup.

## Notes

- **Don't post the URL anywhere public.** Anyone with it can route traffic through the Codespace.
- **The URL changes** for each new Codespace. To keep the same URL, resume an existing Codespace (Code → Codespaces → click the existing one) instead of creating a new one each time.
- Codespaces has a monthly free quota; a proxy session uses a few minutes of it.
- If `npm install` ever errors with "no package.json" or similar, one of the proxy folders has gone empty — re-pull main and try again.
