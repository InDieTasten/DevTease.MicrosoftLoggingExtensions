Microsoft Logging extensions
============================

## 1. Common Abstraction

Consisting of:

- ILogger<>
- ILoggerProvider
- ILoggerFactory
- ILoggingBuilder

Useful for

- Developers only needing to really learn one abstraction in and out
- Frameworks neatly plugging into the abstraction (easy to replace frameworks)

## 2. See initialization in Program.cs

Configuration by default when creating an ASP.NET Core  page.

## 3. See usage of the ILogger interface in HomeController.cs

- Dependency Injection pattern
- Clean interface

See [here](https://docs.microsoft.com/en-us/dotnet/api/microsoft.extensions.logging.loglevel?view=aspnetcore-2.1)
on when to use what log level

## 4. See configuration in appsettings.(Development).json

Update the minimum log levels for particular categories

## 5. Adding scopes

Snippet for Console logger to show scopes
```json
"Console": {
    "IncludeScopes": "true"
}
```

Using the ILogger.BeginScope in the HomeController.Contact action

## 6. Where to continue

- Structered Logging
- Implement custom providers
- [LoggerMessage pattern](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/logging/loggermessage?view=aspnetcore-2.1)
- EventIds