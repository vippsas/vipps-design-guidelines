---
sidebar_label: Button guidelines
sidebar_position: 20
hide_table_of_contents: true
pagination_next: null
pagination_prev: null
---


import ApiSchema from '@theme/ApiSchema';
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# Button guidelines

<!-- START_COMMENT -->

💥 Please use the documentation pages here: <https://developer.vippsmobilepay.com/docs/vipps-design-guidelines/>. 💥

<!-- END_COMMENT -->

## Style

Vipps buttons are available in white text on orange.

| Rectangular button  | Pill button  |
| - | - |
| ![Rectangular orange - EN](images/rectangle-orange-EN.png) | ![Pill white - EN](images/pill-orange-EN.png) |

See the [Assets](assets.md) page to download variations of the Vipps buttons.

### Exceptions (WCAG AAA)

Our orange buttons with white text meet the Web Content Accessibility Guidelines (WCAG) demands for AA (mid range).
If your website must meet the WCAG AAA (highest accessibility range), you are allowed to render our buttons in higher contrast, either white or black background.
Use `prefers-contrast` and `-ms-high-contrast` CSS media queries to detect if your users have settings that request high contrast.

| Rectangular button  | Pill button  |
| - | - |
| ![Rectangular white - EN](images/rectangular-white-EN.png) | ![Pill white - EN](images/pill-white-EN.png) |
| ![Rectangular black - EN](images/rectangular-black-EN.png) | ![Pill white - EN](images/pill-white-EN.png) |

This exception only applies to color. Don't create your own Vipps buttons or alter the font, button radius, or padding within the button in any other way.

## Approved verbs


<Tabs
defaultValue="norwegian"
groupId="verbs"
values={[
{label: 'Norwegian', value: 'norwegian'},
{label: 'English', value: 'english'},
]}>
<TabItem value="norwegian">
* "Betal med Vipps"
* Logg inn med Vipps
* Registrer med Vipps
* Fortsett med Vipps
</TabItem>

<TabItem value="english">
* Pay with Vipps
* Log in with Vipps
* Register with Vipps
* Continue with Vipps
</TabItem>
</Tabs>

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