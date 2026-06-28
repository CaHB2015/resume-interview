# Interview Topics Map

Capability to interview topic mapping. Use this to generate interview questions and follow-up trees.

## Redis

### Cache Problems
- **Cache Penetration**: Query non-existent data, bypass cache to DB. Solution: Bloom filter, empty value cache.
- **Cache Breakdown**: Hot key expires, concurrent requests hit DB. Solution: Mutex lock, logical expiration.
- **Cache Avalanche**: Mass keys expire simultaneously. Solution: Random TTL, multi-level cache, rate limiting.
- **Hot Key**: Single key has extremely high QPS. Solution: Local cache, key replication, read/write separation.

### Data Structures
- **String**: Counter, distributed lock, session cache.
- **Hash**: Object storage, shopping cart.
- **List**: Message queue, latest feed.
- **Set**: Tag system, friend relationship, intersection/union.
- **Sorted Set**: Leaderboard, delay queue, range query.

### Persistence
- **RDB**: Point-in-time snapshot, fork process, suitable for backup.
- **AOF**: Append-only log, fsync strategy, data security.
- **Hybrid**: RDB + AOF, fast recovery + data security.

### High Availability
- **Master-Slave Replication**: Full sync, incremental sync, replication offset.
- **Sentinel**: Automatic failover, leader election, client notification.
- **Cluster**: Hash slot, data sharding, resharding.

### Distributed Lock
- **SETNX**: Single instance lock, expiration time, Lua script atomicity.
- **Redlock**: Multi-node lock, majority consensus, clock drift problem.

## MySQL

### Index
- **B+ Tree**: Leaf node linked list, range query, disk IO optimization.
- **Clustered Index**: Primary key index, data storage order.
- **Secondary Index**: Non-primary key index, back to table lookup.
- **Covering Index**: Index contains query fields, avoid back to table.
- **联合索引**: Leftmost prefix, index pushdown.
- **Index Failure**: Function on column, implicit type conversion, OR condition, LIKE prefix.

### Transaction
- **ACID**: Atomicity, Consistency, Isolation, Durability.
- **Isolation Levels**: Read Uncommitted, Read Committed, Repeatable Read, Serializable.
- **MVCC**: Read view, undo log, version chain, consistent read.
- **Lock**: Shared lock, exclusive lock, intention lock, gap lock, next-key lock.

### Performance
- **Explain**: type, key, rows, Extra, filtered.
- **Slow Query**: slow_query_log, long_query_time, mysqldumpslow.
- **Query Optimization**: Avoid SELECT *, batch insert, pagination optimization.

### Architecture
- **Master-Slave Replication**: Binary log, relay log, semi-sync.
- **Read-Write Separation**: Proxy-based, application-based.
- **Sharding**: Horizontal split, distributed ID, cross-shard query.

## Spring Boot

### Core Principles
- **Auto Configuration**: spring.factories, @Conditional, starter mechanism.
- **IoC Container**: Bean lifecycle, scope, dependency injection.
- **AOP**: Proxy pattern, aspect, advice types, execution expression.

### Web Layer
- **DispatcherServlet**: Request handling flow, handler mapping, view resolver.
- **Interceptor**: PreHandle, postHandle, afterCompletion, execution order.
- **Global Exception Handling**: @ControllerAdvice, @ExceptionHandler, custom exception.

### Data Access
- **Transaction Management**: @Transactional, propagation, isolation, rollback rules.
- **Connection Pool**: HikariCP configuration, pool sizing, monitoring.
- **Multi-DataSource**: Dynamic routing, @DS annotation, transaction consistency.

## JWT & Security

### JWT
- **Structure**: Header, Payload, Signature.
- **Stateless Authentication**: Token generation, validation, refresh mechanism.
- **Security**: Token storage (HttpOnly cookie vs localStorage), XSS/CSRF protection.
- **Token Refresh**: Access token + refresh token, sliding expiration.

### Spring Security
- **Filter Chain**: SecurityFilterChain, authentication filter, authorization filter.
- **RBAC**: Role-based access control, method-level security, URL-level security.
- **Password Encoding**: BCrypt, salt mechanism, password policy.

## RabbitMQ

### Reliability
- **Publisher Confirm**: Async confirm, return callback, retry mechanism.
- **Consumer Ack**: Manual ack, retry strategy, dead letter queue.
- **Message Persistence**: Queue persistence, message persistence, lazy queue.

### Patterns
- **Work Queue**: Fair dispatch, prefetch, multiple consumers.
- **Pub/Sub**: Fanout exchange, broadcast consumption.
- **Routing**: Direct exchange, topic exchange, header exchange.
- **Dead Letter Queue**: TTL, max-length, rejection, delayed processing.
- **Delayed Queue**: TTL + dead letter, delayed plugin.

### Common Problems
- **Duplicate Consumption**: Idempotency, deduplication table, Redis SETNX.
- **Message Ordering**: Single queue, partition key, consumer serialization.
- **Message Accumulation**: Consumer scaling, memory alert, flow control.

