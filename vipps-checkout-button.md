<!-- START_METADATA
---
title: Checkout button
sidebar_label: Checkout button
sidebar_position: 60
description: Use Checkout Direct and other "Buy now" checkout-button.
pagination_prev: Null
pagination_next: Null
---
END_METADATA -->

# Checkout button

Make it super easy for customers to check out straight from a product page with Checkout Direct and our "Buy now" checkout-*button*!

The *button* is provided in multiple variants and colors and can be tailored to your page.

To be able to use the badge on your site you need to add the Vipps Checkout Button JavaScript library.
The library should preferably be added between your page's `<head>...</head>`-tags and only once per page:

```html
<script async type="text/javascript" src="https://checkout.vipps.no/checkout-button/v1/vipps-checkout-button.js"></script>
```

If you don't have access to edit your websites code directly, you can also place the JavaScript library just before the *button*.

## Example button

You can find a demo and examples of all the variants [here](https://checkout.vipps.no/checkout-button/v1).

![Checkout Button](images/vipps/vipps-checkout-button.png)

```html
<vipps-checkout-button variant="orange" branded="true"></vipps-checkout-button>
```

### Attributes

All attributes are optional.

| Attribute | Description                                                                       | Default  |
|:----------|:----------------------------------------------------------------------------------|:---------|
| variant   | The color variant of the button. Supported values: `orange`, `purple`, `stroked`. | `orange` |
| language  | ISO 639-1 alpha-2 language code. Supported values: `en`, `no`.                    | `no`     |
| rounded   | The button will have rounded corners (oval shape) when set to `true`              | `false`  |
| stretched | Will fill the whole with of the parent container when set to `true`               | `false`  |
| branded   | Brand with the Vipps-logo                                                         | `false`  |

### Customization

You can customize the placement and size of the *button* by either applying your own CSS-style with the `class` or `style` attribute.

If the *button* is too small or too large to fit your content, you can override the `font-size` to scale the *button* as follows:

```html
<vipps-checkout-button variant="orange" variant="purple" style="font-size: 1.5rem;"></vipps-checkout-button>
```

Which will scale the *button* to 1.5x the size of the root font-size. You may also use `px` or `em` values to scale the *button*.

The *button* is an `inline` element by default, which means it will stay on the same line as sibling elements.

So to center or fill the *button* you have to set `display: block` on the element to prevent it from being `inline`.

Use `text-align` with `display:block` to align the *button*:

```html
<vipps-checkout-button variant="stroked" style="display: block; text-align: center;"></vipps-checkout-button>
```

## Integrations

Read more about integrating with Vipps Checkout Direct [here](vipps-checkout-api.md#alternative-2-vipps-checkout-direct---we-handle-the-checkout-and-redirect-the-user-back-to-you).

### Example integration

```html
<html>
  <head>
    <title>Merchant website</title>
    <script async type="text/javascript" src="https://checkout.vipps.no/vippsCheckoutSDK.js"></script>
    <script async type="text/javascript" src="https://checkout.vipps.no/checkout-button/v1/vipps-checkout-button.js"></script>
  </head>
  <body>
    <vipps-checkout-button id="checkout-button" variant="orange" branded="true"></vipps-checkout-button>
    <script>
      document
        .getElementById("checkout-button")
        .addEventListener("click", function () {
          // Relay an initiate session request to Vipps Checkout API through the merchant's backend
          fetch("<MERCHANT BACKEND CREATE SESSION URL>", {
            method: "POST",
          })
            .then((response) => response.json())
            .then((data) => {
              VippsCheckoutDirect({
                checkoutFrontendUrl: data.checkoutFrontendUrl,
                language: "no",
                token: data.token,
              });
            })
            .catch((error) => {
              // Handle at least these two types of errors here:
              // 1. Fetch to create session endpoint failed
              // 2. VippsCheckout SDK not loaded resulting in VippsCheckout not being defined
            });
        });
    </script>
  </body>
</html>
```
