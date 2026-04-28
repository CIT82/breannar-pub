# Project 0: Template Analysis (Part 1)
**Template Name:** [Klar](https://themewagon.com/themes/free-bootstrap-5-html5-website-template-klar/)
**Bootstrap Version:** [v5.2.1]

---

## Section 1: The &lt;head&gt;
* **External CSS:** [Bootstrap](./css/theme.min.css), [aos](./css/theme.min.css)
    * From my findings through `/css/theme.css`, they combined both the bootstrap css and aos css required by the libraries and appended them to the same file. I don't really like this decision, though I do like that the css is local, I would prefer to keep them seperate. Seperating them myself could lead to errors as they may have applied custom overrides (doubt it), but I don't want to risk messing with it. I will probably create a style.css later on.
* **Custom CSS:** `<style>@font-face</style>`
    * Outside of changing inline styles in the body, the only custom css applied in the header is through a `style` tag for `font-face`. This was done for the `Inter` fonr to create a custom handler for how they wanted to load the font into the index.
