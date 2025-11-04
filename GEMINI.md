# GEMINI.md

## Directory Overview

This directory contains a static, single-page wedding invitation website for Amit & Priyanka. The page is visually rich, featuring animations, background music, and interactive elements.

## Key Files

*   `index.html`: The main and only HTML file, containing the structure, content, styling (inline CSS), and client-side logic (inline JavaScript) for the entire website.
*   `song.mp3`: The background music for the website.
*   `aplogo.png`: The favicon and logo for the couple.
*   `ganpati.png`: An image of Lord Ganesha displayed at the top of the page.
*   `couple1.png`, `couple2.png`, `couple3.png`, `couple4.png`: Images of the couple used in a "polaroid" style photo gallery.
*   `airport.svg`, `mandap.svg`, `taxi.svg`: Icons used in an animated "helpful information" section to show the route to the venue.

## Usage

This is a static website. To view it, simply open the `index.html` file in a web browser. There is no build process or server required.

## Change Log

*   **Venue Section:**
    *   Increased the `min-height` of the venue section on mobile to prevent text from overlapping with the icons.
    *   Adjusted the `endY` position of the taxi animation to be lower on both mobile and desktop.
    *   Centered the text content of the venue card vertically to prevent overlap with the airport icon.
*   **Button Size:** Adjusted the size of the buttons on mobile for better visibility.
*   **SVG Icon Sizes:** Increased the size of the airport, mandap, and taxi icons.
*   **Firework Animation:**
    *   Added a firework animation to the Sangeet section.
    *   The animation is triggered when the section is visible.
    *   The fireworks are particle-based and continuous.
    *   The animation is responsive and uses the website's color palette.
    *   The animation was refined to be more "natural" with varying rocket speeds, burst sizes, and a gravity effect.
*   **`top.svg` Integration:**
    *   Added `top.svg` as a background image to the top section, spanning end-to-end with a gradient fade on all four borders.
    *   Updated `top.svg` to a less tall version for better visual fit.
    *   Adjusted the `mask-image` CSS property for a more pronounced fade at the bottom of `top.svg`.
    *   Removed horizontal padding and bottom margin from the `.ganesh-section` to ensure `top.svg` spans end-to-end and to remove any unwanted visual borders.
    *   Merged the Ganesh mantra and Ganpati icon into a single cohesive top section.
*   **Page Layout Reordering:**
    *   Reordered elements in the `welcome-section` to place the couple's names above the welcome message.
    *   Moved the Ganpati image to be below the Ganesh mantra within the top section.
*   **Shehnai Scroll Animation:**
    *   Added `shehnai.svg` images (left and right, mirrored) to the `welcome-section`.
    *   Implemented a scroll-driven animation for the shehnai images using JavaScript, making them appear and rotate as the user scrolls down, and recede when scrolling up.
    *   The animation is directly controlled by the scroll position relative to the `welcome-section`.
    *   Shehnais are initially off-screen on page load and animate smoothly into view within a defined scroll range.
    *   CSS `transform` properties are directly manipulated by JavaScript on `requestAnimationFrame` calls for smooth scrubbing, without relying on CSS transitions for the animated properties.
*   **Shehnai Animation:**
    *   Rebuilt the animation to be directly controlled by the window's scroll position for a "scrubbable" effect.
    *   Adjusted the size and vertical position of the shehnais to be larger and in line with the ampersand.
    *   The shehnais now start in a half-visible state at the top of the page and animate into full view on scroll.
*   **Polaroid Photos:**
    *   Adjusted the `top` position of the polaroid photos to align them correctly with the rope they are hanging from, using values calculated from the rope's Bezier curve.
*   **Ganesh Section:**
    *   Moved the Ganpati icon from the Ganesh section to the Welcome section, just above the couple's names.
    *   Doubled the height of the Ganesh section by increasing its vertical padding.
    *   Reduced the size of the Ganpati icon by 30%.
    *   Moved the Ganesh mantra up to the top of the section.
*   **Top SVG:**
    *   Fixed an issue where the `top.svg` background image was not spanning the full width of the screen by using `width: 100vw` and removing `overflow-x: hidden` from the body.
