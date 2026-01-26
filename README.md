# ◈ GHOSTLINK (BluePineApple)

"GhostLink is your all‑in‑one cyberpunk personal portal: a portable, customizable, quality‑first web environment built entirely on the client side."

GhostLink is a modular, portable personal-portal framework built entirely with HTML, CSS, and JavaScript. It bundles entertainment, productivity, customization, and privacy tools into a single cohesive styled interface.

---

## CORE MISSION
* **Fully Portable:** Easy-to-host website environment that runs anywhere.
* **Unrestricted Access:** One-click entry to tools, games, and AI utilities.
* **Lightweight:** Client-side only with zero server dependencies.
* **Quality of Life:** A thematically cohesive and feature-packed web experience.

---

## GAMING HUB
Access 600+ free HTML games, web ports, and browser-friendly tools powered by a customized gn-math script.

---

## AI TERMINAL
A powerful, local-first AI interface utilizing the Groq API for high-speed processing.

* **Privacy First:** API keys are stored in local browser storage; no server required.
* **Multimodal:** Supports image understanding and advanced vision tasks.
* **Sleek UI:** Clean, streamlined terminal-style interface.
* **High Performance:** Optimized for high token limits and rapid requests.
* 
---

## WEB PROXY (Experimental)
*Currently in Research & Development phase (basically haven't started :')*

* **Planned Features:**
  * Unblocked browsing via integrated client-side/minimal server proxy.
  * Multiple proxy engines with automatic fallback modes.
  * URL encryption and obfuscation.
  * Optional tab cloaking integration.

---

## UI SYSTEM & CUSTOMIZATION
The heart of GhostLink is its highly responsive and customizable dashboard.

* **Dynamic HUD:** Real-time splash text, clock, battery status, network ping, and FPS counter.
* **Aesthetic:** Smooth, animated UI with cyberpunk/hacker-terminal styling.
* **Deep Customization:** Modify accent colors, fonts, and themes on the fly.
* **Persistence:** All settings persist across tabs and browser sessions via LocalStorage.
* **Tab Cloaking:** Preset or custom disguises.
* **Custom App System:** Install, edit, or delete your own HTML tools.
  * Built-in App Editor (HTML content, Name, Sidebar Icons).
  * SVG Icon library and sidebar pinning.
* **App Marketplace:** Pull community apps and games from remote repositories with one-click installation.
* **Custom backgrounds**
* **Customizable keyboard shortcuts** 
* **Settings Import/Export**


---

## PRIVACY & SECURITY
* **No Tracking:** Zero server-side data collection.
* **Local Storage:** All preferences and data stay in your browser.
* **Secure Keys:** API keys never leave your client environment.

---

## DEVELOPER FRIENDLY
* **Open Source:** Fully transparent and open files.
* **Extensible:** Easy to modify, theme, or build upon.
* **Clean Code:** Organized file structure for easy navigation.
* **Universal:** Works anywhere you can run a standard HTML file.

---

## GETTING STARTED
GhostLink is built for Developers, Students, Privacy Advocates, and Gamers.

1. **Download:** Grab the `ghostlinksinglefile.html`(large file) or `jsdlvrloader.html`(small loader) or any modular components.
2. **Run:** Run the file anywhere you can run HTML.
3. **Host:** Upload to GitHub Pages, Netlify, or any static hosting service.
4. **Customize:** Mess around with site settings, add and install apps, and set-up the AI.

---

## MODDING & LIGHTWEIGHT DEPLOYMENT

### 1. Customizing the Core UI (`customizable.html`)
The `customizable.html` file acts as the primary shell. You can hardcode your own identity into the system:

* **Hardcoding Presets:** Locate the `const tabPresets` array to add your own school/work disguises that persist even if local storage is cleared.
* **Default Themes:** Modify the `:root` CSS variables (lines 8-20) to set a permanent "Signature Theme" (e.g., change `--accent` to `#ff003c` for a Cyberpunk Red look).
* **Startup Logic:** Edit the `type()` function to change the automated terminal welcome message that appears on boot.

### 2. Setting Up Your Remote Repository
To use the `jsdlvrloader.html` system, you must host your modified files on GitHub:

1.  Create a public GitHub repository (e.g., `my-ghostlink-hub`).
2.  Upload your modified `customizable.html` (or `ghostlinksinglefile.html`).
3.  Create a **Release** or simply push to the `main` branch.

### 3. Implementing the Lightweight Loader
The `jsdlvrloader.html` file is designed to bypass filters and provide ultra-fast loading by pulling from the JSDelivr Global Edge network.

**Update the loader script with your info:**
```javascript
(async () => { 
    // Replace 'username' and 'repo' with your GitHub details
    const url = "[https://cdn.jsdelivr.net/gh/YOUR_GITHUB_USERNAME/YOUR_REPO@latest/customizable.html?v=](https://cdn.jsdelivr.net/gh/YOUR_GITHUB_USERNAME/YOUR_REPO@latest/customizable.html?v=)" + Date.now();
    const response = await fetch(url); 
    const html = await response.text(); 
    document.open(); 
    document.write(html); 
    document.close(); 
})();
```
### 4. Run
Run your loader anywhere you can run html!

---

## CREDITS
* **Lead Developer:** xRevan (me)
* **Some AI**
* **Gaming Scripts:** Built using customized gn-math scripts and community-sourced game ports.
* **AI Engine:** Powered by Groq API integration.

---
*Stay Linked. Stay Ghost. Stay GhostLink 👻* 
JSDeliver link for ya nerds: https://cdn.jsdelivr.net/gh/virtuan4-max/ghostlinkhub/
