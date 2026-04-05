# Domain-Sovereign Architecture (DSA) v5
**Author:** Bilal Mahmud  
**Date:** 2026-04-06  
**Version:** 5.0  
**Status:** Definitive Methodology Document

---

## Part 1 — The Argument

Software does not fail first because its frameworks are old, its endpoints are too many, or its infrastructure is badly arranged. It fails earlier than that. It fails when the truth of the business is fragmented across technical layers and left to be coordinated by human memory. A unit that should be governed as one thing is broken apart: its meaning lives in a model, its visibility rules in a frontend conditional, its operational consequences in controllers and listeners, its persistence shape in ORM configuration, its integrations in adapters, its search behavior in query code. No single place contains the whole. No single authority defines the terms. The system still runs, but it runs by scattered agreement. That is where the real failures begin: security vulnerabilities because who may see what was decided ad hoc at the screen that happened to render it; purposeless processes because operations execute without the consequences that give them business meaning; drifting truth because rules change in one layer and remain fossilized in another. These are not incidental defects. They are the structural result of distributing business truth across layers that were never qualified to own it.

Datum Theory names the deeper reality that conventional architecture fragments. A meaningful unit of software reality is not merely a record, a class, a field, or a component. It is a Datum: the least atomic unit that still retains business identity, and it exists simultaneously in three dimensions. It has a semantic dimension, which answers what it is. It has a presentational dimension, which governs how it appears to different actors and under what conditions. It has an operational dimension, which governs how it lives, changes, persists, reacts, and participates in processes. These dimensions are not optional, and they are not created by architecture. They are already there. Conventional architecture does not invent them; it only fragments them. Datum Theory therefore does not begin with code structure. It begins with ontology: software contains meaningful units whose truth is inherently three-dimensional. Once that is seen clearly, the architectural consequences are unavoidable.

Domain-Sovereign Architecture is the governance doctrine that follows when Datum Theory is taken seriously as an architectural principle. DSA does not merely argue that the domain should be important, or central, or carefully modeled. It makes a stronger claim: the domain must be sovereign over all three dimensions of every Datum in the system. Sovereignty means authority, not proximity. The domain does not merely sit near the truth. It defines the terms on which truth is expressed everywhere else. It governs what a thing is, how it may be seen, how it may be changed, what it causes when it changes, how it is stored, how it is searched, how it is admitted from outside the system boundary, and how any consumer is allowed to interact with it. Infrastructure does not negotiate these terms. It serves them.

This is the point at which DSA departs decisively from conventional Domain-Driven Design. DDD was a major correction to shallow software thinking because it insisted that the domain must be modeled faithfully and that business meaning cannot be reduced to technical convenience. But DDD, in practice and often in principle, stopped at semantic protection. It defended meaning while leaving presentation to UI layers and persistence to infrastructure layers, hoping disciplined design would keep them aligned. Datum Theory exposes the incompleteness of that settlement. Meaning alone is not enough. A meaningful software unit also has a governed visible life and a governed operational life. DSA therefore extends DDD beyond semantic modeling into full-dimensional governance. DDD protected what a thing means. DSA insists that the same authority must govern what that thing means, how it appears, and how it acts. That is why DSA is not a mere variant of DDD. It is DDD carried to its logical conclusion under the ontology of the Datum.

From that claim, the visible features of DSA follow as consequences rather than preferences. Contract-driven UI is not a clever frontend pattern. It is what must happen if the presentational dimension of a Datum belongs to the domain. If who may see a field, who may edit it, what actions are available, and how a screen differs by role are all expressions of business truth, then the frontend has no right to invent them. It must render what the domain governs. A web client, a mobile application, an admin panel, a printable document, or any future consumer may differ as delivery surfaces, but none of them may assume authority over presentational truth. They are renderers of domain contracts. In DSA, presentation is not delegated; it is served.

The same is true of routing and process entry. A single entry-point API is not a stunt and not a minimalist aesthetic. It is the transport consequence of domain sovereignty. If the domain governs what operations exist, what they mean, and how requests should be interpreted, then the API layer does not need to become a second architecture full of business-shaped controllers. It needs only to receive a request, construct a context, hand it to the domain-governed dispatcher, and return the result. The controller becomes transport. The registry becomes a manifestation of governed operational truth. Multiple routes and multiple controllers are not forbidden by physics; they are rendered unnecessary by a more authoritative domain. Once the domain owns process meaning, the API has no legitimate work left except transport and security.

