# prior to microservices

Before we jump to what is microservices architectural pattern; we first need to understand two more architectural patterns(Monoliths and Service Oriented Architecture aka SOA) as microservices born to solve pitfalls of these two patterns.  
 
 ## Monoliths
	Pros	
		- Easier to design as it developed and deployed as a single unit and is strongly coupled hence no complex modules like messaging, queues, cross process communication required. 
        	- Performance as no networks hops, no serialization/de-serialization layers, no sharing of computational power, etc.
        	- Process debugging is much simpler due single code base and single running process.
	Cons
		- Single Technology platform
			1. single process for an app led to using same technology for tasks which can be done better in other platforms e.g. document handling can be done better in .Net platform than in node.js
			2. Future upgrade is problem, need to upgrade whole app.
		- Inflexible deployment
			1. Even small change led to whole app deployment which forces to rigorous testing every product release
			2. Long development cycles
        - Inefficient compute resources
            1. CPU/RAM is shared across all components of monolith app, no way to allocate these resources to some specific component which needs it more i.e. we have scale compute power to whole process.
        - Large and complex
            1. Large and complex code base
            2. Testing might not always detects all the bugs
            3. Difficult to maintain as small change might affect other components due to high cohesiveness and inter dependency between components. 
		
 ## SOA(Service Oriented architecture
	Pros
		- Technology agnostic data sharing between two or more apps i.e. via XML files
		- Polyglot between services i.e. no dependency on platforms as communication is done based on standard protocol (SOAP/WSDL) e.g. Java service can communicate with .net service using standard protocols
    Cons
        - Complicated and expensive ESB(Enterprise Service Bus) or in .Net WCF ecology it can be endpoint service 
            1. Solves all cross cutting concerns like routing, exception handling, authentication and authorization hence quickly becomes bloated and expensive
            2. Single point of failure aka SPOF
        - Lack of tooling
            1. SOA was supposed to have short development cycles unlike monoliths but due to lack of testing and automation tools this problem persisted
            2. No time savings achieved

# microservices introduction
    - Problems with Monoliths and SOA led to new architectural paradigm with more modularity and simpler APIs
    - Characteristics
        1. Componentization via services
        2. Built and organized around business capabilities
        3. Decentralized governance
        4. Decentralized data management
        5. Infra automation
        6. Design for failure
        7. Smart endpoints and dumb pipes 
    - References: https://www.martinfowler.com/articles/microservices.html
    - Comprehensive documentation : https://microservices.io
    - Detailed Udemy course by Memi Lavi: https://www.udemy.com/course/microservices-architecture-the-complete-guide

