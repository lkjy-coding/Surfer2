# Surfer2

Surfer2 is an upgraded version of Surfer, but it can really go online, search online, and even support watching videos online. Compared to Surfer, Surfer2 has a wider range of territories. So, make the most of Surfer2!

## Important tips

# Warning

Currently known in version 3.00.00, in `surfer:settings`: When switching **between dark/light colors** in settings', the switch is too direct and **may be visually unfriendly**, **especially when switching to light mode**. In 3.10.00, this issue was fixed. **Currently, it is strongly recommended that you immediately stop using version 3.00.00.**

## The tips

Now I am trying to make the connection by Surfer2 safe,but I'm still not sure about it.So **I don't suggest you to enter something important on it**.

---

# Updates

## 1.00.00

- \-

## 1.10.00

- Roughly corrected the issue of some websites automatically calling the system browser redirect
- Enhanced connection security as much as possible
- Implemented UA switching

## 1.20.00

### 🚀 New Features

- **UA Switching (No hard redirect)**: Improved mobile/desktop mode switching without `/m` hard redirect
- **Adaptive Viewport**: Webpage frame now auto-adapts, no need to scroll horizontally
- **Error Code Reference**: Added detailed error code reference panel (-7, -101, -103, -105, -118, -130, -200, -300)
- **Settings Panel**: New comprehensive settings interface
- **Light/Dark Theme Toggle**: Support switching between light and dark mode
- **Blacklist/Whitelist**: Domain filtering with customizable blacklist/whitelist
- **Bookmarks (Favorites)**: Add, manage, and double-click to load websites
- **Local Persistence**: All settings, bookmarks, and lists are saved locally

### ⚙️ Enhanced

- **Auto-reload Toggle**: Disable auto-reload on connection failure (configurable in settings)
- **Security Badge**: Enhanced site trustworthiness indicator

### 🐛 Fixed

- Removed faulty `/m` hard redirect for UA switching
- Fixed page display issues with better viewport adaptation

## 1.30.00

### 🚀 New Features

#### 1. Internal Domain Foundation
- Laid the groundwork for internal `surfer:*` domains.
- Added routing logic to distinguish between external websites and built-in pages.

#### 2. Enhanced URL Normalization
- Improved address bar input handling.
- Automatically adds `https://` prefix when missing.
- Converts simple search terms to Bing search queries.

#### 3. Basic Local Storage for Settings
- Settings (auto-reload, whitelist, blacklist) now persist across sessions.
- Bookmarks and notebook data structure prepared (UI coming in later versions).

---

### ⚙️ Enhanced

- **Iframe Sandbox Security**: Refined sandbox permissions to block unwanted popups and redirects while keeping core functionality intact.
- **Error Handling**: Better timeout detection and user-friendly error messages for common network issues (-7, -101, -103).

---

### 🐛 Fixed

- Fixed an issue where some websites would still open links in the system browser despite previous fixes.
- Corrected URL bar display after internal navigation (history stack now updates properly).
- Resolved a bug where the reload button would not work correctly on certain pages.

---

### 🛠️ Technical Improvements

- Refactored navigation logic (`navigateTo`, `goBack`, `goForward`) to support both external and internal URLs.
- Improved iframe load event handling to reduce false "timeout" errors on slow connections.
- Code restructuring to prepare for internal page system (`surfer:settings`, `surfer:note`, `surfer:chess`).

---

## 🧠 How to Use

| Feature | Action |
|---------|--------|
| Normal browsing | Type any URL or search term in the address bar |
| Reload | Click ⟳ button |
| History navigation | Use ◀ (back) and ▶ (forward) buttons |

---

## 📦 Upgrade Notes

- This version is a **foundational update** – no visible internal pages yet, but the system is ready for them.
- All settings from 1.20.00 are automatically migrated.
- External browsing behavior should be identical to 1.20.00, but with improved stability.

---

## 🐞 Known Limitations

- Internal domains (`surfer:*`) are not yet user-accessible (UI coming in 2.00.00).
- Background customization not yet available (introduced in 2.10.00).

## 2.00.00

## Big Update!

## 🚀 New Features

### 1. Internal Domain: `surfer:settings`
- All settings have been moved to the built-in `surfer:settings` page.  
- The original settings button now redirects to this internal domain.  
- Settings (auto-reload, whitelist, blacklist) are automatically saved to local storage.

### 2. Internal Domain: `surfer:note`
- A real-time local notebook.  
- Everything you type is automatically saved to your browser.  
- You can clear the note with one click.

### 3. Internal Domain: `surfer:chess`
- Play Tic-Tac-Toe against a simple AI.  
- The robot moves automatically after your turn.  
- You can restart the game at any time.

### 4. Boss Key (Emergency Switch)
- Press the **B** key anywhere in Surfer2.  
- It instantly jumps to `surfer:settings` (the settings page).  
- Perfect for quickly hiding what you were browsing.

---

## 🧠 How to Use

| Action | Method |
|--------|--------|
| Open settings | Type `surfer:settings` in the address bar, or press **B** |
| Open notebook | Type `surfer:note` in the address bar |
| Play chess | Type `surfer:chess` in the address bar |
| Boss key | Press **B** at any time |

---

## 🛠️ Technical Notes

- All internal pages work without an internet connection.  
- Notes and settings are stored locally using `localStorage`.  
- The chess AI is a simple rule‑based bot (easy mode).  
- Boss key does not close the window – it only navigates to the settings page for privacy.

## 2.10.00

