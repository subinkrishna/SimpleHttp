# simple-http
A simple basic HTTP library 

> Note: 
> This is an experimental library, supports only GET & POST. I am not actively working in this repository.

**Usage**
```java
String resposeAsString = Http.get("http://www.bing.com/search")
                  .query(Pair.of("q", "apple"))
                  .userAgent("MyFancyUserAgent") // Custom User-Agent
                  .verbose() // Prints log
                  .noRedirect() // No auto-redirections on 3xx
                  .asString();
```

```java
ResponseType response = Http.get("http://www.mywebsite.com/search")
                  .query(Pair.of("p1", "v1"), Pair.of("p2", "v2")
                  .map(JsonMapper.forType(ResponseType.class)); // Response mapping
```
