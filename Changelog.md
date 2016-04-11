Version 1.0.2
  * Moved source to trunk in svn
  * Added support for search venue by name of a place

Version 1.0.1

  * Moved the source for the java code, gae code and tests to the correct maven format (src/main/java, src/main/test)
  * Updated unit tests to read the test data files from the classpath
  * moved tests/gae code under main repo

TODO:
  * fix the svn format. Right now the main code is not under trunk :(


Version 1.0.0-RC2

  * Changed default version into 20110615
  * Changed venuesSearch method to return VenuesSearchResult instead of VenueGroup array

Version 1.0.0-RC1

  * Added missing Javadocs
  * Minor code cleanup

Version 0.6.0

  * Support for tips/unmark endpoint ([Issue #47](https://code.google.com/p/foursquare-api-java/issues/detail?id=#47))
  * Support for tips/markdone endpoint ([Issue #46](https://code.google.com/p/foursquare-api-java/issues/detail?id=#46))
  * Support for venues/photos endpoint ([Issue #40](https://code.google.com/p/foursquare-api-java/issues/detail?id=#40))
  * Support for venues/marktodo endpoint ([Issue #42](https://code.google.com/p/foursquare-api-java/issues/detail?id=#42))
  * Support for venues/tips endpoint ([Issue #39](https://code.google.com/p/foursquare-api-java/issues/detail?id=#39))
  * Support for photos/add endpoint ([Issue #20](https://code.google.com/p/foursquare-api-java/issues/detail?id=#20))
  * Support for tips/search endpoint ([Issue #18](https://code.google.com/p/foursquare-api-java/issues/detail?id=#18))
  * Support for checkins/deletecomment endpoint ([Issue #15](https://code.google.com/p/foursquare-api-java/issues/detail?id=#15))
  * Support for checkins/addcomment endpoint ([Issue #14](https://code.google.com/p/foursquare-api-java/issues/detail?id=#14))
  * Added experimental parameters (categoryId, url, providerId and linkedId) into venues/search endpoint handler
  * Added photourl property into CompactTip entity
  * Added fetchDataMultipartMime method to IOHandler interface. Method is used for sending multipart data along with api request
  * Added MultipartParameter class to represent multipart parameters

Version 0.5.0

  * Support for users/setpings endpoint ([Issue #36](https://code.google.com/p/foursquare-api-java/issues/detail?id=#36))
  * Support for users/todos endpoint ([Issue #30](https://code.google.com/p/foursquare-api-java/issues/detail?id=#30))
  * Support for users/venuehistory endpoint ( [Issue #31](https://code.google.com/p/foursquare-api-java/issues/detail?id=#31) )
  * Support for users/tips endpoint ([Issue #29](https://code.google.com/p/foursquare-api-java/issues/detail?id=#29))
  * Support for users/badges endpoint ([Issue #27](https://code.google.com/p/foursquare-api-java/issues/detail?id=#27))
  * Support for users/leaderboard endpoint ([Issue #26](https://code.google.com/p/foursquare-api-java/issues/detail?id=#26))
  * Support for tips/marktodo endpoint ([Issue #25](https://code.google.com/p/foursquare-api-java/issues/detail?id=#25))
  * Support for tips/add endpoint ([Issue #17](https://code.google.com/p/foursquare-api-java/issues/detail?id=#17))
  * Renamed Todos entity into TodoGroup
  * Changed TodoGroup to inherit from Group
  * Changed Todo entity's tip property from String to CompleteTip
  * Changed unlocks property from Checkin array to BadgeUnlock array in Badge entity
  * Added isMayor property to Checkin entity
  * Added hint property to Badge entity
  * Moved todo and done properties from CompactTip to CompleteTip
  * Changed TipNotification, TipAlertNotification, Photo, Recommendation and TipGroup to use CompleteTip instead of CompactTip
  * Added VenueHistory and VenueHistoryGroup entities
  * Added Badges, BadgeSet, BadgeSets and BadgeUnlock entities
  * Added LeaderboaderItemGroup entity

Version 0.4.0

  * Implementation for all api calls involved in Foursquare Venues Project ([Issue #52](https://code.google.com/p/foursquare-api-java/issues/detail?id=#52))
  * Added UserGroups entity
  * Added Link, LinkProvider and LinkGroup entities
  * Added Keyword, KeywordGroup, Reason, ReasonGroup, Recommendation, RecommendationGroup, Warning and Recommended entities
  * Merged FriendGroup entity into UserGroup entity
  * Merged FriendGroups entity into UserGroups entity
  * Added venue property into Photo entity
  * Added type property to UserGroup
  * Changed CompactTip entity's todo and done fields from UserGroup to UserGroups
  * Support for venues/flag endpoint ([Issue #43](https://code.google.com/p/foursquare-api-java/issues/detail?id=#43))
  * Support for venues/links endpoint ([Issue #41](https://code.google.com/p/foursquare-api-java/issues/detail?id=#41))
  * Support for venues/herenow endpoint ([Issue #38](https://code.google.com/p/foursquare-api-java/issues/detail?id=#38))
  * Support for venues/explore endpoint ([Issue #37](https://code.google.com/p/foursquare-api-java/issues/detail?id=#37))
  * Support for photos/ID endpoint ([Issue #19](https://code.google.com/p/foursquare-api-java/issues/detail?id=#19))
  * Support for tips/ID endpoint ([Issue #16](https://code.google.com/p/foursquare-api-java/issues/detail?id=#16))
  * Support for venues/proposeedit end-point ([Issue #44](https://code.google.com/p/foursquare-api-java/issues/detail?id=#44))

Version 0.3.0

  * Refactored all API calls to return Result objects ([Issue #48](https://code.google.com/p/foursquare-api-java/issues/detail?id=#48) and [Issue #49](https://code.google.com/p/foursquare-api-java/issues/detail?id=#49))
  * Added support for Notifications ([Issue #48](https://code.google.com/p/foursquare-api-java/issues/detail?id=#48))
  * Added classes for Badge, Leaderboard, Mayorship, Message, Score, Tip and TipAlert notification types ([Issue #48](https://code.google.com/p/foursquare-api-java/issues/detail?id=#48))
  * Changed API requests to return more detailed information about failures in ResultMeta object ([Issue #49](https://code.google.com/p/foursquare-api-java/issues/detail?id=#49))
  * Changed API requests to return null results instead of crashing ([Issue #49](https://code.google.com/p/foursquare-api-java/issues/detail?id=#49))
  * Removed IOException throwing from IOHandler ([Issue #49](https://code.google.com/p/foursquare-api-java/issues/detail?id=#49))
  * Added support for using JSON callback syntax in API requests ([Issue #49](https://code.google.com/p/foursquare-api-java/issues/detail?id=#49))
  * Added support for passing version parameter
  * Renamed CompleteTodos entity into Todos
  * Moved tips and todos from CompleteVenue to CompactVenue
  * Added Badge, BadgeImage, LeaderBoardItem and LeaderboardScore entities
  * Changed usersCheckins method's userId parameter to default to self
  * Fixed bug in venuesAdd method that prevented method from working (threw class cast exception)
  * Fixed bug in usersRequests method that prevented it from working (wrong field name in result parsing)
  * Deprecated Google App Engine support library because DefaultIOHandler seems to work fine with GAE nowadays

Version 0.2.0

  * Support for specials/ID endpoint ([Issue #23](https://code.google.com/p/foursquare-api-java/issues/detail?id=#23))
  * Support for specials/search endpoint ([Issue #24](https://code.google.com/p/foursquare-api-java/issues/detail?id=#24))
  * Support for settings/all endpoint ([Issue #21](https://code.google.com/p/foursquare-api-java/issues/detail?id=#21))
  * Support for settings/set endpoint ([Issue #22](https://code.google.com/p/foursquare-api-java/issues/detail?id=#22))
  * Support for users/checkins endpoint ([Issue #28](https://code.google.com/p/foursquare-api-java/issues/detail?id=#28))
  * Support for checkins/ID endpoint ([Issue #45](https://code.google.com/p/foursquare-api-java/issues/detail?id=#45))
  * Support for checkins/recent endpoint ([Issue #13](https://code.google.com/p/foursquare-api-java/issues/detail?id=#13))
  * Support for users/request endpoint ([Issue #32](https://code.google.com/p/foursquare-api-java/issues/detail?id=#32))
  * Support for users/unfriend endpoint ([Issue #33](https://code.google.com/p/foursquare-api-java/issues/detail?id=#33))
  * Support for users/approve endpoint ([Issue #34](https://code.google.com/p/foursquare-api-java/issues/detail?id=#34))
  * Support for users/deny endpoint ([Issue #35](https://code.google.com/p/foursquare-api-java/issues/detail?id=#35))
  * Added FriendGroup, FriendGroups and Scores entities
  * Added friends, following and scores properties into CompleteUser entity
  * Added name property into Location entity
  * Added Setting entity
  * Added finePrint, icon, title, state, provider and redemption properties into CompleteSpecial entity
  * Added SpecialGroup entity group
  * Added url property into CompacrVenue entity
  * Added pluralName property to Category entity
  * Added unit test project
    * Added unit tests for FoursquareApi / special method
    * Added unit tests for FoursquareApi / specialsSearch FoursquareApi class method
    * Added unit tests for SettingsAll and settingsSet FoursquareApi class methods
    * Added unit tests for checkin, checkinsAdd and checkinsRecent FoursquareApi class methods
    * Added unit tests for user, usersSearch, usersCheckins and usersFriends FoursquareApi class methods
    * Added unit tests for usersRequest, usersApprove, usersDeny and usersUnfriend FoursquareApi class methods
  * Upgraded license from LGPL 2.1 to LGPL 3
  * Fixed bug in JSONFieldParser that prevented entity setter methods from working
  * Fixed bug in usersFriends method that prevented method from working

Version 0.1.6

  * Added Maven repository into version control system
  * Added empty result check to venuesSearch method
  * Increased Google App Engine IOHandler's timeout to 10 sec
  * Fixed [issue #9](https://code.google.com/p/foursquare-api-java/issues/detail?id=#9) Chracter Encoding seems to be a problem for results
  * Fixed [issue #10](https://code.google.com/p/foursquare-api-java/issues/detail?id=#10) Android JSON API doesn't include JSONObject.getName (Thanks to Thom Nichols)
  * Fixed [issue #11](https://code.google.com/p/foursquare-api-java/issues/detail?id=#11) usersSearch: array is called 'results', not 'users' (Thanks to Thom Nichols)
  * Fixed [issue #12](https://code.google.com/p/foursquare-api-java/issues/detail?id=#12) Request parameters should be URL-Encoded (Thanks to Thom Nichols)

Version 0.1.5

  * Added support for Google App Engine
  * Fixed [issue #7](https://code.google.com/p/foursquare-api-java/issues/detail?id=#7) Can't access oAuthToken (Thanks to Thom Nichols)
  * Fixed [issue #8](https://code.google.com/p/foursquare-api-java/issues/detail?id=#8) OAuth authenticateCode: JSONException: no value for response (Thanks to Thom Nichols)

Version 0.1.4

  * New version numbering
  * Maven support
  * Added oAuthToken parameter to FoursquareApi constructor
  * Added setoAuthToken method to FoursquareApi class
  * Support for users/friends endpoint (Thanks to Gutzeit)
  * Added authentication system
  * Changed IOHandler's thrown exception to IOException

Version 0.13 (old version numbering)

  * Changed FoursquareEntity class into interface
  * Changed FoursquareEntity interface to inherit from Serializable
  * Added connection disconnecting to DefaultIOHandler
  * Added non existing field skipping support which defaults to true
  * Added method for setting whatever parser should skip non-exisiting fields
  * Added todo, done and url properties into CompactTip entity
  * Added new UserGroup and CompleteTip entities
  * Added missing FoursquareEntity super class into Comment, CompactTip, Source and Todo classes

Version 0.11 (old version numbering)

  * Moved stats from CompleteVenue to CompactVenue entity
  * Added new Mayor, Photos and Tips entities
  * Changed from Checkin[.md](.md) items to CheckGroup[.md](.md) groups in HereNow entity
  * Changed mayor property from CompactUser to Mayor in CompleteVenue
  * Changed PhotoGroup to Photos entity in CompleteVenue
  * Changed tips property from TipGroup to in Tips in CompleteVenue

Version 0.1 (old version numbering)

  * Initial release
  * Basic functionality
  * Initial entity model
  * Default IO Handler
  * Support for following endpoints
    * users/ID
    * users/search
    * users/requests
    * venues/ID
    * venues/add
    * venues/categories
    * venues/search
    * venues/trending
    * checkins/add