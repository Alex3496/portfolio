# LucideIcon Component

A custom Astro component for using Lucide icons with the same styling capabilities as the existing Icon component.

## Usage

```astro
---
import LucideIcon from './LucideIcon.astro';
---

<!-- Basic usage -->
<LucideIcon icon="mail" />

<!-- With custom size -->
<LucideIcon icon="phone" size="1.5rem" />

<!-- With custom color -->
<LucideIcon icon="map-pin" color="var(--accent-regular)" />

<!-- With gradient -->
<LucideIcon icon="user" gradient />

<!-- With both size and gradient -->
<LucideIcon icon="briefcase" size="2rem" gradient />
```

## Available Icons

Current icons available in the system:

- `mail` - Email icon
- `phone` - Phone icon  
- `map-pin` - Location/pin icon
- `globe` - Globe/world icon
- `languages` - Languages icon
- `user` - User/person icon
- `briefcase` - Briefcase/work icon
- `graduation-cap` - Education/graduation icon

## Adding New Icons

To add a new Lucide icon:

1. Go to [Lucide Icons](https://lucide.dev/)
2. Find your desired icon
3. Copy the SVG code
4. Extract only the inner elements (paths, circles, etc.) - remove the `<svg>` wrapper
5. Add to the `lucideIconPaths` object in `LucideIcon.astro`

Example:
```typescript
'new-icon': `<path d="..."/><circle cx="..." cy="..." r="..."/>`,
```

## Props

- `icon`: (required) The name of the icon from `lucideIconPaths`
- `size`: (optional) Custom size using CSS units (default: `1em`)
- `color`: (optional) Custom color (default: `currentcolor`)
- `gradient`: (optional) Apply gradient effect (default: `false`)

## Features

- ✅ Same styling system as existing Icon component
- ✅ Responsive sizing with CSS custom properties
- ✅ Gradient support with CSS variables
- ✅ Proper accessibility with `aria-hidden="true"`
- ✅ SVG optimization for performance
- ✅ TypeScript support for icon names
