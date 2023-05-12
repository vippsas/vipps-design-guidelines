---
sidebar_label: Button guidelines
sidebar_position: 20
hide_table_of_contents: true
pagination_next: null
pagination_prev: null
---

# Button guidelines

See the [Assets](assets.md) page to download the Vipps buttons.

## Style

Vipps buttons are only available in one style: white text on orange.

![Vipps payment button styles](images/style.svg)

### Exceptions (WCAG AAA)

Our orange buttons with white text meet the WCAG demands for AA.
If your website need WCAG AAA, we allow to render our buttons in higher contrast, either white or black background.
Use prefers-contrast and -ms-high-contrast CSS media queries to detect if your user have settings that asks for high contrast.

| Rectangular button  | Pill button  |
| - | - |
| ![Rectangular white - EN](images/rectangular-white-EN.png) | ![Pill white - EN](images/pill-white-EN.png) |
| ![Rectangular black - EN](images/rectangular-black-EN.png) | ![Pill white - EN](images/pill-white-EN.png) |

This exception only applies to color. Don't create your own Vipps buttons or alter the font, button radius, or padding within the button in any other way.

## Best practices

### ✅ Do

- Use only the buttons provided by Vipps.
- Use the same style of button throughout your site.
- The button text should only use a verb approved by Vipps.
- Ensure that the size of the Vipps buttons remains equal to or larger than other buttons.
- Ensure that you choose a background color that contrasts with the button color.

### 🔥 Don’t

- Don't create your own Vipps buttons or alter the font, color, button radius, or padding within the button in any way.
- Don't use Vipps buttons to initiate any action other than a flow controlled by Vipps (either opening our app or a Vipps landing page).
- Don't make the Vipps button smaller than other buttons.
- Don't use a background color that's similar to the button color.
- Don't add hover effects.
- Don't add stroke.

![Cart with two buttons](images/cart-two-buttons.svg)

👍 If you place a Vipps button next to another button, make sure the Vipps button is of equal size or larger.


[figma-link]: https://www.figma.com/file/8678DAVOSUQbD6VhZVUGuh/Vipps-Design-Toolkit?type=design&node-id=1%3A972&t=MTp5hTbXodmc0qUs-1