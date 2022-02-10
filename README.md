#**DATABASE

#**What is the difference between clustered and non clustered index in SQL?	

A Clustered index is a type of index in which table records are physically reordered to match the index.

A Non-Clustered index is a special type of index in which contains pointers to the data

3. A table can only have one clustered index whereas it can have many non clustered index.
4. B/C Clustered index is on disk it can provide faster reads then a non-clustered index

Clustered is like books in a library, nonclustered is like a card with the location of a book


#**Can you explain the types of join statements	Inner Join - middle of left & right

Right Join - right and middle 
Left Join - left and middle
Full Join - everything
Cross-Join - cartesian product
Given two tables can you inner join and order it in descending order by a specific ID	SELECT class.class_name 
FROM class 
INNER JOIN student_class 
ON class.class_id = student_class.class_id 
ORDER BY class.max_seats_available DESC


#**what are primary and foreign keys	primary key is unique identifier, foreign key is a PK indicates a PK in a different table

Foreign keys give data integrity
#**How would you test adding or deleting something from a database without altering it	
Transactions


#**What are Constraints?	
SQL constraints are used to specify rules for data in a table.

NOT NULL
CHECK
DEFAULT
UNIQUE
PRIMARY KEY
FOREIGN KEY

ex. CREATE TABLE table_name ( Column1 VARCHAR NOT NULL);


#** What are Entities and Relationships?	
Entities - person/place/thing whose data can be stored in DB
Relationship: link between entities, ex. Customer name is related to acc #, contact info.


#**Advantages of normilization?	

Better Database organization
More Tables with smaller rows
Efficient data access
Quickly find the information
Easier to implement Security


#**What is the difference between DROP and TRUNCATE commands?	

DROP command removes a table and it cannot be rolled back from the database whereas TRUNCATE command removes all the rows from the table.
#**What is ACID property in a database?	
ACID stands for Atomicity, Consistency, Isolation, Durability. 

It is used to ensure that the data transactions are processed reliably in a database system.
Are NULL values same as that of zero or a blank space?	A NULL value is not at all same as that of zero or a blank space. 

NULL value represents a value which is unavailable, unknown, assigned or not applicable 

a zero is a number and blank space is a character.


#**What is a DB Relationship and what are they?	

Relationships are defined as the connection between the tables in a database. 

One to One Relationship. (one employee has 1 ID card)

One to Many Relationship. (One city has many customers)

Many to Many Relationship. (One student can register for many classes, and a class can contain many students)


#**What is a having clause? What is a where clause? What is the difference between 'HAVING' CLAUSE and a 'WHERE' CLAUSE?	

The main difference between WHERE and HAVING clause comes when used together with GROUP BY clause, In that case WHERE is used to filter rows before grouping and HAVING is used to exclude records after grouping.
Having used with aggregates while Where is used with column data


#**What are aggregate functions?	

Aggregate functions are used to evaluate mathematical calculation and returns a single value. These calculations are done from the columns in a table. For example- max(),count() are calculated with respect to numeric.
What are scalar functions SQL?	An SQL scalar function is a user-defined function written in SQL and it returns a single value each time it is invoked


**User-defined aggregate function***
What is a View? What are Views used for?	A In SQL, a view is a virtual table based on the result-set of an SQL statement

Used for:
Restricting access to data.
Making complex queries simple.
Ensuring data independence.
What is a Datawarehouse?	Datawarehouse refers to a central repository of data where the data is assembled from multiple sources of information.
What is cursor in SQL Server?	A Cursor is a database object that represents a result set and is used to manipulate data row by row
Index syntax	CREATE INDEX index1 ON table1 (col1)
view syntax	CREATE VIEW view1 AS 
SELECT col1, col2 
FROM table1 
WHERE ...
Syntax for LEFY/RIGHT/INER/OUTER JOIN tables A and B	SELECT <select LIST>
FROM TableA A
<left/right/inner/outer> JOIN TableB B
ON A.Key = B.Key
Syntax for Joining A to B and getting only A values Or joining A and B and not getting inner values	SELECT <select LIST>
FROM TableA A
<left/right/inner/outer> JOIN TableB B
ON A.Key = B.Key
WHERE a.KEY is NULL
<for outer join> OR B.key IS NULL
Group by vs. Order BY	ORDER BY alters the order in which items are returned.
GROUP BY will aggregate records by the specified columns which allows you to perform aggregation functions on non-grouped columns (such as SUM, COUNT, AVG, etc).
  
**Abstract class vs. Interface?
with abstract classes, you can declare fields that are not static and final, and define public, protected, and private concrete methods. 

With interfaces, all fields are automatically public, static, and final, and all methods are public. 

In addition, you can extend only one class, whether or not it is abstract, whereas you can implement any number of interfaces.
.NET managed vs unmanaged code	Code written in C# or Visual Basic .NET will when compiled run only in the CLR which provides garbage collection/memory managementunmanaged code can't rely on the CLR to provide this kind of portability.
What did you use for backend	ASP.NET /Ext.JS

  
#** Abstract class vs Abstract Method	Abstract class: is a restricted class that cannot be used to create objects
 