## ✨ New Features

### 1. Settings Page (`surfer:settings`) – Full Customization
- **Custom window appearance**  
  - Change background color, container background, and border color  
  - Upload a local image as background (automatically converted to Base64)  
  - Enter an image URL as remote background  
- **Custom font support**  
  - Four options: **Follow System**, **Segoe UI**, **Monospace (UTF-8)**, **Universal Chinese Font (Noto Sans CJK SC)**  
- All style preferences are saved automatically to `localStorage`

### 2. Notebook Page (`surfer:note`)
- Real‑time local note‑taking  
- Auto‑save on every keystroke  
- One‑click clear button

### 3. Chess Page (`surfer:chess`) – Rule Demo Added
- **Rule demonstration game**  
  - One‑click demo shows a typical opening (center vs. corner)  
  - Helps new players understand the basic rules  
- Play against a simple AI (easy mode)  
- Reset game at any time

### 4. Boss Key – Visual Button
- **On‑screen B button** (same as pressing keyboard `B`)  
- Removed the old floating text hint in the bottom‑right corner  
- Pressing either the button or the `B` key instantly jumps to `surfer:settings`

---

## 🛠️ Technical Improvements

- All internal pages now respect **global font & background settings**  
- Background images can be uploaded **without external hosting** (Base64)  
- Chess AI uses a simple but stable rule‑based logic  
- Better event handling for dynamic style switching

---

## 🧠 How to Use the New Features

| Feature | Action |
|---------|--------|
| Open settings | Type `surfer:settings` in the address bar, or press **B** |
| Open notebook | Type `surfer:note` |
| Play chess | Type `surfer:chess` |
| Rule demo (chess) | Click **🎬 规则演示局** button inside the chess page |
| Boss key | Click the **B** button on the toolbar or press keyboard **B** |
| Custom background | Go to settings → upload image or pick color → click *Apply Style* |

---

## 📦 Upgrade Notes

- All previous settings (whitelist, blacklist, auto‑reload) are **fully compatible**  
- Custom styles are stored in `localStorage` and will **persist after restart**  
- No external dependencies added – still a single HTML file

---

## 🐞 Known Limitations

- Background images uploaded as Base64 may increase storage usage slightly  
- Chess AI is intentionally simple (not unbeatable) – suitable for casual play

## 2.20.00

## 🐞 Bug Fixes

### 1. Fixed `surfer:note` Not Working Properly
- **Issue:** Notebook page failed to load and the address bar domain did not update.
- **Fix:** Corrected internal routing logic — the address bar now correctly shows `surfer:note` when the notebook page is active. Note content now saves and loads reliably.

### 2. Fixed Background Reset Issue in `surfer:settings`
- **Issue:** After setting a custom background image or color, changing other settings (e.g., font, container color) would reset the background to default.
- **Fix:** Style values are now saved independently and applied correctly without overwriting each other. Background, font, container background, border color, and acrylic mode are stored and restored separately.

---

## ✨ New Features

### 1. Removed Boss Key Popup Hints
- All floating text hints related to the Boss Key have been **completely removed**.
- Only the **B button** remains on the toolbar (visual button). Pressing either the button or the `B` key instantly jumps to `surfer:settings`.

### 2. Built-in Color Picker (Color Wheel)
- Replaced plain text color inputs with **native HTML color wheels** (`<input type="color">`) in the settings page.
- Better user experience for selecting background colors, container backgrounds, and border colors.

### 3. Acrylic (Frosted Glass) Style
- Added a **toggle switch** in settings to enable/disable **acrylic / frosted glass effect**.
- When enabled, the main window uses `backdrop-filter: blur()` and semi-transparent backgrounds for a modern translucent look.

### 4. One-Click Hide Window
- Added a **🙈 Hide** button on the toolbar.
- Clicking it instantly hides the entire Surfer2 window (opacity + visibility hidden).
- A temporary **👁️ Show Window** button appears to restore the window.
- Perfect for quickly hiding the browser when needed (privacy / quick escape).

---

## 🛠️ Technical Improvements

- Internal page routing now correctly updates the **address bar domain** for all three internal pages (`surfer:settings`, `surfer:note`, `surfer:chess`).
- Style persistence logic was **refactored** to prevent background resets.
- Acrylic mode can be enabled/disabled independently from other style settings.
- Hide/restore functionality is handled with smooth UI feedback.

---

## 🧠 How to Use New Features

| Feature | Action |
|---------|--------|
| Fix note page | Type `surfer:note` in address bar → works correctly now |
| Fix background reset | Go to `surfer:settings` → change background, font, colors → they will all persist together |
| Boss Key | Click **B** button on toolbar or press keyboard **B** (no extra popups) |
| Color wheel | In settings, click any color picker (background, container, border) |
| Acrylic mode | Go to settings → check **亚克力磨砂效果** → click *Apply Style* |
| Hide window | Click **🙈 Hide** button on toolbar → a *Show Window* button appears to restore |

---

## 📦 Upgrade Notes

- All previous settings (whitelist, blacklist, auto‑reload, custom styles) are **fully migrated**.
- Acrylic mode is **disabled by default** – enable it manually in settings.
- The hide window feature does not close or reload the page – it only hides the visual container.

---

## 🐞 Known Limitations

- Acrylic effect may have reduced performance on very low‑end devices (can be turned off).
- Hide window button is for privacy/quick hide – does not lock or password‑protect the window.

## 2.20.01

## 🐞 Bug Fixes

