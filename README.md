# SF Crosshair
**Advanced Crosshair System for FiveM**
> **by SantaFe Team 🇲🇦**

> **Framework: ESX & QBCore (Auto-detect)**

A professional and highly customizable crosshair system for FiveM with advanced sharing features and modern UI. Create, customize, and share your perfect crosshair with other players.

---

## ✨ Features

### 🎯 **Crosshair Customization**
- **16 Crosshair Styles** - Multiple pre-designed styles to choose from
- **Full Customization** - Size, thickness, color, opacity, gap, outline, and center dot
- **Custom Images** - Load crosshairs from external URLs with predefined options
- **Real-time Preview** - See changes instantly before applying
- **Universal Compatibility** - Works with all weapons (no blacklist restrictions)

### 💾 **Save & Manage**
- **Unlimited Favorites** - Save and manage your favorite crosshairs
- **Edit Names** - Click pencil icon to rename your favorites
- **Unique Codes** - Each favorite gets a visual identifier code
- **Database Persistence** - All settings saved across sessions

### 🤝 **Advanced Sharing System**
- **PIN System** - Each player gets a unique 6-digit PIN for easy sharing
- **Nearby Sharing** - Share with players within configurable distance (default: 10m)
- **PIN Sharing** - Send crosshairs to any online player using their PIN
- **Accept/Reject Modal** - Recipients can preview and choose to accept or reject
- **Auto-save** - Accepted crosshairs automatically saved to favorites
- **Character Names** - Uses in-game character names (ESX/QBCore)

### 🖼️ **Custom Images**
- **Predefined Images** - Server-configured image options in config
- **URL Loading** - Load from any public URL (imgur, discord CDN, etc.)
- **PNG Support** - Transparent PNG images for best results
- **Click to Load** - Easy selection from predefined options

### 🎨 **Modern Interface**
- **6 Tabs** - Styles, Settings, Favorites, Share, Image, About
- **Responsive Design** - Clean, modern UI with smooth animations
- **About Section** - Complete information, links, and branding
- **Protected Elements** - Store and Discord links cannot be modified

---

## 📋 Dependencies

| Resource | Required |
|---|---|
| mysql-async | ✅ Yes |
| ESX or QBCore | ✅ Yes (auto-detected) |

---

## 🚀 Installation

1. Download and extract `SF-Crosshair` to your resources folder
2. Import `crosshair.sql` into your database
3. Add `ensure SF-Crosshair` to your `server.cfg`
4. Configure `config.lua` to your preferences (optional)
5. Restart your server

---

## 📊 Database

Run `crosshair.sql` in your database before starting the resource. This creates:

- `crosshair_configs` - Player crosshair configurations
- `crosshair_favorites` - Saved favorite crosshairs  
- `crosshair_pins` - Unique PINs for sharing system

> Tables are created automatically on first start if they don't exist.

---

## ⚙️ Configuration

```lua
-- Command to open crosshair menu
Config.Command = 'crosshair'

-- Default keybind (players can change in FiveM settings)
Config.OpenKey = 'F5'

-- Show crosshair only when aiming
Config.ShowOnlyWhenAiming = true

-- Disable native GTA crosshair
Config.DisableNativeCrosshair = true

-- Distance for nearby player sharing
Config.ShareDistance = 10.0

-- Predefined custom images (server-configured)
Config.CustomImages = {
    {
        name = "Dot",
        url = "https://example.com/dot.png",
        preview = "Simple dot crosshair"
    },
    {
        name = "Circle", 
        url = "https://example.com/circle.png",
        preview = "Circle crosshair"
    },
    -- Add more images here
}
```

---

## 🎮 Usage

### Opening the Menu
- Use `/crosshair` command or press `F5` (configurable)
- Rebind key in FiveM Settings > Key Bindings

### Interface Tabs

**🎨 Styles** - Choose from 16 crosshair styles

**⚙️ Settings** - Full customization:
- Size (10-60px)
- Thickness (1-10px) 
- Color (preset colors + custom picker)
- Opacity (10-100%)
- Gap (0-20px)
- Outline (on/off)
- Center dot (on/off)

**❤️ Favorites** - Manage saved crosshairs:
- Save current configuration with custom name
- Load favorites instantly
- Edit names (click pencil icon)
- Delete unwanted favorites
- Copy unique codes

