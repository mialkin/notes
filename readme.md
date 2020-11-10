# Technical documentation

[Knowledge map (SVG)](https://raw.githubusercontent.com/mialkin/documentation/master/knowledge%20map.svg)

[Перевод технических терминов](translation.md)

## .NET

- C#
  - Boxing and unboxing
  - [Access modifiers](dotnet/csharp/access%20modifiers.md)
  - [Asynchronous programming](dotnet/csharp/asynchronous%20programming.md)
    - [Async/await best practices](dotnet/csharp/asynchronous/async%20await%20best%20practices.md)
    - [Exceptions](dotnet/csharp/asynchronous/exceptions.md)
    - [Execution Context](dotnet/csharp/asynchronous/execution%20context.md)
    - [Synchronization context](dotnet/csharp/asynchronous/synchronization%20context.md)
    - [Task scheduler](dotnet/csharp/asynchronous/task%20scheduler.md)
  - [Attributes](dotnet/csharp/attributes.md)
    - [Nullable static analysis attributes](dotnet/csharp/nullable%20static%20analysis%20attributes.md)
  - [Constructor execution order](dotnet/csharp/constructor%20execution%20order.md)
  - [Covariance and contravariance](dotnet/csharp/covariance%20and%20contravariance.md)
  - [Lambda expressions](dotnet/csharp/lambda%20expressions.md)
  - [Nullable reference types](dotnet/csharp/nullable%20reference%20types.md)
  - Operators and expressions
    - [Equality operator](dotnet/csharp/equality%20operator.md)
  - [Reflection](dotnet/csharp/reflection.md)
  - TPL
    - [↑ Task-based asynchronous pattern](https://docs.microsoft.com/en-us/dotnet/standard/asynchronous-programming-patterns/task-based-asynchronous-pattern-tap)
    - [Reporting task progress](dotnet/csharp/asynchronous/reporting%20progress.md)
  - [Tricks](dotnet/csharp/tricks.md)
  - [↑ Document your code with XML comments](https://docs.microsoft.com/en-us/dotnet/csharp/codedoc)
  - [↑ Local functions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/local-functions)
- .NET API
  - System
    - Classes
      - Array
      - [Delegate](dotnet/api/system/delegate/delegate.md)
        - Action\<T>
        - Func\<TResult>
        - [Event](dotnet/api/system/delegate/event.md)
      - Exception
      - GC
        - Properties
          - MaxGeneration
        - Methods
          - Collect(Int32)
          - CollectionCount(Int32)
          - GetGeneration(Object)
          - GetTotalMemory(Boolean)
          - SuppressFinalize(Object)
          - WaitForPendingFinalizers()
      - Lazy\<T>
      - MarshalByRefObject
      - Object
        - Methods
          - [Equals](dotnet/api/system/object/equals.md)
          - [GetType](dotnet/api/system//object/getType.md)
          - [ToString](dotnet/api/system/object/toString.md)
          - [Finalize](dotnet/api/system/object/finalize.md)
          - [MemberwiseClone](dotnet/api/system/object/memberwiseClone.md)
          - [ReferenceEquals](dotnet/api/system/object/referenceEquals.md)
      - String
      - Tuple\<T1>
      - ValueType
        - Enum
        - Guid
        - Nullable\<T>
    - Enums
    - Interfaces
      - IComparable\<T>
      - ICloneable
      - IDisposable
    - Structs
  - System.Collections.Concurrent
    - ConcurrentDictionary\<T>
    - ConcurrentQueue\<T>
    - ConcurrentStack\<T>
  - System.IO
    - FileStream
    - MemoryStream
  - System.Linq
    - [Expression tree](dotnet/api/system/linq/expression%20tree.md)
    - Interfaces
      - [IQueryable\<T>](dotnet/api/system/linq/iqueryable.md)
  - System.Threading
    - [Task Parallel Library (TPL)](dotnet/api/system/threading/tpl.md)
    - Classes
      - Interlocked
      - Monitor
      - Mutex
      - ReaderWriterLock
      - ReaderWriterSlimLock
      - Semaphore
      - SynchronizationContext
      - [Thread](dotnet/api/system/threading/thread.md)
      - [ThreadPool](dotnet/api/system/threading/threadpool.md)
    - Structs
      - CancellationToken
      - SpinLock
      - SpinWait
  - System.Threading.Tasks
    - Classes
      - Parallel
      - [Task](dotnet/api/system/threading/tasks/task/task.md)
        - [Properties](dotnet/api/system/threading/tasks/task/properties.md)
      - [Task\<TResult>](dotnet/api/system/threading/tasks/task_t/task.md)
      - TaskFactory
- .NET Core
  - CoreCLR
    - Memory managment
      - Garbage collector (GC)
      - Managed heap
        - Small object heap (SOH)
    - Just-in-time (JIT) compilation
  - CoreFx
    - [ASP.NET Core](dotnet/asp.net/asp.net%20core.md)
      - Dependency injection
      - Middleware
      - Host
      - Configuration
      - Options
      - Environments
      - [Logging](dotnet/asp.net/logging.md)
      - Routing
      - Security
        - Authentication
        - Authorization
      - [↑ SignalR](https://dotnet.microsoft.com/apps/aspnet/signalr)

## Computer science

- Algorithms
  - Sorting algorithms
    - Insertion sort
    - Selection sort
    - Merge sort
    - Quick sort
    - Bubble sort
  - Analysis of algorithm
    - Time complexity
    - Space complexity
    - Big O notation
- [Asymmetric cryptography](computer%20science/asymmetric%20cryptography.md)
- Data structures
  - Hash-based structures
    - Hash table
    - Hash tree
- Object-oriented programming (OOP)
  - Abstraction
  - Incapsulation
  - Inheritance
  - Polymorphism

## Databases

- ACID
  - Atomicity
  - Consistency
  - Isolation
  - Durability
- Cursor
- Database normalization
- Document databases
  - CouchDB
  - Elasticsearch
  - MongoDB
- Execution plan
- Function
- In-memory databases
  - Memcached
  - Redis
- Relational databases
  - Microsoft SQL Server
  - Oracle Database
  - SQLite
  - [PostgreSQL](db/postgres/postgres.md)
- Stored procedure
- SQL
  - T-SQL
  - [PL/SQL](db/oracle/plsql.md)
- [Terminology](db/terminology.md)
- Transaction
  - Isolation levels
    - Read uncommitted
    - Read commmitted
    - Repeatable read
    - Serializable
- Trigger
- Window function

## Design

- [Design patterns](software%20design/design%20patterns/design%20patterns.md)
- Design principles
  - [Composition over inheritance](software%20design/composition%20over%20inheritance.md)
  - DRY
  - [Explicit Dependencies Principle](software%20design/explicit%20dependencies%20principle.md)
  - Idempotence
  - KISS
  - SOLID
    - Single responsibility principle
    - Open-closed principle
    - Liskov substitution principle
    - Interface segregation principle
    - [Dependency Inversion Principle](software%20design/dependency%20inversion/dependency%20inversion.md)
  - YAGNI
- Unified Modeling Language (UML)
  - Diagrams
    - Class diagram
    - Sequence diagram

## Programming

- [Docker](programming/docker/docker.md)
  - [Docker Compose](programming/docker/compose.md)
- Git
  - Git flows
    - [Ветки](programming/git/branches.md)
      - [Релиз](programming/git/release.md)
      - [Именование релизных веток](programming/git/branch%20names.md)
- [Kubernetes](programming/kubernetes/kubernetes.md)
  - [kubectl](programming/kubernetes/kubectl.md)
- [Microservices](programming/microservices.md)
- [Regular expressions](programming/regular%20expressions/regular%20expressions.md)
- [Telegram bot](programming/telegram/telegram%20bot.md)
- Testing
  - Unit testing
    - [Unit testing best practices](programming/testing/unit%20testing%20best%20practices.md)
  - Integration testing
  - Load testing
  - Stress testing

## Unix

- [Environment variables](unix/environment%20variables.md)
- [macOS](unix/macos/macos.md)
  - [Finder](unix/macos/finder.md)
  - [Jekyll](unix/macos/jekyll.md)
  - [Terminal](unix/macos/terminal.md)
- Linux
  - CentOS
    - [YUM](unix/yum.md)
  - [Ubuntu](unix/ubuntu.md)
    - [APT](unix/apt.md)
- [shell](unix/shell.md)
  - [Bourne again shell (bash)](unix/bash.md)
  - Tools
    - System
      - [crontab](unix/crontab.md)
      - [df](unix/df.md)
      - [du](unix/du.md)
      - [htop](unix/htop.md)
      - [systemctl](unix/systemctl.md)
      - [tmux](unix/tmux.md)
    - Files
      - [chmod](unix/chmod.md)
      - [less](unix/less.md)
      - [rg](unix/rg.md)
      - [tail](unix/tail.md)
      - [tar](unix/tar.md)
      - [vim](unix/vim.md)
    - Network
      - [iproute2](unix/iproute2.md)
      - [rsync](unix/rsync.md)
      - [scp](unix/scp.md)
      - [ssh](unix/ssh.md)
- [Nginx](unix/nginx.md)

## Web

- [CSS](web/css/css.md)
- [gRPC](web/grpc.md)
- [HTML](web/html/html.md)
- [↑ HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP)
- [JavaScript](web/javascript/javascript.md)
- [JSON Web Token (JWT)](web/jwt.md)
- [OAuth 2.0](web/oauth.md)
- [↑ OpenAPI 3.0](https://swagger.io/blog/news/whats-new-in-openapi-3-0)
- [React](web/react/react.md)
- [Representational State Transfer (REST)](rest.md)
- [Web APIs](web/api/api.md)
- [WebSocket](websocket.md)