The same principle reaches persistence. In conventional systems, persistence shape is quietly dictated by infrastructure and then treated as if the domain should adapt to it. DSA rejects that inversion. If a Datum governs its operational dimension, then its persistence shape is not an accidental detail of the ORM. It is part of the terms under which that Datum exists in software reality. The entity defines what must be persisted and how it is identified. Infrastructure stores it, but it does not define it. The model becomes descriptive rather than authoritative. The repository becomes an adapter rather than a co-author. The database remains real, important, and necessary, but it is demoted from source of truth to servant of truth. This is what sovereignty means in practice: infrastructure is free to optimize, scale, swap technologies, and evolve its mechanisms, but it is not free to redefine the business reality it stores.

DSA also changes how external integrations are understood. External providers, federated search, imported data, and third-party APIs are usually treated as integration problems first and domain problems second. DSA reverses that order. The domain defines what external data must mean when admitted into the system, what shape it must take to count as relevant, how it should be merged with owned data, what counts as duplication, what sorts are meaningful, and which source outranks which when truth conflicts. Integration is therefore not a hole in sovereignty; it is one of the places sovereignty matters most. The outside world may provide data, but it does not define meaning inside the system. The domain does.

This is why DSA must be stated in uncompromising terms. The domain is not one concern among others. It is the highest authority over business truth. It governs not only meaning and rules, but also the contracts of presentation, persistence, process, integration, and system evolution. Everything else exists downstream of that authority. The UI renders. The API transports. The database stores. External systems provide inputs and effects. Infrastructure remains necessary, but no longer legislative. It is executive. It does not decide what the business reality is. It implements the reality already governed by the domain.

Once built this way, the economic argument is no longer a slogan but a direct consequence of architectural structure. If the domain governs the three dimensions of the system’s meaningful units, then the product can be fully specified before infrastructure is written. Business conversations define semantic truth. Figma and user conversations define presentational truth. Use cases, events, provider contracts, and persistence contracts define operational truth. At that point the product already exists in its highest-value form: not yet deployed, not yet rendered, not yet persisted by a particular stack, but completely described in the only place that matters. What remains is execution. The API becomes thin wiring. The UI becomes contract rendering. Repositories become adapters. Models become table descriptors. Infrastructure work remains real, but its intellectual role changes. It is no longer the place where business truth is invented. It is where business truth is carried into operation.

That is why DSA changes team economics. A system built according to DSA does not require the same repeated business thinking to happen separately in analysis, backend, frontend, and database design. The burden of coordinated truth collapses into one governing asset: the domain. Once that is complete, a small team can build software that would otherwise require large amounts of coordination overhead simply to keep duplicated truth aligned. This is not because developers become trivial. It is because duplicated decision-making is removed from the delivery layers. The intelligence is concentrated where it belongs. The domain is the product. Infrastructure is mechanical execution of that product.

Domain-Sovereign Architecture should therefore be taken seriously not as a style, not as a stricter layering preference, and not as a provocative variant of DDD. It is the governance doctrine implied by Datum Theory. If software is truly composed of meaningful units with semantic, presentational, and operational dimensions, then any architecture that fragments those dimensions and distributes their authority across layers is structurally unsound. DSA answers that unsoundness directly. It restores unified authority to the only place qualified to hold it: the domain. And once that move is made, the rest of the architecture becomes clear, smaller, cheaper, and more honest.

**Domain-Sovereign Architecture is a software methodology in which the domain becomes the highest authority over business truth, governing not only meaning and rules, but also the contracts of presentation, persistence, process, integration, and system evolution.**

---

## Part 2 — The Foundation

Datum Theory establishes the ontological ground on which DSA stands. It begins from a simple but devastating observation: meaningful software units are treated as if they can be safely fragmented across layers, yet every real system depends on those units remaining coherent. A thing in software is never only what it means. It also appears to different actors under governed conditions, and it also lives, changes, persists, reacts, and participates in processes. These are not implementation details added later by developers. They are already there in the reality of the software. Datum Theory gives that reality a name.

