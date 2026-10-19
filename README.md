# Bridgeway — Modern Payments Landing Page

A modern, responsive landing page concept for **Bridgeway**, designed to communicate a simpler way to manage digital payments through a clean interface, bold typography, and distinctive visual elements.

> **Your way to better payments.**  
> Accept, send, and reconcile payments in one place.

## ✨ Overview

Bridgeway is a landing page UI project focused on creating a polished, responsive user experience. The design combines a plum-and-lime color palette, custom SVG background shapes, reusable Vue components, and responsive layouts to create a distinctive visual identity.

## 🚀 Features

- **Responsive design** — layouts adapted for desktop and mobile screens.
- **Custom hero section** — layered SVG shapes and curved backgrounds.
- **Reusable Vue components** — organized components for the header, hero section, buttons, and brand mark.
- **Responsive navigation** — navigation links and call-to-action buttons arranged for different screen sizes.
- **Custom visual styling** — plum and lime colors, typography, and carefully positioned imagery.
- **Mobile-friendly experience** — simplified hero backgrounds, readable text, and appropriately sized images on smaller screens.
- **Clean component structure** — maintainable code using Vue's Composition API and `<script setup>` syntax.

## 🛠️ Tech Stack

- **Vue 3** — component-based UI development.
- **Vite** — development server and build tool.
- **Tailwind CSS** — utility-first styling.
- **CSS & SVG** — custom shapes, layered backgrounds, and responsive styling.
- **JavaScript** — component logic and UI behavior.

## 📂 Project Structure

```text
bridgeway/
├── public/
├── src/
│   ├── assets/
│   │   └── water.jpg
│   ├── components/
│   │   ├── BrandMark.vue
│   │   ├── BaseButton.vue
│   │   ├── Header.vue
│   │   └── HeroSection.vue
│   ├── App.vue
│   ├── main.js
│   └── style.css
├── index.html
├── package.json
└── vite.config.js
```

*The structure above is illustrative; adjust the filenames and folders to match the actual repository.*

## ⚙️ Getting Started

### Prerequisites

- Node.js
- npm

### Installation

1. Clone the repository:

   ```bash
   git clone YOUR_GITHUB_REPOSITORY_URL
   ```

2. Navigate to the project directory:

   ```bash
   cd bridgeway
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open the local URL displayed in your terminal.

### Build for Production

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

## 🎨 Design Highlights

### Color Palette

| Color | Purpose |
|---|---|
| Plum / Dark Purple | Primary backgrounds and visual depth |
| Lime / Yellow | Highlights and calls to action |
| White | Typography and contrast |

### UI Design

- Layered SVG shapes create a distinctive hero background.
- Responsive CSS adapts the visual composition to mobile devices.
- Reusable components keep the interface consistent.
- Clear typography and call-to-action elements establish visual hierarchy.

## 📱 Responsive Experience

The layout is designed to adapt across screen sizes.

- **Desktop:** brand mark and navigation links on the left, with the primary call to action on the right.
- **Mobile:** a simplified navigation layout, readable hero content, and a rectangular image without the desktop clipping effects.

## 🧠 What I Practiced

- Building reusable components with Vue 3.
- Creating responsive layouts with CSS and Tailwind CSS.
- Working with inline SVGs and custom background shapes.
- Applying mobile-specific styling using media queries.
- Organizing a frontend project for readability and maintainability.

## 🔮 Future Improvements

- Add smooth scrolling and subtle entrance animations.
- Build out the Benefits and Contact Us sections.
- Improve accessibility and keyboard navigation.
- Add cross-browser testing and performance optimizations.
- Deploy the landing page for public access.

## 👩‍💻 Author

**Nisreen Salem**

Frontend Developer focused on building modern, responsive, and visually engaging web experiences.

- GitHub: [NisreenSalem](https://github.com/NisreenSalem)
- Dribbble: [NisreenSalem97](https://dribbble.com/NisreenSalem97)

---

*Built with Vue 3, Vite, and Tailwind CSS.*
