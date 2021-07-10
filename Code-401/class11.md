
### Spring App Basics:
- First step: use the Spring Initializr to generate a new project with the required dependencies (Spring Web, Thymeleaf, and Spring Boot DevTools).
- Second step: Create a Web Controller as shown below: 
    - HTTP requests are handled by a controller. You can easily identify the controller by the @Controller annotation.
    - The `@GetMapping` annotation ensures that HTTP GET requests to certain link (in this case /greeting) are mapped to the required method( in this case greeting() method).
    - `@RequestParam` binds the value of the query string parameter name into the name parameter of the greeting() method.
    - After that the implementation of the method body relies on a view technology (in this case, Thymeleaf) to perform server-side rendering of the HTML.
`@SpringBootApplication`
  `public class ServingWebContentApplication {`

  `public static void main(String[] args) {`
  `SpringApplication.run(ServingWebContentApplication.class, args);`
  `}`

`}`

-  Third step: Spring Boot Devtools: it is module aim at try and improve the development time while working with the Spring Boot application.

- Fourth step: Run the Application
the following class is crated by the Spring Initializr 
`@Controller`
`public class GreetingController {`

	`@GetMapping("/greeting")`
	`public String greeting(@RequestParam(name="name", required=false, defaultValue="World") String name, Model model) {`
		`model.addAttribute("name", name);`
		`return "greeting";`
	`}`

`}`
- Fifth step: Build an executable JAR: to run the application we can use two methods: 
   -  using command line with Gradle. `./gradlew bootRun`
   - build a single executable JAR file that contains all the necessary dependencies, classes, and resources and run that.  you can build the JAR file by using `./gradlew build` and then run the JAR file, as follows:
     `java -jar build/libs/gs-serving-web-content-0.1.0.jar`
`

- six step: Add home page: you can add the static resources including HTML and JavaScript and CSS inside the rood ./static. for the home page (welcom), spring automatically will take the index.html file(  src/main/resources/static/index.html).
  
### Spring MVC and Thymeleaf: 
- Spring model attributes: Spring MVC calls the pieces of data that can be accessed during the execution of views model attributes. The equivalent term in Thymeleaf language is context variables
-  Request parameters: it can be easily accessed in Thymeleaf views such as access the q parameter as follows  `<p th:text="${param.q}">Test</p>`
-  