### 1. Fixed `surfer:chess` Board Position
- **Issue:** Chess board was displayed at the bottom of the page instead of the center.
- **Fix:** Added a flex wrapper (`.chess-wrapper`) to properly center the chess board vertically and horizontally.

### 2. Fixed Background Image Rotation/Shift in Landscape Mode
- **Issue:** When using a landscape background image on a mobile device, re-entering Surfer2 caused the background to rotate or shift abnormally.
- **Fix:** Separated the background into an independent fixed layer (`<div class="bg-layer">`). The background now stays perfectly centered and covered regardless of device orientation or viewport size.

### 3. Fixed Background Image Not Updating After Switching
- **Issue:** After setting a new background image and saving settings, the new image did not take effect – the old image remained.
- **Fix:** Refactored the style persistence logic. Background images are now saved and loaded independently. The new image is applied immediately when "Apply Style" or "Save All Settings" is clicked.

### 4. Refined Acrylic (Frosted Glass) Effect
- **Issue:** Acrylic effect previously applied only to the toolbar and container background, which was inconsistent with the intended design.
- **Fix:** Acrylic mode now creates a **separate overlay layer** that sits between the background image and the main container. When enabled:
  - The background layer remains fully visible underneath
  - An acrylic blur layer covers the entire screen
  - The Surfer2 container becomes semi-transparent with backdrop blur
  - Result: A true **frosted glass effect** over the entire window, matching the visual design of modern operating systems

---

## ✨ New Features

### None in this release (pure bugfix and polish)

---

## 🛠️ Technical Improvements

- **Separated background layer** – independent from main container, preventing orientation and scaling issues
- **Acrylic layer isolation** – blur effect now applies globally rather than per-element
- **Style persistence refactored** – background image, container color, font, border color, and acrylic mode are all saved and restored correctly without conflicts
- **Chess layout now properly centered** using flexbox

---

## 🧠 How to Test the Fixes

| Fix | How to Verify |
|-----|----------------|
| Chess board position | Open `surfer:chess` → Board should be vertically and horizontally centered |
| Background rotation | Set a landscape background → rotate device → background stays fixed and properly covered |
| Background switch | Set background A → save → set background B → save → background B appears immediately |
| Acrylic effect | Enable Acrylic in settings → entire window should have frosted glass effect, background visible underneath |

---

## 📦 Upgrade Notes

- All previous settings (background, colors, fonts, acrylic mode) are **fully compatible** – no data loss
- The new acrylic effect requires `backdrop-filter` support (modern browsers only)
- Background layer now uses `position: fixed` – this may affect extremely old browsers, but all modern browsers work perfectly

---

## 🐞 Known Limitations

- Acrylic effect may cause slight performance overhead on very low-end devices (can be disabled in settings)
- Background images uploaded as Base64 are stored in `localStorage` – very large images may hit storage limits (typically 5-10MB)

## 2.30.00

### 🚀 New Features

#### 1. New Internal Domain: `surfer:easyabroad`
- Integrated **EasyAbroad Second Edition** (without emoji in title) into Surfer2.
- Provides all-in-one travel assistant features:
  - 📍 Auto IP location detection (country, local time, timezone)
  - 💱 Real‑time currency exchange rate conversion
  - 🌍 Smart translation (auto detect source language, supports ZH/EN/JA)
  - 🌐 Quick navigation to international websites (YouTube, X, Google, Wikipedia)
- Fully self‑contained, no external dependencies.

#### 2. New Internal Domain: `surfer:chajian`
- Added **plugin entry point** for future extensions.
- Currently displays a placeholder page indicating the plugin system is under development.
- Designed to support:
  - Ad filtering
  - Script extensions
  - Theme marketplace
  - Third‑party plugin loading

#### 3. Initial Page Set to `about:blank`
- Surfer2 now launches with a **blank page** instead of loading any external website by default.
- Improves startup performance and privacy.

#### 4. Version Info Moved to Bottom of Settings Page
- The Surfer2 version number and available internal domains are now displayed at the **bottom** of `surfer:settings` page.
- Removed version number from the settings page title for a cleaner look.

---

### 🛠️ Technical Improvements

- **EasyAbroad integration** uses the same IP detection, exchange rate API, and translation API as the standalone version.
- All EasyAbroad functions are fully functional inside Surfer2 without any additional network requests beyond the original APIs.
- Internal routing logic extended to support `easyabroad` and `chajian` domains.
- The plugin page serves as a stable foundation for future plugin ecosystem.

---

## 🧠 How to Use New Features

| Feature | Action |
|---------|--------|
| Open EasyAbroad | Type `surfer:easyabroad` in address bar |
| Open plugin center | Type `surfer:chajian` in address bar |
| Start with blank page | Launch Surfer2 → automatically loads `about:blank` |
| Check version info | Go to `surfer:settings` → scroll to bottom |

---

## 📦 Upgrade Notes

- All previous settings (whitelist, blacklist, auto‑reload, custom styles, acrylic mode) are **fully compatible** – no data loss.
- EasyAbroad runs entirely inside Surfer2 – no need to open a separate page or tab.
- The plugin system is **not yet functional** – only the entry point is ready. Actual plugins will be added in future versions (2.40.00+).

---

## 🐞 Known Limitations

- EasyAbroad’s exchange rate and translation APIs rely on external free services – occasional rate limits or downtime may occur.
- Plugin system is currently a placeholder; no actual plugins are available yet.
- `about:blank` may not be recorded in history for some edge cases (normal browsing unaffected).

