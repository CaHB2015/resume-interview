# Output Templates

Templates and examples for generating interview-oriented project outputs.

## 1. Resume Project Experience (项目经历)

### Data Disclaimer (MUST appear in every output)

Every output document MUST begin with the following disclaimer:

> **数据说明**：以下项目经历中的性能指标（响应时间、QPS、命中率等）为基于技术方案的合理估算值，仅供参考。请根据你的项目实际情况进行调整后再写入简历。面试时请确保能解释数据的来源和测量方法。


### CRITICAL RULES (READ BEFORE GENERATING)

1. **4-6 bullets ONLY**
2. **Each bullet = ONE technical highlight** (never combine multiple)
3. **Each bullet <= 2 sentences, <= 100 Chinese characters**
4. **Each bullet MUST include data** (percentage, latency, QPS, etc.)
5. **Structure**: Business Scenario + Technical Solution + Specific Action + Data Result

### Template

```
**Project Name**: [Domain] + [Core Tech]

**Tech Stack**: Tech1 | Tech2 | Tech3 | Tech4

**Project Experience**:
- [Business Scenario] + [Technical Solution] + [Specific Action] + [Data Result]
- [Business Scenario] + [Technical Solution] + [Specific Action] + [Data Result]
- [Business Scenario] + [Technical Solution] + [Specific Action] + [Data Result]
- [Business Scenario] + [Technical Solution] + [Specific Action] + [Data Result]
```

### Good Examples

**Example 1: Campus Second-hand Trading Platform (Spring Boot + MySQL + Redis + JWT)**

> **Project Name**: Campus Second-hand Trading Platform
>
> **Tech Stack**: Spring Boot, MySQL, Redis, Spring Security, JWT, Docker
>
> **Project Experience**:
> - 负责商品查询链路优化，构建 Redis + MySQL 数据访问架构，对热点商品数据进行缓存预热与动态更新，商品列表查询响应时间从 120ms 降至 15ms，数据库 QPS 压力降低约 70%
> - 围绕高并发查询场景设计缓存治理方案，结合布隆过滤器、逻辑过期及互斥锁机制应对缓存穿透、缓存击穿与缓存雪崩问题，缓存命中率从 75% 提升至 95%，异常请求率下降约 80%
> - 设计统一身份认证与权限控制体系，基于 JWT + Spring Security 实现无状态鉴权方案，并构建 RBAC 权限模型完成接口级访问控制，支持 5 种角色、30+ 接口的细粒度权限管理
> - 负责订单核心链路设计，围绕订单创建、支付、取消等业务流程建立状态流转机制，覆盖 6 种订单状态、12 种状态流转路径，异常订单处理效率提升约 60%
> - 基于业务访问模式优化数据库结构，设计联合索引与覆盖索引方案，通过 Explain 分析执行计划定位并优化慢查询问题，核心查询 SQL 执行时间从 200ms 降至 8ms，慢查询数量减少 90%

**Example 2: AI Stock Analysis System (Spring Boot + FastAPI + Redis Streams + Milvus)**

> **Project Name**: AI Agent-driven Smart Stock Analysis System
>
> **Tech Stack**: Spring Boot, FastAPI, Redis Streams, MySQL, Milvus, Docker
>
> **Project Experience**:
> - 负责视频分析流程编排，基于 Redis Streams 实现双后端异步任务分发，采用 Consumer Group 模式保证消息不重复消费，任务吞吐量提升约 60%，支持多 Worker 水平扩展
> - 设计 LLM Gateway 统一模型调度网关，实现三档模型自动降级策略（Simple/Medium/Complex），配合指数退避重试机制，模型调用成功率从 85% 提升至 99.2%
> - 负责置信度计算引擎开发，基于四维度加权评分模型（历史准确率 40% + 近 30 天准确率 30% + 收益风险比 20% + 稳定性 10%），映射 AAA~C 五级置信度等级，批量计算效率提升约 80%
> - 集成 Milvus 向量数据库构建博主记忆系统，存储视频转写文本的 384 维 Embedding 向量，支持语义检索和按博主过滤，历史观点匹配准确率达到 92%
> - 设计 JWT 双令牌认证体系，Access Token 有效期 2 小时 + Refresh Token 有效期 7 天，基于 HandlerInterceptor 实现请求拦截鉴权，认证响应时间 < 30ms

### Bad Examples (NEVER generate these)

