# Haytham Borchani — About Me

A personal "About Me" page for **Haytham Borchani** — Applied AI Engineer at
BNP Paribas. It presents a short bio, experience, skills, education
and contact links, and embeds a small chat assistant so visitors can ask
questions directly.

## Live page

Published with **GitHub Pages** from this repo's `main` branch.

## Chat assistant 

The page embeds a chat widget that connects to an assistant server over the
**Socket.IO** channel. The server URL is defined at the top of `index.html`:

```js
window.CHAT_SERVER_URL = "http://localhost:5005";
```

> GitHub Pages serves static files only — it cannot run the assistant server.
> The chat will only respond once `CHAT_SERVER_URL` points at a server. `localhost:5005` works only on your own machine.

The rest of the page works with no server — the bio, experience, skills and
contact links are fully static.

## Run locally

```powershell
python -m http.server 8000
```

Then open <http://localhost:8000>.
