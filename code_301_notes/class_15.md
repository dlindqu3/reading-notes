# Code 301 Reading Notes 
### 15. Read: 15 - Authentication 

####  source: Roger A. Grimes, "What is OAuth? How the Open Authorization Framework Works" [link](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

1. OAuth is an example of secure, third-party, user-agent, delegated authorization. 
2. Example - use your gmail to login to another website, like netflix. 
3. steps: 
- first website connects to second and provides user's verified identity 
- second site generates a token and secret
- first site gives these to client
- client's software provides the token and secret for their authorization provider
- authentication and approval of transaction 
- user is given an approved access token 
- user gives the approved access token to the first website 
- the first website gives the approved access token to the second website 
- the second website lets the first website access the second on behalf of the user
- the user sees a transaction occur 
4. OpenID is a authentication software, a recent iteration is bundled in as an authentication step in OAuth  

#### source: "Authentication and Authorization Flows" [link](https://auth0.com/docs/get-started/authentication-and-authorization-flow)

1. authentication determines who the user is, authorization determines what they will have access to. 
2. the authorization code flow exchanges an authorization code for a token. 
3. PKCEs reduce the risks of public clients. 
4. Implicit Flow with Form Post is an option that can replace authorization code flow for public clients or clients that can't store client secrets. 
5.  client credentials flow provides authorization between B2B client-software interfaces. 
6. Device authorization flow provides authorization after a user clicks a link. 
7. resource owner password flow handles sign-in with a password and username, and is not recommended. 

## Things I want to learn more about: 
- steps to set up software for OAuth
 