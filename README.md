


# OpusCraft

OpusCraft is a front-end portfolio project that demonstrates the construction of a complete institutional website for a fictional luxury piano brand. Based on a course exercise, the project was developed to apply and solidify essential modern web development concepts, including **Semantic HTML5**, **Modular CSS3**, and **Responsive Design**.

The challenge was to recreate a taught technical structure and apply it to an original theme, resulting in an elegant and functional site that serves as a high-quality showcase for the brand's products and services.

**Check out the live project:** [https://mateus-bernardi.github.io/opuscraft/](https://mateus-bernardi.github.io/opuscraft/)

##  Table of Contents

*   [About The Project](#about-the-project)
*   [Project Pages](#project-pages)
*   [Key Features and Applied Concepts](#key-features-and-applied-concepts)
    *   [Semantic HTML5](#semantic-html5)
    *   [Modular and Component-Based CSS3](#modular-and-component-based-css3)
    *   [Responsive Design](#responsive-design)
    *   [JavaScript for Interactivity](#javascript-for-interactivity)
    *   [Accessibility (A11y)](#accessibility-a11y)
*   [Tech Stack](#tech-stack)
*   [File Structure](#file-structure)
*   [How to Run the Project](#how-to-run-the-project)
*   [Challenges & Learnings](#challenges--learnings)
*   [License](#license)

## About The Project

This project originated as a course exercise with a key challenge: to apply a taught technical structure to a completely original theme. I chose to create **OpusCraft**, a brand for artisanal pianos, which allowed me to focus on creating a clean, elegant, and premium user experience.

 To put these concepts into practice, I developed a complete institutional website. It includes an **engaging homepage**, detailed **product pages** with galleries and technical sheets, a functional **quote form**, and service sections such as **insurance plans**.

 The technical goals were clear from the start:
 *   To write **clean, semantic, and accessible HTML5**.
 *   To build a **robust and scalable CSS3 architecture** with a modular approach.
 *   To ensure a **responsive design** for a seamless experience across all devices.
 *   To implement interactivity and animations with **vanilla JavaScript**, without relying on frameworks.

##  Project Pages

The project consists of several interconnected pages to create a complete browsing experience:

| Page | File (`.html`) | Description |
| :--- | :--- | :--- |
| **Home** | `index.html` | Brand introduction, featured models, technology, and testimonials. |
| **Pianos** | `pianos.html` | Catalog with all available piano models. |
| **Insurance** | `seguros.html` | Details about insurance and maintenance plans, with benefits and an FAQ. |
| **Quote** | `orcamento.html` | Form to request a quote for pianos or insurance plans. |
| **Contact** | `contato.html` | Contact form, store information, and location map. |
| **Terms** | `termos.html` | Page with terms and conditions for purchasing and using services. |
| **Piano Detail** | `pianos/maestro-grand.html` | Individual page for each model, with an image gallery, specs, and a technical sheet. |

##  Key Features and Applied Concepts

This project is not just about visual appearance but also about the quality of the code and the methodology behind it.

### Semantic HTML5
The site's structure uses semantic HTML5 tags to ensure clarity, accessibility, and SEO.
-   **Main Structure:** `<header>`, `<main>`, `<footer>`, and `<nav>` define the main sections of each page.
-   **Content:** `<section>`, `<h1>`-`<h6>`, and `<blockquote>` are used to organize content logically and hierarchically.
-   **Definition Lists:** The Frequently Asked Questions section (`seguros.html`) uses `<dl>`, `<dt>`, and `<dd>` to correctly associate questions with their answers.

### Modular and Component-Based CSS3
The stylesheet is organized in a highly modular fashion, making the code easier to maintain and scale.
-   **Single Entry Point:** The `style.css` file acts as the main importer, bringing together all other CSS modules.
-   **Division by Components:** Styles are split into specific folders and files for each component (`header.css`, `footer.css`, `componentes.css`), section (`introducao.css`, `depoimento.css`), and page (`orcamento.css`).
-   **CSS Variables:** Global properties like colors and fonts are defined as CSS Variables (Custom Properties) in `utilidades/cores.css`, allowing for easy and consistent theming.

```css
/* Example from utilidades/cores.css */
:root {
  --color-0: #ffffff;
  --color-11: #111111;
  --color-p1: #ffbb00;
  --color-p5: #332200;
}

/* Example from utilidades/componentes.css */
.botao {
  background: linear-gradient(#ffbf00, #f2a50c);
  color: var(--color-p5);
}
```

### Responsive Design
The website is fully responsive and adapts to different screen sizes, from mobile devices to desktops.
-   **Media Queries:** `@media` queries are used to adjust the layout, font sizes, and visibility of elements at specific breakpoints (like 800px and 600px).
-   **Flexible Layouts:** The use of Flexbox and Grid Layout allows components to reorganize fluidly and efficiently.

### JavaScript for Interactivity
Vanilla JavaScript is used to add interactivity and enhance the user experience.
-   **Scroll Animations:** Page elements have subtle fade-in animations (`fadeInDown`) as the user scrolls, controlled by the `simple-anime.js` script.
-   **Interactive Components:** Features like the accordion in the FAQ section are controlled via JS to expand and collapse answers.
-   **Dynamic Selection:** On the quote form, JS controls which fields are displayed based on the user's choice (Piano or Insurance).

### Accessibility (A11y)
Basic accessibility practices were implemented to make the site more inclusive.
-   **ARIA Attributes:** `aria-label` is used to provide context for navigation elements and sections. `aria-expanded` and `aria-controls` are used in the FAQ to indicate the state of the accordion buttons.
-   **Links and Buttons:** All navigation links and buttons are clearly identifiable and have visible `:hover` and `:focus` states.

## Tech Stack

* **HTML5:** Structured with semantic tags for better SEO and accessibility.

* **CSS3:** Leveraged advanced features like Custom Properties, Grid, Flexbox, and a modular file structure for maintainability.

* **JavaScript (ES6+):** Used for DOM manipulation, event handling, and creating all interactive features from scratch.

* **Simple-Anime.js:** A lightweight, dependency-free JavaScript library for scroll animations.

##  File Structure

The project is organized with a clear and intuitive folder structure, separating HTML, CSS, JavaScript, and assets.

```
opuscraft/
├── css/
│   ├── utilidades/ (colors, typography, components)
│   ├── global/ (header, footer)
│   ├── home/ (introducao, tecnologia, etc.)
│   ├── pianos/
│   ├── seguros/
│   ├── contato/
│   ├── orcamento/
│   ├── termos/
│   └── style.css (main file that imports the others)
│
├── img/
│   ├── fotos/
│   ├── icones/
│   ├── parceiros/
│   └── redes/
│
├── js/
│   ├── plugins/simple-anime.js
│   └── script.js
│
├── pianos/
│   ├── maestro-grand.html
│   ├── nocturne-etude.html
│   └── sonata-concert.html
│
├── index.html
├── pianos.html
├── seguros.html
├── contato.html
├── orcamento.html
└── termos.html
```

##  How to Run the Project

This is a static web project. No dependencies or build processes are required.

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/Mateus-Bernardi/opuscraft.git
    ```
2.  **Navigate to the project folder:**
    ```sh
    cd opuscraft
    ```
3.  **Open the `index.html` file** in your preferred browser.

For a better development experience, it is recommended to use a local server, such as the **Live Server** extension for Visual Studio Code, which automatically reloads the page after any code changes.

##  Challenges & Learnings

* **Balancing CSS-Only vs. JavaScript Solutions:** One challenge was deciding when to use clever CSS tricks (like the `:checked` selector for the budget form details) versus when to use JavaScript. This project reinforced the idea that while CSS-only solutions are impressive, JavaScript often provides more robust, maintainable, and accessible solutions for complex interactivity (like the FAQ accordion).

* **The Power of a Design System:** Establishing a strict system for colors, typography, and spacing from the beginning was a valuable lesson. Using CSS Custom Properties made enforcing this system effortless and any global changes trivial.

* **Accessibility is Not an Afterthought:** Building components like the FAQ with accessibility in mind from the start (using `button` elements, `aria-` attributes) is far more effective than trying to add it later.  



##  License  

This project is distributed under the MIT License.