## 2.40.00

### 🚀 New Features

#### 1. New Internal Domain: `surfer:maps`
- Integrated **online map** using OpenStreetMap.
- Fully interactive map with drag, zoom, and pan support.
- Perfect for location lookup and route planning directly inside Surfer2.

#### 2. New Internal Domain: `surfer:weather`
- Real‑time weather lookup for any city worldwide.
- Powered by **wttr.in** – enter city name (e.g., Beijing, London, New York) to get current temperature and conditions.
- Clean card‑style display that adapts to light/dark mode.

#### 3. New Internal Domain: `surfer:pages`
- **One‑stop dashboard** for all Surfer2 internal domains.
- Displays a grid of cards for every available `surfer:*` domain.
- Click any card to instantly navigate to that internal page.
- Includes: settings, note, chess, easyabroad, maps, weather, chajian.

#### 4. Light/Dark Mode Toggle Restored
- Re‑added **one‑click light/dark mode switch** in `surfer:settings`.
- Works independently from background images and acrylic effect.
- Settings are saved to `localStorage` and persist across sessions.
- All internal pages (including EasyAbroad, maps, weather, pages) adapt correctly to the selected mode.

#### 5. Version Information as Dedicated Setting Item
- Moved version display from tiny bottom text to **a standalone settings group** in `surfer:settings`.
- Clearly shows:
  - Current Surfer2 version (`2.40.00`)
  - List of all available internal domains

#### 6. EasyAbroad Style Adaptation
- Fixed color contrast issues in EasyAbroad page:
  - Text and background colors now properly adapt to **light/dark mode**.
  - Cards, borders, and text contrast are consistent with Surfer2’s global theme.
  - No more hard‑to‑read text regardless of background settings.

#### 7. Plugin: Infrared Transmitter (in `surfer:chajian`)
- Added **Infrared Transmitter plugin** to the plugin center.
- When hardware supports infrared (ConsumerIr API on Android), the plugin attempts to send an IR signal.
- Displays appropriate feedback:
  - ✅ “IR test sent” if hardware supports it
  - ⚠️ “Device does not support IR” if not available
- Future plugins (ad filter, script extensions, theme store) will be added here.

---

### 🛠️ Technical Improvements

- **Theme consistency** – All internal pages now respect light/dark mode and custom styles.
- **Map integration** uses OpenStreetMap embed – no API key required.
- **Weather API** uses free `wttr.in` service – no registration needed.
- **IR plugin** checks for `navigator` capabilities and reports hardware support status.
- **Page navigation grid** is fully responsive – works on desktop and mobile.

---

## 🧠 How to Use New Features

| Feature | Action |
|---------|--------|
| Open online map | Type `surfer:maps` in address bar |
| Check weather | Type `surfer:weather` → enter city name → click “查询天气” |
| View all internal domains | Type `surfer:pages` → click any card |
| Switch light/dark mode | Go to `surfer:settings` → check/uncheck “浅色模式” |
| Check version info | Go to `surfer:settings` → scroll to “版本信息” section |
| Test IR transmitter | Go to `surfer:chajian` → click “测试发射红外线” |

---

## 📦 Upgrade Notes

- All previous settings (whitelist, blacklist, auto‑reload, custom styles, acrylic mode, light mode) are **fully compatible** – no data loss.
- EasyAbroad now inherits Surfer2’s theme – no separate style adjustments needed.
- Maps and weather work offline after initial load (cached resources).
- IR transmitter requires **actual hardware** – most desktop PCs will not support it; Android devices with IR blasters (Xiaomi, Huawei, Samsung) may support it.

---

## 🐞 Known Limitations

- Weather API may be rate‑limited under heavy use (free service).
- Maps require internet connection to load tiles.
- IR transmitter plugin depends on system hardware – most devices will show “not supported”. This is expected.
- `surfer:pages` does not automatically refresh if a new internal domain is added in future updates (static list for now).

## 2.50.00

### 🐞 Bug Fixes

#### 1. Fixed `surfer:weather` HTML Code Leak
- **Issue:** Weather page displayed raw HTML tags (e.g., `<!DOCTYPE html>`) instead of clean weather data.
- **Cause:** The wttr.in API occasionally returns HTML-formatted content when the response is not pure text.
- **Fix:** Added response sanitization – all `<` and `>` characters are now stripped from the weather output. Only plain text temperature and conditions are displayed.

#### 2. Fixed Acrylic Effect Scope
- **Issue:** Acrylic (frosted glass) effect previously applied to the entire page, including the background image layer, causing the background to become blurry.
- **Cause:** The acrylic blur was applied to the whole body overlay.
- **Fix:** Acrylic effect now ONLY applies to the `.surfer-container` (the browser window area). The background image remains completely sharp and unaffected by blur. The acrylic layer sits between the background and the container.

#### 3. Fixed EasyAbroad Text Color in Dark Mode
- **Issue:** After previous updates, EasyAbroad page titles and text turned black on dark background, making them completely unreadable.
- **Cause:** EasyAbroad components did not inherit Surfer2’s global text color styles.
- **Fix:** Added explicit `!important` color rules for `.easyabroad-container` and all its child elements. Text now displays properly as `#e2e8f0` in dark mode and `#1e293b` in light mode.

---

### ✨ New Features

