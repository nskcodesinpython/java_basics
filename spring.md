Maven - Knowledge Accumulator in German - POM - Project Object Model - can manage project build, reporting and documentation from central piece of informat.


Spring - provides configuration model and comprehensive programming for enterprise application
       - integrates all other frameworks

Spring boot - creates stand-alone, production grade Spring-based application that you can just run
            - opinonated view of Spring platform
            - Built in server
            - Auto configuration (WAR files)

Configuration:
    - Jar files - Java ARchive files - class files
    - DB - Oracle - H2 - MySQL
    
    - WAR files - Web ARchive files

- Bill of Materials - checking if all the jar files are in the right version

POJO - private variables - getters and setters - encapsulation
- Dependancy Injection
- MVC
- Security


Design patterns:
  MVC - Model View Controller
    Model - Retreiving and storing data, Mainitaining state, notification of observers of change in state
    View - UI, renders ListBox controls, acilitates selection
    Controller - responsinle for responding to user inputs, handles ListBox selection event, sends information to model
  Seperation of concerns
  
  client --> web.xml --> dispatcher servlet/ front controller (Handler Mapping) @Controller --> Servlet 
  ---> service/Model/DAO model --> DB --> Model object --> View Resolver (spring-config.xml) ---> View
  --> Servlet --> Jasper --> Client
  
  API - Application Programming Interface 
  REST API - State of an object (XML/JSON)- REpresentational State Transfer
           - CRUP operation
           - HTTP Methods
                - post
                - get
                - put
                - delete

Dependancy Injection
  - Design Pattern - Idea - Object graph
 Dynamic Binding - A a = new B();
    - Avoids Tight Coupling
    - @Component, @Autowired, @Qualifier
    - Easier to do Unit Testing

Class Home{
  @Autowired
  @Qualiier("act")
  NetModem modem;
 }
 interface NetModem{
}

@Component("act")
class Act implements NetModem{

}
@Component("hath")
class Hathway implements NetModem{

}

Maven Project:
Group ID - package name
Artifact ID - project name
Version ID - project version

Advantages 
  - Default Project Structure
  - Auto download dependancy
  - Auto compile
  - Server starting and stopping

Spring Boot - Dependant WAR files
  - SpringWeb - for web application
  - ThymeLeaf - handling HTML
  - JPA 
  - H2
  - Spring Boot Actuator - Debugging
  
Spring Boot - Project Structure
SpringApplication.run(...)
  - Sets up default configuration
  - Starts Spring Application automatically
  - Auto Class path scan
  - Start/Stop server

@SpringBootApplication
class A{
 public Static void main(String[] args){
   ConfigurableApplicationContext c = SpringApplication.run(A.class,args);
   B b = c.get.Bean(B.class);
   b.methodname();
  }
}

@Component
class B{
  //variables and methods
}


Servlet - Server Component
        - Static request
        - Dynamic request
web.xml - Deployment Descriptor
        - WEB.INF
        
application properties
       - spring.mvc.view.prefix = /pathname/
       - spring.mvc.view.suffix = .jsp

JSTL - JSP Standard Tag Library --> Expression Language

ModelAndView - setViewName()
             - addObject("key",value)
             
 JPA - Java Persistance API

Annotations:

@SpringBootApplication
@AutoWired
@RequestMapping
@ResponseBody
@RequestParam
@Controller
@Component
@value