A Datum is the least atomic unit of meaningful software existence. It is the smallest unit that still retains business identity. Below the Datum, there is only raw data. Bits, bytes, strings, and numbers remain real, but they no longer retain the business meaning of the thing itself. The Datum is where meaning remains whole.

Every Datum exists simultaneously in three dimensions. The semantic dimension answers what the Datum is: its identity, invariants, valid states, transitions, relationships, and domain truth. The presentational dimension governs how the Datum appears: who may see it, who may edit it, what form it takes, and how its representation changes by context, role, or state. The operational dimension governs how the Datum lives and reacts: how it is persisted, how it participates in processes, what consequences it produces when acted upon, what events it records, how it is searched, and how it admits external data into its meaning. These dimensions are concurrent. They are not layers, and they are not optional.

Conventional architecture distributes those dimensions across technical surfaces and then asks developers to keep them aligned. That is why business truth drifts. Semantic authority is split between domain models, controllers, and schemas. Presentational authority is left to conditional rendering in screens. Operational authority is scattered across handlers, listeners, adapters, and persistence mappings. Datum Theory rejects that fragmentation at the root. The Datum must remain whole.

DSA is the governance doctrine that follows from this ontology. If a Datum is inherently semantic, presentational, and operational, then the domain must be the highest authority over all three dimensions. That is the sovereignty principle. The domain is not ignorant of infrastructure; it governs infrastructure. The domain is not merely central to business meaning; it is authoritative over the terms on which that meaning is rendered, stored, processed, integrated, and evolved. Infrastructure, UI, API, and external systems do not define business reality. They serve a reality already defined by the domain.

This is why DSA is not simply another reformulation of DDD. DDD protected semantic integrity. DSA extends that protection into full-dimensional governance. It accepts the achievements of DDD, but refuses to stop at semantic modeling. If the Datum is whole, then sovereignty must also be whole. The domain must govern what the Datum means, how it appears, and how it acts. DSA is therefore Datum Theory translated into architecture.

---

## Part 3 — How DSA Is Built

DSA is not produced by requirements documents that later decay into guesswork. It is built through structured conversations that generate authoritative artifacts directly. The methodology maps to how serious software is actually born: people who know the business describe it, people who understand systems translate it, people who use the system reveal what must be visible or hidden, and developers implement what has already been governed.

### 3.1 The People

| Role | Responsibility |
|---|---|
| Business Owner / Domain Expert | Knows the business reality, rules, vocabulary, constraints, and consequences |
| Domain Architect | Translates that business reality into governed domain structures |
| UX Designer | Produces visual specifications that reveal presentational truth |
| End User | Reveals role-specific visibility, editability, workflow, and practical friction |
| Developer | Implements the governed artifacts mechanically and precisely |

### 3.2 The Four Conversations

| Conversation | Participants | Produces |
|---|---|---|
| Conversation 1 | Business Owner ↔ Domain Architect | Entities, Value Objects, Use Cases, Domain Events, Repository Interfaces, persistence shape |
| Conversation 2 | Domain Architect (internal) | Aggregate boundaries, context separation, event choreography, decomposition logic |
| Conversation 3 | End User ↔ Domain Architect | Visibility rules, editability rules, action availability, role-specific contracts |
| Conversation 4 | Domain Architect → Developer | Implementation specification, tests, domain code, delivery wiring |

### 3.3 The Figma-to-Contract Pipeline

When a UX designer produces a Figma screen that shows what different actors see, that screen is not merely visual guidance. In DSA, it is raw material for presentational governance. The domain architect reads the design and encodes its governed differences into contract classes. If one actor sees a field as editable, another sees it as hidden, and a third sees it as read-only, those distinctions are not left in the frontend. They are translated into domain contracts.

```text
Figma screen for Client Admin:    Figma screen for Agent:
[ Hotel Name ]  editable          [ Hotel Name ]  read-only
[ Commission ] editable           (Commission hidden)
[ Contact ]    editable           [ Contact ]     editable

→ becomes HotelFormContract::build(PermissionKey ...$permissions)
```

The designer does not need to write DSA code. The architect does not need to improvise UI rules. The developer does not need to decide which role sees what. The domain governs the presentational reality; the frontend later renders it.

