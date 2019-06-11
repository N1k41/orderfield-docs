---
id: pages
title: Pages
sidebar_label: Pages
---

The following default pages can be configured in OrderField:

- [Home](#home)
- [Catalog](#catalog) 
    - [Item tile](#item-tile)
    - [Item detail](#item-detail) 
- [Favorites](#favorites)
- [Orderhistory](#orderhistory)
- [Checkout](#checkout)
- [Search](#search)

## Home

*Basic configuration*
```json
{
    "code" : "home",
    "i18n" : [],
    "name" : "Home",
    "sortOrder" : 1,
    "type" : "home"
}
```

*Attributes*
- [banner](attributes.md#banner)
- [blocks](attributes.md#blocks)

## Catalog

*Basic configuration*
```json
{
    "code" : "catalog",
    "i18n" : [],
    "name" : "Catalog",
    "sortOrder" : 1,
    "type" : "catalog"
}
```
*Attributes*
- [showThumbnails](attributes.md#showThumbnails)
- [facetgroups](attributes.md#facetgroups)
- [banner](attributes.md#banner)

## Item tile
Determines the content of tiles shown on the catalog page

*Basic configuration*
```json
{
    "code" : "item_catalog",
    "i18n" : [],
    "name" : "Item catalog",
    "sortOrder" : 1,
    "type" : "catalog"
}
```
*Attributes*
- [showFavoriteIcon](attributes.md#showFavoriteIcon)
- [showAttributes](attributes.md#showAttributes)
- [showFacets](attributes.md#showFacets)


## Item details
Determines the content of the item details page

*Basic configuration*
```json
{
    "code" : "item_details",
    "i18n" : [],
    "name" : "Item details",
    "sortOrder" : 1,
    "type" : "catalog"
}
```
*Attributes*
- [showFavoriteIcon](attributes.md#showFavoriteIcon)
- [showAttributes](attributes.md#showAttributes)
- [showFacets](attributes.md#showFacets)
- [showSalesOrderAddressInfo](attributes.md#showSalesOrderAddressInfo)


## Favorites
*Basic configuration*
```json
{
    "code" : "favorites",
    "i18n" : [],
    "name" : "Favorites",
    "sortOrder" : 1,
    "type" : "catalog"
}
```
*Attributes*
- [showFavoriteIcon](attributes.md#showFavoriteIcon)
- [showAttributes](attributes.md#showAttributes)
- [showFacets](attributes.md#showFacets)
- [facetgroups](attributes.md#facetgroups)
- [banner](attributes.md#banner)

## Orderhistory
*Basic configuration*
```json
{
    "code" : "orderhistory",
    "i18n" : [],
    "name" : "Order history",
    "sortOrder" : 1,
    "type" : "orderhistory"
}
```
*Attributes*
- [banner](attributes.md#banner)
- [facetgroups](attributes.md#facetgroups)

## Checkout
*Basic configuration*
```json
{
    "code" : "checkout",
    "i18n" : [],
    "name" : "Checkout",
    "sortOrder" : 1,
    "type" : "checkout"
}
```
*Attributes*
- [showDeliveryColumn](attributes.md#showDeliveryColumn)
- [showTermsAndConditionsCheckbox](attributes.md#showTermsAndConditionsCheckbox)
- [customerReferenceMaxLength](attributes.md#customerReferenceMaxLength)
- [showUomInfoForUoms](attributes.md#showUomInfoForUoms)
- [showOrderType](attributes.md#showOrderType)

## Search
*Basic configuration*
```json
{
    "code" : "search",
    "i18n" : [],
    "name" : "Search",
    "sortOrder" : 1,
    "type" : "search"
}
```

*Attributes*
- [facetgroups](attributes.md#facetgroups)
