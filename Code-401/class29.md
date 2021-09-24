### Resources:
- [Overview: Saving data with Room](https://developer.android.com/training/data-storage/room)
-[Defining entities in Room](https://developer.android.com/training/data-storage/room/defining-data)
-[Related entities in Room](https://developer.android.com/training/data-storage/room/relationships)
-[Accessing data with Room](https://developer.android.com/training/data-storage/room/accessing-data#java)

#### [lab](https://github.com/Ahmad-A2020/taskmaster):
![lab29](/Code-401/ScreenShot/lab29-1.PNG)
![lab29](/Code-401/ScreenShot/lab29-2.PNG)

#### Overview: Saving data with Room:
with Room Library, you can save data in database (SQL lite). in particularly Room provides the following benefits:
- Compile-time verification of SQL queries.
- Convenience annotations that minimize repetitive and error-prone boilerplate code.
- Streamlined database migration paths.

To use Room we will follow the following steps:
- add the required dependence.
-Primary components:  There are three major components in Room:
       - The database class that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
       - Data entities that represent tables in your app's database.
       - Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.

#### Defining entities in Room:
You define each Room entity as a class that is annotated with @Entity. A Room entity includes fields for each column in the corresponding table in the database, including one or more columns that comprise the primary key.
As for the primary code, Each Room entity must define a primary key that uniquely identifies each row in the corresponding database table. The most straightforward way of doing this is to annotate a single column with @PrimaryKey.

#### Related entities in Room
- Define one-to-one relationships: A one-to-one relationship between two entities is a relationship where each instance of the parent entity corresponds to exactly one instance of the child entity, and vice-versa.
        - First, create a class for each of your two entities. One of the entities must include a variable that is a reference to the primary key of the other entity.
        -  create a new data class where each instance holds an instance of the parent entity and the corresponding instance of the child entity.
        -  Add the @Relation annotation to the instance of the child entity, with parentColumn set to the name of the primary key column of the parent entity and entityColumn set to the name of the column of the child entity that references the parent entity's primary key.
- Define one-to-many relationships: A one-to-many relationship between two entities is a relationship where each instance of the parent entity corresponds to zero or more instances of the child entity, but each instance of the child entity can only correspond to exactly one instance of the parent entity.
        - First, create a class for each of your two entities.
        - create a new data class where each instance holds an instance of the parent entity and a list of all corresponding child entity instances.
        - Add the @Relation annotation to the instance of the child entity, with parentColumn set to the name of the primary key column of the parent entity and entityColumn set to the name of the column of the child entity that references the parent entity's primary key.
        - Finally, add a method to the DAO class that returns all instances of the data class that pairs the parent entity and the child entity.
- Define many-to-many relationships: A many-to-many relationship between two entities is a relationship where each instance of the parent entity corresponds to zero or more instances of the child entity, and vice-versa.


#### Accessing data with Room
