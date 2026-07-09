# Virtual Twin — web front-end

A static landing page that lets recruiters chat with **Haytham Borchani's virtual
twin**, a [Rasa](https://rasa.com)-powered assistant. The page embeds the
[rasa-webchat](https://github.com/botfront/rasa-webchat) widget and talks to a
Rasa server over the **Socket.IO** channel.

This repo contains **only the front-end**. The Rasa assistant (NLU data, domain,
flows, custom actions) lives in a separate private repository.

## Live page

Published with **GitHub Pages** from this repo's `main` branch.

## Configuration

The widget connects to the Rasa server defined at the top of `index.html`:

```js
window.RASA_SERVER_URL = "http://localhost:5005";
```

> GitHub Pages serves static files only — it cannot run Rasa. The chat will only
> respond once `RASA_SERVER_URL` points at a Rasa server that is reachable from
> the public internet (a hosted server, or a tunnel such as `ngrok` for demos).
> `localhost:5005` works only on your own machine.

## Run locally

```powershell
python -m http.server 8000
```

Then open <http://localhost:8000> (with a Rasa server running on port 5005).
