<p align="center"> 
  <img src="https://cdn.jsdelivr.net/gh/virtuan4-max/ghostlinkhub@main/assets/logo.png" width="220" /> 
</p> 
<h1 align="center">G H O S T L I N K</h1> 
<p align="center"> 
  <b>Your all-in-one cyberpunk personal portal. Welcome to the hub ;P</b><br/> 
  <sub>Client-side only · Fully portable · Unrestricted access · No tracking 
</p> 
<p align="center"> 
  <a href="https://cdn.jsdelivr.net/gh/virtuan4-max/ghostlinkhub/"><img src="https://img.shields.io/jsdelivr/gh/hm/virtuan4-max/ghostlinkhub?style=flat-square&color=orange&label=jsDelivr" /></a> 
  <a href="https://github.com/virtuan4-max/ghostlinkhub"><img src="https://img.shields.io/github/stars/virtuan4-max/ghostlinkhub?style=flat-square&color=6ecbff" /></a> 
  <a href="https://discord.gg/dKs2sUNUXd"><img src="https://img.shields.io/badge/Discord-Join-5865F2?style=flat-square&logo=discord&logoColor=white" /></a> 
  <a href="https://deepwiki.com/virtuan4-max/ghostlinkhub"><img src="https://deepwiki.com/badge.svg" alt="Ask DeepWiki"></a>
</p> 

--- 

GhostLink is a modular, portable personal-portal framework built entirely with HTML, CSS, and JavaScript. It bundles entertainment, productivity, customization, and privacy tools into a single cohesive styled interface. 

--- 

## 🎮 Gaming Hub 

