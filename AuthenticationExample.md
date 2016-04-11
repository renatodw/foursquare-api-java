### Introduction ###

Some operation require that user has been authenticated with the Foursquare. Foursquare uses OAuth 2.0 to do that.

_**Note** that you can save OAuthToken in database for the user and do not need to request it every time user accesses Foursquare._

### API credentials ###

In order to use FoursquareApi you need API credentials. You can get these credentials by registering your client to Foursquare at https://foursquare.com/oauth/.

### Code example ###

```

public class AuthenticationExample {
  
  public void authenticationRequest(HttpServletRequest request, HttpServletResponse response) {
    FoursquareApi foursquareApi = new FoursquareApi("Client ID", "Client Secret", "Callback URL");
    try {
      // First we need to redirect our user to authentication page. 
      response.sendRedirect(foursquareApi.getAuthenticationUrl());
    } catch (IOException e) {
      // TODO: Error handling
    }
  }
  
  public void handleCallback(HttpServletRequest request, HttpServletResponse response) {
    // After user has logged in and confirmed that our program may access user's Foursquare account
    // Foursquare redirects user back to callback url. 
    FoursquareApi foursquareApi = new FoursquareApi("Client ID", "Client Secret", "Callback URL");
    // Callback url contains authorization code 
    String code = request.getParameter("code");
    try {
      // finally we need to authenticate that authorization code 
      foursquareApi.authenticateCode(code);
      // ... and voilà we have a authenticated Foursquare client
    } catch (FoursquareApiException e) {
     // TODO: Error handling
    }
  }
  
}

```