abstract method: can only be used in an abstract class, and it does not have a body. The body is provided by the child class. 

cannot call the method unless body provided in subclass

same for abstract class, cannot create abstract class, only the ones that extend it.)
Mvc vs mvvm	MVC format is specifically designed to create a separation of concerns between the model and view, the MVVM format with data-binding is designed specifically to allow the view and model to communicate directly with each other.

In MVC you interact with controller, in MVVM the view
Stack & Heap (Memory Space)	The stack is used for static memory allocation while the heap is used for dynamic memory allocation.Variables allocated on the stack have their memory allocated at compile time and access is very fast.Variables allocated on the heap have their memory allocated at runtime and accessing this memory is slightly slower.
OOP Concepts	Abstraction, Encapsulation, Inheritance, Polymorphism
Define Encapsulation	Encapsulation is when we hide implementation details from user (data hiding).

In Java we can make data private and only accessible via public methods to better hide data details.
Define Inheritance/Multiple inheritence	A mechanism that defines a new class that inherits the properties and behaviors (methods) of a parent class. Superclass/Base Class (Parent) → Subclass/Derived Class (Child). 


Any inherited behavior may be redefined and overridden in the subclass.
benefit of inheritance	Avoids duplication of code.
what is multiple inheritance?	Multiple inheritance is when a class inherits from more than one superclass. A problem arises when there is more than one property/method to inherit with the same name.
Inheritance - Method Overriding	A subclass inherits properties and methods from the superclass. When a subclass alters a method from a superclass by defining a method with exactly the same signature, it overrides that method. This can either be a refinement or a replacement of the superclass' method.Implementing abstract methods of an abstract class or implementing methods of an interface is also method overriding.
CLR VS JVM	CLR was designed to be language-neutral, JVM was designed to be Java-specific - CLR allows for cross language integrationCLR was originally only Windows-compatible, JVM works with all major OSs
What is an immutable object in Java?	Immutable objects are those whose state cannot be changed once created. Any modification will result in a new object
Name design patterns & define	Singleton - A singleton class shouldn't have multiple instances in any case and at any cost. Ex. Casino Tournament class

Flyweight - Flyweight pattern is used when we need to create a large number of similar objects ex -casino Deck class .

Factory In Factory pattern, we create object without exposing the creation logic to the client

Ex. Casino Round class creating everything

Prototype - fully initialized instance to be copied
How does inheritance break the encapsulation barrier around a class and increase coupling?	Any change to the parent affects the child because every child gets a copy of the parent class
Define garbage collection and can wer manually run in java? How about C#?	Garbage collection is the process inside JVM which reclaims memory from dead objects for future allocation.

yes - java with system.GC(), C# with Dispose() or Finalize()
Describe overloading and overriding	Both overloading and overriding allow you to write two methods of different functionality but with the same name, but overloading is compile time activity while overriding is run-time activity.
is-a vs has-a relationship OOP	Is-A is inheritance (cat is an animal)has-a is composition (car has an engine)
Can you override a static method?	No because they are resolved at compile time
Static in C#?	In C#, static means something that cant be instantiated.

 You cant create an object of a static class and cant access static members using an object.

Have to access with object name - ex. (Calculator.sum(10,5)); to call the methods
What are generics in C#.NET?	Genetics allow for writing the code for a class without specifying the data type(s) that the class works on. 

You specify the data type when you declare an instance of a generic class. 

This allows a generic class to be specialized for many different data types while only having to write the class once
Abstraction vs. Encapsulation	In abstraction, problems are solved at the design level.
 While in encapsulation, problems are solved at the implementation level. 

We can implement abstraction using abstract class and interfaces. 