#### 1. Maps and Weather Integrated into Plugin Center
- `surfer:maps` and `surfer:weather` are no longer standalone internal domains.
- They are now **tabs inside `surfer:chajian`** (Plugin Center).
- For backward compatibility, typing `surfer:maps` or `surfer:weather` automatically redirects to `surfer:chajian` with a status message.
- Plugin center now features three tabs:
  - 🗺️ **Online Map** (OpenStreetMap embed)
  - 🌤️ **Weather Forecast** (wttr.in powered)
  - 📡 **Infrared Transmitter** (hardware-dependent)

#### 2. Plugin Center Tab Interface
- Clean tab switching UI inside `surfer:chajian`.
- Each plugin has its own dedicated pane.
- Future plugins can be easily added as additional tabs.

---

### 🛠️ Technical Improvements

- **Weather API sanitization** – Removes HTML tags from wttr.in responses, preventing broken layout.
- **Acrylic layer separation** – Blur effect isolated to browser container, preserving background image clarity.
- **EasyAbroad color inheritance** – Forced CSS rules ensure text readability regardless of system theme.
- **Redirect handling** – Old internal domains (`maps`, `weather`) now gracefully redirect to plugin center with user feedback.

---

## 🧠 How to Use

| Feature | Action |
|---------|--------|
| Open maps | Type `surfer:chajian` → click "🗺️ 在线地图" tab |
| Check weather | Type `surfer:chajian` → click "🌤️ 天气预报" tab → enter city name |
| Old shortcuts | `surfer:maps` or `surfer:weather` redirect to plugin center automatically |
| Test IR transmitter | Go to `surfer:chajian` → "📡 红外线发射" tab → click test button |

---

## 📦 Upgrade Notes

- `surfer:maps` and `surfer:weather` still work as shortcuts (redirect). Users who bookmarked them will not experience broken links.
- Acrylic effect now behaves as intended – background images remain sharp.
- EasyAbroad is fully readable in both light and dark modes.

---

## 🐞 Known Limitations

- Weather API may still return odd characters for some cities – sanitization handles most cases.
- IR transmitter requires actual hardware support (Android with ConsumerIr). Most desktop PCs will show "not supported" – this is expected.

## 3.00.00

### 🚀 New Features

#### 1. New Internal Domain: `surfer:embassy`
- Direct shortcut to **ChineseEmbassyV5** (the China embassy information website).
- Opens the page inside Surfer2’s iframe for seamless integration.
- Access by typing `surfer:embassy` in the address bar.

#### 2. `surfer:note` – Markdown & LaTeX Support
- Full **Markdown** rendering using `marked.js`.
- **LaTeX math formulas** rendered with `KaTeX` (both inline `$...$` and block `$$...$$`).
- Split view: edit Markdown on the left, preview rendered HTML on the right.
- Features:
  - 💾 **Save** – stores note content to `localStorage` automatically.
  - 📄 **Export HTML** – downloads the rendered note as a standalone HTML file.
- Perfect for technical notes, documentation, or math-heavy writing.

#### 3. `surfer:translate` – Dedicated Translation Page
- Extended language support: **14 languages** including:
  - Chinese, English, Japanese, Korean, French, German, Spanish, Russian, Italian, Portuguese, Arabic, and more.
- Clean two-column layout with source/target language selection.
- Powered by MyMemory translation API (free tier).
- Separated from EasyAbroad for focused translation tasks.

#### 4. `surfer:count` – All-in-One Calculator
Supports **four modes** with automatic detection:

| Mode | Example | Description |
|------|---------|-------------|
| **Math Expression** | `2+3*4`, `sqrt(16)`, `2^10` | Standard arithmetic and math functions using JavaScript eval |
| **Currency Exchange** | `100 USD to EUR` | Real-time汇率 conversion via exchangerate-api |
| **Unit Conversion** | `10 km to mile`, `5 kg to lb` | Supports km, mile, m, cm, mm, kg, g, lb |
| **Function Plotter** | `plot sin(x)`, `plot x^2` | Graphs mathematical functions using function-plot.js |

**Audio Feedback** – Click the 🔊 button to have the result read aloud using Web Speech API.

---

### ✨ Enhancements

#### EasyAbroad Translation Language Range Expanded
- Added **8 more languages** to EasyAbroad’s translation module:
  - Korean (한국어), French, German, Spanish, Russian, Italian, Portuguese, Arabic.
- Now supports 12 languages total.

---

### 🔧 Technical Improvements

- **Markdown rendering** – sanitized HTML output, safe for display.
- **LaTeX rendering** – graceful error handling for invalid formulas.
- **Function plotting** – uses `function-plot` library, supports any JavaScript math expression.
- **Speech synthesis** – built‑in browser support, no external API required.
- **Unit conversion** – basic but practical for everyday use (distance, mass).

---

## 🧠 How to Use New Features

| Feature | Action |
|---------|--------|
| Open embassy info | Type `surfer:embassy` |
| Write notes with math | Type `surfer:note` → write Markdown + `$$E=mc^2$$` |
| Translate text | Type `surfer:translate` → select languages → enter text |
| Calculate anything | Type `surfer:count` → enter expression, currency, unit, or `plot sin(x)` |
| Hear result | Click 🔊 button after calculation |

---

## 📦 Upgrade Notes

- All previous settings and internal domains are **fully compatible**.
- `surfer:note` replaces the old simple textarea with a full Markdown editor (old notes are automatically migrated from `localStorage`).
- `surfer:translate` is separate from `surfer:easyabroad` – both remain available.
- The calculator’s `plot` function requires an internet connection to load the plotting library.

---

## 🐞 Known Limitations

