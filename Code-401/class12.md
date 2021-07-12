### [Baeldung: Spring Request Mapping](https://www.baeldung.com/spring-requestmapping)
- RequestMapping — by Path: the HTTP request, and a header for the request can be specifying as shown in the example below.
  
  `@RequestMapping(value = "/ex/foos",headers = "key=val", method = GET)`
  `@ResponseBody`
  `public String postFoos() {`
  `return "Post some Foos";`
  `}`
- We can map a request based on its Accept header via the @RequestMapping headers attribute that add as parameter of the RequestMapping. 
  `headers = "Accept=application/json"`.
-  RequestMapping With Path Variables: the below example explain use of the path variable
   `@RequestMapping(value = "/ex/foos/{id}", method = GET)`
   `@ResponseBody`
   `public String getFoosBySimplePathWithPathVariable(`
   `@PathVariable("id") long id) {`
   `return "Get a specific Foo with id=" + id;`
   `}`
- RequestMapping With Request Parameters: the below example explain using of the request params
  `@RequestMapping(value = "/ex/bars", method = GET)`
  `@ResponseBody`
  `public String getBarBySimplePathWithRequestParam(`
  `@RequestParam("id") long id) {`
  `return "Get a specific Bar with id=" + id;`
  `}`

  
###  [Spring guide: Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
- create new spring project using Spring Initializr.
- Define a Simple Entity
- Create Simple Queries: Spring Data JPA focuses on using JPA to store data in a relational database. Its most compelling feature is the ability to create repository implementations automatically, at runtime, from a repository interface.
- Create an Application Class: Spring Initializr creates a simple class for the application.
- Build an executable JAR: You can run the application from the command line with Gradle or Maven. You can also build a single executable JAR file that contains all the necessary dependencies, classes, and resources and run that. Building an executable jar makes it easy to ship, version, and deploy the service as an application throughout the development lifecycle


### [Baeldung: Comparing repositories](https://www.baeldung.com/spring-data-repositories)