### 3.4 Artifact Authority

| Artifact | Governing Conversation | Authority |
|---|---|---|
| Entity fields, business rules, persistence shape | Business Owner ↔ Architect | Business Owner |
| Aggregate boundaries, repository interfaces, context lines | Architect (internal) | Domain Architect |
| UI visibility, editability, action permissions | End User ↔ Architect / Designer → Architect | End User and UX intent, governed by Architect |
| Final implementation specification | Architect → Developer | Domain Architect |

### 3.5 Why Artifacts Live Where They Live

`toPersistence()` belongs on the entity because persistence shape is derived from what the thing is. It comes from the business conversation, not from the ORM. UI contracts live in separate classes because they come from a different governing conversation with different authority and a different change rhythm. Aggregate boundaries and interfaces live where the architect defines structural authority. This is not arbitrary organization. It is the artifact map of the conversations that produced the system.

### 3.6 The Minimal Resource Model

A company can complete the entire domain layer using business conversations, Figma designs, one domain architect, and one developer before writing a single line of API code, before touching a database, and before building a frontend. When that domain is complete, the product is already specifiable in its highest-value form.

| What is complete | What it means |
|---|---|
| Entities implement persistence sovereignty | Migrations and repository writes become derivative |
| Repository and provider interfaces exist | Delivery implementations become adapters |
| Use cases are tested | Controllers become thin transport |
| UI contracts are defined | Frontend rendering becomes mechanical |
| Domain events are defined | Integration points are explicit |
| Search and federation rules are modeled | External data is admitted on domain terms |

**When the domain is complete, the product is specifiable. When the product is specifiable, the execution is mechanical.**

---

## Part 4 — The Domain

The domain must be organized in a way that reflects Datum Theory itself. The taxonomy of constructs should therefore follow the three dimensions of the Datum rather than a flat inventory of classes. What belongs to the semantic dimension belongs first. What governs presentational truth belongs second. What governs operational life belongs third. The shared kernel exists to support all three.

### 4.1 Semantic Dimension Constructs — What a Datum Is

The semantic dimension contains those constructs that define identity, meaning, invariants, valid states, transitions, relationships, and business language.

#### Entity
A domain object with identity and lifecycle. It enforces rules through explicit business methods and may raise domain events.

```php
final class Client extends AggregateRoot implements PersistableInterface
```

Rules:
- Has identity, usually through an ID value object
- Mutable only through explicit business methods
- Implements `PersistableInterface` when it governs persistence shape
- Extends `AggregateRoot` when it raises domain events

#### Value Object
An immutable typed wrapper with validation and no independent identity.

```php
final class Money
{
    public function __construct(
        private readonly float $amount,
        private readonly string $currencyCode,
    ) { ... }
}
```

Rules:
- `final`
- All properties `readonly`
- Validated in constructor
- No setters
- Equality by value, not by reference

#### Enum
A closed set of valid values with behavior attached.

```php
enum SubscriptionState: string
{
    case Onboarding = 'onboarding';
    case Active     = 'active';
    case Expired    = 'expired';

    public function canTransitionTo(self $next): bool { ... }
    public function isHardBlocked(): bool { ... }
    public function isWriteRestricted(): bool { ... }
}
```

Rules:
- Backed enum
- Carries business behavior as methods
- State transitions live here, not as raw strings elsewhere

#### Specification
A composable business rule that determines whether an entity satisfies a condition.

```php
final class HotelIsAvailableForDates implements SpecificationInterface
{
    public function isSatisfiedBy(Hotel $hotel): bool { ... }
}
```

Rules:
- Single condition
- Composable with AND / OR / NOT
- Used inside use cases or query methods, not as UI logic

#### Collection
A typed wrapper around domain objects where domain rules about groups belong.

```php
final class HotelSearchResultCollection
{
    public function merge(self $other): self { ... }
    public function deduplicate(): self { ... }
    public function sortBy(HotelSortOrder $order): self { ... }
    public function paginate(int $page, int $perPage): self { ... }
    public function preferContracted(): self { ... }
}
```

Rules:
- Immutable operations return new instances
- Group-level business rules live here
- No infrastructure knowledge

#### Factory
Creates domain objects or object graphs whose construction is non-trivial.