- **Math eval** uses `eval()` – only trusted expressions should be evaluated. This is safe inside the local environment.
- **Plotting** works only for single-variable functions (`y = f(x)`).
- **Unit conversion** covers only basic units (distance, mass). More units can be added in future updates.
- **Currency rates** depend on exchangerate-api (free tier – may have rate limits).
- **Speech synthesis** requires user interaction (browser autoplay policy) – the button click triggers it.

## 3.10.00

### 🐞 Critical Fixes

#### 1. `surfer:embassy` Full‑screen Display Issue
- **Problem:** The embassy information page (ChineseEmbassyV5) was cut off — only the first few lines were visible.
- **Root cause:** The iframe did not inherit the correct height from its flex parent container.
- **Solution:** The internal page now uses `display: flex; flex-direction: column; height: 100%` and the iframe is set to `flex: 1; height: 100%`.  
  **Result:** The embassy page now fills the entire viewing area perfectly.

#### 2. `surfer:count` – From Command Line to Full Graphical Interface
- **Before:** Single input field + one line of text result → felt like a terminal / CMD.
- **After:** A **tab‑based graphical calculator** with four dedicated panels:

| Tab | Function | Interactive Elements |
|-----|----------|----------------------|
| 🧮 Math | Expression evaluation | Input field, calculate button, speech output |
| 💱 Currency | Live exchange rates | Currency selectors, amount input, API call |
| 📏 Unit conversion | Length & mass conversion | Dropdowns + quick‑action button grid |
| 📈 Function plot | Mathematical graph drawing | Expression input, live plot, voice description |

- **Added features:**
  - Quick‑convert buttons: `km ↔ mile`, `kg ↔ lb`
  - **Speech synthesis** (🔊 button) – reads the result aloud
  - Plotting uses `function-plot.js` – supports `sin(x)`, `x^2`, `sqrt(x)`, `x*sin(x)`, etc.

---

### ✨ Improvement

#### 3. Smooth Theme Transition (No “Flashbang”)
- **Problem:** Instant light/dark mode switching caused a sudden brightness change (eye strain / “flashbang” effect).
- **Solution:** Added CSS `transition` rules to all themed elements:
  - `body`, `.surfer-container`, `.internal-page`, `.settings-group`, `.calc-tab`, `.page-card`, etc.
  - Transition duration: `0.25s – 0.35s` with easing.
- **Result:** Theme changes are now smooth, gradual, and comfortable for the eyes.

---

### 🛠️ Technical Notes

- **Embassy iframe** – no external dependencies, works entirely inside Surfer2.
- **Calculator** – all four modes are fully functional without page reload.
- **Theme transition** – affects background, text, cards, borders, and backdrop‑filter layers.
- **Speech synthesis** – requires user interaction (button click) due to browser autoplay policies.

---

## 🧠 How to Use

| Feature | Action |
|---------|--------|
| Open embassy page | Type `surfer:embassy` → full‑screen iframe |
| Use calculator | Type `surfer:count` → switch tabs |
| Plot a function | Type `surfer:count` → go to **📈 函数绘图** tab → enter `sin(x)` → click “绘制图像” |
| Listen to result | Click the **🔊 朗读** button after any calculation |
| Smooth theme switch | Go to `surfer:settings` → toggle light/dark mode → watch the gentle transition |

---

## 📦 Upgrade Notes

- All previous internal domains (`settings`, `note`, `chess`, `easyabroad`, `translate`, `pages`, `chajian`) remain fully functional.
- The embassy page now displays correctly on all screen sizes.
- The calculator no longer feels like a terminal – it is a proper graphical tool.

---

## 🐞 Known Limitations

- **Exchange rate API** is free‑tier – occasional rate limits may occur.
- **Function plotting** requires an internet connection (library loads from CDN).
- **Speech synthesis** voice quality depends on the user’s operating system and browser.

## 3.20.00

### 🚀 New Features

#### 1. Calculator Rebuilt as Pure GUI (Button‑Based Interface)
- **Complete replacement** of the old command‑line style input with a **full graphical calculator**.
- **Buttons include:**
  - Digits `0–9` and decimal point `.`
  - Basic operators: `+`, `-`, `×`, `÷`
  - Clear (`AC`) and backspace (`⌫`)
  - Scientific functions: `√`, `x²`, `sin`, `cos`, `tan`, `π`
  - Equals (`=`) to evaluate expression
  - 🔊 **Speech output** – reads the result aloud
  - 📈 **Plot function** – draws the graph of the current expression
- All buttons have visual feedback (scale‑down on press).

#### 2. Expression Engine
- Supports:
  - Basic arithmetic (`2+3*4`)
  - Parentheses (`(2+3)*4`)
  - Scientific functions: `sin`, `cos`, `tan` (input in radians)
  - Constants: `π` (pi)
  - Power notation: `x²` (converted to `^2` internally)
  - Square root: `√(expression)`
- Invalid expressions show clear error messages without crashing.

---

### 🐞 Bug Fixes

#### 3. Fixed `surfer:pages` Text Visibility in Light Mode
- **Problem:** In light mode, the text on navigation cards (`surfer:pages`) was almost invisible (same color as background).
- **Root cause:** The `.page-card` color was not explicitly set for light mode; it inherited a dark color.
- **Fix:** Added explicit light‑mode styles:
  ```css
  body.light-mode .page-card {
      background: #ffffff;
      border: 1px solid #e2e8f0;
      color: #1e293b;
  }
  ```

