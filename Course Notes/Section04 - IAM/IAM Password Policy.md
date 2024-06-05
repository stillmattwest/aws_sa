# IAM Password Policy

IAM allows the admin to set a variety of parameters regarding user passwords, including length, types of characters, and password reuse. 

## MFA

AWS also allows you to set MFA.

You definitely want to protect your root account and hopefully your IAM users.

Unfortunately, you can't use the same device for the root and admin accounts for the main user (you). That sucks and unless you want to get a physical MFA device (which can get lost) it forces you to choose which account to protect.

## MFA Options

* Virtual MFA Device (example: Google Authenticator or Authy)
* Universal 2nd Factor (U2F) Security Key. A USB device that acts as a physical key.
* Hardware Key Fob. Has a digital number.
* Hardware key fob for AWS Gov Cloud

You can set password policy in **IAM Account Settings** and you can set up MFA by clicking on the **AWS Account Name** in the upper right.

From there, the settings are pretty intuitive.
