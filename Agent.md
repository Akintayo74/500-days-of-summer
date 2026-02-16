# AGENT.md

## Project: 500 Days of Summer — Web Experience

### What This Is

A web-native recreation of the animated title card sequences from the film *500 Days of Summer*, starting with the "(500)" scene and evolving over time into a fully interactive, scroll-driven experience. This is not a static wallpaper or a screenshot upload — every element (tree, buildings, sky, counter) exists as a real DOM element or SVG, independently addressable and animatable.

### Why I'm Building It

This is a **living creative sandbox** — a long-term project that grows with me as I develop my animation and frontend skills. It serves three purposes:

1. **Practice ground**: Every new animation technique I learn (from Josh Comeau's Whimsical Animations course, Carl's GSAP courses, or elsewhere) gets applied here on something I actually care about.
2. **Self-expression**: The film resonates with me, and this project is a way to translate that into my craft.
3. **Portfolio piece**: Over time, this becomes a showcase of technical skill and design sensibility — not a project I finished and forgot, but one that visibly evolved.

### The Vision

**Starting point (now):** Faithfully recreate the first title card — the "(500)" scene with the parchment background, hand-drawn cityscape, tree with green leaves, and the day counter. The scene should feel alive with subtle ambient animations (swaying branches, gentle parallax, atmospheric drift) using just CSS and SVG.

**Medium-term:** Recreate the other title card states — the "(1)" scene with the sun, blooming flowers, birds, and warm golden tones. Implement the iconic counter flip from (500) to (1).

**Long-term:** A scroll-driven narrative experience where scrolling moves through the emotional arc of the film. The counter ticks down, the environment shifts (sky color, tree state, weather), and the user journeys from Day 500 to Day 1. New elements and interactions get added as I learn new techniques.

### Technical Decisions

- **Vite** with the vanilla template. No framework — just HTML, CSS, and JS.
- **No React.** This is a visual/animation project, not a data-driven app. Direct DOM access is an advantage here, especially for future GSAP integration.
- **SVG for illustrated elements** (tree, buildings, etc.) so individual parts (branches, leaves, windows) can be targeted and animated independently. The tree is the most important element to get right as SVG.
- **Raster/CSS for textures** — the parchment background can use images or CSS gradients/noise.
- **CSS animations first.** I'm using native CSS transforms, transitions, and keyframes for all initial ambient animations. This is what I know well right now.
- **GSAP later.** GSAP comes in when I need timeline orchestration, scroll-driven coordination across multiple elements, or dynamic/programmatic animation control. I have Carl's Creative Coding Club course catalog ready for when that time comes.
- **Performance-conscious from the start.** GPU-friendly transforms and compositing so the project can accumulate complexity without needing refactors.

### How I'm Building This

**I am coding this entirely by hand.** Claude (via Claude Code or chat) is here for advice, brainstorming, and debugging — not to generate the project for me. This is a learning project and the point is to build the skills through doing the work myself.

### Current Skill Set

- Strong CSS animation fundamentals (completed Josh Comeau's CSS for JS Devs and Joy of React courses)
- Currently in Module 2 of Josh Comeau's Whimsical Animations course (SVG animations)
- Comfortable with HTML, CSS, JS, React, TypeScript
- GSAP: not yet started, but have Carl's full course catalog ready

### Element Breakdown (First Scene)
![500 Days of Summer first scene to recreate](/home/akintayo74/Downloads/500-days-of-summer.webp)

| Element | Implementation | Animation Potential |
|---|---|---|
| Parchment sky/background | CSS gradients + noise texture or raster image | Subtle color shifts across scenes |
| Hand-drawn cityscape | SVG (individual buildings as groups) | Parallax, window lights, silhouette changes |
| Tree (trunk + branches) | SVG with named groups per branch | Swaying, seasonal changes, growth |
| Leaves | SVG elements within tree group | Falling particles, color changes, bloom |
| Ground/earth | SVG or CSS | Texture shifts |
| Day counter "(500)" | HTML/CSS text | Flip animation, countdown |