```php
final class ReservationFactory
{
    public function fromQuotation(Quotation $quotation): Reservation { ... }
}
```

Rules:
- Pure language construct
- No database access
- Handles semantic construction complexity

#### DTO
A plain data carrier used to move input or output without owning business logic.

```php
final class CreateClientDTO
{
    public function __construct(
        public readonly string $name,
        public readonly string $code,
    ) {}
}
```

Rules:
- No behavior beyond construction
- Public readonly properties
- Validation belongs in entities or use cases

#### Semantic Interfaces

```php
interface UseCaseInterface
{
    public function execute(mixed $request): mixed;
}

interface SpecificationInterface
{
    public function isSatisfiedBy(mixed $entity): bool;
    public function and(self $other): self;
    public function or(self $other): self;
    public function not(): self;
}
```

#### Semantic Rules of the Domain
- Business meaning lives here first
- No framework imports
- No HTTP concerns
- No database queries
- No filesystem or transport concerns

### 4.2 Presentational Dimension Constructs — How a Datum Appears

The presentational dimension contains those constructs that govern visibility, editability, action availability, navigation, and role-specific rendering truth.

#### ContractInterface
The base contract interface for governed presentation.

```php
interface ContractInterface
{
    public function build(PermissionKey ...$permissions): array;
}
```

#### ContractProviderInterface
The interface through which a domain object may provide its own governed contract.

```php
interface ContractProviderInterface
{
    public function toContract(PermissionKey ...$permissions): array;
}
```

#### FormContract
Defines fields for create/edit forms, their visibility, editability, types, and validation rules.

#### TableContract
Defines columns, visibility, and sortability for list views.

#### ActionContract
Defines which actions are visible and enabled for a given Datum in a given context.

#### NavigationContract
Defines navigational structure, visibility, and hierarchy.

#### SessionContract
The master presentational contract returned at login. It contains user context, enabled modules, navigation, and permissions, allowing the frontend to derive application rendering from one governed source.

#### Presentational Enums
Shared typed values for presentation.

```php
enum FieldType: string { ... }
enum ActionType: string { ... }
```

Rules:
- Contracts are pure language constructs
- Computed at runtime
- Framework-independent
- Governed by business truth, not screen code
- Frontend consumes, never legislates

### 4.3 Operational Dimension Constructs — How a Datum Lives and Reacts

The operational dimension contains those constructs that govern persistence, events, process participation, dispatching, search, integration, and system-level execution of business consequences.

#### PersistableInterface
Entity sovereignty over persistence shape.

```php
interface PersistableInterface
{
    public function toPersistence(): array;
    public function toIdentity(): array;
}
```

Rules:
- Infrastructure reads persistence shape
- Infrastructure never defines persistence shape
- Adding a field touches entity, `toPersistence()`, and migration — not repository logic

#### AggregateRoot
Collects domain events internally. Infrastructure pulls them after persistence.

```php
abstract class AggregateRoot
{
    private array $domainEvents = [];

    protected function raise(DomainEventInterface $event): void
    {
        $this->domainEvents[] = $event;
    }

    public function pullDomainEvents(): array
    {
        $events = $this->domainEvents;
        $this->domainEvents = [];
        return $events;
    }
}
```

Rules:
- Zero infrastructure dependency
- Collects rather than dispatches
- Infrastructure dispatches after save

#### DomainEventInterface and Domain Events

```php
interface DomainEventInterface
{
    public function occurredAt(): \DateTimeImmutable;
    public function eventName(): string;
}
```

Rules:
- Events are immutable
- Named as past-tense facts
- Raised inside entities
- Dispatched after persistence

#### RepositoryInterface
Defines read/write contracts for data owned by the system.

```php
interface ClientRepositoryInterface
{
    public function findById(ClientId $id): Client;
    public function save(Client $client): void;
    public function delete(ClientId $id): void;
}
```

Rules:
- Returns domain objects, never ORM models
- Throws domain exceptions, never framework exceptions
- Tenant scoping belongs in implementations
- Write authority exists only for owned data

#### ProviderInterface
Defines contracts for external data sources. Read-only by nature.

```php
interface ExternalHotelProviderInterface
{
    public function search(HotelSearchQuery $query): HotelSearchResultCollection;
    public function providerName(): string;
}
```

