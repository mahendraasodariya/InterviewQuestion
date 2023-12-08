# InterviewQuestion
Interview Questions
==========================================================================================================================================
---*************SQL*************---
==========================================================================================================================================
1)what is magic table ?
->
Magic tables are the temporary logical tables that are created by the SQL server whenever there are insertion or deletion or update( D.M.L)  operations. 
The recently performed operation on the rows gets stored in magic tables automatically. These are not physical table but they are just temporary internal tables. 
These magic tables can’t be retrieved directly, we need to use triggers to access these magic tables to get the deleted and inserted rows.
->Basically it's use in trigger 

2)What is View in sql server ? 
->A VIEW in SQL Server is like a virtual table that contains data from one or multiple tables. It does not hold any data and does not exist physically in the database. 
Similar to a SQL table, the view name should be unique in a database. It contains a set of predefined SQL queries to fetch data from the database.

3)what is cursor  ?
->A Cursor is a temporary memory that is allocated by the database server at the time of performing the Data Manipulation Language operations on a table,
   such as INSERT, UPDATE and DELETE etc. It is used to retrieve and manipulate data stored in the SQL table.

4)What is composite key  in sql ?
->A composite key in SQL can be defined as a combination of multiple columns, and these columns are used to identify all the rows that are involved uniquely. 
Even though a single column can't identify any row uniquely, a combination of over one column can uniquely identify any record.

5)Self join in depth 

6)what is hash join in sql server?
The name Hash join comes from the hash function(). This hash join is useful for middle to large inputs, 
but it is not efficient for every small set. 
Hash join requires at least one equi join(=), and it supports all joins (left/ right semi/ anti join). 
Hash join is the only physical operator that needs memory. Hash join consists of 2 phases.
i)Building or blocking phase
ii)Probe or non-blocking phase

****************Reference Links: 
https://www.sqlservertutorial.net/

==========================================================================================================================================
---*************C#/Net Core *************---
==========================================================================================================================================
1)what is sealed class  ?
->In C#, when we don't want a class to be inherited by another class, we can declare the class as a sealed class.
  A sealed class cannot have a derived class. We use the sealed keyword to create a sealed class. For example,

2)what is readonly  ?
->The readonly keyword is a modifier that can be used in four contexts: In a field declaration, readonly indicates that assignment 
to the field can only occur as part of the declaration or in a constructor in the same class

3)what is constant ?
->Constants are immutable values which are known at compile time and do not change for the life of the program.
 Constants are declared with the const modifier. Only the C# built-in types (excluding System. Object) may be declared as const
 . User-defined types, including classes, structs, and arrays, cannot be const 

4)what is static class?
->a static class cannot be instantiated. In other words, you cannot use the new operator to create a variable of the class type.
 Because there is no instance variable, you access the members of a static class by using the class name itself.
e.g. utility class  -> UtilityClass.MethodA(); 

5)What are the Net core benefits ?
 ->ASP.NET Core provides the following benefits:

  -A unified story for building web UI and web APIs.
  -Architected for testability.
  -Razor Pages makes coding page-focused scenarios easier and more productive.
  -Blazor lets you use C# in the browser alongside JavaScript. Share server-side and client-side app logic all written with .NET.
  -Ability to develop and run on Windows, macOS, and Linux.
  -Open-source and community-focused.
  -Integration of modern, client-side frameworks and development workflows.
  -Support for hosting Remote Procedure Call (RPC) services using gRPC.
  -A cloud-ready, environment-based configuration system.
  -Built-in dependency injection.
  -A lightweight, high-performance, and modular HTTP request pipeline.
    -Ability to host on the following :
    -Kestrel
    -IIS
    -HTTP.sys
    -Nginx
    -Apache
    -Docker
    -Side-by-side versioning.
    -Tooling that simplifies modern web development.


6).Net Core Startup Class ?
->It contains an optional Configure Services method to configure app services. A service is a reusable module that provides functionality.
Need to register services in the Configure Services method and consumed throughout the application via dependency injection.
Includes a Configure method to build the app’s request processing pipeline.

7)How to get Distinct data from array  ?
-> Using  Distinct() function 
e.g.
  string[] animals = { "Cat", "Alligator", "Fox", "Donkey", "Cat" };
  string[]  dist = animals.Distinct().ToArray();

8)What is C# Solid Principals ?
->  SOLID Principles
      SOLID is the short form of the five important design principles:
      S: Single-responsibility principle
      O: Open/Closed Principle (OCP)
      L: Liskov Substitution Principle
      I: Interface Segregation Principle
      D: The Dependency Inversion Principle (DIP)
        Software engineers commonly implement all five principles and provide some important benefits for developers.
  * Benefits of the SOLID principle *
       i)   Accessibility
       ii)  Ease of refactoring
       iii) Extensibility
       iv)  Debugging
       v)   Readability

9)Where are SOLID principles used?
->
  It can be applied to software components, microservices, and classes. Utilising this principle, the code becomes easier to maintain and test; 
  it makes software simpler to implement, and it helps to ward off unexpected side effects of future changes.

9)Desing Patterns in C#
->
REF : https://refactoring.guru/design-patterns/
---------------------*********Linq************----------------------------
1)What is entity framework core?
->it's ORM (object-relational mapper)
Entity Framework (EF) Core is a lightweight, extensible, open source and cross-platform version of the popular Entity Framework data access technology. 
EF Core can serve as an object-relational mapper (O/RM), which: Enables .NET developers to work with a database using .NET objects.

2)FirstorDefault() vs First()

3)FirstOrDefaultAsync() vs SingleOrDefault()
->
  The main difference between SingleAsync and FirstAsync is that SingleAsync will throw an
  exception if there is more than one element in the collection that satisfies the specified
  condition, while FirstAsync will return the first element it finds and then stop.
****************Reference Links: 
https://www.interviewbit.com/c-sharp-interview-questions-for-5-years-experience/
==========================================================================================================================================
---*************Angular*************---
==========================================================================================================================================
1)What is SSR(server side rendering)
->
2)explain directives and types
->ng-if , ng-for
3)explain props
->
4)what is template in angular
->
5)how to pass data one component to another using service 
-> using observable
6)authentication
->
7)pipes
->
8)abstract class
->
9)polymorphism
->
10)inheritance
->
11)encapsulatoin
->
12)What are the class decorators in Angular?
->A class decorator is a decorator that appears immediately before a class definition, which declares the class to be of the given type, and provides metadata suitable to the type

The following list of decorators comes under class decorators,

@Component()
@Directive()
@Pipe()
@Injectable()
@NgModule()

13)What are class field decorators?
->
  The class field decorators are the statements declared immediately before a field in a class definition that defines the type of that field. 
  Some of the examples are: @input and @output,
  @Input() myProperty;
  @Output() myEvent = new EventEmitter();

14)What is ngOnDestroy
->
---------------------*********Security************----------------------------
12)Preventing Cross-site Scription (XSS)    -https://angular.io/guide/security
13)Trusting values with the DOMSanitizer
14)HTTP Attacks (CSRF and CSSI)
15)Authentication using Json Web Tokens (JWT)    
16)Authorization : Router Guards     - https://codecraft.tv/courses/angular/routing/router-guards/

****************Reference Links: 
1)https://github.com/sudheerj/angular-interview-questions#what-is-angular-framework 
2)https://angular-university.io/

==========================================================================================================================================
---*************Azure*************---
========================================================================================================================================== 
1)Azure CI/CD
2)Azure Storage 
