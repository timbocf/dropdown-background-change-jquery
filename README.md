# Dropdown Background Change with jQuery

A compact HTML/jQuery demonstration that changes the page's background image when an option is selected from a dropdown.

## Features

- Three background options: **bg1**, **bg2** and **bg3**.
- The first background is selected on initial load.
- Background changes happen immediately on selection.
- CSS handles image selection and sizing; jQuery handles the change event.

## Run locally

Download or clone the repository and open **dropdown-changes-background-with-jquery.htm** in a browser. Keep the **images** directory next to the HTML file.

You can also serve the repository with an optional local server:

~~~bash
python3 -m http.server 8000
~~~

Then visit http://localhost:8000/dropdown-changes-background-with-jquery.htm.

## Dependencies

The page loads **jQuery 3.3.1** from code.jquery.com with an integrity attribute. A network connection is needed to retrieve that script unless the browser has cached it. No npm install or compilation is required.

## Files and expected assets

| Path | Purpose |
| --- | --- |
| [dropdown-changes-background-with-jquery.htm](dropdown-changes-background-with-jquery.htm) | Markup, inline CSS, dropdown and change handler |
| images/bg1.jpeg | Background used by the bg1 class |
| images/bg2.jpeg | Background used by the bg2 class |
| images/bg3.jpeg | Background used by the bg3 class |

## How it works

The select element has a **target** class, and each option's value is a background class name. Once the document is ready, jQuery attaches a change handler.

The handler removes the body's existing classes and adds the selected option's value. CSS classes then apply their corresponding background images with no repeat and a width of 100% of the containing area.

## Add another background

1. Add an image to **images**.
2. Define a new CSS class pointing to that image.
3. Add an option whose value exactly matches the class name.

No extra JavaScript branch is required.

## Implementation notes

The handler removes **all** classes from the body. If this example is incorporated into a larger page, narrow that behavior to background classes so unrelated layout/theme classes survive.

The background sizing preserves image proportions but does not guarantee full viewport coverage. Adjust the CSS if a cover-style background is desired.

## Manual checks

Select each option and confirm its image appears. If nothing changes, check the browser console, CDN connectivity, image filenames and letter case.
