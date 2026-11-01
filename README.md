# qbo-claude-assistant-site

Static information pages for the Benemetry QuickBooks assistant, the internal Intuit app
"Claude assistant" of Benemetry Ltd. Published with GitHub Pages from `main` at `/`:
https://jayp127.github.io/qbo-claude-assistant-site/

| Page | Intuit field it serves |
|------|------------------------|
| `index.html` | Launch URL (host domain `jayp127.github.io`) |
| `privacy.html` | Privacy Policy URL |
| `eula.html` | EULA URL |
| `reconnect.html` | Connect/Reconnect URL |
| `disconnect.html` | Disconnect URL |
| `support.html` | Support contact |
| `callback.html` | Production OAuth redirect URI |

## Rules

- Every page is self-contained: no scripts, stylesheets, images, fonts, forms or redirects, and a
  `no-referrer` policy. `callback.html` receives a one-time OAuth code in its query string; nothing on
  this site may read, store or forward it.
- `callback.html` is registered with Intuit as the production redirect URI. Never move or rename it.
- Pushing to `main` publishes. After a push, run `scripts/check-site.sh` from Benemetry's private
  QuickBooks project; it verifies the build, the HTTPS setup and the rules above.
- The `<head>` block is identical on every page; change the style in all of them at once.

Owner: Benemetry Ltd, jay@benemetry.com.
