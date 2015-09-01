# Two-factor authentication from WiKID #
The WiKID Strong Authentication System is a public key-based two-factor authentication system. It is flexible, extensible, and secure alternative to tokens,certs & passwords. Application support for Java, Windows, PHP, Ruby, Python, SugarCRM, webmail, OpenVPN, LDAP, TACACS+, etc.  Open source token clients include a J2SE client and a Firefox extension (in beta).

The token client encrypts the user's PIN with the WiKID server's public key and sends it to the server along with a one-time use AES key. If the PIN is correct, the account active and the encryption valid, the one-time password is generated (via java random), encrypted by the token client's public key and the AES key and returned.

If the security domain is configured for https mutual authentication, a hash of the valid ssl cert and the URL are also sent with the OTP.  The token client will attempt to fetch the SSL cert from the URL and hash it.  If the hashes match, the URL is presented as valid and the default browser is launched to the valid website.  This prevents MITM attacks against web applications.

## Documentation ##
We have recently published a number of how-tos:

[Add two-factor authentication to Ruby](http://www.wikidsystems.com/documentation/howtos/how-to-add-wikid-two-factor-authentication-to-a-ruby-application/)

[Add two-factor authentication to PHP](http://www.wikidsystems.com/documentation/howtos/how-to-add-wikid-two-factor-authentication-to-a-php-application/)

[How to use Radius for two-factor authentication with Apache](http://www.howtoforge.com/apache_radius_two_factor_authentication)

[How to prevent phishing with mutual authentication](http://www.howtoforge.com/prevent_phishing_with_mutual_authentication)

[Secure SSH with two-factor authentication](http://www.howtoforge.com/secure_ssh_with_wikid_two_factor_authentication)

[How to configure OpenVPN for WiKID](http://www.howtoforge.com/openvpn_wikid_strong_authentication)



