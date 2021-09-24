### Resources:
- [Review: High-level HTTP](https://dev.to/dangolant/things-i-brushed-up-on-this-week-the-http-request-lifecycle-)
- [Java HTTP Request example](https://www.baeldung.com/java-http-request)

#### [lab](https://github.com/Ahmad-A2020/quotes):
![lab9](\Code-401\ScreenShot\lab9-1.PNG)
![lab9](\Code-401\ScreenShot\lab9-2.PNG)

### Review: High-level HTTP
HTTP request lifecycle
- Step 1: Local Processing
- Step 2: Resolve an IP:   Like the processing done locally, resolving an IP from a "DNS server"2 is a sequence that includes many steps, and includes failovers if the first request fails to return an address.
- Step 3: Establish a TCP Connection
- Step 4: Send an HTTP Request
- Step 5: Tearing Down and Cleaning Up

### Java HTTP Request example
- Java class HttpUrlConnection is used to performing HTTP requests in Java.
- starting from JDK 11 Java offer HttpClient API is
- to create requests, we will create HttpUrlConnection instance using the openConnection() method of the URL class as follows:
`URL url = new URL("http://example.com");`
`HttpURLConnection con = (HttpURLConnection) url.openConnection();`
`con.setRequestMethod("GET");`
-  to add parameters to a request, we have to set the doOutput property to true, then write a String of the form param1=value¶m2=value to the OutputStream of the HttpUrlConnection instance
- Adding headers to a request can be achieved by using the setRequestProperty() method:
`con.setRequestProperty("Content-Type", "application/json");`
- To read the value of a header from a connection, we can use the getHeaderField() method:
`String contentType = con.getHeaderField("Content-Type");`
- To set the timeout values(These values define the interval of time to wait for the connection to the server to be established or data to be available for reading.), we can use the setConnectTimeout() and setReadTimeout() methods:
`con.setConnectTimeout(5000);`
`
- to read the cookies from a response, we can retrieve the value of the Set-Cookie header and parse it to a list of HttpCookie objects:
`String cookiesHeader = con.getHeaderField("Set-Cookie");`
`List<HttpCookie> cookies = HttpCookie.parse(cookiesHeader);`
Next, we will add the cookies to the cookie store:
`cookies.forEach(cookie -> cookieManager.getCookieStore().add(null, cookie));`
-  to enable or disable automatically following redirects for a specific connection, we  usie the setInstanceFollowRedirects() method:
`con.setInstanceFollowRedirects(false);`
- Reading the response of the request can be done by parsing the InputStream of the HttpUrlConnection instance.