## Docker & Deployment

### Docker
- **Image**: Multi-stage build, layer caching, minimal base image.
- **Container**: Resource limits, health check, log management.
- **Networking**: Bridge, host, overlay, port mapping.
- **Compose**: Multi-container orchestration, dependency, environment variable.

### CI/CD
- **Pipeline**: Build, test, deploy stages, artifact management.
- **Blue-Green Deployment**: Zero-downtime, traffic switching, rollback.
- **Canary Release**: Gradual rollout, A/B testing, monitoring.

## System Design

### Scalability
- **Horizontal Scaling**: Stateless design, session externalization, load balancing.
- **Vertical Scaling**: Database optimization, caching, async processing.
- **Database Scaling**: Read replicas, sharding, CQRS.

### Reliability
- **Circuit Breaker**: Hystrix, Resilience4j, failure threshold, half-open state.
- **Rate Limiting**: Token bucket, sliding window, distributed rate limiting.
- **Retry**: Exponential backoff, jitter, max retry, idempotency.

### Performance
- **Caching Strategy**: Cache aside, read/write through, write behind.
- **Async Processing**: Message queue, event-driven, eventual consistency.
- **Connection Pooling**: Database, HTTP client, thread pool sizing.

## Python (FastAPI / Django)

### Async Programming
- **asyncio**: Event loop, coroutine, task scheduling, `async/await` semantics.
- **ASGI vs WSGI**: Asynchronous request handling, concurrent connections, Uvicorn/Gunicorn.
- **Async ORM**: AsyncSession, database driver compatibility, connection pooling.

### Type Safety & Validation
- **Pydantic**: Model validation, field validators, nested models, JSON schema generation.
- **Type Hints**: Generic types, Protocol, TypeVar, runtime vs static checking.

### Framework Internals
- **FastAPI Depends**: Dependency injection, yield dependencies, nested dependencies, caching.
- **Django ORM**: QuerySet lazy evaluation, N+1 problem (`select_related`/`prefetch_related`), database migration.
- **Middleware**: ASGI middleware, request/response interception, CORS, authentication middleware.

### Task Queue
- **Celery**: Broker selection (Redis vs RabbitMQ), task serialization, retry policy, rate limiting.
- **Periodic Tasks**: Celery Beat, crontab schedule, distributed lock for periodic tasks.

## Go

### Concurrency Model
- **Goroutine**: Lightweight thread, GMP scheduling model, goroutine leak detection.
- **Channel**: Buffered vs unbuffered, select statement, channel direction, close semantics.
- **Sync Primitives**: `sync.Mutex`, `sync.RWMutex`, `sync.WaitGroup`, `sync.Once`, `atomic`.
- **Context**: `context.WithTimeout`, `context.WithCancel`, cancellation propagation, value passing.

### Memory Management
- **Escape Analysis**: Stack vs heap allocation, compiler decision, `go build -gcflags=-m`.
- **GC**: Tri-color marking, write barrier, GC tuning (`GOGC`), STW minimization.
- **Slice vs Array**: Slice header (ptr/len/cap), append growth strategy, memory leak with subslicing.

### Interface & Reflection
- **Interface**: Implicit implementation (duck typing), empty interface `any`, type assertion vs type switch.
- **Reflection**: `reflect.Type`, `reflect.Value`, performance cost, use cases (serialization, ORM).

### HTTP & Web
- **Gin Router**: Radix tree, route grouping, parameter binding, custom validator.
- **Middleware Pattern**: `func(http.Handler) http.Handler`, chaining, recovery middleware.
- **Connection Management**: Keep-alive, idle connection pool, timeout configuration.

## Vue.js / React (Frontend)

### Core Concepts
- **Virtual DOM**: Diff algorithm, reconciliation, key prop importance, patch process.
- **Component Lifecycle**: Vue (setup/onMounted/onUnmounted) vs React (useEffect cleanup), side effect management.
- **Reactivity**: Vue 3 Proxy-based reactivity, React useState/useReducer, stale closure problem.

### State Management
- **Vuex/Pinia**: Module design, actions vs mutations, Pinia composition API style.
- **Redux/Zustand**: Reducer pattern, middleware (thunk/slice), Zustand simplicity vs Redux Toolkit.
- **Cross-component Communication**: Props drilling, provide/inject, Context, event bus.

### Performance Optimization
- **Lazy Loading**: Route-level code splitting, dynamic import, Suspense/defineAsyncComponent.
- **Rendering Optimization**: Vue `v-once`/`v-memo`, React `memo`/`useMemo`/`useCallback`.
- **Bundle Optimization**: Tree shaking, code splitting, chunk strategy, gzip compression.

### Engineering
- **Build Tools**: Vite (ESM + esbuild) vs Webpack (bundle-based), HMR principle, plugin system.
- **TypeScript**: Generic components, utility types, type-safe routes, discriminated unions.
- **Testing**: Vitest/Jest unit tests, component testing (Vue Test Utils / React Testing Library), E2E (Playwright).
