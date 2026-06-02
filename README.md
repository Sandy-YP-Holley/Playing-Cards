# CSS Flexbox Playing Cards Layout

A clean, responsive UI component that renders interactive playing cards using semantic HTML5 and advanced CSS Flexbox architecture. This project serves as a practical implementation of complex alignment strategies, contrasting parent flex containers against individual item alignments (`align-self`).

---

## 🛠️ Core CSS Flexbox Mechanics

This project goes beyond basic flex positioning by mixing container properties with individual item overrides:

* **Parent Grid Control (`#playing-cards`):** Acts as the primary flex container. It centers the deck horizontally using `justify-content: center` and utilizes `flex-wrap: wrap` to gracefully drop cards to a new row on smaller viewport widths.
* **Smart Spacing (`gap`):** Implements a clean `20px` spacing strictly between neighboring card elements without polluting outer block margins.
* **Component Distribution (`.card`):** Uses `justify-content: space-between` on the main axis to push the left, middle, and right components to opposite edges of the card.
* **Cross-Axis Isolation (`align-self`):** Overrides standard stretching behavior to accurately position card elements exactly where they belong in a real card layout:
  * `.left` is pinned to the top corner via `flex-start`.
  * `.middle` sits perfectly centered via `center`.
  * `.right` is anchored to the bottom corner via `flex-end`.
* **Nested Flex Structures:** The `.middle` component pulls double duty. It acts as a **flex item** to center itself vertically within the card, and simultaneously acts as a **flex container** (`display: flex; flex-direction: column`) to vertically stack internal suite content.

---

## ✨ Features

* **No-Image Assets:** Uses native HTML unicode character strings (`♠`, `♣`, `♥`) for high-fidelity rendering that scales seamlessly without blurriness.
* **Strict Layout Boundaries:** Explicit card aspect ratios (`150px` x `220px`) matching standard playing card structural conventions.
* **Fully Responsive:** Fluid reflow mechanics that shift instantly from desktop grids to single-column mobile views.

---

## 📂 Project Structure

```text
├── index.html   # Semantic card structure and suit configurations
└── styles.css   # Layout engine, alignment modifiers, and card cosmetics
