
# How to set-up Single Sign On (SSO)

## Key terminology

1. **Identity Provider (IdP)** - this is the your responsibility.  Your IdP is where you create, maintain, and manage identity information for users while providing authentication services to relying applications within a federation or distributed network. Identity Providers offer user authentication as a service.
2. **Service Provider (SP)** - this is the responsibility of Digital Theatre+.  As a Service Provider, Digital Theatre+ do not authenticate users but instead request authentication decisions from your Identity Provider. As a Service Providers, Digital Theatre+ relies on Identity Providers to assert the identity of a user.
3. **SAML** - Security Assertion Markup Language (SAML) is an open standard that allows Identity Providers (IdP) to pass authorisation credentials to Service Providers (SP).
4. **SSO** - SAML enables Single-Sign On (SSO), a term that means users can log in once, and those same credentials can be reused to log into other service providers.

## Supported Identity Providers and SAML versions

1. You may use any Identity Provider which is compliant with SAML 2.0 and provides a publically accessible Identity Provider XML metadata URL.
2. Digital Theatre+ use Shibboleth as a Service Provider, which does not support SAML 1.1.
3. Digital Theatre+ supports the [UK Access Management Federation for Education and Research](https://www.ukfederation.org.uk/) (UK Federation).

## Variance of process

The current process differs depending on whether you are using [UK Access Management Federation for Education and Research](https://www.ukfederation.org.uk/) (UK Federation) or not.

## Non-UK Federation process


### Step 1 - Add the Digital Theatre+ Service Provider to your Identity Provider
You must add our Service Provider metadata to your Identity Provider.  The specific steps to do this will depend on the IdP solution your organisation uses.  Your IT team will be able to do this for you.  The Digital Theatre+ Service Provider metadata is as follows:
```
Service Provider Name: shibboleth
Service Provider Entity ID: https://www.digitaltheatreplus.com
Metadata: https://www.digitaltheatreplus.com/Shibboleth.sso/Metadata
Assertion Consumer Service (ACS) URL: https://www.digitaltheatreplus.com/Shibboleth.sso/SAML2/POST
```
### Step 2 - Provide Digital Theatre+ with the URL to your Identity Provider Metadata XML

You must provide the URL to where you have published your Identity Provider metadata XML to Digital Theatre+.
   1. Please [use this form to send this information to Digital Theatre+](https://forms.gle/Dij9dt8vGMDMoEa59).
   2. If your IT department is unclear how to do this, usually searching on Google for the keywords '[how to publish idp metadata xml](https://www.google.com/search?source=hp&ei=j8hCXr3sGIW4lwTIjpSQDw&q=how+to+publish+idp+metadata+xml&oq=how+to+publish+idp+metadata+xml&gs_l=psy-ab.12...1325.1325..2345...0.0..0.105.193.1j1......0....2j1..gws-wiz.....8..0i362i308i154i357.463wfKe40Ts&ved=0ahUKEwj977jG6MnnAhUF3IUKHUgHBfIQ4dUDCAw)' along with your IdP software provider name will yield detailed instructions.


### Step 3 - Digital Theatre+ will add your Identity Provider to their Service Provider configuration
1. Digital Theatre+ technology team must add the URL to your IdP XML metadata to their SP configuration.  
1. For reference, Digital Theatre+ use Shibboleth as a Service Provider.
1. Digital Theatre+ aim to complete requests made in step 2 above within the same working day.

### Step 4 - Digital Theatre+ will validate that their Service Provider has retrieved your Identity Provider Metadata XML correctly
Digital Theatre+ will validate:
    1. Your IdP has been [added to the Digital Theatre+ SP configuration](https://s3-eu-west-1.amazonaws.com/dtpserverconfiguration/shibboleth2.xml)
    2. Your IdP XML metadata URL is accessible (using a web browser)

### Step 5 - Digital Theatre+ will configure their platform to allow you to select your organisation on the Sign In page
5. The final step must not be completed until **all** of the above have been done.  Digital Theatre+ will add the following to the website management system:
    1. add your organisation name
    2. the URL included in the entityID parameter in your IdP XML metadata
    3. the URL to your published IdP XML metadata
    4. the internal Digital Theatre+ **group** account your users will be authenticated as

Once all five steps above are completed, you and your users will be able to select your organisation from the list of Single Sign On (SSO) providers and authenticate users to access Digital Theatre+.

## UK Federation process

The UK Federation Identity Provider (IdP) has already been configured for use with the Digital Theatre+ Service Provider (SP).  If your organisation uses UK Federation for Single Sign On (SSO):

### Step 1 - Provide Digital Theatre+ with the URL to your Identity Provider Metadata XML
Please [use this form to request Digital Theatre+ set up the Service Provider to authenticate your users](https://forms.gle/Dij9dt8vGMDMoEa59).

### Step 2 - Digital Theatre+ will validate that your organisation appears in UK Federation metadata
Digital Theatre+ will validate that organisation appears in the UK Federation aggregated IdP metadata XML: http://metadata.ukfederation.org.uk/ukfederation-metadata.xml

### Step 3 - Digital Theatre+ will configure their platform to allow you to select your organisation on the Sign In page
1. Digital Theatre+ will add the following to the website management system:
   1. your organisation name
   2. the URL associated with the organisation from the entityID parameter in the [UK Federation IdP XML metadata](http://metadata.ukfederation.org.uk/ukfederation-metadata.xml)
   3. the URL to the [UK Federation IdP XML metadata](http://metadata.ukfederation.org.uk/ukfederation-metadata.xml)
   4. the internal Digital Theatre+ **group** account your users will be authenticated as

Once all two steps above are completed, you and your users will be able to select your organisation from the list of Single Sign On (SSO) providers and authenticate users to access Digital Theatre+.