**🤝 Share** - Advanced sharing system:
- **Your PIN** - 6-digit code displayed prominently
- **Nearby Players** - Auto-detect players within range
- **Send by PIN** - Enter recipient's PIN to send anywhere
- **Accept/Reject** - Preview incoming crosshairs before accepting
- **Auto-save** - Accepted crosshairs saved to favorites

**🖼️ Image** - Custom crosshair images:
- **Predefined Options** - Server-configured images (click to load)
- **URL Loading** - Load from any public URL
- **PNG Support** - Transparent backgrounds recommended
- **Size Guide** - 64x64 or 128x128px optimal

**ℹ️ About** - Information and links:
- Script features and description
- SantaFe Team information
- Store and Discord links (protected)
- Version information

---

## 🔄 Sharing System

### How to Share Crosshairs

1. **Save to Favorites First** - Only favorites can be shared
2. **Go to Share Tab** - Select which favorite to share
3. **Choose Method**:
   - **Nearby**: Refresh list, select player within 10m
   - **By PIN**: Enter recipient's 6-digit PIN
4. **Send** - Recipient gets notification and preview

### Receiving Crosshairs

1. **Notification** - Chat message when someone sends you a crosshair
2. **Preview Modal** - Opens automatically showing the crosshair
3. **Accept/Reject** - Choose whether to keep it
4. **Auto-save** - Accepted crosshairs saved to your favorites
5. **Notification** - Sender gets confirmation of your choice

### PIN System

- **Unique PIN** - Each player gets a 6-digit PIN on first join
- **Always Visible** - Shown in header and Share tab
- **Copy Function** - Click copy button to share with friends
- **Cross-server** - Works with any online player

---

## 🎨 Customization Tips

### Best Practices
- **Bright Colors** - Use #B0F527, #FF0000, #00FF00 for visibility
- **Optimal Size** - 15-25px works best for most situations
- **Outline** - Enable for better contrast against backgrounds
- **Multiple Favorites** - Save different configs for different weapons/situations

### Custom Images
- **Format** - PNG with transparent background
- **Size** - 64x64 or 128x128 pixels (square format)
- **Hosting** - Use imgur, discord CDN, or other reliable hosts
- **Performance** - Avoid very large images

---

## 🔧 Framework Compatibility

**Auto-detection** - No manual configuration needed:
- **ESX** - Detects `es_extended` export automatically
- **QBCore** - Detects `qb-core` export automatically  
- **Character Names** - Uses framework character names in sharing
- **Fallback** - Works without framework (uses Steam names)

---

## 📝 Commands & Controls

| Command | Description |
|---|---|
| `/crosshair` | Open/close crosshair menu |
| `ESC` | Close menu |
| `F5` | Default keybind (configurable) |

---

## 🐛 Troubleshooting

**Crosshair not showing:**
- Ensure crosshair is enabled in Settings tab
- Check if `Config.ShowOnlyWhenAiming` requires aiming
- Verify `Config.DisableNativeCrosshair` setting

**PIN not visible:**
- Open crosshair menu - PIN shows in header
- Check Share tab for PIN display
- PIN generates automatically on first join

**Sharing not working:**
- Ensure crosshair is saved in Favorites first
- Check both players are online
- Verify PIN is correct (6 digits)
- For nearby: ensure within configured distance

**Custom images not loading:**
- Verify URL is publicly accessible
- Use PNG format with transparent background
- Check image size (recommended: 64x64 to 128x128px)
- Ensure stable internet connection

**Database issues:**
- Confirm mysql-async is running
- Import `crosshair.sql` before first start
- Check server console for MySQL errors
- Verify database connection in server.cfg

---

## � Version System

**Current Version:** 1.0.0

Features automatic update checking:
- Checks GitHub on server start
- Displays changelog for new versions
- Configurable update notifications
- Version comparison and warnings

---

## 🛡️ Support & Links

**SantaFe Team** 🇲🇦
- **Discord:** https://discord.gg/gsUpFV3KgR
- **Store:** https://santafedev.store/
- **Docs:** https://docs.santafedev.store/
- **Made with ❤️ in Morocco**

---

## 📄 License & Protection

This resource is protected and licensed by SantaFe Team.
- Redistribution prohibited
- Resale prohibited  
- Modification of protected elements prohibited
- Commercial use requires license

---

**SF Crosshair - Professional FiveM Crosshair System**
*Developed by SantaFe Team 🇲🇦*
