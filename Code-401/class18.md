Resources: 
-[Many to many relationships](https://www.baeldung.com/hibernate-many-to-many)
- [Security: a humorous overview](https://scholar.harvard.edu/files/mickens/files/thisworldofours.pdf)

### Many to many relationships: 
A many-to-many relationship occurs when multiple records in a table are associated with multiple records in another table
- @ManyToMany annotation can be used for specifying this type of relationships in Hibernate.
- a good example illustrate this relation is the employee and project: on which any given employee can be assigned to multiple projects and a project may have multiple employees working for it, leading to a many-to-many association between the two.
- to dreate the modle of Jpa we will add the following at each class (model)

                @Entity
                @Table(name = "Employee")
                public class Employee {
                // ...
                
                    @ManyToMany(cascade = { CascadeType.ALL })
                    @JoinTable(
                        name = "Employee_Project", 
                        joinColumns = { @JoinColumn(name = "employee_id") }, 
                        inverseJoinColumns = { @JoinColumn(name = "project_id") }
                    )
                    Set<Project> projects = new HashSet<>();
                   
                    // standard constructor/getters/setters
                }


                @Entity
                @Table(name = "Project")
                public class Project {    
                // ...
                
                    @ManyToMany(mappedBy = "projects")
                    private Set<Employee> employees = new HashSet<>();
                    
                    // standard constructors/getters/setters   
                }


### Security: a humorous overview
-  writer point is that security people need to get their priorities straight. The “threat model” section of a security paper resembles the script for a telenovela that was written by a paranoid schizophrenic: there are elaborate narratives and grand conspiracy theories, and there are heroes and villains with fantastic (yet oddly constrained) powers that necessitate a grinding battle of emotional and technical attrition. In the real world, threat models are much simpler (see Figure 1). Basically, you’re either dealing with Mossad or not-Mossad. If your adversary is not-Mossad, then you’ll probably be fine if you pick a good password and don’t respond to emails from ChEaPestPAiNPi11s@virus-basket.biz.ru. If your adversary is the Mossad, YOU’RE GONNA DIE AND THERE’S NOTHING THAT YOU CAN DO ABOUT IT. The Mossad is not intimidated by the fact that you employ https://. If the Mossad wants your data, they’re going to use a drone to replace your cellphone with a piece of uranium that’s shaped like a cellphone, and when you die of tumors filled with tumors, they’re going to hold a press conference and say “It wasn’t us” as they wear t-shirts that say “IT WAS DEFINITELY US,” and then they’re going to buy all of your stuff at your estate sale so that they can directly look at the photos of your vacation instead of reading your insipid emails about them. In summary, https:// and two dollars will get you a bus ticket to nowhere. Also, SANTA CLAUS ISN’T REAL. When it rains, it pours.