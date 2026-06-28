# Capability Map

Technology stack to capability mapping. Use this to convert code implementations into interview-ready capability descriptions.

## Backend Framework

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| Spring Boot | Microservice Architecture, Auto Configuration, Dependency Injection | Spring Bean lifecycle, auto-configuration principle, starter mechanism |
| Spring MVC | Web Layer Architecture, Request Handling | DispatcherServlet, HandlerMapping, interceptor mechanism |
| MyBatis / JPA | ORM Design, Data Access Layer | SQL optimization, lazy loading, N+1 problem |
| Spring Cloud | Distributed Architecture, Service Governance | Service discovery, load balancing, circuit breaking, gateway |

## Database

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| MySQL | Relational Database, Index Design, Transaction Management | B+ tree, MVCC, lock mechanism, Explain analysis |
| Redis | Caching Design, Distributed Lock, Session Management | Cache penetration/breakdown/avalanche, data structures, persistence |
| MongoDB | Document Database, Flexible Schema | Aggregation pipeline, index strategy, sharding |
| Elasticsearch | Full-text Search, Log Analysis | Inverted index, analyzer, DSL query |

## Authentication & Authorization

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| JWT | Stateless Authentication, Token Mechanism | Token refresh, payload design, security considerations |
| Spring Security | Authorization Architecture, Access Control | Filter chain, RBAC, method-level security |
| OAuth2 | Third-party Authentication, Authorization Protocol | Authorization code flow, implicit flow, client credentials |
| Shiro | Permission Management, Session Management | Realm, Filter, Session management |

## Message Queue

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| RabbitMQ | Reliable Message Delivery, Async Processing | Message acknowledgment, dead letter queue, delayed queue |
| Kafka | High-throughput Message Stream, Event Sourcing | Partition, consumer group, offset management |
| RocketMQ | Distributed Message, Transaction Message | Message tracing, ordered message, broadcast consumption |

## Deployment & Operations

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| Docker | Containerization, Environment Isolation | Image layering, Dockerfile best practices, container networking |
| Kubernetes | Container Orchestration, Service Management | Pod, Service, Deployment, ConfigMap |
| Jenkins/GitLab CI | CI/CD Pipeline, Automated Deployment | Pipeline design, stage management, artifact management |
| Nginx | Reverse Proxy, Load Balancing | Location matching, upstream configuration, static resource serving |

## Monitoring & Logging

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| ELK Stack | Log Collection, Analysis, Visualization | Filebeat, Logstash pipeline, Kibana dashboard |
| Prometheus + Grafana | Metrics Monitoring, Alerting | PromQL, alert rules, dashboard design |
| SkyWalking | Distributed Tracing, Performance Analysis | Trace, span, agent mechanism |
| Micrometer | Application Metrics, Health Check | Counter, Gauge, Timer, health endpoint |

## Frontend (if applicable)

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| Vue.js / React | Component Architecture, State Management | Virtual DOM, lifecycle, state management (Vuex/Redux) |
| TypeScript | Type Safety, Code Quality | Type inference, generics, utility types |
| Webpack / Vite | Build Tool, Module Bundling | Tree shaking, code splitting, HMR |
| Axios | HTTP Client, API Communication | Interceptors, error handling, request cancellation |

## Architecture Patterns

| Pattern | Capability | Interview Angle |
|---------|-----------|-----------------|
| Microservices | Service Decomposition, Distributed Architecture | Service boundary, communication, data consistency |
| DDD | Domain-Driven Design, Business Modeling | Bounded context, aggregate root, domain event |
| CQRS | Command Query Separation, Read/Write Optimization | Event sourcing, eventual consistency |
| Event-Driven | Async Architecture, Decoupling | Event bus, saga pattern, eventual consistency |

## Python Backend

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| FastAPI | Async Web Framework, Type-safe API Design | ASGI lifecycle, dependency injection, Pydantic validation, async endpoints |
| Django | Full-stack Web Framework, ORM | MTV pattern, QuerySet optimization, middleware chain, admin system |
| Flask | Lightweight Web Framework | WSGI, Blueprint modular design, extension ecosystem |
| SQLAlchemy | ORM, Database Abstraction | Session management, relationship loading (lazy/eager), migration (Alembic) |
| Celery | Distributed Task Queue | Broker (Redis/RabbitMQ), task retry, result backend, periodic tasks |

## Go Backend

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| Gin | High-performance HTTP Framework | Router (radix tree), middleware chain, context management, binding/validation |
| Echo | Minimalist Web Framework | Handler, data binder, custom middleware, error handling |
| gRPC | RPC Framework, Service Communication | Protobuf serialization, streaming modes, interceptor, service mesh integration |
| Go-Zero | Microservice Framework | Service discovery, rate limiting, circuit breaker, code generation |
| GORM | ORM for Go | Auto migration, association handling, scopes, hooks |

## AI / ML

| Technology | Capability | Interview Angle |
|-----------|-----------|-----------------|
| PyTorch | Deep Learning Framework | Autograd, dynamic computation graph, model export (ONNX), distributed training |
| LangChain | LLM Application Framework | Chain composition, Agent reasoning, RAG pipeline, memory management |
| Vector Database (Milvus/Pinecone/Weaviate) | Semantic Search, RAG Infrastructure | Embedding indexing, ANN algorithm (HNSW/IVF), metadata filtering |
| FastAPI + Model Serving | ML Model Deployment | Async inference, batch processing, model versioning, health check |
| Prompt Engineering | LLM Interaction Design | Few-shot, chain-of-thought, structured output, token optimization |
