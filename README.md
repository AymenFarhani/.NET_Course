A Quick Comparaison Between Spring Boot and ASP.NET
 
 
 Feature                      | Spring Boot                                          | ASP.NET Core

  Web Framework               | Spring MVC, @RestController, @RequestMapping         | ASP.NET Core MVC, [ApiController], MapGet/MapPost
  Dependency Injection        | @Autowired, @Service, @Component                     | AddScoped/AddSingleton, constructor injection
  Middleware / Filters        | Filter, HandlerInterceptor                           | Middleware pipeline, app.Use(), IExceptionFilter
  ORM / Data Access           | Spring Data JPA, CrudRepository, @Transactional      | Entity Framework Core, DbContext, LINQ
  Security / JWT              | Spring Security + JwtFilter + SecurityContextHolder  | JwtBearer + [Authorize] + HttpContext.User
  Validation                  | @Valid, @NotNull, BindingResult, ConstraintValidator | [Required], ModelState.IsValid, ValidationAttribute
  Exception Handling          | @ControllerAdvice + @ExceptionHandler                | UseExceptionHandler, Middleware, IExceptionFilter
  IConfiguration, IOptions<T>
  Environment Profiles        | application-dev.properties, @Profile                 | appsettings.Development.json, ASPNETCORE_ENVIRONMENT
  Custom Config Binding       | @ConfigurationProperties(prefix="app")               | services.Configure<T>(Configuration.GetSection("App"))
  Build Tool / Packaging      | Maven or Gradle, JAR/WAR                             | .NET CLI, DLL + EXE
  Hot Reload                  | spring-boot-devtools                                 | dotnet watch run
  API Documentation           | Springdoc / Swagger-UI                               | Swashbuckle (Swagger for NET)
  DB Migrations               | Flyway / Liquibase                                   | EF Core Migrations (Add-Migration, Update-Database)
  Unit Testing                | JUnit, Mockito                                       | xUnit, NUnit, Moq
  IDE Support                 | IntelliJ, Eclipse                                    | Visual Studio, VS Code
  Configuration               | application.yml/properties, @Value, @ConfigurationProperties | appsettings.json, 