BAD 1 - Too long, lists multiple features (实际生成的问题):
"负责 SpringBoot 业务层架构设计与实现，基于三层架构（Controller / Service / Mapper）构建用户认证、视频分析流程编排、博主管理、付费权限等核心模块，使用 MyBatis Plus 简化数据访问层，统一封装 Result<T> 响应体和 ErrorCode 错误码体系，通过 @RestControllerAdvice 实现全局异常处理，覆盖参数校验、业务异常、认证异常等 8 类异常场景。"

BAD 2 - No data:
"负责 JWT 认证体系设计，实现 Access Token + Refresh Token 双令牌机制。"

BAD 3 - Vague:
"使用 Redis 提升了系统性能。"

BAD 4 - Feature list:
"实现了用户管理、订单管理、商品管理、支付管理等功能。"

## 2. Project Self Introduction (项目自我介绍)

### 30 Seconds Template

```
我负责开发了一个[项目领域]系统，采用[核心技术栈]。主要工作是[核心工作1]，以及[核心工作2]。
```

**Example**:
> 我负责开发了一个校园二手交易平台，采用 Spring Boot + MySQL + Redis 技术栈。主要工作是设计了基于 Redis 的商品查询缓存架构，以及基于 JWT 的无状态认证方案。

### 1 Minute Template

```
我负责开发了一个[项目领域]系统。

技术上采用[技术栈]，[架构概述]。

在[技术点1]上，我[具体做法1]，[效果1]。

在[技术点2]上，我[具体做法2]，[效果2]。

[整体架构/其他亮点]。
```

**Example**:
> 我负责开发了一个校园二手交易平台。
>
> 技术上采用 Spring Boot 作为后端框架，MySQL 存储数据，Redis 做热点缓存，JWT 实现认证。
>
> 在缓存设计上，我引入了布隆过滤器防止缓存穿透，逻辑过期防止缓存击穿，互斥重建防止缓存雪崩，缓存命中率从 75% 提升到 95%。
>
> 在认证授权上，我设计了基于 JWT 的无状态认证方案，结合 Spring Security 实现 RBAC 权限控制，支持 5 种角色、30+ 接口的细粒度管理。
>
> 数据库层面，通过索引优化和 Explain 分析，核心查询 SQL 执行时间从 200ms 降至 8ms。

### 3 Minutes Template

```
我负责开发了一个[项目领域]系统。

**业务背景**：[业务需求和挑战]。

**架构设计**：采用[技术栈]，整体采用[架构模式]。

**技术挑战与解决方案**：
1. [技术点1]：[问题] + [方案] + [效果]
2. [技术点2]：[问题] + [方案] + [效果]
3. [技术点3]：[问题] + [方案] + [效果]

**技术成果**：[量化成果总结]。

**技术成长**：[个人技术提升]。
```

## 3. Interview Question Bank (面试题库)

### Template

```
**[Category]**

| Question | Why Asked | Answer Direction | Follow-up | Difficulty |
|----------|-----------|------------------|-----------|------------|
| [Question] | [Why] | [Direction] | [Follow-up] | ⭐⭐⭐ |
```

### Example (Redis)

```
| Question | Why Asked | Answer Direction | Follow-up | Difficulty |
|----------|-----------|------------------|-----------|------------|
| Why Redis for caching? | Tech selection ability | Performance, data structures, persistence, clustering | Why not local cache? | ⭐⭐ |
| How to solve cache penetration? | Cache governance | Bloom filter, empty value cache | Bloom filter principle? False positive rate? | ⭐⭐⭐ |
| How to solve cache breakdown? | High concurrency design | Mutex lock, logical expiration | Logical expiration implementation details? | ⭐⭐⭐ |
| How to solve cache avalanche? | System stability | Random TTL, multi-level cache, rate limiting | Multi-level cache architecture? | ⭐⭐⭐ |
| How to maintain cache consistency? | Data consistency | Cache Aside, delayed double delete | Delayed double delete timing issues? | ⭐⭐⭐⭐ |
```

## 4. Follow-Up Trees (追问树)

### Template

```
[Root Question]
├── [Follow-up 1]
│   ├── [Deep follow-up 1.1]
│   │   ├── [Detail 1.1.1]
│   │   └── [Detail 1.1.2]
│   └── [Deep follow-up 1.2]
├── [Follow-up 2]
│   └── [Deep follow-up 2.1]
└── [Follow-up 3]
```

## 5. Upgrade Roadmap (升级路线图)

### Template

```
| Technology | JD Frequency | Current Project | Priority | Suggestion |
|------------|--------------|-----------------|----------|------------|
| [Tech] | ⭐⭐⭐⭐⭐ | Yes/No | High/Med/Low | [Suggestion] |
```