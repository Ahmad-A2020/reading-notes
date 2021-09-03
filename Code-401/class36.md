### REsources: 
- [Amplify and Cognito](https://docs.amplify.aws/lib/auth/getting-started/)
### Amplify and Cognito
- introduction :  The Amplify Auth category provides an interface for authenticating a user. Behind the scenes, it provides the necessary authorization to the other Amplify categories.
  - work steps: 
  - To start provisioning auth resources in the backend, go to your project directory and execute the command: `amplify add auth`
   -  push your changes to the cloud, execute the command: `amplify push` 
   -  Install Amplify Libraries Add the following dependency to your app's build.gradle
                           dependencies {
                           implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
                            }
   - Add the Auth plugin before calling Amplify.configure
   - Register a user:  The default CLI flow as mentioned in the getting started guide requires a username, password and a valid email id as parameters to register a user. Invoke the following api to initiate a sign up flow.

                      AuthSignUpOptions options = AuthSignUpOptions.builder()
                      .userAttribute(AuthUserAttributeKey.email(), "my@email.com")
                      .build();
                       Amplify.Auth.signUp("username", "Password123", options,
                       result -> Log.i("AuthQuickStart", "Result: " + result.toString()),
                      error -> Log.e("AuthQuickStart", "Sign up failed", error)
                      );AuthSignUpOptions options = AuthSignUpOptions.builder()
                       .userAttribute(AuthUserAttributeKey.email(), "my@email.com")
                        .build();
                      Amplify.Auth.signUp("username", "Password123", options,
                      result -> Log.i("AuthQuickStart", "Result: " + result.toString()),
                       error -> Log.e("AuthQuickStart", "Sign up failed", error)
                          );
  
   - confirm the user:The next step in the sign up flow is to confirm the user. flow by calling the following method:
  
  
                      Amplify.Auth.confirmSignUp(
                      "username",
                     "the code you received via email",
                     result -> Log.i("AuthQuickstart", result.isSignUpComplete() ? "Confirm signUp succeeded" : "Confirm sign up not complete"),
                     error -> Log.e("AuthQuickstart", error.toString())
                       );
   
  
   - Login:  flow by calling the following method:

                     Amplify.Auth.signIn(
                    "username",
                     "password",
                     result -> Log.i("AuthQuickstart", result.isSignInComplete() ? "Sign in succeeded" : "Sign in not complete"),
                       error -> Log.e("AuthQuickstart", error.toString())
                     );