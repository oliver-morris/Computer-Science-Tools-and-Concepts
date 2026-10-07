# Authentication

## Overview
Authentication is "the process or action of proving or showing something to be true, genuine, or valid" or in computing aspect: "the process or action of verifying the identity of a user or process". This allows users to access their data/account and **only** theirs.

Multi-factor authentication is crucial for better security to avoid any unwanted access from attackers. For example, many modern systems use both password and either passkey or a 2FA verification code sent to email/phone/authenticator app. To be MFA, the different authentication methods must fall under different categories:
- Something you know (PINs, Passwords, etc)
- Something you have (Email, Phone, Debit Card, etc)
- Something you are (Fingerprint, Face ID, etc)
- Context location (Being close to an item)

Using multiple from the same category is not recommended e.g. an attacker could have access to somebody's phone and then have access to their phone and email. Some secure systems like your bank card may not require two factors every time. For example:
- Bank cards: allow contactless so you only need the card (something you have). Requires PIN every so often to check for fraud
- Websites: only make you log in once and can save the login to the device (something you have). Requires re-login after a predetermined period.

These things are implemented to improve the easy of the customer and experience but can present possible security risks with attackers stealing these items.


## Authentication Methods


## Resources
Types of Digital Authentication - https://www.geeksforgeeks.org/computer-networks/types-of-digital-authentication
