# Setup
## Reddit Client ID
A Reddit Client ID is needed to access Reddit from 3rd party clients.

### Reddit Client ID creation steps
![Create application](/screenshots/create_application.png)

1. Go to [reddit.com/prefs/apps](https://www.reddit.com/prefs/apps) and login if
necessary
2. Click `create another app...`. Do not re-use any Client ID for any app other
than Continuum.
3. Set the name to Continuum
4. Set the type to `installed app`
5. Set redirect uri to `continuum://localhost`. If the redirect uri is set
incorrectly it won't work.
6. Complete the `reCAPTCHA`
7. Click `create app`
8. Copy the Client ID of your newly created app. It is recommended to save it
in the notes of your entry for Reddit in your password manager.

![Client ID](/screenshots/client_id.png)

> [!NOTE]
>
> This is just an example Client ID. It was created and deleted. Keep
> yours private.

### Adding a Reddit Client ID to Continuum
The method of adding a Client ID to Continuum depends on whether this is the
first time the app is being set up.

**Initial setup:**
1. Open Continuum and press `GET STARTED`
2. Select your theme colors, if you like, and press `DONE`
3. Enter your Client ID and press `OK`
4. Wait for Continuum to restart

**Changing the Client ID:**
1. Go to [`Settings in the side bar`](/screenshots/settings.png)
1. Select [`Reddit API Client ID`](/screenshots/continuum_client_id1.png)
2. Press [`Reddit API Client ID`](screenshots/continuum_client_id2.png)
3. Enter your [Client ID](screenshots/enter_client_id.png). It is
best to copy and paste it.
5. Press [`OK`](screenshots/post-saved_client_id_override.png)
6. Wait for Continuum to restart

# Common errors
The most likely cause for this is the `redirect uri` is set incorrectly. The
big tell is if you can view Reddit in guest mode, aka without logging in.

## Correct username and password does not work
Continuum depends on
[Android System Webview](https://play.google.com/store/apps/details?id=com.google.android.webview)
by default for logging into Reddit. So if having the login issue, your best
course of action would be to upgraded to the latest version of Android
possible, and then the latest version of
[Android System Webview](https://play.google.com/store/apps/details?id=com.google.android.webview)
possible.

Reddit's login password now requires
[XHR](https://en.wikipedia.org/wiki/XMLHttpRequest) to work. Older versions of
[Android System Webview](https://play.google.com/store/apps/details?id=com.google.android.webview)
don't support [XHR](https://en.wikipedia.org/wiki/XMLHttpRequest).

The current and known good version of
[Android System Webview](https://play.google.com/store/apps/details?id=com.google.android.webview)
is `131.0.6778.135`.

### WebView updating
Updating
[Android System Webview](https://play.google.com/store/apps/details?id=com.google.android.webview)
can be tricky. You likely can't search and see it in the
[Google Play Store](https://play.google.com/store/games) app on your phone.

The best way is to find the app in the `Apps` section of `Settings`. The search
box in the top right can make it easier to find in the long list of apps. Once
you select
[Android System Webview](https://play.google.com/store/apps/details?id=com.google.android.webview)
go to the bottom. You can see your version. Click on `App details`. This will
take you directly to
[Android System Webview](https://play.google.com/store/apps/details?id=com.google.android.webview)
listing in the [Google Play Store](https://play.google.com/store/games) app. If
there is an update available it will be shown.

### Alternative versions of WebView
There are
[Dev](https://play.google.com/store/apps/details?id=com.google.android.webview.dev),
[Beta](https://play.google.com/store/apps/details?id=com.google.android.webview.beta),
and
[Canary](https://play.google.com/store/apps/details?id=com.google.android.webview.canary)
versions of
[Android System Webview](https://play.google.com/store/apps/details?id=com.google.android.webview).
These aren't recommended, but under rare circumstances they might be useful to
get a newer version of
[Android System Webview](https://play.google.com/store/apps/details?id=com.google.android.webview).

Once installed you need to enable
[Developer options](https://developer.android.com/studio/debug/dev-options),
you can go to them in `Settings`. Within is an option called
`WebView implementation` where you can pick which `WebView` is active.
