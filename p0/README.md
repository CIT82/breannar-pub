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

## Section 3: Site Inventory (Bottom Half)

### 1. Article Preview
* **Line Numbers:** 193-259
* **Top-Level Classes:** `container`, `row`, `rounded-5`, `shadow`, `col-12`, `col-md-6`
* **Research:** This next section is a preview of a bunch of different article cards that they have made to show content pages for the site. They use a parent wrapping with a black background and then inside of that wrapper apply a container to ensure the background covers the entire width. Then inside of the container there is a row, defining gaps for the columns that will be inside. Then each card is put into a column wrapper which then contains all the card fields like an image, heading, description and an anchor tag.

### 2. Pricing Sectoin
* **Line Numbers:** 278-304
* **Top-Level Classes:** `container`,`row`,`d-flex`,`align-items-center`
* **Research:** The pricing section is a container with only one row but breaks out two different sections into their own parts with col-12 on small screens and col-6 with medium screens. It also utilizes flexbox and aligning the elements to the center of the page so the cols aren't pushed off to the sides creating a large gap in the center.

### 3. Features Section
* **Line Numbers:** 305-348
* **Top-Level Classes:** `container-fluid`, `position-relative`, `position-absolute`
* **Research:** A major functionality about the features section is that the entire section is animated. Meaning that once it appears on screen there is a fade effect with parts of the section sliding into place. They achieve this effect with the position relative and then attaching the child elements with position-absolute.

### 4. Reviews Section
* **Line Numbers:** 349-512
* **Top-Level Classes:** `container`, `row`, `d-flex`, `align-items-center`
* **Research:** The review section take a lot of inspiration into how the pricing section was setup with a wrapping container, a row inside that is set to flexbox and aligning the items center. The section utilizes svgs to create stars in the cards that they have created, of course each card is in a column and rounded appropriately.

### The Footer
* **Line Numbers:** 516-598
* **Top-Level Classes:** `bg-black`, `border-top`, `container`, `row` 
* **Research:** The footer creates the same amount of padding gap the rest of the sections have following in suit. It also uses a black background to set itself out from the previous section and a border too creating a nicer transition. It is made up of the brand name and lists of links helping navigate to other pages, even though there still is a sticky nav. It keeps everything centered inside of the container.

## Section 4: The Scripts
* **Vendor JS Files:** [Bootstrap](./js/bootstrap.bundle.js) Line 607, [aos](./js/aos.js) Line 608
* **Main JS File:** There is no "main" js file as they only utilize bootstrap and aos that they linked seperately. However, they do include 2 script tags that have inline JS. One script tag inits AOS, the other script tag is for aos as well letting the browser know where the scrollPos is through an event listener as well as debugging for the developer the scroll position in the console.
