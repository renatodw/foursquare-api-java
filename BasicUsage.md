### Introduction ###

This example describes how to do a basic query to Foursquare.

_**Note** that some operations need user to be authenticated with the Foursquare. More from that subject in [AuthenticationExample](AuthenticationExample.md) page_

### Code example ###

```
  public void searchVenues(String ll) throws FoursquareApiException {
    // First we need a initialize FoursquareApi. 
    FoursquareApi foursquareApi = new FoursquareApi("Client ID", "Client Secret", "Callback URL");
    
    // After client has been initialized we can make queries.
    Result<VenuesSearchResult> result = foursquareApi.venuesSearch(ll, null, null, null, null, null, null, null, null, null, null);
    
    if (result.getMeta().getCode() == 200) {
      // if query was ok we can finally we do something with the data
      for (CompactVenue venue : result.getResult().getVenues()) {
        // TODO: Do something we the data
        System.out.println(venue.getName());
      }
    } else {
      // TODO: Proper error handling
      System.out.println("Error occured: ");
      System.out.println("  code: " + result.getMeta().getCode());
      System.out.println("  type: " + result.getMeta().getErrorType());
      System.out.println("  detail: " + result.getMeta().getErrorDetail()); 
    }
  }
```