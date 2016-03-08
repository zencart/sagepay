# Zen Cart Sagepay Integration

## Integrations

Currently the only integration is for the Sagepay Form API

Integration for Sagepay Server coming soon.


## Installation

Currently no core files are changed, so you can just upload these files into the relevant directories within your store.
**Note: You should not copy the README, LICENSE or changelog.txt files to your live server.**
 
The code will automatically create any required database tables when it is first run.

When installing the payment module from your admin > modules > payment, the following should be noted

* For the password field, this must be your encrypted password, not your Sagepay login password.
* If you are in testing mode, you may want to set the Debug Mode to `log` or `Log and Email`

## Dependencies

Currently Sagepay requires that you have the PHP mcrypt module installed.
If you have the Suhosin extension installed, you may have problems with this module.
Please see [this faq entry](https://www.zen-cart.com/content.php?342-The-Sagepay-Form-module-has-an-error-regarding-Suhosin for more details) for more details.

## Testing

Details for Credit Card numbers that can be used for testing are shown in the admin > modules > payment page for Sagepay, and repeated here.

* VISA 4929000000006
* MASTERCARD 5404000000000001
* DELTA 4462000000000003
* SOLO 6334900000000005 Issue 01
* DOMESTIC MAESTRO 5641820000000005 Issue 01
* AMEX 374200000000004
* ELECTRON 4917300000000008
* JCB 3569990000000009
* DINERS 36000000000008

You will need to supply the following values for
CV2, Billing Address and Billing Post Code Numbers.

* CV2 123
* Billing Address Numbers 88
* Billing Post Code Numbers 412

These are the only values which will return as Matched.

You will also need to enter the 3D Secure password as " password " (it is case sensitive)<br >
so as the 3D Secure authentication returns Fully Authenticated.

## Attribution

This Integration was initially inspired by a [Nixak module](https://www.zen-cart.com/downloads.php?do=file&id=959) which also has a corresponding [Forum Support Thread](https://www.zen-cart.com/showthread.php?219158-Sagepay-Form-Integration)

