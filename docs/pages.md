---
id: pages
title: Pages
sidebar_label: Pages
---

## Default pages

The following default pages can be configured in OrderField:

- [Home](#home-page) (<span style="color:green">home</span>)
- [Catalog page](#catalog-page) (<span style="color:green">catalog</span>)
    - Item tile <span style="color:green">item_catalog</span>
    - Item detail page <span style="color:green">item_details</span>
- Favorites <span style="color:green">favorites</span>
- Orderhistory <span style="color:green">orderhistory</span>
- Checkout <span style="color:green">checkout</span>
- Search <span style="color:green">search</span>

## Home page

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

*Available options*
- Banner (one)
- Blocks (multiple)

## Catalog page

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

*Available options*
- Banner (one)
- Facetgroups


Setting
ShowThumbnails

*Sub pages*
- Item tile <span style="color:green">item_catalog</span>
- Item detail page <span style="color:green">item_details</span>




##Items in catalog page
code: item_catalog

*Available settings*
- showThumbnails
- 

*Content*
- facetgroups


Page settings
- 

Page options
- facetgroups
- banners
- blocks
- attributes
