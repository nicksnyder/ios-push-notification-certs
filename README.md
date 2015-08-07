# ios-push-notification-certs
How to create and update Apple iOS push notification certificates

## How to generate a certificate signing request

1. In the Applications folder on your Mac, open the Utilities folder and launch Keychain Access.
2. Within the Keychain Access drop down menu, select Keychain Access > Certificate Assistant > Request a Certificate from a Certificate Authority.
3. In the Certificate Information window, enter the following information:
  - In the User Email Address field, enter your email address (doesn't really matter).
  - In the Common Name field, create a name for your certificate (AppName Push). This is how it will appear in your keychain.
  - The CA Email Address field should be left empty.
  - In the "Request is" group, select the "Saved to disk" option.
4. Click Continue and choose a name for your certificate signing request file (e.g. AppNamePush.certificateSigningRequest)

At this point you have a certificate signing request and a private key in your keychain.

DO save your certificate signing request (check it in to source control) because you can reuse it when your push certificates expire (in 1 year).

## Generating a push certificate

This step assumes that you have a certificate signing request.

1. Sign in to [Apple's Developer Portal](https://developer.apple.com/membercenter/)
2. Go through the process to create a new push certificate (sandbox or production) and upload your certificate signing request when prompted for it.
3. Download the certificate from Apple (i.e. aps_development.cer or aps_production.cer)

## Configuring your push server

This step assumes that you have one or more push certificates.






