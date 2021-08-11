### Resources:
- [Spring and Sockets](https://spring.io/guides/gs/messaging-stomp-websocket/)
### Using WebSocket to build an interactive web application
- **WebSocket:** is a computer communications protocol, providing full-duplex communication channels over a single TCP connection. The WebSocket protocol was standardized by the IETF as RFC 6455 in 2011, and the WebSocket API in Web IDL is being standardized by the W3C. WebSocket is distinct from HTTP.
- Simple (or Streaming) Text Oriented Message Protocol (STOMP), formerly known as TTMP, is a simple text-based protocol, designed for working with message-oriented middleware (MOM). It provides an interoperable wire format that allows STOMP clients to talk with any message broker supporting the protocol.
- work steps : 
     - step : create spring application using Spring Initializr including adding the following dependency.
                implementation 'org.webjars:webjars-locator-core'
                implementation 'org.webjars:sockjs-client:1.0.2'
                implementation 'org.webjars:stomp-websocket:2.3.3'
                implementation 'org.webjars:bootstrap:3.3.7'
                implementation 'org.webjars:jquery:3.1.1-1'
     - step2: Create a Resource Representation Class: create two modles(classes) to handle the messages (json formate) as shown below:
                  - first model 
                   public class HelloMessage {
            
              private String name;
            
              public HelloMessage() {
              }
            
              public HelloMessage(String name) {
              this.name = name;
              }
            
              public String getName() {
              return name;
              }
            - second model
              public void setName(String name) {
              this.name = name;
              }
              }
    
                package com.example.messagingstompwebsocket;

                public class Greeting {
                
                private String content;
                
                public Greeting() {
                }
                
                public Greeting(String content) {
                this.content = content;
                }
                
                public String getContent() {
                return content;
                }
                
     - step3: Create a Message-handling Controller as shown below:
               @Controller
               public class GreetingController {
                
                @MessageMapping("/hello")
                @SendTo("/topic/greetings")
                public Greeting greeting(HelloMessage message) throws Exception {
                Thread.sleep(1000); // simulated delay
                return new Greeting("Hello, " + HtmlUtils.htmlEscape(message.getName()) + "!");
                }                
                }

     - step4: Configure Spring for STOMP messaging:this is by create a class (name it WebSocketConfig) that implement WebSocketMessageBrokerConfigurer interface and then override configureMessageBroker and registerStompEndpoints methods as shown below:
               @Configuration
               @EnableWebSocketMessageBroker
               public class WebSocketConfig implements WebSocketMessageBrokerConfigurer {

              @Override
              public void configureMessageBroker(MessageBrokerRegistry config) {
              config.enableSimpleBroker("/topic");
              config.setApplicationDestinationPrefixes("/app");
              }
            
              @Override
              public void registerStompEndpoints(StompEndpointRegistry registry) {
              registry.addEndpoint("/gs-guide-websocket").withSockJS();
              }

            }   
    
     - Create a Browser Client: Create an index.html file (check the resource); this HTML file imports the SockJS and STOMP javascript libraries that will be used to communicate with our server through STOMP over websocket. We also import app.js, which contains the logic of our client application.
