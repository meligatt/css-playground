Notes from talk: Sara Soueidan on Inclusively Responsive UIs with CSS and SVG • ColdFront 2018.
- url: https://www.youtube.com/watch?v=TbOxPhcVzCc
- user query:  prefer-reduced-motion
- css variables (:root element)
- variable fonts: font-variation-settings property
- @support rule
- @font-face
- provide fallbacks for newer css properties not suppoerted by all browsers,/
- use new properties as a way of progresive enhancement. but provide a stable css way as well.
- CSS level 5 spec: @media (light-level: dim | washed) (no browser support)
- hsl prefered than rgb for creating a11y color themes.
-html data attributes
- css masks insread of css filter to change svg's used as a background.
- best a11y practice to use svg today: inline them in the html
- vendor media query for high contrast: @media screen and (-ms-high-contrast: active) { ... }
-tips for UI's to work well with high contrast themes activated by the user, without controlling the colors:
1. dont use css background images to deliver content/important info.
2. icons: use svg inline, style the svg using system color keywords. (fill: currentColor | highlight |windowText ) instead of specifying an specific color.
3.replace shadows with borders in High contrast mode. border: 5px solid transparent (HC mode will apply a color to it by default)
4. color swatched are lost on HCM, give it semantic: <input type="color" disabled value="#FFFFF"> (not safari support) alternative: markup color swatches using SVG. <rect> (design system form mozilla) https://protocol.mozilla.org/)
5. do not remove FOCUS. visible focus is a WCAG requirement.
6. avoid overridiing default browser focus styles. if so, provide a better alternative.
- apply visible focus just on keyboard interaction, not mouse. using: a:focus-visible{ outline: 2px solid hsl(248, 82%, 60%)} browser suppor is low, provide a polifill WICG/focus-visible