Rules:
- Read-only
- Domain defines required shape
- Infrastructure implements transport and mapping
- Used for externally owned data

#### Search Pattern
Search is not a query convenience. It is governed operational meaning when multiple data sources, ranking rules, or deduplication rules are involved.

Core constructs:
- `SearchQuery` as validated input
- `SearchResult` as source-agnostic meaning
- `SearchResultCollection` as governed merge, deduplication, sort, and pagination logic
- Sort enums as governed ranking semantics

Why it belongs here:
- Matching rules are business rules
- Deduplication precedence is business truth
- Provider merge order is business truth
- Search output shape is domain authority

#### RequestContext
A unified request descriptor built by delivery infrastructure and consumed by domain dispatching. Though created from HTTP transport, it belongs to the shared domain kernel because it becomes the governed operational input to use-case resolution.

#### ResourceRegistry
Maps governed `resource + operation` pairs to use cases.

#### ResourceDispatcher
Executes the resolved use case and attaches the governed contract to the result.

#### DispatchResult
The unified operational output shape: success, data, contract, meta, error.

#### TenantContext
Per-request singleton holding resolved tenant state.

Rules:
- Set by middleware or delivery infrastructure
- Read in the domain
- Never mutated from business logic

#### Exceptions
A root hierarchy grounded in `DomainException extends \RuntimeException`.

```text
DomainException
├── TenantException
├── ValidationException
├── NotFoundException
├── AuthorizationException
└── [Context]Exception
```

Rules:
- Domain throws domain exceptions
- Exceptions are named as business facts, not generic failures

### 4.4 The Shared Kernel

The shared kernel contains constructs that support all three dimensions without belonging to only one bounded context.

```text
Shared/
├── TenantContext.php
├── RequestContext.php
├── ValueObjects/
│   ├── Money.php
│   └── Currency.php
├── Contracts/
│   ├── FieldType.php
│   ├── ActionType.php
│   ├── ContractInterface.php
│   ├── PersistableInterface.php
│   ├── ContractProviderInterface.php
│   ├── DomainEventInterface.php
│   ├── UseCaseInterface.php
│   ├── SpecificationInterface.php
│   └── SessionContract.php
├── Dispatching/
│   ├── ResourceRegistry.php
│   ├── ResourceDispatcher.php
│   └── DispatchResult.php
├── Abstracts/
│   └── AggregateRoot.php
└── Exceptions/
    ├── DomainException.php
    ├── TenantException.php
    ├── ValidationException.php
    ├── NotFoundException.php
    └── AuthorizationException.php
```

### 4.5 Permitted and Forbidden Constructs

The domain may use pure language constructs such as native types, `DateTimeImmutable`, SPL interfaces, `JsonSerializable`, `Stringable`, readonly properties, named arguments, match expressions, and enums.

The domain may never use framework imports, database queries, HTTP requests or responses, filesystem calls, environment access, DI container lookups, or external HTTP clients. Those belong to delivery infrastructure.

---

## Part 5 — The Delivery Layers

DSA does not remove delivery layers. It removes their legislative authority.

### 5.1 API as Transport

The API does not define business operations. It carries them.

#### HTTP Header Contract

| Component | Carries | Example |
|---|---|---|
| `Authorization` | Identity | `Bearer {token}` |
| `X-Resource` | What — CamelCase plural | `Hotels`, `ClientRoles` |
| `X-Operation` | How — lowercase | `list`, `confirm`, `create` |
| `X-Id` | Which record | `142` |
| Query params | Read payload | `?search=cairo&page=1` |
| Request body | Write payload | JSON object |

Resource naming is CamelCase plural. Operation naming is lowercase. Standard operations include `list`, `show`, `create`, `update`, `delete`. Domain-specific operations such as `confirm`, `cancel`, `activate`, and `search` are equally valid because routing authority belongs to the domain.

#### The Routes File in Five Lines

```php
Route::middleware(['auth:sanctum', 'tenant', 'headers'])->group(function () {
    Route::get('/',    [ApiController::class, 'handle']);
    Route::post('/',   [ApiController::class, 'handle']);
    Route::put('/',    [ApiController::class, 'handle']);
    Route::patch('/',  [ApiController::class, 'handle']);
    Route::delete('/', [ApiController::class, 'handle']);
});
```

