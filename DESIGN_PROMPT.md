# MotusDAO AI Psychology Platform - Design System Prompt

## Overview
Create a modern, sophisticated AI psychology platform with a neumorphic-glassmorphic hybrid design system. The app features a dynamic 3D spacetime background, multi-theme support, and a comprehensive chat interface with CELO blockchain integration.

## Core Design Philosophy
- **Neumorphic-Glassmorphic Hybrid**: Combines soft, elevated surfaces with translucent glass effects
- **Dynamic & Interactive**: 3D animations, smooth transitions, and responsive interactions
- **Multi-Theme Support**: White, Dark, and Matrix (cypherpunk) themes
- **Blockchain Integration**: CELO payment system with smart account functionality
- **Psychology-Focused**: Calming, supportive visual language for mental health context

## Color Palette

### Primary Colors
```css
--primary-black: #1a1a1a
--primary-blue: #6366f1
--primary-gray: #6b7280
--pastel-purple: #e0e7ff
--pastel-pink: #fce7f3
--pastel-cyan: #ecfeff
--soft-white: #fafafa
```

### Gradient Combinations
- **Primary**: `linear-gradient(to right, #9333ea, #ec4899)` (Purple to Pink)
- **Secondary**: `linear-gradient(to right, #3b82f6, #06b6d4)` (Blue to Cyan)
- **Background**: `linear-gradient(45deg, rgba(168, 85, 247, 0.08) 0%, rgba(236, 72, 153, 0.06) 25%, rgba(244, 114, 182, 0.08) 50%, rgba(168, 85, 247, 0.06) 75%, rgba(236, 72, 153, 0.08) 100%)`

## Typography
- **Primary Font**: Inter (weights: 300, 400, 500, 600, 700)
- **Display Font**: Jura (weights: 300, 400, 500, 600, 700)
- **Accent Font**: Playfair Display (weights: 600, 700)

### Typography Classes
```css
.modern-typography-large {
  font-size: clamp(2rem, 5vw, 4rem);
  line-height: 1.1;
  font-weight: 700;
  letter-spacing: -0.02em;
}

.modern-typography-medium {
  font-size: clamp(1.25rem, 3vw, 2rem);
  line-height: 1.3;
  font-weight: 600;
  letter-spacing: -0.01em;
}
```

## Component Design System

### 1. Background System
- **Animated Gradient Background**: Moving gradient with multiple radial overlays
- **3D Spacetime Background**: Interactive Three.js particle system with mouse interaction
- **Theme-Specific Colors**: 
  - White: Soft pastels and whites
  - Dark: Deep blues, purples, pinks
  - Matrix: Neon green on black

### 2. Navigation Bar
```css
/* Rounded transparent navbar with backdrop blur */
backdrop-blur-xl bg-white/10 border border-white/20 rounded-3xl
shadow-[0_8px_32px_rgba(0,0,0,0.1)]
```

**Features:**
- Fixed positioning with scroll-based opacity changes
- Gradient logo with hover animations
- Wallet connection status with copy functionality
- Mobile-responsive hamburger menu
- Smooth animations using Framer Motion

### 3. Glassmorphic Cards
```css
backdrop-blur-[20px] bg-white/10 border border-white/15 rounded-3xl
shadow-[0_8px_32px_rgba(0,0,0,0.1)]
filter: drop-shadow(0 0 20px rgba(255,255,255,0.1))
```

**Usage:**
- Feature cards with hover effects (scale, translate)
- Chat message containers
- Modal dialogs
- Status indicators

### 4. Button System

#### Primary Buttons
```css
background: linear-gradient(to right, #9333ea, #ec4899);
color: white;
border-radius: 16px;
transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
```

#### Secondary Buttons
```css
backdrop-blur-[20px] bg-white/10 border border-white/15
hover:bg-white/20 hover:scale-105
```

### 5. Chat Interface
- **Message Bubbles**: Gradient backgrounds for user, glassmorphic for AI
- **Transaction History**: Sidebar with transaction links
- **Payment Status**: Real-time status indicators
- **Input Area**: Glassmorphic design with focus states

### 6. Theme System

#### White Theme
- Light background with subtle gradients
- Soft shadows and borders
- High contrast text

#### Dark Theme
- Dark background (#0b0b0f)
- Bright accent colors
- Glowing effects

#### Matrix Theme
- Black background (#000000)
- Neon green accents (#10b981)
- Glowing text shadows
- Cyberpunk aesthetic

## Animation & Interaction

### Transitions
```css
.smooth-transition {
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.smooth-transition-slow {
  transition: all 0.6s cubic-bezier(0.4, 0, 0.2, 1);
}
```

### Hover Effects
- Scale transforms (1.05x)
- Shadow enhancements
- Color transitions
- Backdrop blur changes

### Loading States
- Spinning indicators
- Pulse animations
- Skeleton loaders
- Progress bars

## Layout Structure

### Homepage
1. **Hero Section**: Large typography, CTA buttons, animated 3D element
2. **Features Grid**: 6 feature cards with icons and descriptions
3. **CTA Section**: Gradient background with call-to-action
4. **Footer**: Simple, clean footer with links

### Chat Page
1. **Header**: Role selection, payment mode, balance display
2. **Main Chat**: Message history with transaction info
3. **Sidebar**: Transaction history and status
4. **Input**: Message input with send button

## Responsive Design
- **Mobile-First**: Optimized for mobile devices
- **Breakpoints**: sm, md, lg, xl
- **Grid System**: CSS Grid and Flexbox
- **Typography**: Fluid typography with clamp()

## Accessibility
- High contrast ratios
- Keyboard navigation
- Screen reader support
- Focus indicators
- ARIA labels

## Technical Implementation

### Dependencies
- **Next.js 14**: React framework
- **Tailwind CSS**: Utility-first CSS
- **Framer Motion**: Animation library
- **Three.js**: 3D graphics
- **GSAP**: Advanced animations
- **Privy**: Wallet integration

### Key Components
1. `RoundedTransparentNavbar`: Main navigation
2. `SpacetimeBackground`: 3D particle system
3. `ThemeManager`: Theme switching
4. `ColorThemeToggle`: Theme selector
5. `HeroAnimation`: 3D animated element

## Implementation Notes
- Use CSS custom properties for theming
- Implement proper error boundaries
- Add loading states for all async operations
- Ensure proper TypeScript types
- Optimize for performance with lazy loading
- Implement proper SEO meta tags

## File Structure
```
app/
├── globals.css (Design system)
├── layout.tsx (Root layout)
├── page.tsx (Homepage)
├── chat/page.tsx (Chat interface)
└── components/
    ├── RoundedTransparentNavbar.tsx
    ├── ThemeManager.tsx
    └── three/
        ├── SpacetimeBackground.tsx
        ├── HeroAnimation.tsx
        └── ColorThemeToggle.tsx
```

This design system creates a sophisticated, modern interface that balances visual appeal with functionality, specifically tailored for an AI psychology platform with blockchain integration.

