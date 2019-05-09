# Cadent FED Aptitude Test - Markup, Style, and Pre-processors

## Introduction

This exercise is designed to test your understanding of the fundamental concepts HTML and CSS. The below prompt is going to walk you through a scenario where you're going to have to view a design and then make it come to life using nothing but HTML and CSS. Here are some of the items that it will test:

- Semantic markup
- Basic selectors
- Pseduo-selectors
- Sass preprocessing & it's elements
- Style architecture
- CSS animations

## Prompt

Congratulations! Someone that you cold just accepted your offer to help them redo their website. They chose you because they took a look at your Github and knew that you had extensive experience in styling their application.

They're looking to develop a prototype that they can bring to their leaders to show them just how much updating their style can do for their brand appearance. Rather than proving out a full fledged application, they have chosen the route of doing some UI engineering and develop something to really deliver a wow!

They have a design, and they're leaving the rest up to you. Good thing you have a template that you've developed so you can get coding right away.

The first thing that they want you to work on is the sidebar of their website. Once complete, they're going to re-assess your position. Depending on the quality of work you provide, you should be in for the long term!

### Tasks

- Develop the sidebar of their website based upon the design. The sidebar includes everything from the Avatar and down.

### Things you must use

Your client's are pretty picky. They want you to use at least one of the each of the following:

- 1 pseudo-selector
- 1 mixin
- 1 animation

### Items you will be evaluated on

- How did you architect your styles? Is there a specific convention that you typically use?
- How scale-able are those styles? Did you give them room to change the color in an instant?
- Did you choose a scale-able styling convention? Are they going to have problems with namespace clashing further on down the road?
- What kind of elements did you use in the markup? Are screen readers going to have a tough time scanning through it?
- How well did you implement some of the more accepted modern CSS attributes?

### Prototype

The design team has provided you with a prototype that they exported from Sketch up onto InVision. They removed some of the other components on the screen so that they could better focus your attention to the component that needs to be worked on.

Click on the link and use the password below to access the prototype:

- Link: https://invis.io/CMQTL3U5TBS
- PW: `letsdothis!`

## Getting Started

This project has a complete boilerplate for you, ready to use to start developing. This boilerplate assumes you have a working knowledge of node and npm.

Fork the repository and download it locally to your machine. If you don't have node already installed, either use homebrew for a mac or use the NodeJs website.

### Starting the development instance

You're going to need 2 terminal sessions open at once running 2 different processes.
In the 1st terminal session, run the following:

```shell
npm run start
```

This will start up the development instance and reload your solution anytime a file changes.
In the 2nd terminal session, run the following:

```shell
npm run style:watch
```

This will queue up Sass to compile all of your CSS rules down into one CSS file, every-time you make a change.

## Completing the assignment

Once you feel that you have completed everything to the best of your ability, please commit your changes and upload your work to a Codesandbox of your choice and forward the link to your recruiter.

Make sure that you keep a local copy of it as that you'll be asked to review it when you come in for your in-person interview.

Good luck!

<hr>

# Addendum

## Cadent FED Aptitude Test: Review

### Stage 1: Mock-up, gather resources

The provided design was used to mock-up a high-fidelity, static wireframe in Adobe Xd. This working draft allowed for accurate and efficient abstraction of the original "client" design in terms of desired colors, anticipated svg resources, and overall layout.

### Stage 2: Build

Appropriate semantic markup for the sidebar's structure was researched and adapted from past projects involving similar requirements. The animation controlling the sidebar's reveal from the hamburger toggle button utilizes a bit of JavaScript to control the application of a `show` class on the parent elements making up the sidebar. All other animations and styles were achieved entirely using Sass which was transpiled into CSS using the `style:watch` script provided in the project's package.json file. One of the more common animations, a `transition` effect was abstracted into its own mixin and stored along with other scalable styles in the project's config.scss file. This file also specifies variables for the primary and secondary colors presented in the client's design. These variables are referenced throughout the style-rules of the menu.scss file and can easily be modified from the config file based on any interest of quickly trying out different color schemes for the sidebar.

Pseudo-selectors were used to target the children of the menu toggle button (using `:nth-child`) to specify a `transform` animation, as well as within menu.scss itself to apply styling during mouse-over detection using `:hover`.

### Stage 3: Refinement

Once all aspects of the sidebar's layout, styling and animation were complete, steps were taken to evaluate the semantic markup and test accessibility using Chrome's built-in screen reader. Elements lacking meaningful semantic context were modified to include `aria-label`, `role`, and `tabindex` attributes as necessary relative to the perceived functionality of the design. With more time to work on the sidebar UI, I'd look into ways of modifying or removing the hamburger toggle's focus outline while maintaining the element's accessibility.

Final efforts were directed at improving maintainability aspects of the code itself. This involved checking that all class names in the markup followed a secure and meaningful naming-methodology as well as ensuring that the order of CSS properties within each style-rule followed a similar pattern throughout.
