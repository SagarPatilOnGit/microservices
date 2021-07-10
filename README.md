# microservices
Introduction

Before we jump to what is microservices architectural pattern we first need to understand two more architectural patterns(Monoliths and Service Oriented Architecture aka SOA) as microservices born to solve pitfalls of these two patterns.  
 
 ## Monoliths
	Pros	
		- Easier to design as it developed and deployed as a single unit and is strongly coupled hence no complex modules like messaging, queues, cross process communication required. 
        	- Performance as no networks hops, no serialization/de-serialization layers, no sharing of computational power, etc.
        	- Process debugging is much simpler due single code base and single running process.
	Cons
		- Single Technology platform
			1. single process for an app leads to using same technology for tasks which can be done better in other platforms e.g. document handling can be done better in .Net platform than in node.js
			2. Future upgrade is problem, need to upgrade whole app.
		- Inflexible deployment
			1. Even small change leads to whole app deployment which forces to rigorous testing every product release
			2. Long development cycles
		
 ## SOA(Service Oriented architecture)
	Pros
		- Technology agnostic data sharing between two or more apps i.e. via XML files
		- Polyglot between services i.e. no dependency on platforms as communication is done based on standard protocol (SOAP/WSDL) e.g. Java service can communicate with .net service using standard protocols
        - 
