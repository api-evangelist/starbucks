# Starbucks

Starbucks provides partner APIs for ordering, loyalty program integration, store locations, and menu data through their developer portal. These APIs enable authorized partners to integrate Starbucks ordering, rewards, and store discovery into their applications.

- **Website:** [https://www.starbucks.com/](https://www.starbucks.com/)
- **Developer Portal:** [https://developer.starbucks.com/](https://developer.starbucks.com/)
- **API Portal:** [https://portal.starbucks.com/](https://portal.starbucks.com/)
- **Privacy Policy:** [https://www.starbucks.com/responsibility/privacy-policy](https://www.starbucks.com/responsibility/privacy-policy)
- **Terms of Service:** [https://www.starbucks.com/about-us/company-information/online-policies/terms-of-use](https://www.starbucks.com/about-us/company-information/online-policies/terms-of-use)

## APIs

### Starbucks API

The Starbucks API provides partner access to ordering workflows, loyalty program management, store location discovery, and menu data. Authorized partners use OAuth2 bearer token authentication to integrate Starbucks experiences into their applications and services.

**Tags:** Food Service, Coffee, Ordering, Loyalty, Store Locator, Menu

| Resource | URL |
|---|---|
| Portal | [https://developer.starbucks.com/](https://developer.starbucks.com/) |
| Documentation | [https://portal.starbucks.com/](https://portal.starbucks.com/) |
| OpenAPI | [openapi/starbucks-starbucks-api-openapi.yml](openapi/starbucks-starbucks-api-openapi.yml) |
| Spectral Rules | [rules/starbucks-rules.yml](rules/starbucks-rules.yml) |
| Capabilities | [capabilities/food-service.yaml](capabilities/food-service.yaml) |

## OpenAPI Specifications

| API | File |
|---|---|
| Starbucks API | [openapi/starbucks-starbucks-api-openapi.yml](openapi/starbucks-starbucks-api-openapi.yml) |

**Operations:** Get API Status, List Menu Categories, List Menu Items, Get Menu Item, List Stores, Get Store, Get Loyalty Account, List Loyalty Transactions, Create Order, Get Order

## Capabilities

### Shared Definitions

| File | Description |
|---|---|
| [capabilities/shared/starbucks-api.yaml](capabilities/shared/starbucks-api.yaml) | Starbucks API — menu, stores, loyalty, and ordering |

### Workflow Capabilities

| Capability | File | Description |
|---|---|---|
| Food Service | [capabilities/food-service.yaml](capabilities/food-service.yaml) | Menu discovery, store finding, loyalty management, and mobile ordering in one workflow |

## Spectral Rules

| File | Description |
|---|---|
| [rules/starbucks-rules.yml](rules/starbucks-rules.yml) | Spectral ruleset enforcing Starbucks API conventions |

## JSON Schemas

| Schema | File |
|---|---|
| Menu Item | [json-schema/starbucks-menu-item-schema.json](json-schema/starbucks-menu-item-schema.json) |
| Store | [json-schema/starbucks-store-schema.json](json-schema/starbucks-store-schema.json) |
| Loyalty Account | [json-schema/starbucks-loyalty-account-schema.json](json-schema/starbucks-loyalty-account-schema.json) |

## JSON Structures

| Structure | File |
|---|---|
| Menu Item | [json-structure/starbucks-menu-item-structure.json](json-structure/starbucks-menu-item-structure.json) |
| Store | [json-structure/starbucks-store-structure.json](json-structure/starbucks-store-structure.json) |

## JSON-LD Context

| File | Description |
|---|---|
| [json-ld/starbucks-context.jsonld](json-ld/starbucks-context.jsonld) | JSON-LD context mapping Starbucks concepts to schema.org vocabulary |

## Examples

| Example | File |
|---|---|
| List Menu Categories | [examples/starbucks-list-menu-categories-example.json](examples/starbucks-list-menu-categories-example.json) |
| List Stores | [examples/starbucks-list-stores-example.json](examples/starbucks-list-stores-example.json) |
| Create Order | [examples/starbucks-create-order-example.json](examples/starbucks-create-order-example.json) |
| Get Loyalty Account | [examples/starbucks-get-loyalty-account-example.json](examples/starbucks-get-loyalty-account-example.json) |

## Vocabulary

| File | Description |
|---|---|
| [vocabulary/starbucks-vocabulary.yml](vocabulary/starbucks-vocabulary.yml) | Domain vocabulary for Starbucks food service, loyalty, and ordering concepts |

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
