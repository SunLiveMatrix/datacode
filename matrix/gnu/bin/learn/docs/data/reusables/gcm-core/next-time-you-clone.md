The next time you clone an HTTPS URL that requires authentication, Git will prompt you to log in using a browser window. You may first be asked to authorize an {% data variables.product.prodname_oauth_app %}.{% ifversion not ghae %} If your account or organization requires [two-factor auth](/authentication/securing-your-account-with-two-factor-authentication-2fa), you'll also need to complete the 2FA challenge.{% endif %}