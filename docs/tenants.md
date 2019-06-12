---
id: tenants
title: Tenants
sidebar_label: Tenants
---

The main settings are defined in collection _main > main__settings_

These settings can be overridden in collection: _tenant > tenant__settings_

|Attribute|Format|Remarks|
|---|---|---|
|ga_tracking_id|<span style="color:orange">**Optional** </span> <br />GA Tracking ID</span><br /><br />**Example** <br /> <span style="color:green">{"key" : "ga_tracking_id", "value" : "UA-87774626-1"}</span>||
|gtm_tracking_id|<span style="color:orange">**Optional** </span> <br />GTM Tracking ID</span><br /><br />**Example** <br /> <span style="color:green">{"key" : "gtm_tracking_id", "value" : "UA-87774626-1"}</span>|<ul><li>Not in use (yet)</li></ul>|
|quantity_picker|<span style="color:orange">**Optional** </span><br/>Indicates which quantity picker should be used</span> <br/><br/>**Example** <br /> <span style="color:green">{"key" : "quantity_picker", "value" : "relative"}</span><br/><br/>**Syntax**<br><span style="color:green">absolute</span> (default) ; <span style="color:green">relative</span>|<ul><li><span style="color:green">absolute</span><br/>shows the absolute quantity and uses that value for calculations (e.g. 1 box of 12 pieces -> 12 pieces)</li><li><span style="color:green">relative</span><br/>shows the number of sales units and uses that value for calculations (e.g. 1 box of 12 pieces -> 1 box) </li></ul>|
|MAIL_ORDER_CONFIRMATION|<span style="color:orange">**Optional** </span> <br />Settings of the order confirmation emails <br /><br />**Sub-attributes** <br /><ul><li><span style="color:green">mail_from</span><br/>From-address</li><li><span style="color:green">mail_cc</span> (array)<br/>CC to </li><li><span style="color:green">mail_bcc</span> (array)<br/>BCC to</li><li><span style="color:green">default_template_id</span><br/>Postmark template ID</li><li><span style="color:green">template_ids</span> (array)<br/>Postmark template ID per language</li><li><span style="color:green">logo_url</span><br/>Logo URL</li><li><span style="color:green">mail_sender_name</span><br/>Name of the sender</li></ul>|<ul><li>If no settings are available, the default OrderField values are used</li></ul>|
|show_breadcrumbs| <span style="color:orange">**Optional** </span> <br />Indicates if breadcumbs should be shown<br /><br />**Example** <br /> <span style="color:green">{"key" : "show_breadcrumbs","value" : false,"roles" : []}</span><br/><br /> **Syntax** <br /> <span style="color:green">true</span> (default) ; <span style="color:green">false</span>||