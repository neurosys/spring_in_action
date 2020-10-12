
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

--- ???
@Component
@Controller
@Service
