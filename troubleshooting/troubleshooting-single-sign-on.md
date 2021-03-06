# Troubleshooting SSO issues

## Always try this first

If you're having issues signing into Digital Theatre+ using Single Sign On (SSO) please try the following:

1. Clear cache and cookies.  If you need instructions how to do this, please refer to [clear-my-cache.com](https://clear-my-cache.com/)
2. Restart your computer
3. Try a different browser

If the issue persists, please follow these steps to send information to Digital Theatre+.

## Information to provide to Digital Theatre+

Below this list is a link to a form which will collect key information to enable Digital Theatre+ to help you.  You will be asked for the following:

1. Provide an explanation the steps required to recreate the problem you are experiencing (the more detail, the quicker we can help)
1. Confirm that cache and cookies have been cleared
1. Confirm that the computer has been restarted
1. Confirm whether you are accessing Digital Theatre+ via EZProxy
1. Confirm whether you are using UK Federation or OpenAthens to sign in
1. Confirm what [this page](https://www.digitaltheatreplus.com/Shibboleth.sso/Session) says after you attempt to login
1. Provide the full error message that is displayed, if any
1. Provide a PDF containing the full output of [the Google BrowserInfo page](https://toolbox.googleapps.com/apps/browserinfo/)
1. Provide a PDF containing the full output of: [the SameSite Cookie test page](https://samesite-sandbox.glitch.me/)
1. Provide a copy of all messages recorded by the browser console.  If you need instructions how to do this, please refer to [this guide on Zapier.com](https://zapier.com/help/troubleshoot/behavior/view-and-save-your-browser-console-logs)
1. Optionally, provide a username and password for a test account that Digital Theatre+ may use to debug the issue for you

You may wish to consider recording your web browser session using a service such as [Screencastify](https://www.screencastify.com/) which will allow you to record your web browser session for free.  You can then send this to Digital Theatre+ for reference.

## Request support from Digital Theatre+

You can [request support for technical issues via this form](https://forms.gle/UtLHsRoDCrKdBTiG8)

## Error messages

### Message was signed, but signature could not be verified

The certificate that was used to sign the message didn't match the one the SP expected based on metadata. That can be caused by, in order of likelihood:

1. The certificate in the IdP metadata is different from the one being used. The IdP should change them so they match.
1. If PKIX(CN matching with a signed root) is being used, the CN of the certificate used to sign the message is not the same as the CN expected by the KeyName of that provider's metadata.
1. The IdP is using the wrong entityID and mistakenly trying to spoof another IdP.
