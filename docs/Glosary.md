
@Configuration
    Found at class level
    Indicates to Spring that this is a configuration class that will provide
        beans to the Spring application context

@Bean
    Found at method level (inside a class annotated with @Configuration)
    The objects they return should be added as beans in the application context
        (where, by default, their respective bean IDs will be the same as the
        names of the methods that define them).

Component Scanning - Spring can automatically discover components from
    application's classpath and create them as beans in the Spring App Context

Autowiring - Spring automatically injects the components with the beans that
    they depend on

Autoconfiguration - Spring Boot can make reasonable guesses of what components
    need to be configured and wired together, based on entries in the classpath,
    env variables and other factors


@SpringBootApplication
    Found at class level
    Composite annotation that contains:
        @SpringBootConfiguration
        @EnableAutoConfiguration
        @ComponentScan


@SpringBootConfiguration
    Found at class level
    Designates this class as a configuration class. This is a specialized form
        of the @Configuration annotation


@EnableAutoConfiguration
    Found at class level
    Enables Spring Boot automatic configuration. This annotation tells Spring
        Boot to automatically configure any components that it thinks you’ll need

@ComponentScan
    Found at class level
    Enables component scanning. This lets you declare other classes with
        annotations like @Component, @Controller, @Service, and others, to have
        Spring automatically discover them and register them as components in
        the Spring application context.

@RunWith()
    Found at class level
    Is a JUnit annotation, providing a test runner that guides JUnit in running
        a test. Think of it as applying a plugin to JUnit to provide custom testing
        behavior.
    Found it as @RunWith(SpringRunner.class) which means JUnit is given
        SpringRunner, a Spring-provided test runner that provides for the creation
        of a Spring application context that the test will run against

@SpringBootTest
    Found at class level
    Tells JUnit to bootstrap the test with Spring Boot capabilities. Something
    similar to calling run with a context in main()

@Controller
    Found at class level
    Class that handles requests and provides responses to those requests.
        In the case of a browser-facing application, a controller responds by
        optionally populating model data and passing the request on to a view
        to produce HTML that’s returned to the browser
    Spring component scanning automatically discovers the classes annotated
        with @Controller, creates an instance of it and provides it as a bean in
        the Spring application context. In fact other annotation would work the
        same as this one (@Component, @Service, @Repository), but this one is
        more descriptive of the role it has in application

@GetMapping("/")
    Found at method level (method inside a class annotated with @Controller)
    Mapps an URL to a handler. The string returned is the name of a view (in
        this case made with Thymeleaf). The name of the template is derived
        from this string with the prefix of '/templates/' and the suffix of
        '.html' 

@GetMapping
    NOTICE THAT IT HAS NO PATH AND THERE IS A VERSION WITH PATH
    Found at method level (in classes annotated with @RequestMapping)
    Specifies that this is the method that should be called when the path
        specified by @RequestMapping is hit with an http GET. 

@RequestMapping(method=RequestMethod.GET)
@RequestMapping("/somepath")
    Found at class or method level
    When applied at the class level, specifies the kind of requests that this
        controller handles



@WebMvcTest
    Found at class level
    This is a special test annotation provided by Spring Boot that arranges for
        the test to run in the context of a Spring MVC application.

Table 2.1: Spring MVC request-mapping annotations

+----------------------------------------------------+
| Spring MVC request-mapping list of annotations     |
+-----------------+----------------------------------+
| Annotation      | Description                      |
+-----------------+----------------------------------+
| @RequestMapping | General-purpose request handling |
+-----------------+----------------------------------+
| @GetMapping     | Handles HTTP GET requests        |
+-----------------+----------------------------------+
| @PostMapping    | Handles HTTP POST requests       |
+-----------------+----------------------------------+
| @PutMapping     | Handles HTTP PUT requests        |
+-----------------+----------------------------------+
| @DeleteMapping  | Handles HTTP DELETE requests     |
+-----------------+----------------------------------+
| @PatchMapping   | Handles HTTP PATCH requests      |
+-----------------+----------------------------------+

--- ???
@Component
@Service
@Repository
