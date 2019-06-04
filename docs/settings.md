---
id: settings
title: Settings
sidebar_label: Settings
---

The following settings can be applied.

## Tenant settings

Collection: _tenant > tenant__settings_

|Attribute|Format|Remarks|
|---|---|---|
|<span style="color:green">ga_tracking_id</span>|<span style="color:orange">**Optional** </span> <br />GA Tracking ID</span><br /><br />**Example** <br /> <span style="color:green">{"key" : "ga_tracking_id", "value" : "UA-87774626-1"}</span>||
|<span style="color:green">gtm_tracking_id</span>|<span style="color:orange">**Optional** </span> <br />GTM Tracking ID</span><br /><br />**Example** <br /> <span style="color:green">{"key" : "gtm_tracking_id", "value" : "UA-87774626-1"}</span>||
|<span style="color:green">quantity_picker</span>|<span style="color:orange">**Optional** </span><br/>Indicates which quantity picker should be used</span> <br/><br/>**Values**<br><span style="color:green">absolute ; relative</span><br/><br/>**Example** <br /> <span style="color:green">{"key" : "quantity_picker", "value" : "relative"}</span>|<ul><li><span style="color:green">absolute</span> (default) <br/>shows the absolute quantity and uses that value for calculations (e.g. 1 box of 12 pieces -> 12 pieces)</li><li><span style="color:green">relative</span><br/>shows the number of sales units and uses that value for calculations (e.g. 1 box of 12 pieces -> 1 box) </li></ul>|
|<span style="color:green">MAIL_ORDER_CONFIRMATION</span>|<span style="color:red">**Required** </span> <br />Settings of the order confirmation emails <br /><br />**Sub-attributes** <br /><ul><li><span style="color:green">mail_from</span><br/>From-address</li><li><span style="color:green">mail_cc</span> (array)<br/>CC to </li><li><span style="color:green">mail_bcc</span> (array)<br/>BCC to</li><li><span style="color:green">default_template_id</span><br/>Postmark template ID</li><li><span style="color:green">template_ids</span> (array)<br/>Postmark template ID per language</li><li><span style="color:green">logo_url</span><br/>Logo URL</li><li><span style="color:green">mail_sender_name</span><br/>Name of the sender</li></ul>||
| <span style="color:green">show_breadcrumbs</span> | <span style="color:orange">**Optional** </span> <br />Indicates if breadcumbs should be shown<br /><br />**Example** <br /> <span style="color:green">{"key" : "show_breadcrumbs","value" : false,"roles" : []}</span><br/><br /> **Syntax** <br /> <span style="color:green">true ; false</span>||
## Page settings

|Setting|Locations|
|---|---|
|<span style="color:green">showThumbnails </span> <br />Indicates that thumbnails should be shown<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "showThumbnails", "value" : true</span>|tenant__pages > catalog|
|<span style="color:green">showFavoriteIcon </span> <br />Indicates that favorite icons should be shown<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "showFavoriteIcon", "value" : true</span>|tenant__pages > item_catalog <br/>tenant__pages > item_details|
|<span style="color:green">showAttributes </span> <br />Determines which attributes should be shown<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "showAttributes", "value" : [ ]</span>|tenant__pages > item_details|
|<span style="color:green">showFacets </span> <br />Determines which facets should be shown<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "showAttributes", "value" : ["scent", "color"]</span>|tenant__pages > item_details|
|<span style="color:green">facetgroups </span> <br />Determines which facetgroups should be shown as filters<br /><br />**Example** <br /> <span style="color:green">["scent", "color","season","usage"]</span>|tenant__pages > item_catalog|
|<span style="color:green">showSalesOrderAddressInfo  </span> <br />Set this to false if no delivery address info is available for previous orders. The previous orders will then be shown in a more compact list.<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "showSalesOrderAddressInfo", "value" : true</span>|tenant__pages > item_details|
|<span style="color:green">showDeliveryColumn  </span> <br />Determines if delivery column is shown<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "showDeliveryColumn", "value" : true</span>|tenant__pages > checkout|
|<span style="color:green">showTermsAndConditionsCheckbox  </span> <br />Determines if terms & conditions checkbox is shown<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "showTermsAndConditionsCheckbox", "value" : true</span>|tenant__pages > checkout|
|<span style="color:green">customerReferenceMaxLength  </span> <br />Determines max length of the reference field<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "customerReferenceMaxLength", "value" : 25</span>|tenant__pages > checkout|
|<span style="color:green">showUomInfoForUoms </span> <br />Determines to which customer group the pallet calculation is shown<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "showUomInfoForUoms ", "value" :  ["PL"]</span>|tenant__pages > checkout|
|<span style="color:green">showOrderType </span> <br />Determines if Order Type choice is shown<br /><br />**Example** <br /> <span style="color:green">"platform" : "all", "key" : "showOrderType", "value" : false</span>|tenant__pages > checkout|

## Customer (group) settings
[See ERP data](erpdata.md#klanten)