700+ free games and HTML5 ports powered by the [gn-math](https://github.com/gn-math) community game library. (I do plan on adding my own games and riping all of gn-maths🥹) 

- **Favorites** — heart any game to save it; toggle a filter to show only your picks 
- **Download** — save any game as a standalone `.html` file to run offline 
- **Ad Cleaned** — ad injections and sidebar spam are stripped before rendering 

--- 

## 🤖 AI Terminal 

A fast, local-first AI interface running on the [Groq API](https://groq.com). 

- **Works out of the box** — ships with cloud-managed rotating API keys, no setup needed 

- **Custom key support** — supply your own Groq key in Settings for guaranteed priority 

- **Multimodal** — attach up to 5 images at once; auto-switches to the `llama-4-scout` vision model when images are detected 

- **Model selection** — choose from `llama-3.3-70b`, `groq/compound`, `groq/compound-mini`, and more 

- **Session management** — full chat history saved to `localStorage`, browseable via the sidebar history panel 

- **Markdown rendering** — responses render with full formatting support 

- **Privacy first** — keys and history never leave your browser 

--- 

## 🌐 Web Proxy 

A full multi-tab proxy browser built right into the dashboard, powered by [Scramjet](https://github.com/MercuryWorkshop/scramjet) + BareMux + Epoxy transport. 

- **Multi-tab browsing** — tabs, address bar, back/forward/reload, and a loading bar 

- **Built-in ad blocker** — service worker blocks requests to 29+ ad/tracker domains at the network level before they load 

- **Wisp server management** — ships with 4 servers, auto-picks the fastest, add your own `wss://` any time 

- **DevTools** — inject Eruda into any proxied page with one click 

--- 

## Dashboard & Everything Else 

GhostLink is also a full-featured personal dashboard with deep customization built in. 

- **Dynamic HUD** — live clock, battery status, FPS counter, ping monitor, and typewriter splash text on the home screen 

- **Theme engine** — change accent color, background, text colors, blur, brightness, and fonts (including any Google Font by URL) on the fly 

- **Tab cloaking** — preset disguises (Google, Classroom, Desmos, etc.) or fully custom title + favicon, with an about:blank cloaker 

- **Custom apps** — install your own HTML tools or URL shortcuts, pick an icon, and pin them to the sidebar 

- **App marketplace** — pull community apps from the remote GitHub repo with one-click install 

- **Keyboard shortcuts** — rebind the home, games, and panic keys; add custom `Alt + Key` bindings for any section 

- **Drag-and-drop sidebar** — reorder nav items however you want 

- **Settings import/export** — export your entire config (apps, shortcuts, theme, nav order) to `.json` and import it on any device 

- **Live presence** — online user counter and total visit tracker powered by Supabase Realtime 

- **README & version viewer** — click ◈ to read the live README or browse the last 30 commits with full changelogs; auto-update checker pops a modal when something new drops 

- **Repo tools** — browse and download any file from the GhostLink GitHub repo, view YHS assets with a lightbox, or load an experimental 3D site visualizer 

--- 

## Self-Hosting 
**The loader & js:** 

Download the ```index.html```,```sw.js``` and ```bareworker.js``` from the self hosting folder in the [github repo](https://cdn.jsdelivr.net/gh/virtuan4-max/ghostlinkhub@main/) or create ones yourself with the code from the jsdlvr links. 

- [index.html](https://cdn.jsdelivr.net/gh/virtuan4-max/ghostlinkhub@master/self%20hosting/index.html) 
- [sw.js](https://cdn.jsdelivr.net/gh/virtuan4-max/ghostlinkhub@master/self%20hosting/sw.js) 
- [bareworker.js](https://cdn.jsdelivr.net/gh/virtuan4-max/ghostlinkhub@master/self%20hosting/bareworker.js) 

*note: you can host only the index.html if you need to, but the proxy wont work becuse it NEEDS the service worker and bareworker to function.😅😅* 

--- 

## How It was Built 

GhostLink is *(almost)* zero-dependency on the client side. The all files are vanilla HTML, CSS, and JavaScript as a multi-paged single-page application. 

The game library fetches gn-math statistics, assets, and cover images using the jsdelivr cdn. Games are rendered directly into iframes. 

The AI terminal makes direct `fetch` calls to the Groq API from the client. Cloud keys are fetched from a remote vault at startup, shuffled, and rotated per-message. Image attachments are detected and trigger an automatic model swap. 

The proxy runs through a registered service worker (`sw.js`) that intercepts fetch events, routes traffic through Scramjet, and kills ad requests before they resolve. BareMux manages the WebSocket transport layer and Epoxy handles the Wisp protocol underneath. 

--- 

## External Dependencies 

| Library | Version | Purpose | 
|---|---|---| 
| [Scramjet](https://github.com/MercuryWorkshop/scramjet) | CDN | Proxy request rewriting | 
| [BareMux](https://github.com/MercuryWorkshop/bare-mux) | `2.1.7` | WebSocket transport layer | 
| [Groq API](https://groq.com) | — | AI inference | 
| [Supabase JS](https://supabase.com) | `2.39.7` | visit counter | 
| [Font Awesome](https://fontawesome.com) | `6.5.1` | Icons | 
| [Eruda](https://github.com/liriliri/eruda) | CDN | In-browser DevTools (proxy) | 
| [jsDelivr](https://www.jsdelivr.com) | CDN | CDN for loader and assets | 

--- 

## Credits 

**SOLE Developer:** [xRevan](https://github.com/virtuan4-max) @xrevannn on discord :P

**Games** Built using customized [gn-math](https://github.com/gn-math) scripts and community-sourced game ports. 

**Proxy** [Scramjet](https://github.com/MercuryWorkshop/scramjet) + BareMux + Epoxy Transport by [MercuryWorkshop](https://github.com/MercuryWorkshop) and the base og version was developed by @scentedcheeseburge on discord (W❤️‍🩹❤️‍🩹)

**AI Engine:** Powered by [Groq API](https://groq.com). 

**Some AI** (Un poco de Gemini y mucho de Claude 🥹) 

--- 

*JSDelivr link for ya nerds 🙄 https://cdn.jsdelivr.net/gh/virtuan4-max/ghostlinkhub/* 
