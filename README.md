# simplesamlphp-authgoogleoauth2
An authentication module for simplesamlphp which authenticates against Google OAuth2

I created this largely because of Google's OpenID 2.0 deprecation. I used OpenID for authentication to RightScale,
among other things.

# Installation

You'll first need to go to the Google developer console and create an application which your users will be asked to
"trust" when they use this authentication mechanism. This is the same as the typical OAuth process when you enable
an application to access your google account information. In this case, the only thing this application accesses about
your account are your user details.

https://console.developers.google.com/project

Then, a simple entry in your simplesamlphp config is all you need.

## config/authsources.php
```
  'authgoogleoauth2' => array(
      'authgoogleoauth2:authgoogleoauth2',
      'client_id' => 'yourclientid.apps.googleusercontent.com',
      'client_secret' => 'Your Secret',
      'developer_key' => 'Your API Key',
    ),
```