# NovaStream Theme for Jellyfin

A premium dark theme for Jellyfin 10.11.10+ inspired by Apple TV and Plex. Features glassmorphism, cinematic effects, and smooth animations.

## Features

- **Apple TV / Plex Style** - Premium dark interface
- **Glassmorphism** - Frosted glass effects with backdrop blur
- **Cyan Accent Colors** - Modern streaming platform look
- **Smooth Animations** - Hover effects, transitions, page animations
- **Responsive** - Works on desktop, mobile, and TV clients
- **Customizable** - Easy to modify via CSS variables
- **Pure Black Background** - Perfect for OLED displays

## Compatibility

- Jellyfin 10.11.x and above
- All web browsers (Chrome, Firefox, Safari, Edge)
- Jellyfin mobile apps (iOS/Android)
- Jellyfin media player

## Installation

### CDN (Recommended)

1. Open Jellyfin Dashboard > Branding > Custom CSS
2. Add the following line:
   ```css
   @import url('https://cdn.jsdelivr.net/gh/Geounix/novastream@master/theme.css');
   ```
3. Click **Save** - No restart required

### Skin Manager Plugin

1. Install the Skin Manager plugin from the Jellyfin plugin catalog
2. Add the NovaStream repository URL
3. Select and apply NovaStream from the plugin interface

## Customization

### Change Accent Color

Add to Dashboard > Branding > Custom CSS:

```css
:root {
  --ns-accent: #ff6b6b;        /* Red */
  --ns-accent: #51cf66;        /* Green */
  --ns-accent: #ffd43b;        /* Yellow */
  --ns-accent: #cc5de8;        /* Purple */
  --ns-accent: #ff922b;        /* Orange */
  --ns-accent: #00d4ff;        /* Cyan (default) */
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
- Verify the CDN URL is correct
- Check browser console for CSS errors (F12)

### Glassmorphism not working
- Ensure your browser supports `backdrop-filter`
- Chrome, Edge, and Safari have full support
- Firefox has full support since v103

## License

GPL-3.0 - Same as Jellyfin