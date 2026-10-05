# Treeline Supply

Treeline Supply is a premium alpine equipment landing experience tailored for skiers who move quickly through changing terrain[cite: 21]. The platform showcases performance ski equipment meant for powder laps and fast resort days[cite: 18]. The project treats the user's scroll like a terrain test, utilizing cinematic frame sequences, crisp technical metadata, and a restrained design approach[cite: 21].

## ✨ Features

* **Cinematic Scroll Sequences:** A 520vh hero scroll sequence preloads 203 local frames, updating the image via a `useScrollFrame` hook based on section-relative scroll progress[cite: 21, 22].
* **Interactive Gear Scrubbing:** A 480vh sticky gear section scrolls through 232 local frames while revealing reactive cards for products like the Polar VLT 22, GripLock Pro, Kore 99 Carbon, and Ridge Plant 16[cite: 22].
* **Alpine Design System:** The visual language mimics ski film title cards and field notes, utilizing graphite and navy surfaces, powder white text, pale cyan indicators, and a signature lime green (`#d7ff63`) for active states[cite: 21].
* **Custom Typography:** The UI pairs the Anton font for wordmarks and headings, IBM Plex Mono for technical copy, and Instrument Serif for editorial accents[cite: 18, 21].
* **Field Lookbook:** Features a dotted dark lookbook section with a responsive three-column desktop (or one-column mobile) grid to showcase product imagery[cite: 22].

## 🛠️ Tech Stack

* **Core:** React and TypeScript[cite: 19].
* **Build Tool:** Vite[cite: 19].
* **Icons:** Lucide React[cite: 19].
* **Styling:** Tailwind-compatible styling utilizing CSS variables and semantic classes within `src/styles.css`[cite: 21, 22].

## 📁 Project Architecture

* `src/App.tsx`: Manages the landing-page composition, data arrays, and the reusable `useScrollFrame` hook for frame preloading and selection[cite: 21].
* `src/styles.css`: Houses the responsive alpine layout, dotted technical surfaces, overlays, and typography rules[cite: 21].
* `public/assets/`: Contains all local image assets, ensuring the runtime never relies on external image CDNs or hotlinking[cite: 21, 22].

## 🚀 Getting Started

This project uses Vite for fast development and building[cite: 19]. 

**Available Scripts:**

* **Start Development Server:** Run `npm run dev` to start the Vite dev server, which is configured to listen on host `0.0.0.0` and port `3000`[cite: 19, 21].
* **Build for Production:** Run `npm run build` to compile the TypeScript files and bundle the project[cite: 19].
* **Preview Build:** Run `npm run preview` to locally preview the production build on port `3000`[cite: 19].
