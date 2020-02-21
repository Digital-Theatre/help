
# Authentication options

Digital Theatre+ provides a number of options for you and your organisation to authenticate and gain access to the service.

Note that these options are mutually exclusive, and cannot be used in combination with one another.

## Summary of authentication options

1. **Recommended**: Single Sign On (SSO) using your Identity Provider
2. **Recommended**: Username and Password
3. IP Authentication
4. EZProxy with IP Authentication

## Recommended authentication methods

Use of Single Sign On (SSO) or Username and Password are preferred as both provide:
* the most security to your users
* minimisation of the administrative and support burden to your organisation
* re-assurance that the quality of experience is not diminished by intermediaries

### Single Sign On (SSO) using your Identity Provider (IdP)

1. This allows you to use your existing authentication solution - including UK Federation, OpenAthens, Google or Shibboleth - where you authenticate your users, and provide an assertion to Digital Theatre+ that the user is permitted access
2. The process for setting this up is described in [setting up single sign on](Setting-up-Single-Sign-On-(SSO))

### Username and password

1. Digital Theatre+ can provide a username and password that can be used by one or many individuals. These credentials can be associated with a non-existent email address

## Other options

### IP Authentication

1. This allows you to provide Digital Theatre+ with an IP address or range of IP addresses where requests from your users will originate from
2. Any request from these IP addresses is signed in to your account

The use of IP Authentication infers a responsibility on yourself to
* ensure that the IP address information Digital Theatre+ hold is always up to date
* ensure that the IP addresses provided only allow the business entity under contract access to Digital Theatre+
* ensure the security of those networks and systems behind those IP addresses is well kept

Generally security experts recommend against IP authentication.  IP addresses are losing their grounding in physical locations. As IP address space fills up, access at increasingly uses dynamic IP addresses in local, non-public networks. Cloud access points and VPN tunnels are now common.   With networked mobile devices and increasingly sophisticated security threats, IP-based access cannot be recommended for use.

### EZProxy using IP Authentication

1. This allows your users to make requests through your EZProxy instance, which EZProxy forwards to Digital Theatre+ and then returns the response to your users
2. To use EZProxy, you provide Digital Theatre+ with the IP address of your EZProxy instance, and only that IP Address is permitted access to the service

This is our least preferred option, as our customers experience tell us that:
* Many EZProxy instances are poorly configured
* Customers using EZProxy have many problems arising from using it - performance and degraded user experience being the most noticeable to end users
* Many customers lack the necessary technical expertise, resources or budget to resolve these issues
* Users expect to be able to use websites directly, rather than through an intermediary system.
* EZProxy represents an increasingly attractive target for bad actors to perform 'man-in-the-middle' attacks. A compromised EZProxy server could be a potent attack vector into the systems of every user of a library's resources

Additionally, looking forward web development experts consider:
* The current wave of browser development is focussed on security and privacy; systems that attempt to sit in the middle of transmission between browser and content are going to become more and more difficult to work with
