## Glossary of Terms 
  - data integrity - maintenance, assurance of the accuracy and consistency of, data over its entire life-cycle
  - consistency - data is consistent when it satisfies all integrity constraints
  - data integrity - data is accurate, consistent, and reliable
  - integrity constraints - rules that help ensure the quality of data , e.g. primary key, foreign key, unique, check, not null, etc.
  - concurrent access - multiple users can access the same data at the same time
  - data abstraction - DBMS provides users with a conceptual view of the data, shielding them from the complexities of physical storage.
  - data independence - changes in the physical storage of data do not affect the application program 
  - data redundancy - storing the same data in more than one place
  - entity represents a real-world object
  - attribute represents some property of interest that further describes an entity
  - relationship among two or more entities represents an interaction among the
entities; for example, a works-on relationship between an employee and a project. 
  - database state or snapshot - database at a particular moment in time.

## Notes

- Database is efficient (store, retrive, manupulate, trunscate, delete) whileas file system is not.
  ```ts
    const Database = provides( [ "security" , "integrity" , "consistency etc" , "whileas" ] ) 
    const FileSystem != provides( [ "relation between data" , "constraints" , "query capabilities" ] ) 
  ```

  DBMS (supports) ACID properties [Atomicity, Consistency, Isolation, Durability] , normalising, indexing, etc.
  Filesystem is far less inferior to DBMS in terms of data management, because of poor transaction optimisation, concurrency control , transaction management, etc.

- "database as a well-organized library, and the DBMS as the helpful librarian who assists you in finding and managing the books (data)" - Fundamentals of Database Systems, 7th Edition, Elmasri, Navathe

- Users can **tailored views (multiple views)** of data, focusing on elements relveant to the tasks, enhances security and simplifies data access.

- Multiple users can access the data at the same time (concurrent access) ensuring data integrity, and reduce redundancy and reduce storage overhead.

### Three levels of data abstraction

- physical level - how data is stored in disk (bits, bytes, records, etc.). Internal Schema ,  It's the DBMS's blueprint for efficiently storing and accessing data on disk.
|"The internal schema defines storage mechanisms and indexing."

- logical level - defines entities, attributes, relationships, and constraints using a high-level data model. (independent of physical storage details). Conceptual Schema, focuse on overall organiation of data.
|"The conceptual schema ensures logical consistency across applications."

- view level -  user views - how data appears to the user (specific to user). External Schema, focuse on specific user's view of data (customised data)
|"The external schemas customize access and presentation for end-users or applications."

Three schema architecture promotes data independance (changes in one level do not affect other levels),
Mapping between levels facilitates easy transformation of requests for each level.

![image](https://github.com/user-attachments/assets/ccce4051-dcd0-4027-89b7-6e236e61682e)


### Data independence
- Logical data independence is the capacity to change the conceptual schema without having
to change external schemas or application programs.
- Physical data independence , change the internal schema without having to
change the conceptual (or external) schemas.

### Data language and interfaces

These are used to interact with the database, and are of two types:
- DDL (Data Definition Language) - used to define the database structure (CREATE, ALTER, DROP, etc.)
- DML (Data Manipulation Language) - used to manipulate the data in the database (SELECT, INSERT, UPDATE, DELETE, etc.)

use mind palace here 
![image](https://github.com/user-attachments/assets/fc08d8c3-95fb-453c-83d0-ccf08eeee932)
![image](https://github.com/user-attachments/assets/f9e023db-f2cb-4cb2-8e79-4c38d6504ec3)

DBMS Interfaces
Menu-Based Interfaces for Browsing
Forms-Based Interfaces
Graphical User Interfaces
Natural Language Interfaces
Interfaces for Parametric Users
Interfaces for the DBA

## DBMS Enviroment
Goes through complex software enviroment
- Operating system : DBMS has to interacte with OS , managing storage, resources, data read / write operations, disk space. DBMS relies on OS for file management, memory management, process management, etc.
- Network system : Client server communication in distributed database systems
- Utilites tool : backup, recovery, data import/export, perfomance monitoring, security management, access authorization.


## Types of DBMS 
- Hierarchical DBMS - (older and depreciated) - tree like structure
- Network DBMS - (older and depreciated) - network like structure
- Relational DBMS - (most popular) - table like structure
- Object-oriented DBMS - (complex data types) - object like structure

can you create relation in oodms like rdbms? yes

## Data models
Data models provide the formal structure and semantics of the database (e.g., E-R model for conceptual design). The schema is a static metadata definition at multiple levels (internal, conceptual, external), while an instance is a dynamic snapshot of the data within the schema.
