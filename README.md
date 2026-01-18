<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# CampusPilot - Campus Learning Dashboard

A responsive, reactive React + TypeScript web application built with Vite and Tailwind CSS for campus event management, task tracking, and learning collaboration.

## 🎯 Features

### ✨ Fully Responsive Design
- **Mobile-First Approach**: Optimized for smartphones, tablets, and desktops
- **Adaptive Layouts**: 
  - Mobile (< 768px): Sidebar toggles, full-width content, touch-optimized buttons
  - Tablet (768px - 1024px): Sidebar visible, optimized spacing
  - Desktop (> 1024px): Full three-column layout with sidebar, main content, and right panel

### ⚡ Reactive State Management
- Real-time state updates using React hooks
- Efficient memoization with `useMemo` for performance
- Toast notifications with smooth animations
- Dynamic event filtering and tracking

### 📱 Mobile-Specific Enhancements
- Touch-friendly UI with minimum 44x44px tap targets
- Collapsible sidebar with overlay on mobile
- Hidden search bar and secondary panels on smaller screens
- Responsive padding and spacing
- Improved scrollbar styling

### 🎨 Dynamic UI Components
- EventsPage with event browsing and registration
- MainDashboard with task management and schedule
- RightPanel with live challenges (desktop only)
- MiniFloatingCalendar with date selection
- TopBar with notifications and cohort selector
- Animated toast notifications

## 🚀 Run Locally

**Prerequisites:**  Node.js (v16+)

1. Install dependencies:
   ```bash
   npm install
   ```

2. Run the development server:
   ```bash
   npm run dev
   ```

3. Open your browser and navigate to `http://localhost:5173`

## 🏗️ Build for Production

```bash
npm run build
```

The optimized build will be created in the `dist` directory.

## 📋 Project Structure

```
├── components/              # React components
│   ├── Sidebar.tsx         # Navigation sidebar (responsive)
│   ├── TopBar.tsx          # Header with search & notifications
│   ├── MainDashboard.tsx   # Dashboard with tasks & schedule
│   ├── RightPanel.tsx      # Sidebar panel (desktop only)
│   ├── EventsPage.tsx      # Events browsing & registration
│   ├── FullCalendarPage.tsx# Calendar view
│   ├── MiniFloatingCalendar.tsx # Floating calendar widget
│   ├── TaskCard.tsx        # Individual task card
│   ├── LoginPage.tsx       # Login/splash screen
│   ├── TutorialOverlay.tsx # Tutorial overlay
├── hooks/                   # Custom React hooks
│   └── useResponsive.ts    # Responsive breakpoints hook
├── types.ts                # TypeScript type definitions
├── App.tsx                 # Main app component with routing
├── index.tsx               # React entry point
├── index.html              # HTML template
└── vite.config.ts          # Vite configuration
```

## 🎨 Responsive Breakpoints

The app uses Tailwind CSS breakpoints:
- **sm**: 640px
- **md**: 768px (Primary mobile/tablet breakpoint)
- **lg**: 1024px (Primary tablet/desktop breakpoint)
- **xl**: 1280px
- **2xl**: 1536px

### Key Responsive Classes:
- `hidden md:block` - Hidden on mobile, shown on tablet+
- `hidden lg:flex` - Hidden on mobile/tablet, shown on desktop
- `max-h-screen overflow-hidden` - Prevent layout shift
- `px-4 py-6 md:p-8` - Responsive padding

## 🪝 Custom Hooks

### `useResponsive()`
Provides real-time responsive information:
```typescript
const { isMobile, isTablet, isDesktop, width, height } = useResponsive();
```

## 🎯 Responsive Features Implementation

### Mobile Navigation
- Sidebar collapses into a toggleable drawer
- Menu button appears on top-left on mobile
- Overlay closes sidebar when navigating
- Automatic sidebar closure after tab change

### Flexible Layouts
- Main content area adapts to available space
- Scrollable task cards with responsive min-width
- Collapsible panels and sections
- Touch-optimized form controls

### Performance
- Smooth transitions and animations
- Optimized re-renders with React hooks
- Lazy loading of components
- CSS-in-JS for dynamic styles

## 🔧 Development

### Tech Stack
- **React** 19.2.3 - UI framework
- **TypeScript** 5.8 - Type safety
- **Vite** 6.2 - Build tool
- **Tailwind CSS** - Utility-first CSS
- **Lucide React** - Icon library

### Code Quality
- TypeScript strict mode for type safety
- React.FC for functional components
- Proper React hooks usage
- Component composition and reusability

## 📚 Components Guide

See individual component files for detailed documentation on props and usage.

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📄 License

Your license information here.