Whereas encapsulation can be implemented using by access modifier i.e. private, protected and public.
What is a delegate in .NET? Benefit?	Delegates are same are function pointers in C++, but the only difference is that they are type safe, unlike function pointers. Delegates are required because they can be used to write much more generic type-safe functions.
read only var vs constant	Read-only variables can support reference-type variables. Constants can hold only value-type variables.
Integridata interview - Async Await in C#	Async/Await is a mechanism for telling the compiler at which points in your code you will be waiting for something to happen (ex db load or something)
C# - What is the difference between ref & out parameters?	An argument passed as ref must be initialized before passing to the method whereas out parameter needs not to be initialized before passing to a method.
What is Jagged Arrays?	An array of arrays
What is the use of 'using' statement in C#?	The 'using' block is used to obtain a resource and process it and then automatically dispose of when the execution of the block completed.
C# - Can we use "this" command within a static method?	No because we can only use static variables/methods in a static method.
What is the difference between constants and read-only?	Constant variables are declared and initialized at compile time. The value can't be changed afterward. Read-only is used only when we want to assign the value at run time
What is an interface?	Abstract class which only has public abstract methods, which must be implemented in the inherited classes.
What is the difference between Finalize() and Dispose() methods?	Dispose() is called when we want for an object to release any unmanaged resources with them. On the other hand, Finalize() is used for the same purpose, but it doesn't assure the garbage collection of an object
What are generics in C#.NET?	Generics are used to make reusable code classes to decrease the code redundancy, increase type safety, and performance. Using generics, we can create collection classes
What is the base class in .net from which all the classes are derived from?	System.Object
Stack & Heap (Memory Space)	The stack is used for static memory allocation while the heap is used for dynamic memory allocation.Variables allocated on the stack have their memory allocated at compile time and access is very fast.Variables allocated on the heap have their memory allocated at runtime and accessing this memory is slightly slower.
What is polymorphism? BBC	Many forms - we can have objects to present the same interface in different forms 
(Ex We can loop through an array containing different automobiles as vehicles V and then print out their wheels - each one will be different but function call would be same (v.wheels())
Entity Framework	simplifies mapping between objects in your software to the tables and columns of a relational database. takes care of creating database connections and executing commands, as well as taking query results and automatically materializing those results as your application objects.
Class for reading DB C#	DataReader
Private vs protected modifiers	private: The type or member can be accessed only by code in the same class or struct . protected: The type or member can be accessed only by code in the same class , or in a class that is derived from that class
try/catch/finally - does finally always run?	By using a finally block, you can clean up any resources that are allocated in a try block, and you can run code even if an exception occurs in the try block.

Yes unless app crashes
Can you have multiple catch blocks?	Yes and the most specific exception, which comes first, is caught.
Reading text file	The StreamReader and StreamWriter classes are used for reading from and writing data to text files.

sr.ReadLine() to read line by line till the end
What is LINQ?	LINQ (Language Integrated Query) is uniform query syntax in C# and VB.NET to retrieve data from different sources and formats.

 It is integrated in C# or VB, thereby eliminating the mismatch between programming languages and databases, as well as providing a single querying interface for different types of data sources.
what is a sealed class?	Sealed classes are used to restrict the users from inheriting the class

 The keyword tells the compiler that the class is sealed, and therefore, cannot be extended.
what is a partial class? Good example to use it?	Partial class allows us to split the implementation of a class, a struct, a method, or an interface in multiple .cs files

Using Partial Classes multiple developer can work on the same class easily.



FrontEND/OS

Explain CSS selectors	- element selector (div {})
- ID selector - select by HTML element ID (#ID)
- class selector - select by HTML class ID (.id)
- Universal selector - *
-can select multiple elements in one line (div,html, p {})
What's the difference between the "nth-of-type()" and "nth-child()" selectors?	ways to access child notes in CSS Selector
Can you explain the difference between px, em and rem as they relate to font sizing?	Pixels are generally used for font sizes (absolute sized, so they will always be x px).
Use REMs for sizes and spacing.
Use EMs for media queries.

EM/REM scale with device size, pixels are absolute
What does a doctype do?	Including the DOCTYPE in a document ensures that the browser makes a best-effort attempt at following the relevant specifications.
How do you serve a page with content in multiple languages?	Accept-Language header
What is the difference between span and div?	div is a block element
span is inline element
For bonus points, you could point out that it's illegal to place a block element inside an inline element, and that while div can have a p tag, and a p tag can have a span, it is not possible for span to have a div or p tag inside
  
What is kernel?	A kernel is the core of every operating system. It connects applications to the actual processing of data.
  
objective of multiprogramming.	
  The main objective of multiprogramming is to have a process running at all times. With this design, CPU utilization is said to be maximized.

  What is a thread?
  A thread is a basic unit of CPU utilization.
benefits of multithreaded programming.	- there is increased responsiveness to the user- resource sharing within the process- economy- utilization of multiprocessing architecture
Briefly explain FCFS.	FCFS stands for First-come, first-served. 

It is one type of scheduling algorithm. 

In this scheme, the process that requests the CPU first is allocated the CPU first.
What is RR scheduling algorithm?	round-robin scheduling algorithm is primarily aimed for time-sharing systems.

 A circular queue is a setup in such a way that the CPU scheduler goes around that queue, allocating CPU to each process for a time interval
What are necessary conditions which can lead to a deadlock situation in a system?	Deadlock situations occur when four conditions occur simultaneously in a system:

 Mutual exclusion; Hold and Wait; No preemption; and Circular wait.
What is a socket?	A socket provides a connection between two applications. Each endpoint of a communication is a socket.
what is a semaphore? And both types of semaphores	Semaphore is a protected variable or abstract data type that is used to lock the resource being used.

Binary semaphores
Counting semaphores
what is a process?	process is the instance of a computer program that is being executed by one or many threads.
what is a lock/mutex and difference?	A mutex is an object which can be locked.

A lock is the object which maintains the lock. To create a lock, you need to pass it a mutex.
  
  Questions to Study
  
  
  - Referential Integrity
  - Static keyword C#
  - Internal vs public vs private vs protected
  - Deferred Execution
  - Lazy & Fast Loading 