Now cards are clearly readable in both themes.

### 🛠️ Technical Improvements

- Calculator GUI is built with pure HTML/CSS/JS – no external dependencies for the button layout.
- Expression evaluation uses a controlled `eval` context, safe for local use.
- Plotting functionality relies on the CDN‑hosted `function-plot` library.
- Speech synthesis uses the Web Speech API and requires a user click (browser autoplay policy).

### 🧠 How to Use New Features

| Feature | Action |
|---------|--------|
| Open graphical calculator | Type `surfer:count` in the address bar |
| Input numbers / operators | Click the on‑screen buttons |
| Clear current expression | Click `AC` |
| Delete last character | Click `⌫` |
| Calculate result | Click `=` |
| Hear the result aloud | Click the 🔊 button |
| Plot the current expression | Click the 📈 button |
| Open page navigation | Type `surfer:pages` – cards are now clearly readable |
| Toggle light/dark mode | Go to `surfer:settings` – checkbox state is now correct |

### 📦 Upgrade Notes

- All existing internal domains (`settings`, `note`, `chess`, `easyabroad`, `embassy`, `translate`, `pages`, `chajian`) continue to work without changes.
- The old text‑based calculator is completely removed. No migration is needed.
- Existing `localStorage` settings (theme, acrylic, font, background) are untouched.

### 🐞 Known Limitations

- Plotting requires an internet connection (the `function-plot` library is loaded from a CDN).
- Scientific functions (`sin`, `cos`, `tan`) expect **radians**, not degrees. Use `sin(pi/2)` to calculate `sin(90°)`.
- Speech synthesis quality and voice depend on the user’s operating system and browser.
- Plotting may fail for very complex expressions or functions with discontinuities (for example, `tan(x)` near its asymptotes).


## 3.21.00

### 🐞 Bug Fixes

#### 1. `surfer:chess` – Chess Board Background Now Follows Theme
- **Problem:** The chess board cells kept a dark background even when light mode was enabled.
- **Root cause:** The `.chess-cell` style was not overridden for `body.light-mode`.
- **Fix:** Added explicit light‑mode styles for `.chess-cell`:
  - Dark mode: `background: #2d3748`
  - Light mode: `background: #e2e8f0`
- **Result:** Chess board now correctly adapts to both themes without visual glitches.

#### 2. `surfer:translate` – Input Fields Now Follow Theme
- **Problem:** The source/target textareas and result boxes remained dark in light mode.
- **Root cause:** Missing `body.light-mode` overrides for `.translate-textarea` and `.translate-result`.
- **Fix:** Added light‑mode styles:
  - `.translate-textarea` in light mode: `background: #ffffff; border-color: #cbd5e1; color: #1e293b`
  - `.translate-result` in light mode: `background: #f1f5f9`
- **Result:** All translation input/output areas now match the selected theme.

#### 3. `surfer:easyabroad` – Layout Completely Refactored
- **Problem:** The EasyAbroad page had broken, misaligned cards and inconsistent spacing.
- **Root cause:** The layout used a simple flex-wrap without proper grid structure.
- **Fix:** Replaced the old layout with a **CSS Grid** system:
  ```
  .easyabroad-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 20px;
  }
  ```
- **Additional improvements:**
  - Unified card padding and borders
  - Fixed header alignment with consistent margins
  - Added proper border‑bottom separators for info rows
  - Ensured all cards (location, currency, translation) have the same height consistency
  - Navigation links now use a clean wrap‑grid inside the last card
- **Result:** EasyAbroad is now clean, responsive, and visually aligned on both desktop and mobile.

---

### 🧠 How to Test the Fixes

| Fix | Verification |
|-----|--------------|
| Chess board theme | Open `surfer:chess` → toggle light/dark mode → cells should change color |
| Translate background | Open `surfer:translate` → toggle light/dark mode → textareas and result box should switch between dark/light backgrounds |
| EasyAbroad layout | Open `surfer:easyabroad` → cards should form a clean grid (no overlapping, no misalignment) |

---

### 📦 Upgrade Notes

- All previous settings (theme, acrylic, background, etc.) remain unchanged.
- The chess board and translate page now fully respect the active color scheme without breaking existing gameplay or translation functionality.
- EasyAbroad’s layout change does not affect any backend APIs – it only reorganizes the visual presentation.

---

### 🐞 Known Limitations

- The chess board cells do not animate during theme switching (the change is instant, but this is acceptable for a board game).
- EasyAbroad’s grid layout may stack into a single column on very narrow screens (< 360px) – this is intentional for readability.

## 4.00.00

### 🐞 Bug Fixes

#### 1. `surfer:chajian` – Restored Tab Mode, Removed Large Empty Space
- **Problem:** The infrared plugin page had a large blank area above the content, seriously affecting the visual experience.
- **Root cause:** The previous layout used a single‑pane design without proper tab structure, leaving unused space.
- **Fix:** Restored the tab‑based layout:
  - Two tabs: 🗺️ 在线地图 and 📡 红外线发射
  - Each tab contains only its own compact content
  - No extra padding or empty containers
- **Result:** The plugin center is now clean, compact, and visually balanced.

#### 2. `surfer:easyabroad` – Light Mode Text Visibility Fixed
- **Problem:** In light mode, the EasyAbroad title, subtitle, and section headings became completely invisible (black text on dark‑looking background).
- **Root cause:** The text colors were not explicitly defined for `body.light-mode`; they inherited dark mode colors.
- **Fix:** Added light‑mode specific styles:
  - `.easyabroad-header h1` uses a light‑mode gradient (`#1f6392` to `#6b21a5`)
  - `.easyabroad-header p` uses `#4a627a` for readability
  - All card text now uses `color: inherit` to properly follow the theme
