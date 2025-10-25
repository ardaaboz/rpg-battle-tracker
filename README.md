# Velutan Battle Tracker

A modern, intuitive web-based battle tracker designed for tabletop RPG sessions. Built specifically for the "Velutan" campaign's low-HP combat system.

![Velutan Battle Tracker](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## 🎮 Features

### Character Management
- **Drag-and-drop tokens** on a gridded or free-form battlefield
- **Three character types**:
  - **Allies** (Green): Full HP tracking with visual HP rings
  - **Enemies** (Red): Damage log system for tracking incoming hits
  - **Neutrals** (Yellow): Basic positioning and status effects
- **Resizable tokens** by dragging corner handles
- **Custom character portraits** or auto-generated placeholders
- **Status effects** system (Stunned, Poisoned, Blessed, etc.)

### Battle Control
- **Initiative order** management with visual turn tracking
- **Zoom and pan** the battlefield with mouse wheel and click-drag
- **Grid overlay** for tactical positioning (50x50px squares)
- **Undo system** to revert accidental changes
- **Save/Load** complete battle states as JSON files

### Visual Customization
- **Background images**: Choose from preset environments or upload custom images
  - Desert, Forest, Grasslands, Ice, Snow, or Custom
- **Adjustable background opacity** for better token visibility
- **Hideable sidebar** for maximum battlefield space
- **Floating notes window** for session tracking

### Low-HP System Optimized
- Designed for combat systems where characters typically have 2 HP
- Supports fractional damage (0.25, 0.5, 1.0)
- Quick HP adjustment buttons for fast combat resolution

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari)
- No installation required!

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/ardaaboz/rpg-battle-tracker.git
   cd rpg-battle-tracker
   ```

2. **Open the tracker**
   - Simply open `index.html` in your web browser
   - Or use a local server for best results:
     ```bash
     # Using Python
     python -m http.server 8000

     # Using Node.js
     npx serve

     # Using VS Code Live Server extension
     Right-click index.html → "Open with Live Server"
     ```

3. **Start your battle!**
   - Preset characters (Ugg'Nug, Raizo, Vissra, Zaheed, William) load automatically
   - Add enemies and neutrals as needed
   - Track initiative, HP, damage, and status effects

## 📁 Project Structure

```
rpg-battle-tracker/
├── index.html              # Main HTML file with React app
├── css/
│   ├── main.css           # Global styles and resets
│   ├── sidebar.css        # Sidebar and form styles
│   ├── battlefield.css    # Battlefield and token styles
│   ├── context-menu.css   # Right-click menu styles
│   └── initiative.css     # Initiative bar and notes styles
├── images/                 # Character portraits
│   ├── uggnug.png
│   ├── raizo.png
│   ├── vissra.png
│   ├── zaheed.png
│   └── william.png
├── README.md              # This file
└── LICENSE                # MIT License
```

## 🎯 Usage Guide

### Adding Characters

1. **Allies** (require HP):
   - Enter name, select "Ally" type
   - Set HP and Max HP (typically 2/2)
   - Optional: Upload character portrait
   - Click "Add Character"

2. **Enemies** (damage tracking):
   - Enter name, select "Enemy" type
   - Optional: Upload portrait
   - Right-click enemy tokens to log damage
   - Hover to see total damage taken

3. **Neutrals** (positioning only):
   - Enter name, select "Neutral" type
   - No HP tracking or damage logging

### Battlefield Controls

| Action | Input |
|--------|-------|
| Move character | Click and drag token |
| Resize character | Drag bottom-right corner handle |
| Pan battlefield | Click and drag empty space |
| Zoom in/out | Mouse wheel scroll |
| Character menu | Right-click token |
| Toggle grid | Click "Show/Hide Grid" button |

### Initiative Management

- Characters are automatically ordered by initiative (highest first)
- Click any character card to mark them as the current turn (glowing highlight)
- Drag cards to manually reorder initiative

### Context Menu (Right-Click)

Available actions depend on character type:
- **All types**: Rename, change image, add status effects, mark as dead, delete
- **Allies only**: Adjust HP with quick buttons or exact values
- **Enemies only**: Log damage and view damage history

### Saving & Loading

1. **Save Battle**:
   - Click "💾 Save Battle" button
   - Downloads a JSON file with all battle data
   - Includes characters, positions, HP, statuses, and notes

2. **Load Battle**:
   - Click "📂 Load Battle" button
   - Select a previously saved JSON file
   - Restores complete battle state

## 🛠️ Technical Details

### Built With
- **React 18** - UI framework
- **Babel Standalone** - JSX transformation
- **Vanilla CSS** - No preprocessors, fully commented
- **Local Storage** - No backend required

### Browser Compatibility
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Edge 90+
- ✅ Safari 14+

### Performance
- Optimized for up to 50 characters on battlefield
- Smooth 60 FPS animations
- Low memory footprint (~50MB typical)

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Commit your changes**
   ```bash
   git commit -m 'Add some amazing feature'
   ```
4. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
5. **Open a Pull Request**

### Code Style Guidelines
- Use clear, descriptive variable names
- Comment complex logic
- Follow existing CSS organization (separate files by component)
- Test with multiple browsers before submitting

## 📝 Changelog

### Version 1.0.0 (2025-01-XX)
- Initial release
- Drag-and-drop character tokens
- HP tracking for allies
- Damage logging for enemies
- Initiative order management
- Save/Load battle states
- Zoom and pan battlefield
- Grid overlay option
- Custom backgrounds
- Status effects system
- Preset character support

## 🐛 Known Issues

- Image files must be in same directory for relative paths to work
- Context menu may extend off screen on very small displays (auto-repositioning helps but not perfect)
- Undo only tracks last 10 actions

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built for the Velutan D&D campaign
- Inspired by Roll20 and Foundry VTT
- Background images from Unsplash
- Character portraits created by the players

## 📧 Contact

**Project Maintainer**: Arda Aboz
- GitHub: [@ardaaboz](https://github.com/ardaaboz)
- Repository: [https://github.com/ardaaboz/rpg-battle-tracker](https://github.com/ardaaboz/rpg-battle-tracker)

## 🌐 Live Demo

Coming soon: [velutanbattlemap.com](https://velutanbattlemap.com)

---

Made with ❤️ for tabletop RPG enthusiasts
