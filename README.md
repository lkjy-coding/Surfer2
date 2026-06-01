# Surfer2

Surfer2 is an upgraded version of Surfer, but it can really go online, search online, and even support watching videos online. Compared to Surfer, Surfer2 has a wider range of territories. So, make the most of Surfer2!

## Important tips

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
