# Technical documentation

## .NET

- [ASP.NET](asp.net/asp.net.md)
  - [SignalR](asp.net/signalr.md)
- C#
  - Boxing and unboxing
  - [Access modifiers](/csharp/access%20modifiers.md)
  - [Asynchronous programming](/csharp/asynchronous%20programming.md)
    - [Async/await best practices](/csharp/asynchronous/async%20await%20best%20practices.md)
    - [Exceptions](/csharp/asynchronous/exceptions.md)
    - [Execution Context](/csharp/asynchronous/execution%20context.md)
    - [Synchronization context](/csharp/asynchronous/synchronization%20context.md)
    - [Task scheduler](/csharp/asynchronous/task%20scheduler.md)
  - [Attributes](/csharp/attributes.md)
    - [Nullable static analysis attributes](/csharp/nullable%20static%20analysis%20attributes.md)
  - [Constructor execution order](/csharp/constructor%20execution%20order.md)
  - [Covariance and contravariance](/csharp/covariance%20and%20contravariance.md)
  - [Keywords](csharp/keywords/keywords.md)
    - Contextual keywords
      - [yield](csharp/keywords/yield.md)
  - [Lambda expressions](/csharp/lambda%20expressions.md)
  - [Nullable reference types](/csharp/nullable%20reference%20types.md)
  - Operators and expressions
    - [Equality operator](/csharp/equality%20operator.md)
  - [Reflection](/csharp/reflection.md)
  - TPL
    - [↑ Task-based asynchronous pattern](https://docs.microsoft.com/en-us/dotnet/standard/asynchronous-programming-patterns/task-based-asynchronous-pattern-tap)
    - [Reporting task progress](/csharp/asynchronous/reporting%20progress.md)
  - [Tricks](/csharp/tricks.md)
  - [↑ Document your code with XML comments](https://docs.microsoft.com/en-us/dotnet/csharp/codedoc)
  - [↑ Local functions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/local-functions)
- .NET API
  - System
    - Classes
      - Array
      - [Delegate](dotnet/system/delegate/delegate.md)
        - Action\<T>
        - Func\<TResult>
        - [Event](dotnet/system/delegate/event.md)
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
          - [Equals](dotnet/system/object/equals.md)
          - [GetType](dotnet/system//object/getType.md)
          - [ToString](dotnet/system/object/toString.md)
          - [Finalize](dotnet/system/object/finalize.md)
          - [MemberwiseClone](dotnet/system/object/memberwiseClone.md)
          - [ReferenceEquals](dotnet/system/object/referenceEquals.md)
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
  - System.Collections.Generic
    - Classes
      - [Dictionary](dotnet/system/collections/generic/dictionary.md)
    - Interfaces
      - [IAsyncEnumerable\<T>](dotnet/system/collections/generic/iasyncenumerable.md)
  - System.IO
    - FileStream
    - MemoryStream
  - System.Linq
    - [Expression tree](dotnet/system/linq/expression%20tree.md)
    - Interfaces
      - [IQueryable\<T>](dotnet/system/linq/iqueryable.md)
  - System.Threading
    - [Task Parallel Library (TPL)](dotnet/system/threading/tpl.md)
    - Classes
      - Interlocked
      - Monitor
      - Mutex
      - ReaderWriterLock
      - ReaderWriterSlimLock
      - Semaphore
      - SynchronizationContext
      - [Thread](dotnet/system/threading/thread.md)
      - [ThreadPool](dotnet/system/threading/threadpool.md)
    - Structs
      - CancellationToken
      - SpinLock
      - SpinWait
  - System.Threading.Tasks
    - Classes
      - Parallel
      - [Task](dotnet/system/threading/tasks/task/task.md)
        - [Properties](dotnet/system/threading/tasks/task/properties.md)
      - [Task\<TResult>](dotnet/system/threading/tasks/task_t/task.md)
      - TaskFactory
- CLR
  - Memory managment
    - Garbage collector (GC)
    - Managed heap
      - Small object heap (SOH)
  - Just-in-time (JIT) compilation

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
- [Object-oriented programming (OOP)](computer%20science/oop.md)

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

- [Ansible](programming/ansible/ansible.md)
- [Docker](programming/docker/docker.md)
  - [Docker Compose](programming/docker/compose.md)
- [Git](programming/git/git.md)
  - Git flows
    - [Ветки](programming/git/branches.md)
      - [Релиз](programming/git/release.md)
      - [Именование релизных веток](programming/git/branch%20names.md)
- Kubernetes
  - [Creating cluster steps](programming/kubernetes/creating%20cluster.md)
  - [Kubernetes components](programming/kubernetes/components.md)
  - [kubectl](programming/kubernetes/kubectl.md)
  - [Minikube](programming/kubernetes/minikube.md)
    - Learning basics
      - [Create a Kubernetes cluster](programming/kubernetes/create%20cluster.md)
      - [Deploy an app](programming/kubernetes/deply%20app.md)
      - [Explore your app](programming/kubernetes/explore%20app.md)
      - [Expose your app publicly](programming/kubernetes/expose%20app.md)
      - [Scale your app](programming/kubernetes/scale.md)
      - [Update your app](programming/kubernetes/update.md)
- [Microservices](programming/microservices.md)
  - [↑ API Gateway](https://www.nginx.com/blog/building-microservices-using-an-api-gateway)
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
- [Nginx](unix/nginx.md)
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
      - [chown](unix/chown.md)
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
- [User management](unix/user%20managment.md)

## Web

- [CSS](web/css/css.md)
- [CORS](web/cors.md)
- [gRPC](web/grpc.md)
- [HTML](web/html/html.md)
- [↑ HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP)
  - [HTTP headers](web/http%20headers.md)
- [JavaScript](web/javascript/javascript.md)
- [JSON Web Token (JWT)](web/jwt.md)
- [OAuth 2.0](web/oauth.md)
- [↑ OpenAPI 3.0](https://swagger.io/blog/news/whats-new-in-openapi-3-0)
- [React](web/react/react.md)
- [REST](web/rest.md)
- Security
  - CSRF
  - XSS
- [Web APIs](web/api/api.md)
- [WebSocket](websocket.md)
