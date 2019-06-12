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
- [banner](#banner)
- [blocks](#blocks)

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
- [showThumbnails](#showThumbnails)
- [facetgroups](#facetgroups)
- [banner](#banner)

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
- [showFavoriteIcon](#showFavoriteIcon)
- [showAttributes](#showAttributes)
- [showFacets](#showFacets)


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
- [showFavoriteIcon](#showFavoriteIcon)
- [showAttributes](#showAttributes)
- [showFacets](#showFacets)
- [showSalesOrderAddressInfo](#showSalesOrderAddressInfo)


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
- [showFavoriteIcon](#showFavoriteIcon)
- [showAttributes](#showAttributes)
- [showFacets](#showFacets)
- [facetgroups](#facetgroups)
- [banner](#banner)

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
- [banner](#banner)
- [facetgroups](#facetgroups)

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
- [showDeliveryColumn](#showDeliveryColumn)
- [showTermsAndConditionsCheckbox](#showTermsAndConditionsCheckbox)
- [customerReferenceMaxLength](#customerReferenceMaxLength)
- [showUomInfoForUoms](#showUomInfoForUoms)
- [showOrderType](#showOrderType)

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
- [facetgroups](#facetgroups)

## Page attributes

|Attribute|Format|Remarks|
|---|---|---|
|<a name="banner"></a><span style="color:green">banner</span>|Banner settings for this page <br /><br />**Sub-attributes** <br /><ul><li><span style="color:green">img</span><br/>Image url</li><li><span style="color:green">title</span> <br/>Title </li><li><span style="color:green">subTitle</span> <br/>Subtitle</li><li><span style="color:green">buttonText</span><br/>Text in the button</li><li><span style="color:green">linkToPage</span> <br/>Link url</li></ul>|**Applicable to**<ul><li>[Home](pages.md#home)</li><li>[Catalog](pages.md#catalog)</li><li>[Favorites](pages.md#favorites)</li></ul>_Title, subtitle and buttontext can be translated_|
|<a name="blocks"></a><span style="color:green">blocks</span>|Block settings for this page <br /><br />**Sub-attributes** <br /><ul><li><span style="color:green">img</span><br/>Image url</li><li><span style="color:green">title</span> <br/>Title </li><li><span style="color:green">subTitle</span> <br/>Subtitle</li><li><span style="color:green">buttonText</span><br/>Text in the button</li><li><span style="color:green">linkToPage</span> <br/>Link url</li><li><span style="color:green">sortorder</span> <br/>Sort order of this block</li></ul>|**Applicable to**<ul><li>[Home](pages.md#home)</li></ul>_Title, subtitle and buttontext can be translated_|
|<a name="showThumbnails"></a><span style="color:green">showThumbnails </span> |Indicates that thumbnails of the product pictures should be shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showThumbnails", "value" : true} ]</span>|**Applicable to**<ul><li>[Catalog](pages.md#catalog-page)</li></ul>|
|<a name="showFavoriteIcon"></a><span style="color:green">showFavoriteIcon </span> |Indicates that favorite icons should be shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showFavoriteIcon", "value" : true} ]</span>|**Applicable to**<ul><li>[Item tile](pages.md#item-tile)</li><li>[Item details](pages.md#item-details)</li></ul>|
|<a name="showAttributes"></a><span style="color:green">showAttributes </span>|Determines which attributes should be shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showAttributes", "value" : ["barcode" ]} ]</span>|**Applicable to**<ul><li>[Item details](pages.md#item-details)</li></ul>_Difference between facets and attributes is that attributes are unique per product_|
|<a name="showFacets"></a><span style="color:green">showFacets </span>|Determines which facets should be shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showFacets", "value" : ["scent", "color"]} ]</span>|**Applicable to**<ul><li>[Item details](pages.md#item-details)</li></ul>|
|<a name="facetgroups"></a><span style="color:green">facetgroups </span>|Determines which facet groups should be shown as filters<br /><br />**Example** <br /> <span style="color:green">"facetgroups" : ["scent", "color","season","usage"]</span>|**Applicable to**<ul><li>[Catalog](pages.md#catalog)</li><li>[Favorites](pages.md#favorites)</li><li>[Search](pages.md#search)</li></ul>|
|<a name="showSalesOrderAddressInfo"></a><span style="color:green">showSalesOrderAddressInfo  </span>|Set this to <span style="color:green">false</span> if no delivery address info is available for previous orders. The previous orders will then be shown in a more compact list.<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showSalesOrderAddressInfo", "value" : true} ]</span>|**Applicable to**<ul><li>[Item details](pages.md#item-details)</li></ul>|
|<a name="showDeliveryColumn"></a><span style="color:green">showDeliveryColumn  </span>|Determines if delivery column is shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showDeliveryColumn", "value" : true} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|
|<a name="showTermsAndConditionsCheckbox"></a><span style="color:green">showTermsAndConditionsCheckbox  </span>|Determines if terms & conditions checkbox is shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showTermsAndConditionsCheckbox", "value" : true} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|
|<a name="customerReferenceMaxLength"></a><span style="color:green">customerReferenceMaxLength  </span>|Determines max length of the reference field<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "customerReferenceMaxLength", "value" : 25} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|
|<a name="showUomInfoForUoms"></a><span style="color:green">showUomInfoForUoms </span> |Determines to which customer group the pallet calculation is shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showUomInfoForUoms ", "value" :  ["PL"]} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|
|<a name="showOrderType"></a><span style="color:green">showOrderType </span>|Determines if Order Type choice is shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showOrderType", "value" : false} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|
