1) What is ASP.NET?
   
ASP.NET is an open-source, server-side web application framework developed by Microsoft. It is part of the broader .NET ecosystem and is designed for building modern, high-performance, cross-platform web apps, including:
- Web APIs (RESTful services)
- Web applications (MVC, Razor Pages)
- Real-time apps (with SignalR)
- Microservices

  2) Key Advantages of ASP.NET:
     
Cross-platform: Run on Windows, Linux, macOS via .NET Core / .NET 6+
High performance:	One of the fastest web frameworks on benchmarks (thanks to Kestrel server)
Unified platform:	Build APIs, UIs, and microservices in one environment
Built-in Dependency: Injection	Comes with a powerful DI container out of the box
Modern Security:	Built-in support for JWT, OAuth2, OpenID Connect
Minimal APIs (ASP.NET 6+):	Quickly build APIs with minimal boilerplate code
Tooling & IDEs:	Deep integration with Visual Studio, VS Code, and CLI tools
Integrated Testing:	Easy integration with xUnit, Moq, etc. for unit and integration testing
Hot reload support:	Fast feedback during development
Strong ecosystem:	Rich set of libraries, NuGet packages, and community support

3)  How ASP.NET Works?
   
- Request Pipeline
ASP.NET uses a middleware-based request pipeline, which means every HTTP request passes through a sequence of components:
Client Request
    ↓
Kestrel (Web Server)
    ↓
Middleware (Authentication, Routing, etc.)
    ↓
Endpoint (Controller / Minimal API / Razor Page)
    ↓
Response Sent Back

-  Core Concepts:
- Kestrel: A fast, cross-platform web server used by ASP.NET.
- Middleware: Components added in Program.cs to handle authentication, logging, routing, etc.
- Routing: Maps HTTP requests to endpoints (MapGet, MapPost, Controllers).
- Controllers / Endpoints: Your business logic lives here.
- Dependency Injection: Services are registered in Program.cs and injected via constructors.

-  Code Example :
var builder = WebApplication.CreateBuilder(args);

// Register services
builder.Services.AddControllers();

var app = builder.Build();

// Middleware setup
app.UseRouting();
app.UseAuthorization();

app.MapControllers(); // Enable controller routing

app.Run();

4) When to Use ASP.NET:
   
- Building enterprise-grade APIs or microservices.
- Creating web UIs with Razor Pages or Blazor.
- Integrating with Microsoft tools (Azure, Identity, etc.).
- Developing scalable apps that must run on multiple platforms.
