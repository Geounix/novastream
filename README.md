# NovaStream Theme for Jellyfin

A modern glassmorphism-inspired dark theme for Jellyfin 10.11.10+ with cyan accents and premium streaming aesthetics.

## Features

- **Glassmorphism Design** - Frosted glass effects with backdrop blur
- **Cyan Accent Colors** - Modern streaming platform look
- **Smooth Animations** - Subtle hover effects and transitions
- **Responsive** - Works on desktop, mobile, and TV clients
- **Customizable** - Easy to modify via CSS variables
- **Minimal** - Clean, content-focused interface

## Compatibility

- Jellyfin 10.11.x and above
- All web browsers (Chrome, Firefox, Safari, Edge)
- Jellyfin mobile apps (iOS/Android)
- Jellyfin media player

## Installation

### Method 1: Manual (Recommended)

1. Copy the `novastream` folder to your Jellyfin server's web root:
   - **Linux:** `/usr/share/jellyfin/web/` or `/var/lib/jellyfin/config/web/`
   - **Windows:** `C:\Program Files\Jellyfin\Server\jellyfin-web\`
   - **Docker:** Mount as a volume or copy to `/jellyfin/jellyfin-web/`

2. Open Jellyfin Dashboard > Branding > Custom CSS

3. Add the following line:
   ```css
   @import url('/novastream/theme.css');
   ```

4. Click **Save** - No restart required

### Method 2: CDN (If Published)

1. Open Jellyfin Dashboard > Branding > Custom CSS

2. Add the following line:
   ```css
   @import url('https://cdn.jsdelivr.net/gh/username/novastream@latest/theme.css');
   ```

3. Click **Save**

### Method 3: Skin Manager Plugin

1. Install the Skin Manager plugin from the Jellyfin plugin catalog
2. Add the NovaStream repository URL
3. Select and apply NovaStream from the plugin interface

## Customization

### Change Accent Color

Edit `variables.css` or add to Dashboard Custom CSS:

```css
:root {
  --ns-accent: #ff6b6b;        /* Red */
  --ns-accent: #51cf66;        /* Green */
  --ns-accent: #ffd43b;        /* Yellow */
  --ns-accent: #cc5de8;        /* Purple */
  --ns-accent: #ff922b;        /* Orange */
}
```

### Adjust Glass Effect

```css
:root {
  --ns-blur: 10px;             /* Lighter blur */
  --ns-blur-heavy: 30px;       /* Heavier blur */
  --ns-glass-bg: rgba(255, 255, 255, 0.08);  /* More opaque glass */
}
```

### Modify Border Radius

```css
:root {
  --ns-radius-sm: 4px;         /* Sharper corners */
  --ns-radius-md: 8px;
  --ns-radius-lg: 12px;
  --ns-radius-xl: 20px;
}
```

## File Structure

```
novastream/
├── theme.css          # Main file (import this one)
├── variables.css      # Customizable CSS variables
├── components.css     # UI component styles
├── animations.css     # Animations and transitions
└── README.md          # This file
```

## Troubleshooting

### Theme not applying
- Clear browser cache (Ctrl+F5 / Cmd+Shift+R)
- Verify file path in `@import` is correct
- Check browser console for CSS errors

### Glassmorphism not working
- Ensure your browser supports `backdrop-filter`
- Some older browsers may not support the blur effect

### Colors look wrong
- Make sure you're using the latest version
- Check if other CSS is overriding NovaStream styles

## Credits

- Built for Jellyfin 10.11.10+
- Inspired by modern streaming platforms
- Glassmorphism design trend

## License

GPL-3.0 - Same as Jellyfin

## Contributing

Contributions welcome! Please test on latest Jellyfin before submitting PRs.