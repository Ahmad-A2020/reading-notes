#### [lab](https://github.com/Ahmad-A2020/horned-animals):
![lab14](/Code-301/screenShot/lab14-1.PNG)

### What is OAuth
- What is OAuth?
- **Answer:** is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential.
- Give an example of what using OAuth would look like.
- **Answer:**The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon.
- How does OAuth work? What are the steps that it takes to authenticate the user?
  - The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
  - The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
  - The first site gives this token and secret to the initiating user’s client software.
  - The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
    - If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
      - The user approves (or their software silently approves) a particular transaction type at the first website.
    - The user is given an approved access token (notice it’s no longer a request token).
    - The user gives the approved access token to the first website.
      - The first website gives the access token to the second website as proof of authentication on behalf of the user.
      - The second website lets the first website access their site on behalf of the user.


- What is OpenID?
- **Answer:**OpenID allows you to create a single login account that you can use for a variety of websites that work in conjunction

### Authorization and Authentication flows
What is the difference between authorization and authentication?
- **Answer:**Authentication and authorization might sound similar, but they are distinct security processes in the world of identity and access management (IAM).
  Authentication confirms that users are who they say they are. Authorization gives those users permission to access a resource.
- What is Authorization Code Flow?
- **Answer:**Authorization code flow is used to obtain an access token to authorize API requests. Access tokens, obtained using authorization code flow, provide permissions for your application to manipulate documents and other resources on behalf of a Mendeley user and make requests for all API resources
- What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
- **Answer:** The Authorization Code Flow + PKCE is an OpenId Connect flow specifically designed to authenticate native or mobile application users.
- What is Implicit Flow with Form Post?
- **Answer:**an alternative to the Authorization Code Flow, OAuth 2.0 provides the Implicit Flow, which is intended for Public Clients, or applications which are unable to securely store Client Secrets
- What is Client Credentials Flow?
- **Answer:**The Client Credentials flow is a server to server flow. There is no user authentication involved in the process.
- What is Device Authorization Flow?
- **Answer:**is an OAuth 2.0 extension that enables devices with no browser or limited input capability to obtain an access token.
- What is Resource Owner Password Flow?
- **Answer:**The Resource Owner Password Credentials flow allows exchanging the username and password of a user for an access token and, optionally, a refresh token. 