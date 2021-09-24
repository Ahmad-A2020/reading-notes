#### Resources:
- [Spring Security overview](https://spring.io/guides/topicals/spring-security-architecture/)
- [Spring Auth cheat sheet](https://github.com/codefellows/seattle-java-401d2/blob/master/SpringAuthCheatSheet.md)

#### [lab](https://github.com/Ahmad-A2020/songr):
![lab16](/Code-401/ScreenShot/lab16-1.PNG)
![lab16](/Code-401/ScreenShot/lab16-2.PNG)
![lab16](/Code-401/ScreenShot/lab16-3.PNG)
![lab16](/Code-401/ScreenShot/lab16-4.PNG)
![lab16](/Code-401/ScreenShot/lab16-5.PNG)


#### [Spring Security overview](https://spring.io/guides/topicals/spring-security-architecture/)
- **Authentication** is the act of proving an assertion, such as the identity of a computer system user. In contrast with identification, the act of indicating a person or thing's identity, authentication is the process of verifying that identity.
    - The main strategy interface for authentication is AuthenticationManager, which has only one method:

                 public interface AuthenticationManager {
                
                Authentication authenticate(Authentication authentication)
                throws AuthenticationException;
                }
    - Spring Security allows you to set up the authentication manager;the following example shows an application that configures the global (parent) AuthenticationManager:
                @Configuration
                public class ApplicationSecurity extends WebSecurityConfigurerAdapter {
                
                
                    @Autowired
                    public void initialize(AuthenticationManagerBuilder builder, DataSource dataSource) {
                    builder.jdbcAuthentication().dataSource(dataSource).withUser("dave")
                    .password("secret").roles("USER");
                    }
                
                }
- **Authorization** is the function of specifying access rights/privileges to resources, which is related to general information security and computer security, and to access control in particular.
  Once authentication is successful, we can move on to authorization, and the core strategy here is AccessDecisionManager
   - **Web Security**: Spring Security in the web tier (for UIs and HTTP back ends) is based on Servlet Filters. Spring Security is installed as a single Filter in the chain, and its concrete type is FilterChainProxy, and  the security filter is a @Bean in the ApplicationContext, and it is installed by default so that it is applied to every request. 
  -createing and Customizing Filter Chains: The default fallback filter chain in a Spring Boot application (the one with the /** request matcher) has a predefined order of SecurityProperties.BASIC_AUTH_ORDER. You can switch it off completely by setting security.basic.enabled=false, or you can use it as a fallback and define other rules with a lower order. To do the latter, add a @Bean of type WebSecurityConfigurerAdapter (or WebSecurityConfigurer) and decorate the class with @Order, as follows:
     ```
     @Configuration
     @Order(SecurityProperties.BASIC_AUTH_ORDER - 10)
     public class ApplicationConfigurerAdapter extends WebSecurityConfigurerAdapter {
     @Override
     protected void configure(HttpSecurity http) throws Exception {
     http.antMatcher("/match1/**")
     ;
     }
     }
     
     ```
     


#### [Spring Auth cheat sheet](https://github.com/codefellows/seattle-java-401d2/blob/master/SpringAuthCheatSheet.md: 
the following is a summarize steps for auth: 
- Step 1: set up a user model and repo
- Step 2: create a controller for that model
- Step 3: UserDetailsServiceImpl implements UserDetailsService
- Step 4: ApplicationUser implements UserDetails
-Step 5: WebSecurityConfig extends WebSecurityConfigurerAdapter
- Step 6: registration page
- Step 7: login page

