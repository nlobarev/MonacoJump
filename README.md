# MonacoJump
Monaco Jump is a single-screen endless jumper Progressive Web App (PWA) featuring fully configurable backgrounds, player characters, and enemies via JSON files. Customize visuals, speeds, positions, and behaviors without code changes—optimized for mobile touch controls and offline play.

[PLAY NOW](https://nlobarev.github.io/MonacoJump/)
___

## ✨ Key Features
- ✅ Jump on enemies’ heads to defeat them
- ✅ Touch Screen and Keyboard support
- ✅ Installable PWA - Add to home screen like a native app
- ✅ 100% Offline Playable - Works without internet after first load
- ✅ JSON Customization - Backgrounds, characters, enemies, settings

## 🎨 Upload Sprites
Create your personalized MonacoJump experience! Upload right-facing sprites only - JavaScript automatically flips for left movement. No duplicate artwork needed.

**📁 Organized Assets Structure**
```
assets/
│
├─ settings/
│   ├── manifest.json
│   ├── custom-icon.png
│   └── custom-background.png    ← Game background image here
│
├── character/                   ← Your hero (Smilla!)
│   ├── default-standing.png
│   ├── walk-right1.png          ← Walk cycle (2-4 frames)
│   ├── walk-right2.png
│   ├── walk-right3.png          ← Optional: more = smoother
│   ├── jump-right1.png          ← Jump cycle (2-3 frames)
│   └── jump-right2.png
│
└── enemies/
    ├── kebab/                   ← Folder = enemy ID in JSON
    │   ├── walk-right1.png
    │   └── walk-right2.png
    ├── pizza/
    │   └── walk-right1.png
    └── pigeon/
        └── walk-right1.png
```
**✨ 5-Minute Upload Workflow**
1. Create right-facing sprites
2. Upload to correct folders - drag & drop!
3. Link in JSON configs - copy/paste paths
4. Refresh browser → Instant preview with auto-flip!

## 🛠️ JSON Configuration
#### Character ( config/character.json )
```
{
  "player": {
    "name": "Smilla",
    "sprites": {
      "idle": ["assets/character/smilla-idle.png"],
      "run":  ["assets/character/smilla-run1.png", "assets/smilla-run2.png"],
      "jump": ["assets/character/smilla-jump.png"]
    },
    "speed": 5,
    "jumpHeight": 14
  }
}
```
#### Enemies ( config/enemies.json )
```
{
  "enemies": [
    {
      "name": "Kebab Monster",
      "height" : 120,
      "width"  : 80, 
      "sprites": ["assets/enemies/kebab-monster/animation_frame_1.png", "assets/enemies/kebab-monster/animation_frame_2.png"]
      "speed": 1.5,
      "yPosition": 0
    },
  ]
}
```
#### Game settings ( config/settings.json )
```
{
  "settings" : {
    "name": "MonacoJump",
    "icon" : "assets/settings/custom-icon.png",
    "background" : "assets/settings/custom-background.png",
  }
}
```
## 🚀 Quick Setup
Serve MonacoJump anywhere! Static files work with any HTTPS server. Choose your method:

**GitHub Pages (Recommended - Free PWA!)**
✅ Auto-HTTPS, PWA-ready, free forever
```
1. git init && git add . && git commit -m "v1"
2. git remote add origin https://github.com/YOUR_USERNAME/monaco-jump.git
3. git push -u origin main
4. Repo Settings → Pages → Source: "main" branch
5. Live: https://YOUR_USERNAME.github.io/monaco-jump/
```

## 🎮 Install & Play Offline
Transform MonacoJump into a native app! One-time setup → forever offline play on phone/desktop

**📱 Mobile (Android/iPhone)**
```
1. Open game URL in Chrome/Safari
2. Tap these icons:
    Android/Chrome: Share → "Add to Home Screen" → "Add"
    iPhone/Safari: Share → scroll → "Add to Home Screen"
3. 🎉 "MonacoJump" icon on home screen!
4. Tap icon → Launches fullscreen, offline!
```

**💻 Desktop (Windows/macOS/Chromebook)**
```
Chrome/Edge:
1. Open game → Click ⋮ (top-right)
2. "Install MonacoJump" or "🧩 Install app"
3. Icon in Apps/Start Menu
4. Launch → Offline native window!
```


