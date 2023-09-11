The Three Schema Architecture, also known as the ANSI/SPARC Architecture, is a conceptual framework for understanding and organizing the components and layers of a database management system (DBMS). It was developed by the American National Standards Institute (ANSI) Standards Planning and Requirements Committee (SPARC) to provide a clear separation between different levels of database functionality. The architecture defines three levels of abstraction:

1. **External Schema (View Level):** This is the topmost level and is concerned with the user's view of the data. It defines how different user groups or applications perceive and interact with the data. 
	- Each external schema represents a specific subset of the overall database that is relevant to a particular user or application. 
	- Users at this level can define their own views, queries, and reports without needing to understand the underlying data structure. 
	- A database containing several schemas sometimes called as **subschema**, this is used to describe a different view of database. 
	- Security mechanism is also provided over here to prevent users from accessing certain parts of DB.
    
2. **Conceptual Schema (Logical Level):** The conceptual schema represents the overall logical structure of the entire database, independent of any specific user's view. 
	- It provides a unified and abstracted representation of the data that is more easily understood by users and developers. 
	- The conceptual schema is designed to capture the essential data relationships, constraints, and integrity rules of the organization's data model.
	Note: Logical Schema is generally referred to as **Database Schema**  
	
3. **Internal Schema (Physical Level):** The internal schema is concerned with how the data is physically stored and organized on the storage devices. 
	- It defines the data storage structures, access methods, indexing, and other physical implementation details. 
	- Changes to the internal schema should not impact the external or conceptual schemas, providing a layer of insulation between the physical storage and the user/application interfaces.

#### DB Schema contains:
- Attributes of table
- consistency constraint (Primary Key)
- Relationships

![[Pasted image 20230816180902.png]]


### The Three Schema Architecture provides several benefits:

- **Data Independence:** The separation of the three schemas allows for different levels of abstraction and reduces the impact of changes at one level on the other levels. This promotes data independence, where modifications to the physical storage do not require changes to the user views or logical structure.
    
- **Flexibility and Modularity:** The architecture allows different user groups to work with their own customized views of the data while maintaining a consistent underlying data model. This promotes flexibility and modularity in the design and development of database applications.
    
- **Security and Access Control:** Different users and applications can be granted appropriate levels of access to the external schema without exposing the internal storage details.
    
- **Scalability and Performance:** The architecture supports optimizing performance at the internal schema level (e.g., indexing, data partitioning) without affecting the way users interact with the data.