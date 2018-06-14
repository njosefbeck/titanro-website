# titanro-website

Took what was currently up at http://titanro.net and re-wrote both the HTML and the CSS. This ensured that the website would look good on all devices. Along the way made some design decisions for mobile and tablet that can be modified / discarded.

The `style` directory contains a number of CSS files, generated using the various `npm scripts` found in `package.json`. `style.min.css` is the one I would use in production.

That being said, if you want to make changes to the CSS, and don't want to deal with running NPM scripts to concat --> auto-prefix --> minify said CSS, then just use `reset.css` and `framework.css`.

A couple of changes that might not immediately be obvious when previewing `index.html` in the browser:

* For the "carousel" code, I cropped the `carousel_default.png` image and renamed it `carousel_default_no_border.png` and moved the border to CSS. This way, in the future, images don't have to contain the border themselves.
* Ideally, the second and third widgets would sit side-by-side and below the "server status" widget on "tablet"-sized screens. Unfortunately, since the widgets are different heights, a CSS + JavaScript solution would be necessary and I didn't have the time to implement.