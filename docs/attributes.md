---
id: attributes
title: Attributes
sidebar_label: Attributes
---

The following attributes can be used to configure an OrderField instance.

## Tenant attributes

Collection: _tenant > tenant__settings_

|Attribute|Format|Remarks|
|---|---|---|
|<span style="color:green">ga_tracking_id</span>|<span style="color:orange">**Optional** </span> <br />GA Tracking ID</span><br /><br />**Example** <br /> <span style="color:green">{"key" : "ga_tracking_id", "value" : "UA-87774626-1"}</span>||
|<span style="color:green">gtm_tracking_id</span>|<span style="color:orange">**Optional** </span> <br />GTM Tracking ID</span><br /><br />**Example** <br /> <span style="color:green">{"key" : "gtm_tracking_id", "value" : "UA-87774626-1"}</span>||
|<span style="color:green">quantity_picker</span>|<span style="color:orange">**Optional** </span><br/>Indicates which quantity picker should be used</span> <br/><br/>**Example** <br /> <span style="color:green">{"key" : "quantity_picker", "value" : "relative"}</span><br/><br/>**Syntax**<br><span style="color:green">absolute</span> (default) ; <span style="color:green">relative</span>|<ul><li><span style="color:green">absolute</span><br/>shows the absolute quantity and uses that value for calculations (e.g. 1 box of 12 pieces -> 12 pieces)</li><li><span style="color:green">relative</span><br/>shows the number of sales units and uses that value for calculations (e.g. 1 box of 12 pieces -> 1 box) </li></ul>|
|<span style="color:green">MAIL_ORDER_CONFIRMATION</span>|<span style="color:orange">**Optional** </span> <br />Settings of the order confirmation emails <br /><br />**Sub-attributes** <br /><ul><li><span style="color:green">mail_from</span><br/>From-address</li><li><span style="color:green">mail_cc</span> (array)<br/>CC to </li><li><span style="color:green">mail_bcc</span> (array)<br/>BCC to</li><li><span style="color:green">default_template_id</span><br/>Postmark template ID</li><li><span style="color:green">template_ids</span> (array)<br/>Postmark template ID per language</li><li><span style="color:green">logo_url</span><br/>Logo URL</li><li><span style="color:green">mail_sender_name</span><br/>Name of the sender</li></ul>|<ul><li>If no settings are available, the default OrderField values are used</li></ul>|
| <span style="color:green">show_breadcrumbs</span> | <span style="color:orange">**Optional** </span> <br />Indicates if breadcumbs should be shown<br /><br />**Example** <br /> <span style="color:green">{"key" : "show_breadcrumbs","value" : false,"roles" : []}</span><br/><br /> **Syntax** <br /> <span style="color:green">true</span> (default) ; <span style="color:green">false</span>||




## Page attributes

|Attribute|Format|Remarks|
|---|---|---|
|<a name="banner"></a><span style="color:green">banner</span>|Banner settings for this page <br /><br />**Sub-attributes** <br /><ul><li><span style="color:green">img</span><br/>Image url</li><li><span style="color:green">title</span> <br/>Title </li><li><span style="color:green">subTitle</span> <br/>Subtitle</li><li><span style="color:green">buttonText</span><br/>Text in the button</li><li><span style="color:green">linkToPage</span> <br/>Link url</li></ul>|<ul><li>Title, subtitle and buttontext can be translated</li></ul>|
|<a name="blocks"></a><span style="color:green">blocks</span>|Block settings for this page <br /><br />**Sub-attributes** <br /><ul><li><span style="color:green">img</span><br/>Image url</li><li><span style="color:green">title</span> <br/>Title </li><li><span style="color:green">subTitle</span> <br/>Subtitle</li><li><span style="color:green">buttonText</span><br/>Text in the button</li><li><span style="color:green">linkToPage</span> <br/>Link url</li><li><span style="color:green">sortorder</span> <br/>Sort order of this block</li></ul>|<ul><li>Title, subtitle and buttontext can be translated</li></ul>|
|<a name="showThumbnails"></a><span style="color:green">showThumbnails </span> |Indicates that thumbnails of the product pictures should be shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showThumbnails", "value" : true} ]</span>|**Applicable to**<ul><li>[Catalog](pages.md#catalog-page)</li></ul>|
|<a name="showFavoriteIcon"></a><span style="color:green">showFavoriteIcon </span> |Indicates that favorite icons should be shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showFavoriteIcon", "value" : true} ]</span>|**Applicable to**<ul><li>[Item tile](pages.md#item-tile)</li><li>[Item details](pages.md#item-details)</li></ul>|
|<a name="showAttributes"></a><span style="color:green">showAttributes </span>|Determines which attributes should be shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showAttributes", "value" : [ ]} ]</span>|**Applicable to**<ul><li>[Item details](pages.md#item-details)</li></ul>|
|<a name="showFacets"></a><span style="color:green">showFacets </span>|Determines which facets should be shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showFacets", "value" : ["scent", "color"]} ]</span>|**Applicable to**<ul><li>[Item details](pages.md#item-details)</li></ul>|
|<a name="facetgroups"></a><span style="color:green">facetgroups </span>|Determines which facet groups should be shown as filters<br /><br />**Example** <br /> <span style="color:green">"facetgroups" : ["scent", "color","season","usage"]</span>|**Applicable to**<ul><li>[Catalog](pages.md#catalog)</li><li>[Favorites](pages.md#favorites)</li><li>[Search](pages.md#search)</li></ul>|
|<a name="showSalesOrderAddressInfo"></a><span style="color:green">showSalesOrderAddressInfo  </span>|Set this to <span style="color:green">false</span> if no delivery address info is available for previous orders. The previous orders will then be shown in a more compact list.<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showSalesOrderAddressInfo", "value" : true} ]</span>|**Applicable to**<ul><li>[Item details](pages.md#item-details)</li></ul>|
|<a name="showDeliveryColumn"></a><span style="color:green">showDeliveryColumn  </span>|Determines if delivery column is shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showDeliveryColumn", "value" : true} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|
|<a name="showTermsAndConditionsCheckbox"></a><span style="color:green">showTermsAndConditionsCheckbox  </span>|Determines if terms & conditions checkbox is shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showTermsAndConditionsCheckbox", "value" : true} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|
|<a name="customerReferenceMaxLength"></a><span style="color:green">customerReferenceMaxLength  </span>|Determines max length of the reference field<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "customerReferenceMaxLength", "value" : 25} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|
|<a name="showUomInfoForUoms"></a><span style="color:green">showUomInfoForUoms </span> |Determines to which customer group the pallet calculation is shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showUomInfoForUoms ", "value" :  ["PL"]} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|
|<a name="showOrderType"></a><span style="color:green">showOrderType </span>|Determines if Order Type choice is shown<br /><br />**Example** <br /> <span style="color:green"> "settings" : [ {"platform" : "all", "key" : "showOrderType", "value" : false} ]</span>|**Applicable to**<ul><li>[Checkout](pages.md#checkout)</li></ul>|

## Customer (group) attributes
[See ERP data](erpdata.md#klanten)

## User settings

_todo_


