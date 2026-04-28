# Project 0: Template Analysis (Part 1)
**Template Name:** [Klar](https://themewagon.com/themes/free-bootstrap-5-html5-website-template-klar/)
**Bootstrap Version:** [v5.2.1]

---

## Section 1: The &lt;head&gt;
* **External CSS:** [Bootstrap](./css/theme.min.css), [aos](./css/theme.min.css)
    * From my findings through `/css/theme.css`, they combined both the bootstrap css and aos css required by the libraries and appended them to the same file. I don't really like this decision, though I do like that the css is local, I would prefer to keep them seperate. Seperating them myself could lead to errors as they may have applied custom overrides (doubt it), but I don't want to risk messing with it. I will probably create a style.css later on.
* **Custom CSS:** `<style>@font-face</style>`
    * Outside of changing inline styles in the body, the only custom css applied in the header is through a `style` tag for `font-face`. This was done for the `Inter` fonr to create a custom handler for how they wanted to load the font into the index.

## Section 2: Site Inventory (Top Half)

### 1. The Navigation/Menu
* **Line Numbers:** Lines 75-111
* **Top-Level Classes:** Main classes are `navbar`,`navbar-dark`,`fixed-top`, not as important are `bg-black` and `px-vw-5`
* **Research:** These main classes define a navbar on the `nav` tag for a darkmode site. They ensure that the nav is fixed to the top, meaning if you scroll down, the nav "sticks" to the top. They also added a black background and horizontal padding with a vw of 5 to make it more centered.

### 2. The Logo/Branding
* **Line Numbers:** Lines 77-86
* **Top-Level Classes:** Main classes are `navbar-brand`, `col-12`, `col-md-auto` and `text-center`, not as important `pe-md-4`, `fs-4`.
* **Research:** The logo is contained inside of the `nav` tag as a link with a class `navbar-brand` which comes with its own styles for a brand inside of the navbar. There is a padding to the right on screens higher than medium and auto aligns itself in columns. On screens smaller than medium the brand takes up the entire row. The font size is 4 and text is centered.

### 3. Mission and CTA
* **Line Numbers:** 114-138
* **Top-Level Classes:** `w-100`,`overflow-hidden`,`position-relative`,`bg-black`,`text-white`
* **Research:** Okay whats interesting here is they are using position-relative. I'm guessing this is due to the fact that they have a custom attribute to the main wrapper div for a fade animation. This is interesting that wrapping tags for `aos` need position relative applied to the container element. Then elements inside use position position-absolute to latch onto the parent. It has a `w-100` making the width the entire screens viewport, with a black background and white text. It also has overflow-hidden, which seems to also effect the animation.

### 4. What we do (skipping abstract pictures section as its not really a content section imo)
* **Line Numbers:** 159-191
* **Top-Level Classes:** `bg-dark` on main wrapper, below is `container`, `px and py`, with `row` and `col` inside.
* **Research:** The template for the next main content section focuses on the what we do or about of the site. Here there is a main wrapper for a background color, and the following tag is a `container` to apply some margin and enable rows and columns to be created inside of it. They also add some additional padding to the x and y of the container to make the section a little cleaner and not against the top edge.
