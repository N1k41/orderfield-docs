---
id: prices
title: Prices
sidebar_label: Prices
---

Prices can be configured per product, per customer or per customer group. The platform also supports tier pricing.

| Attribute | Format | Remarks |
| --- | --- | --- |
| <a name="price.productcode"></a>productcode | <span style="color:red">**Required** </span> <br />Product code to which the price applies<br /><br />**Example** <br /> <span style="color:green">12345</span><br /><br /> **Syntax** <br />Max 50 characters |<ul><li>The product code should match one product</li></ul>|
| <a name="price.prices"></a> prices| <span style="color:red">**Required** </span> <br />Price(s) of your product<br /><br />**Example** <br /> <span style="color:green">[ "price" : 1.6, "currency" : "EUR", "minQuantity" : 1]</span><br /><br /> **Syntax** <br /> <span style="color:green">prices</span> uses 3 sub-attributes:<br/><ul><li><span style="color:green">price</span> (required)<br/>Numeric</li><li><span style="color:green">currency</span> (optional)<br/>ISO 4217</li><li><span style="color:green">minQuantity</span> (optional)<br/>Numeric</li> |<ul><li>Multi currency is supported</li></ul> |
| <a name="price.pricegroup"></a>pricegroup | <span style="color:orange">**Optional** </span> <br />Price group to which the price applies <br /><br />**Example** <br /> <span style="color:green">pricegroup=ALL</span><br /><br /> **Syntax** <br />Max 50 characters |<ul><li>Price groups link customers to prices</li></ul>|
| <a name="price.minQuantity"></a>minQuantity | <span style="color:orange">**Optional** </span> <br />Minimum quantity <br /><br />**Example** <br /> <span style="color:green">120</span><br /><br /> **Syntax** <br />Numeric |<ul><li>The minimum quantity that can be ordered</li>|
| <a name="price.stepping"></a>stepping | <span style="color:orange">**Optional** </span> <br />Number of products per sales unit <br /><br />**Example** <br /> <span style="color:green">12</span><br /><br /> **Syntax** <br />Numeric |<ul><li>Is used when a product ships in bundles of more than one piece per sales unit (e.g. 12 pieces in a box)</li><li>Can be used for pricing per sales unit (instead of pricing per piece)</li></ul>|

>Discounts are set at [customer](customers.md#customer.discounts) level