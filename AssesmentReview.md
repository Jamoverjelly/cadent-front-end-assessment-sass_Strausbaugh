# Cadent FED Aptitude Test: Review

### Stage 1: Mock-up, gather resources

The provided design was used to mock-up a high-fidelity, static wireframe in Adobe Xd. This working draft allowed for accurate and efficient abstraction of the original "client" design in terms of desired colors, anticipated svg resources, and overall layout.

### Stage 2: Build

Appropriate semantic markup for the sidebar's structure was researched and adapted from past projects involving similar requirements. The animation controlling the sidebar's reveal from the hamburger toggle button utilizes a bit of JavaScript to control the application of a `show` class on the parent elements making up the sidebar. All other animations and styles were achieved entirely using Sass which was transpiled into CSS using the `style:watch` script provided in the project's package.json file. One of the more common animations, a `transition` effect was abstracted into its own mixin and stored along with other scalable styles in the project's config.scss file. This file also specifies variables for the primary and secondary colors presented in the client's design. These variables are referenced throughout the style-rules of the menu.scss file and can easily be modified from the config file based on any interest of quickly trying out different color schemes for the sidebar.

Pseudo-selectors were used to target the children of the menu toggle button (using `:nth-child`) to specify a `transform` animation, as well as within menu.scss itself to apply styling during mouse-over detection using `:hover`.

### Stage 3: Refinement

Once all aspects of the sidebar's layout, styling and animation were complete, steps were taken to evaluate the semantic markup and test accessibility using Chrome's built-in screen reader. Elements lacking meaningful semantic context were modified to include `aria-label`, `role`, and `tabindex` attributes as necessary relative to the perceived functionality of the design. With more time to work on the sidebar UI, I'd look into ways of modifying or removing the hamburger toggle's focus outline while maintaining the element's accessibility.

Final efforts were directed at improving maintainability aspects of the code itself. This involved checking that all class names in the markup followed a secure and meaningful naming-methodology as well as ensuring that the order of CSS properties within each style-rule followed a similar pattern throughout.
