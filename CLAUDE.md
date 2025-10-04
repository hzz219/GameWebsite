# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

必须使用中文回答我

## Project Overview

This is a Chinese 3D particle effects visualization website built with Three.js. The project creates an interactive particle system that can transform between different 3D shapes (cube, sphere, pyramid, cylinder) with customizable colors.

## Architecture

- **Single-page application**: Everything is contained in `index.html`
- **Three.js 3D graphics**: Uses Three.js from npmmirror.com CDN for rendering
- **No build process**: Pure HTML/CSS/JavaScript with no compilation step
- **Particle system**: 20,000 particles that can morph between shapes
- **Interactive controls**: Shape morphing button and color picker

## Key Components

### Particle System (`index.html:95-305`)
- Scene initialization and camera setup
- Buffer geometry for efficient particle rendering
- Dynamic color gradients with HSL color space manipulation
- Shape morphing animations with scatter-and-return transitions

### Shape Transformations
- **Cube**: Random distribution within cube boundaries
- **Sphere**: Uniform distribution on sphere surface using spherical coordinates
- **Pyramid**: Constrained distribution within pyramid volume
- **Cylinder**: Distribution on cylinder surface

### Interactive Controls
- Shape button triggers morphing sequence
- Color picker updates particle colors with gradient variations
- OrbitControls for 3D scene navigation

## Development Notes

- Uses npmmirror.com (formerly Taobao CDN) for Three.js loading in China
- Particle colors use vertex colors for individual particle coloring
- Animation uses `requestAnimationFrame` for smooth 60fps rendering
- Shape transitions use a scatter-then-reform pattern for visual effect
- Material uses additive blending for glowing particle effect

## Running the Project

Simply open `index.html` in a web browser. No server or build process required.