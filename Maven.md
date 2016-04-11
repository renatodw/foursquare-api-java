# Maven #

If you want to use Maven for dependency management add following repository into your pom.xml:

```
  <repository>
    <id>foursquareapijava</id>
    <name>Foursquare V2 API for Java Repository</name>
    <url>http://foursquare-api-java.googlecode.com/svn/repository</url>
  </repository>
```

And dependency:

```
  <dependency>
    <groupId>fi.foyt</groupId>
    <artifactId>foursquare-api</artifactId>
    <version>VERSION</version>
  </dependency>
```

Optionally if you need Google App Engine support add also following dependency:

```
  <dependency>
    <groupId>fi.foyt</groupId>
    <artifactId>foursquare-api-gae</artifactId>
    <version>VERSION</version>
  </dependency>
```