
---

## 🧩 How It Works

The app reads the pasted JSON and extracts the VLESS outbound profile:
- `outbounds[].protocol == "vless"`
- `settings.vnext[0].address / port`
- `settings.vnext[0].users[0].id`
- stream settings (`ws`, `tls`, `sni`, `fp`, `alpn`, etc.)

Then it generates:
- a standard **VLESS URI**
- a usable **Sing-box outbound** config
- a basic **Clash** config template including proxy/group/rules

---

## 🛠️ Installation & Deploy

### 1) Upload files
Commit the files to the repo root:
- `index.html`
- `manifest.json`
- `sw.js`
- `icon-192.png`
- `icon-512.png`

### 2) Enable GitHub Pages
Go to:
**Settings → Pages**
- Source: **Deploy from a branch**
- Branch: `main`
- Folder: `/ (root)`
Save.

### 3) Open the website
When Pages finishes deploying, open the URL.

---

## 📲 Install as an App (PWA)

### Desktop (Chrome)
- Open the GitHub Pages URL
- Click the install icon in the address bar (or menu → **Install app**)

### Android (Chrome)
- Open the URL
- Menu → **Add to Home screen** / **Install app**

---

## 🔒 Privacy

- No login, no analytics, no tracking.
- All conversion runs locally in your browser.
- Only the QR image (if remote generator is used) requests an external endpoint.

> If you want a 100% offline QR generator, open an issue or contribute a PR.

---

## ✅ Compatibility

- Chrome / Edge (recommended)
- Firefox (works, PWA install support varies)
- Safari (limited PWA features depending on iOS/macOS version)

---

## 🧪 Notes

- If your JSON doesn’t include a `vless` outbound, conversion will fail with a clear error.
- Some advanced provider formats may require extra mapping — contributions are welcome.

---

## 🤝 Contributing

PRs are welcome:
- Better Clash templates
- Full offline QR generator
- Multi-profile JSON support
- Import/export presets

---

## 📄 License

MIT
