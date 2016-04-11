# Introduction #

_Foursquare V2 API for Java_ is still heavily under development so it contains bugs. To make library better you should do a bug report about all the bugs you encounter.

When reporting bugs you can do few things to help me fix problem quicker and better. For example you may want to submit a patch or even create a unit test to replicate problem. Other things you may consider attaching to report are stack traces and json request data that caused the problem.

The bare minimum is a detailed description of the problem because otherwise i have no way to determine what the problem is.

# Details #

## Awesome bug report ##

_Contains:_

  * Detailed description of the problem
  * Suggestion for a fix
  * If problem is related to some of the end points, attached json data of the problematic request
  * Unit test that confirms problem and/or fix

_**Example of a Awesome bug report:**_

venuesSearch method crashes in FoursquareApi class when using unicode characters in query. For example:

```
  foursquareApi.venuesSearch("30,30", null, null, null, "テスト", null, null);
```

_Attachments:_
  * venuesearch.patch
  * unittest.java
  * venuesearch.json

## Good bug report ##

  * Detailed description of the problem
  * Suggestion for a fix

_**Example of a Good bug report:**_

venuesSearch in FoursquareApi class fails when using unicode characters in query.

Error seems to be in doApiRequest method where values are added to url without encoding.

This could be fixed by changing line 386 from
```
urlBuilder.append(value.toString());
```
to
```
urlBuilder.append(URLEncoder.encode(value.toString(),"UTF-8"));
```

## Bug report ##

_Contains_
  * detailed description of the problem

_**Example of a bug report:**_

venuesSearch in FoursquareApi class fails when using unicode characters in query.

## Invalid bug report ##

_Contains:_
  * Does not contain a detailed description of the problem

_**Example of a Invalid bug report:**_

Does not work !!11 plz fix ASAP!