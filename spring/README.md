# Spring Framework Notes 

## The Spring ApplicationContext
- IoC Container represented by BeanFactory and ApplicationContext 
- BeanFactory = root interface
- ApplicationContext = sub-interface of BeanFactory

Important features:
- Enterprise-specific functionalities
- Resolving messages
- Support internalization
- Publish events
- App layer specific context

Implementations:
- AnnotationConfigApplicationContext (@Configuration, @Component)
- AnnotationConfigWebApplicationContext (same above web-based variant)
- XmlWebApplicationContext (xml based config in a web app)
- FileSystemXMLApplicationContext (load XML config file from FS or URL)
- ClassPathXmlApplicationContext(load XML config file from CP)

## Spring Design Patterns

- Spring is based on DP
- IoC is the main pattern (this is the real deal)
- The entire runtime is based on IoC
- Proxy pattern (every object is wrapped proxies)
- Factory Pattern (IoC)
- Singleton and Prototype (most if not all of the objects levereage these)
- Template Pattern (remote calls JDBC,REST)
- MVC Pattern (entire webframework is based on MVC pat, web pages as well as RESTFUL services)

### IoC The Core Pattern

- Realy THE core pattern
- Not a gangOf4 pattern
- Construction of dependencies relegated to container not to developer
- DI is just flavor of IoC
- Central container constructs and manages the state of all objects
- Hands dependencies to a component as necessary
- Manages dependencies as long as YOU ASK IT from Spring
- Objects are injected at runtime not compile time
- Reduces noise in your code (go ahead try to create a JDBC connection :)
- Reduces object coupling
- Reduces the defects from incorrect constructing object
