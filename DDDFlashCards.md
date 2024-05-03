## Application Layer
THis acts as mediator between the user interface and domain layer, this should use interfaces and abstractions that are defined by the domain layer suche as repositories and services.  
SO the application layer can be deplyed independntly from the infrastructure layer.    
This should follow (CQRS) pattern, keep in mind that the application layer is completeely independent from the domain layer.  



## Domain Layer
This contain the core functionalty of the application.  
This includes domain model.
This should be independnet and cannot be depend on any other layer or external resources  


## Domain model  
This include things like `Aggregates` `Entities` `Value objects` `events` `services`/ .  

## Domain entities and Value Objects
Domain entities are represented by objects ! Each one of them have a unique identity !  
On the contaray *value objects* doesn't have a unique identity.  

## Aggregates  
THey are cluster of objects treated as a single unit of work  

## Domain events   
They are not tied to a specific entity or value.  
They are like an interface to interact with the domain model  

## 4 key prencilbles of the Domain model  
They are 
*focused*  : Only relevnt aspects of the domain, avoid any complexity  
*Explicit*: Well defined, straight forward 
*Isolated*: Decoupled from other layers, like database, interface, network  
*Testable*:   

## 4 key concepts about Ubiquitous Language  
*Evolving*:   Always changing as we progress in the develment of the application to be more accourat and correct and will defined  
*Contextual*:   **Specific to a particuler bounded context** ALSO **avoid any confusion with other cotexts or domains** !!!
*Expressive*:   rich and precise
*Implemented*:   Reflected on the code, tests, documentation, communication of the project  

## 4 key concepts about Value Object  
*Immutable*: Should not allow its aƒttributes to be changed after creation  
*Equatable*: Implement equality based on its attributes, rather thatn on its identity or refernce  
*Replaceable*: Should be easily replace by another value object with the same attributes  without affecting any thing !!  
*Shareable*: Should be safe to share accross multiple domain objects or contexts, without causing side effects or incosistencies  

## 4 key concepts of an Entity
It represents a complex entity or object in the domain, it has a unique identity and a lifecycle, and may have a mutable state.
*Identifiable*:   Unique identifier that distinguishes it from other entites of the same type  
*Mutable*:  May allow its state to be changed as part of its domain behavior, but only in a controlled and consistent way.  
*Consistent*:  Maintain its rules all the times, regardless of its state changes.
*Aggregateable*:  May belong to an aggregate that defines its boundaries and consistency rules  

## 4 key concepts of Context or Bounded Context  
*Bounded*: Clear and explicit boundary that separated it from other conext or domains  
*Consistent*: Ensure it is consistent withen its bounded context  
*Autonomous*: Should be independent and self-contained and should depend on any other contexts or domains ans this can happen thourogh will defined interfaces or protocols
*Integrable*: May communicate or interact with other contexts or domains through well-defined interfaces or protocols  

## 4 key concepts Aggregate  
Cluster or related entities and value objects that form a unit of consistency and transactional integrity.  
An aggregate defines what entities belong together, what are their invariants and rules, and how they can be accessed or modifed.  
*Rooted*: Single entity, called the aggregate root, that serves as the entry point of the aggregate.  
*Consistent*:  Ensure that the entites are valid and that their rules are enforced  
*Isolated*: Should not expose its internal entities or value objects to the outside world, and should only allow access to ther entities and value objects through aggregate root  
*Transactional*: Should be treated as a single unit of work or transaction, and should either succeed or fail as a whole.  

## 4 key concepts of  Repository  
It is a class that is used to access aggregates or entities of a domain model, A repository hides the details of how the aggregates or entites are stored, retrieved, or persisted, and provides a collection-like interface to manipulate them.

*Abstract*: Define an interface that specifies what operations are availabel for aggregates without exposing the underlaying details of how they are implemeented.  
*Concrete*: Define solid interfaces that will interact with the database   
*Consistent*: ENsure that the aggreagate returened by the repo are in consistent state and reflect the latest changes made to them  
*Queryable*: Allow querying or filtering the aggregates or entities based on various criteria 



## 4 key concepts of Domain Event  
*Immutable*: should not allow its state to be changed after creation  
*Descriptive*: Decribe what happend to the domain in very clear and expressive name and attributes  
*Observable*: Should be published to interseted parities using event bus, sending notifications, invoking services, etc.  
*Reactive*: May trigger some actions or reactions in response to it, such as updating the domain state, sending notifications..  

## 4 key concepts of Domain Service  
*Stateless*: Should not have any state or dependencies of its own, and should only rely on paramaters or inputs provided to it.  
*Fuctional*: Perform a single function or operation and return the output or result  
*Injectable*: Should be easily injected or provoided to other entittes or value objects that need it, using dependency injection, service locator, or other techniques.  
*Testable*:   

## 4 key concepts of Commandos  
*Immutable*: Should not all its data or context to be changed after creation  
*Validatable*: Validtes the data before doing the command
*Executable*: It executes some logic on the provided data to it 
*Auditable*: May record some information by who whome when where and it was executed

## 4 key concepts of Factories  