#### The Controller in Ten Lines

```php
final class ApiController
{
    public function handle(Request $request): JsonResponse
    {
        $context = RequestContext::fromHttp(
            headers: $request->headers->all(),
            queryParams: $request->query->all(),
            body: $request->json()->all(),
            method: $request->method(),
        );

        $result = $this->dispatcher->dispatch($context);

        return response()->json($result->toArray(), $result->success ? 200 : 422);
    }
}
```

No new controllers. Ever. The domain governs routing. The API carries requests into that governed mechanism.

### 5.2 UI as Renderer

The UI does not decide business truth. It renders governed contracts.

#### Session Contract

At login, the frontend receives the master rendering contract.

```json
{
  "user": { "id": 42, "name": "Ahmed Hassan" },
  "context": { "client": "Acme Corporation", "isDemo": false, "isReadOnly": false },
  "modules": { "orders": true, "catalog": true, "reporting": true, "wholesale": false },
  "navigation": [{ "key": "Products", "label": "Products", "visible": true, "children": [] }],
  "permissions": ["products.read", "products.manage", "orders.create"]
}
```

#### Frontend with Zero Business Logic

```typescript
navigation.filter(i => i.visible).map(i => <NavItem {...i} />)

contract.fields.filter(f => f.visible).map(f =>
  <Field type={f.type} editable={f.editable} validation={f.validation} />
)

<DataTable columns={contract.columns.filter(c => c.visible)} rows={rows} />

contract.actions.filter(a => a.visible).map(a =>
  <Button enabled={a.enabled}>{a.label}</Button>
)
```

No role names in screen code. No permission keys in conditional rendering. No business logic in the client. Pure rendering.

### 5.3 Infrastructure as Servant

Infrastructure remains necessary. It just stops defining business terms.

#### The Model as Table Descriptor Only

```php
final class ClientModel extends Model
{
    protected $table = 'clients';
    protected $guarded = [];
    protected $casts = [...];
}
```

No business logic. No meaningful accessors. No relationships as a place to hide rules.

#### BaseEloquentRepository Written Once

```php
abstract class BaseEloquentRepository
{
    protected string $modelClass;

    public function save(PersistableInterface $entity): void
    {
        $model = $this->modelClass::firstOrNew($entity->toIdentity());
        foreach ($entity->toPersistence() as $key => $value) {
            $model->$key = $value;
        }
        $model->save();
    }
}
```

The repository implementation becomes mechanical because the entity already defined its persistence terms.

#### Delivery Folder Shape

```text
[application]-api/
├── app/
│   ├── Http/
│   │   ├── Controllers/
│   │   │   └── ApiController.php
│   │   ├── Middleware/
│   │   │   ├── AuthenticateRequest.php
│   │   │   ├── ResolveTenantContext.php
│   │   │   ├── ValidateRequestHeaders.php
│   │   │   └── EnforceReadOnly.php
│   ├── Infrastructure/
│   │   ├── Persistence/
│   │   │   └── [Context]/[Entity]Model.php
│   │   ├── Repositories/
│   │   │   ├── BaseEloquentRepository.php
│   │   │   └── [Context]/Eloquent[Entity]Repository.php
│   │   ├── Providers/
│   │   │   └── [Context]/[Source][Resource]Provider.php
│   ├── Registry/
│   │   ├── ResourceRegistryBootstrapper.php
│   │   └── [Context]/[Context]ResourceMap.php
└── routes/
    └── api.php
```

Infrastructure adapts. It does not decide.

---

## Part 6 — Scalability and Economics

### 6.1 The Scaling Curve

```text
Phase 1 — Shared Hosting (~$5–10/month) — 1–20 clients. Domain: untouched.
Phase 2 — VPS (~$50–100/month) — 20–200 clients. Domain: untouched.
Phase 3 — Cloud (~$500–2,000/month) — 200–2,000 clients. Domain: untouched.
Phase 4 — Database per client — repository implementations change. Domain: untouched.
Phase 5 — Context decomposition only if forced — domain logic: untouched.
```

The point is not that infrastructure disappears. The point is that infrastructure scale no longer forces domain rewrite.

