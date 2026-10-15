# Lab 4: UML Class Diagrams

UML (Unified Modeling Language) class diagrams are a type of diagram used in software engineering to describe the structure and organization of classes, objects, and their relationships in a software system. The purpose of a UML class diagram is to visually represent the classes, attributes, and methods of a software system, and to show how these classes interact with each other.  In COSC 111/121, you would have seen the basic structure of a class diagram to understand inheritance, interfaces, and the relationship of classes (is-a and has-a type relationships).  This lab will expand on this, looking at how we can describe the relationship (associations) between different classes in a system design (aggregation, participation and composition).

A UML class diagram typically consists of a number of rectangles representing classes, with the name of the class written inside. Each class is also usually shown with its attributes, represented as a list of properties, and its operations, represented as a list of methods. Relationships between classes, such as inheritance and aggregation, can be shown using lines and arrowheads.  Included with this is the visibity of attributes and methods).

UML class diagrams are useful for several purposes, such as:

* Describing the design of a software system
* Communicating the design between stakeholders
* Supporting the development of a software system by providing a visual representation of the classes, attributes, and methods
* Helping to catch design flaws early in the development process.

UML class diagrams are just one type of diagram used in UML, and can be used in combination with other types of diagrams, such as activity diagrams, sequence diagrams, and state machine diagrams, to provide a complete picture of a software system.

In addition to the course notes, there are a number of resources available to help.  Please feel free to utilize these to improve your understanding of the construction:
* [Lucid Chart](https://www.lucidchart.com/pages/uml-class-diagram)
* [UML Class Diagrams](https://www.javatpoint.com/uml-class-diagram)
* [Association Classes](https://www.ibm.com/docs/en/rsm/7.5.0?topic=diagrams-association-classes)

Consider the following example that models employees working on different projects from different departments.

![This is an image](/img/worksonclass.png)

In this model there is a **Department** that has multiple **employees** but there could also be empty departments.   Each employee can work for at most one department.  The department is also managed by at most one employee (but may not have a manager) and an employee can manage multiple departments (but can also not be a manager at all).   Each department has at least one **Project** but can be working on multiple projects whereas each project can be associated with at most 1 department but could also not be associated with any department (i.e., the project hasn't been assigned yet).  An employee can be associated (working on) with a project (and can be working on multiple projects but may not be working on any project at all).  A project can have multiple employees but may not have any.   

## Building a UML Class Diagram (40 marks)

This assignment is meant to give you practice with design, especially developing UML class diagrams. The assignment may be done in groups.

### Develop a UML class diagram for the EBook book store. Below is a description of EBook:

Your customer wants a software system for a simple electronic bookstore called EBook. EBook does not store any books itself. It just provides a large catalogue of the books it offers. The catalogue contains for each book the usual information like ISBN-number, title, authors, publisher, price, etc. A customer can order a book over the Internet and pay by credit card. Otherwise, they can phone in or mail their order to the company where clerks will enter the order for them. Both customers and clerks can search the catalog online, and enter and view comments for any book in the catalog. When processing a customer order, the payment is verified first, and if accepted, then the book is ordered directly from the publisher by direct communication with their system. The book is shipped from the publisher to our store, then it is sent to the customer. A customer can order several books per order, and they will get shipped to the customer as they arrive at EBook, i.e. a single order can result in several shippings to the customer. Customers and clerks can inquire about the status of an order any time.

Of course, the catalogue needs some maintenance, so the clerks can add and delete items from the catalogue, as well as update information. Clerks are able to inquire how many books are pending from a specific publisher.

*Cancellation*: A customer can cancel an order as long as it has not yet been sent out to him. In case of a cancellation, EBook either sends a cancel order instruction to the publishers or returns the book(s) to them.

*Return of books*: A customer can return a book within a week. The money will either be credited to his credit card, or the customer receives a refund check.

When working on this, please start with a sketch of the major classes, thinking about how the different components will interact with each other.  When reviewing the description, I would suggest highlighting the items that will appear as classes, (i.e. customer, order, book ....) and then work on the relationships relationship cardinalities and association and participation constraints.

Notes:

 1. Focus on identifying the major classes first.
 2. Make sure to identify all associated attributes of the classes.
 3. Identify relationships between the classes and add cardinality constraints that are known or can be reasonably assumed.
 4. You do not have to add all get/set methods for each class. However, you should have at least 4 methods for each class. Make sure to identify the most important methods for the functioning of the system, but if a class does not have 4 such critical methods then fill up the remainder with get/set methods.

### Deliverables:

Submit a PDF copy of your UML class diagram.  You can build it with any tool you choose (you might want to review the tools from lab 3).  

## Scoring
* [30] Classes with relevant data and methods, and associations (with correct cardinality)
* [10] Presentation and correctness of diagram (layout, arrows, plurals, qualifiers being used the correct way, etc.)
