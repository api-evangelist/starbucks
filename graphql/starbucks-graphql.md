# Starbucks GraphQL Schema

## Overview

This conceptual GraphQL schema models the Starbucks platform — covering store locations, menu items, ordering, loyalty rewards, payments, and customer profiles. It is derived from publicly available information about the Starbucks partner API ecosystem, the My Starbucks Rewards program, and the Starbucks mobile ordering experience.

Starbucks does not publish a public GraphQL endpoint, but this schema captures the domain model that underlies the Starbucks developer platform at https://developer.starbucks.com/.

## Schema Source

- **Provider:** Starbucks
- **Portal:** https://developer.starbucks.com/
- **Documentation:** https://portal.starbucks.com/
- **Schema file:** starbucks-schema.graphql
- **Type:** Conceptual / Derived

## Type Summary

| Category | Types |
|---|---|
| Store | Store, StoreDetails, StoreHours, StoreLocation, StoreFeatures, DriveThrough, MobileOrder, InStoreOrder, Curbside, StoreImage |
| Menu & Product | Product, Beverage, Food, PackagedGoods, Merchandise, ProductDetails, ProductCategory, ProductSize, ProductCustomization, CustomizationOption, Syrup, Milk, Whip, Espresso, Temperature, Decaf, Extra, MenuBoard, SeasonalMenu |
| Offers | SpecialOffer, DailyOffer |
| Ordering | Order, OrderItem, OrderCustomization, OrderStatus, MobileOrderReady |
| Payment | Payment, StarsPay, ApplePay, GiftCard, DigitalCardBalance |
| Loyalty | Loyalty, StarRewards, LoyaltyTier, LoyaltyPoints, Stars, Bonus, StarChallenges, Birthday |
| Personalization | Personalization, DrinkPreferences |
| Customer | Customer, CustomerProfile, MemberID, AccountStatus, AccountHistory |
| Promotions | Offer, PromoCode |
| Auth | APIKey, Token |

## Root Operations

### Queries

- `store(id: ID!): Store` — Retrieve a single store by ID
- `stores(location: LocationInput, radius: Float, filters: StoreFiltersInput): [Store]` — Search stores near a location
- `product(id: ID!): Product` — Retrieve a product by ID
- `menu(storeId: ID!): MenuBoard` — Get the full menu for a store
- `seasonalMenu: SeasonalMenu` — Get current seasonal offerings
- `order(id: ID!): Order` — Retrieve an order by ID
- `customer(id: ID!): Customer` — Retrieve customer profile
- `loyalty(memberId: ID!): Loyalty` — Retrieve loyalty account
- `offers(memberId: ID!): [Offer]` — Get personalized offers for a member

### Mutations

- `placeOrder(input: OrderInput!): Order` — Place a mobile order
- `updateOrderItem(orderId: ID!, itemId: ID!, customization: OrderCustomizationInput!): OrderItem` — Update item in order
- `cancelOrder(id: ID!): OrderStatus` — Cancel an open order
- `redeemOffer(memberId: ID!, offerId: ID!): Offer` — Redeem a loyalty offer
- `redeemStars(memberId: ID!, stars: Int!): StarRewards` — Redeem stars for a reward
- `addGiftCard(memberId: ID!, cardNumber: String!, pin: String!): GiftCard` — Add a gift card to account
- `transferGiftCardBalance(fromCardId: ID!, toCardId: ID!): GiftCard` — Transfer gift card balance

## Authentication

The Starbucks partner API uses OAuth 2.0 bearer tokens. API keys are issued through the developer portal. The `APIKey` and `Token` types model these credentials.

## Notes

- Starbucks Mobile Order and Pay is a core consumer feature; the ordering types reflect that workflow.
- The Star Rewards loyalty program uses "Stars" as its currency unit; two tiers exist (Green and Gold).
- Customization is deep — beverages support milk type, syrup, espresso shots, temperature, whip, and more.
- Seasonal menus and limited-time offers are a significant part of the Starbucks product catalog.
