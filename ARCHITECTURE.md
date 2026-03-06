# Project: Liwen Chiou - Digital Architect Portfolio 💎

This documentation serves as a comprehensive guide for project migration and agent onboarding. It details the architecture, design philosophy, and technical implementation of the "Digital Architect" personal website.

---

## 🏛️ Project Structure Overview

The project is designed as a **modern, high-performance single-page application (SPA)** that requires **zero build steps**. It leverages CDN-based React and Tailwind CSS for maximum agility and direct editability.

### Key Files
- `index.html`: The core application. Contains the React engine, Tailwind configuration, global styles, and all components.
- `assets/`: Static resources including project images and brand assets.
- `liwen2026-12weekreport/`: A specialized sub-app for habit tracking and progress reporting, sharing the same minimalist design language.

---

## 🚀 Technical Architecture

### 1. Engine
- **React 18**: Managed via UNPKG CDN.
- **Babel**: Used for on-the-fly JSX compilation (perfect for rapid iteration).
- **Tailwind CSS 3**: Play CDN integration for dynamic styling.

### 2. State Management
- Uses standard React hooks (`useState`, `useEffect`, `useRef`).
- Navigation is handled via an `activeItem` state, mapping IDs (intro, portfolio, etc.) to component rendering.

---

## 🎨 Design Philosophy: "Digital Architect"

The aesthetic is characterized as **Premium Minimalist with Zen influences**. Every visual update must adhere to these rules:

### 1. Typography (Bilingual Excellence)
We use a precise font stack to balance English and Traditional Chinese (ZH-TW):
- **Serif (Headings/Hero)**: `Playfair Display` (EN) + `Noto Serif TC` (ZH). Used for h1, h2, and high-level emphasis.
- **Sans (Structure/Body)**: `Inter` (EN) + `Noto Sans TC` (ZH). Used for h3, list items, and descriptions.
- **Mono (Utility)**: `JetBrains Mono`. Used for badges, status codes, and identifiers.

### 2. Material System (Glassmorphism)
The project utilizes high-end "Glass" effects:
- **`shadow-glass`**: A deep, soft shadow for levitating elements.
- **`backdrop-blur-xl`**: Creating frosted glass depth.
- **`bg-white/40`**: The standard semi-transparent material.
- **`mesh`**: Radial gradients (`copper` and `slate`) used sparingly in the background to add warmth.

---

## 🧩 Component Breakdown

### `Introduction` (The Hero)
- **Massive Typography**: A bold h1 name combined with a 0.85 line-height for a magazine-style feel.
- **Status Indicator**: An animated pulse badge reflecting current availability.
- **Bio**: High-contrast, well-spaced narrative with a `copper` accent border.

### `Services` (The Business Hub)
- **Author Identification**: A flagship glass card that encapsulates the user's identity and service offerings.
- **Call to Action**: Direct `mailto` links and GitHub integration.

### `Portfolio` (The Showcase)
- **Category Filtering**: A seamless filtering system with liquid-like transitions.
- **Minimalist Cards**: Subtle borders that ignite (`shadow-glow`) upon interaction.

---

## 🤖 Agent Onboarding: How to Maintain the "Pro Max" Quality

When an agent is asked to modify this project, they MUST:

1.  **Check the Palette**: Always use `copper` (#D27B5E) for accents and `slate-ink` (#2D3436) for primary text. Never use generic colors.
2.  **Respect the Grid**: Maintain the `md:px-24` horizontal safe zone and `space-y-20` vertical rhythm.
3.  **Verify Readability**: Ensure Chinese text never uses `font-light`. Always use `font-normal` or `font-medium` with a line-height of `1.75`.
4.  **Interaction First**: Every card or button should have a `transition-all duration-500` or `700` with a subtle transform (like `hover:-translate-y-1`).
5.  **No Placeholders**: If a new module is needed, it must be fully designed with real icons (emojis or Lucide) and professional copy.

---

## 🛠️ Deployment & Migration
This project can be hosted on any static hosting service (GitHub Pages, Vercel, Netlify) by simply uploading the root directory.

> **Current Repository**: `/Users/qiuliwen/Documents/工程師/project/everything-claude-code/personal-site`
> **Author**: Liwen Chiou