### 6.2 Infrastructure Swap Proof

| Change | Domain | API | UI |
|---|---|---|---|
| MySQL → PostgreSQL | None | Repository implementations | None |
| Laravel → Node.js | Translate pure classes | Rewrite thin controller | None |
| Add mobile app | None | None | New contract consumer |
| Add new resource | Domain use cases | Registry wiring only | None |
| Add new field | Entity + `toPersistence()` | Migration only | None |
| Add external provider | ProviderInterface already defined | New adapter class | None |

### 6.3 Development Economics

DSA removes repeated business thinking from backend, frontend, and persistence workstreams. One authoritative domain replaces multiple partial truths. This lowers rework, reduces contradiction, and changes the cost structure of building complex systems.

### 6.4 Infrastructure Economics

Because the domain is infrastructure-independent, a system can begin on extremely cheap infrastructure when its real complexity is business complexity rather than traffic complexity. Infrastructure grows when usage demands it, not because architecture was born fragmented.

### 6.5 Team Economics

The same architecture that makes infrastructure cheap also makes teams smaller. If the domain contains the highest-value intelligence, then the rest of the system becomes implementation of governed truth rather than repeated rediscovery of that truth. The product exists before infrastructure. The intelligence is concentrated where it belongs.

---

## Part 7 — Implementation Checklist

### 7.1 Before Writing Any Code

- Conversation 1 complete — entities, use cases, and business rules specified
- Conversation 3 complete, or Figma designs available for translation into contracts
- Bounded context boundaries agreed
- Datum boundaries understood for core business units
- Presentational governance known before UI implementation
- Operational consequences known before transport implementation

### 7.2 Domain Requirements

- Zero framework imports in any domain class
- All entities that govern persistence implement `PersistableInterface`
- Event-raising entities extend `AggregateRoot`
- All business rules expressed as entities, value objects, enums, specifications, use cases, collections, or contracts
- All user-facing Datums have dedicated contract classes
- All external data sources have `ProviderInterface` in the domain
- All owned data uses repository interfaces in the domain
- All complex search behavior uses governed search constructs
- All use cases are independently unit-testable
- Static analysis at maximum strictness
- Domain business logic fully covered by tests

### 7.3 API Requirements

- Single controller only
- Five routes only, all pointing to the same handler
- Request transformed into `RequestContext`
- Dispatch through `ResourceRegistry` and `ResourceDispatcher`
- No business logic in controllers
- All field persistence flows through `PersistableInterface::toPersistence()`
- `BaseEloquentRepository::save()` or equivalent written once and reused
- External providers implement domain provider contracts
- Models remain table descriptors only

### 7.4 UI Requirements

- No role names in conditional rendering
- No permission keys in conditional rendering
- All forms rendered from contract field definitions
- All tables rendered from contract column definitions
- All actions rendered from contract action definitions
- All navigation rendered from session contract
- Frontend contains no business logic, only rendering logic

A system qualifies as DSA only if the domain is truly authoritative over meaning, presentation, and operation. If any of those dimensions are legislated elsewhere, the methodology has been violated.

---

## Part 8 — Reference Implementation

The reference implementation of Domain-Sovereign Architecture is datum-commerce — an open source, enterprise-grade, multi-tenant e-commerce platform built according to DSA principles in Java and Spring Boot.

datum-commerce is not a tutorial. It is not a boilerplate. It is a production-grade domain built to demonstrate that DSA is executable at real business scale — across catalog management, inventory, order lifecycle, pricing, customer identity with dynamic RBAC, and payment. The domain layer is pure Java with zero Spring dependency. The Spring Boot infrastructure layer serves it. The domain governs. Infrastructure executes.

datum-commerce exists for the community. Developers are invited to read it, fork it, extend it, port it to other languages, and challenge its domain decisions. Every port that produces the same business rules in a different language is a proof of Datum Theory's portability claim — that a domain built according to DSA survives infrastructure migration intact because its truth never lived in the infrastructure to begin with.

The community is the proof. datum-commerce is its starting point.
---

## Closing Identity

**Domain-Sovereign Architecture is a software methodology in which the domain becomes the highest authority over business truth, governing not only meaning and rules, but also the contracts of presentation, persistence, process, integration, and system evolution.**
