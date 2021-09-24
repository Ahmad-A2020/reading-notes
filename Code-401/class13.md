
### Resources:
- [Related data in Spring (focus on the relationship annotations, not the curl requests)](https://www.baeldung.com/spring-data-rest-relationships)
- [Integration Testing in Spring](https://www.baeldung.com/integration-testing-in-spring)

#### [lab](https://github.com/Ahmad-A2020/songr):
![lab13](/Code-401/ScreenShot/lab13-1.PNG)

### relations 
- One-to-One Relationship:In a one-to-one relationship, one record in a table is associated with one and only one record in another table. For example, in a school database, each student has only one student ID, and each student ID is assigned to only one person 
  
     - define two entity classes such as Library and Address  and add the relation ( one-to-one relationship) as shown below.
       `@OneToOne`
       `@JoinColumn(name = "secondary_address_id")`
       `@RestResource(path = "libraryAddress", rel="address")`
       `private Address secondaryAddress;`
       
     - create two repository interfaces for each of Entity as shown below:
      `public interface LibraryRepository extends CrudRepository<Library, Long> {}`
      `public interface AddressRepository extends CrudRepository<Address, Long> {}`
     - Creating the Resources  
       `curl -i -X POST -H "Content-Type:application/json"`
       `-d '{"name":"My Library"}' http://localhost:8080/libraries`
    - Creating the Associations
- One-to-Many Relationship: In a one-to-many relationship, one record in a table can be associated with one or more records in another table. For example, each customer can have many sales orders.    
     - To exemplify a one-to-many relationship, let's add a new Book entity that will represent the “many” end of a relationship with the Library entity, then we wil assossiate the two enterty as following: 
          - book class: 
            `@ManyToOne`
            `@JoinColumn(name="library_id")`
            `private Library library;`
          - Library class:
            `@OneToMany(mappedBy = "library")`
            `private List<Book> books;`
- Many-to-Many Relationship: A many-to-many relationship occurs when multiple records in a table are associated with multiple records in another table. For example, a many-to-many relationship exists between customers and products: customers can purchase various products, and products can be purchased by many customers.            
      - To create an example of a many-to-many relationship, let's add a new model class Author that will have a many-to-many relationship with the Book entity:
          
          - Author Class: 
          `@ManyToMany(cascade = CascadeType.ALL)`
          `@JoinTable(name = "book_author",`
          `joinColumns = @JoinColumn(name = "book_id", referencedColumnName = "id"),`
          `inverseJoinColumns = @JoinColumn(name = "author_id",`
          `referencedColumnName = "id"))`
          `private List<Book> books;`
  
          - Book Class: 
          `@ManyToMany(mappedBy = "books")`
          `private List<Author> authors;`
### [Baeldung: Spring Integration Testing](https://www.baeldung.com/integration-testing-in-spring)