- **Result:** All text in EasyAbroad is now fully readable in both light and dark modes.

---

### 🚀 New Features

#### 3. New Homepage: `surfer:homepage`
- **Purpose:** Provide a clean starting point for browsing and accessing Surfer2 resources.
- **Features:**
  - **Search box** with engine selector:
    - Google
    - Bing
    - Baidu
    - DuckDuckGo
    - GitHub repository search
  - **GitHub repository link** – direct access to the Surfer2 source code
  - Centered layout with gradient title and subtitle
- **Default start page:** Surfer2 now opens `surfer:homepage` by default instead of `about:blank`.

---

### 🧠 How to Use

| Feature | Action |
|---------|--------|
| Open homepage | Type `surfer:homepage` in the address bar (default on launch) |
| Search the web | Enter query → select engine → click search button |
| Search GitHub | Select "GitHub 仓库搜索" → enter repository name or keyword |
| Visit Surfer2 GitHub | Click the GitHub link at the bottom of the homepage |
| Use plugin center | Type `surfer:chajian` → tabs now work correctly without extra blank space |
| Check EasyAbroad in light mode | Switch to light mode in settings → all text is now clearly visible |

---

### 📦 Upgrade Notes

- **Default start page changed** – Surfer2 now launches to `surfer:homepage` instead of `about:blank`. If you prefer the old behavior, you can manually navigate to `about:blank`.
- All previous settings (theme, acrylic, font, background) remain unchanged.
- The plugin center and EasyAbroad fixes do not affect any backend functionality.

---

### 🐞 Known Limitations

- The homepage search engine selector does not save preferences across sessions (defaults to Google each time).
- EasyAbroad’s light mode gradient may appear slightly different depending on the user’s system theme, but remains readable.
- The plugin center tabs do not remember the last active tab after page reload (always defaults to "在线地图").

## 4.10.00

### 🐞 Bug Fixes

#### 1. `surfer:easyabroad` – Light Mode Background Fixed
- **Problem:** In light mode, the EasyAbroad page background turned completely black, making the entire card content unreadable.
- **Root cause:** The `.easyabroad-card` background color was not explicitly overridden for `body.light-mode`.
- **Fix:** Added proper light‑mode styles:
  - `.easyabroad-card` in light mode: `background: #ffffff; border: 1px solid #e2e8f0`
  - All text colors now inherit correctly from parent containers
- **Result:** EasyAbroad is now fully readable in both light and dark modes.

#### 2. Translation Page – Invalid AUTO Source Language
- **Problem:** The error message `'AUTO' IS AN INVALID SOURCE LANGUAGE` appeared when using auto‑detection.
- **Root cause:** The MyMemory API expects `auto` (lowercase) as the source language code, but the langpair format was incorrectly constructed.
- **Fix:** Properly handle the `auto` source language:
  - When source is `auto`, use `auto|target` format
  - When source is `zh_tw`, convert to `zh-TW` for API
  - Added fallback handling for empty or failed translations
- **Result:** Auto‑detection now works correctly without API errors.

---

### 🚀 New Features

#### 3. Simplified ↔ Traditional Chinese Translation
- Added **built‑in conversion** between Simplified Chinese (`zh`) and Traditional Chinese (`zh_tw`).
- No external API call required for Chinese‑only conversions – instant and offline.
- Conversion rules include common character mappings:
  - `们→們`, `会→會`, `个→個`, `后→後`, `关→關`
  - `开→開`, `进→進`, `过→過`, `对→對`, `时→時`
  - `说→說`, `电→電`, `为→為`, `发→發`, `爱→愛`
  - `体→體`, `学→學`, `国→國`, `门→門`, `问→問`, `龙→龍`
- Added **🔄 Swap Languages** button – instantly exchanges source and target languages.

#### 4. Restored Currency Conversion in `surfer:count`
- Added a dedicated **currency exchange module** at the bottom of the calculator page.
- Supported currencies: `CNY`, `USD`, `EUR`, `JPY`, `GBP`.
- Real‑time exchange rates via `exchangerate-api.com`.
- Clear input field, dropdown selectors, and result display.

---

### 🧠 How to Use

| Feature | Action |
|---------|--------|
| Simplified ↔ Traditional translation | Open `surfer:translate` → select `中文(简体)` and `中文(繁体)` → enter text → click translate |
| Swap translation languages | Click the **🔄 交换语言** button |
| Use auto language detection | Select `自动检测` as source language → API will automatically identify the source language |
| Currency conversion | Open `surfer:count` → scroll to the **汇率换算** section → enter amount → select currencies → click 换算 |

---

### 📦 Upgrade Notes

- All previous settings (theme, acrylic, font, background) remain unchanged.
- The translation page now supports 14 languages including Simplified and Traditional Chinese.
- The currency conversion module is separate from the main calculator – both can be used independently.
- The `auto` source language now works correctly with the MyMemory API.

---

### 🐞 Known Limitations

- The Simplified‑Traditional conversion uses a rule‑based character mapping (not semantic) – rare characters may not convert perfectly.
- Exchange rates are fetched from a free API – occasional rate limits may occur (usually resolves after a few seconds).
- The translation API may return the same text as input when the target language is very similar to the source language (e.g., English to English).
