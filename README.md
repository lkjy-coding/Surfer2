# Surfer2
Surfer2 is an upgraded version of Surfer, but it can really go online, search online, and even support watching videos online. Compared to Surfer, Surfer2 has a wider range of territories. So, make the most of Surfer2!

## Important tips

Now I am trying to make the connection by Surfer2 safe,but I'm still npt sure about it.So **I don't suggest you to enter something important on it**.

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

# 2.00.00

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
