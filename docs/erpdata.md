---
id: erpdata
title: ERP Data
sidebar_label: ERP Data
---

Tijdens het aansluiten van je bedrijf wordt je ERP data 'gemapt' naar het datamodel van OrderField. Hieronder de belangrijkste entiteiten en attributes.

* [Klanten](#klanten)
* [Producten](#producten)
* [Prijzen](#prijzen)


## Klanten

Klanten hebben doorgaans onderstaande attributes

| Attribute | Format | Remarks |
| --- | --- | --- |
| <a name="customer.code"></a>code | <span style="color:red">**Required** </span> <br />Your customers's unique identifier <br /><br />**Example** <br /> <span style="color:green">12345</span><br /><br /> **Syntax** <br /> Max 50 characters |<ul><li>Use a unique value for each customer</li><li>Keep the code the same when updating your data</li><li>Use only valid unicode characters. Avoid invalid characters like control, function, or private area characters</li><li>Use the same code for the same customer - across countries or languages</li></ul> |
| <a name="customer.name"></a>name | <span style="color:red">**Required** </span> <br />Your customer's name <br /><br />**Example** <br /> <span style="color:green">Acme Company</span><br /><br /> **Syntax** <br /> Max 150 characters |<ul><li>Try to keep the name clean (avoid codes, remarks, unnecessary characters)</li></ul> |
| <a name="customer.addresses"></a>addresses | <span style="color:red">**Required** </span> <br />Array with your customer's address(es) <br /><br />**Example** <br /> <span style="color:green">["isPrimary":true, "code":"123456", "type":"Delivery", "name":"Cantona Olsztyn", "addressLine1":"ul. Kanta 230", "zipCode":"10-691", "city":"Olsztyn", "countryCode":"PL", "country":"Polska"]</span><br /><br /> **Syntax** <br /> <span style="color:green">addresses</span> uses 9 sub-attributes:<ul><li><span style="color:green">isPrimary</span> (optional)<br/>The default address</li><li><span style="color:green">code</span> (optional)<br/>The _unique_ address Id</li><li><span style="color:green">type</span> (optional)<br/>The address type: shipping or delivery</li><li><span style="color:green">name</span> (required)<br/>Name of the company</li><li><span style="color:green">addressLine1</span> (required)<br/>Street and number</li><li><span style="color:green">zipCode</span> (required)<br/>Zip code</li><li><span style="color:green">city</span> (required)<br/>City</li><li><span style="color:green">countryCode</span> (required)<br/>Two character country code</li><li><span style="color:green">country</span> (optional)<br/>Country name</li></ul> |<ul><li>If your customer has one address, that's fine. Just make sure the required sub-attributes are filled.</li></ul>|
| <a name="customer.phonenumber"></a>phonenumber | <span style="color:orange">**Optional** </span> <br />Your customer's phone number <br /><br />**Example** <br /> <span style="color:green">061234567</span><br /><br /> **Syntax** <br /> Numeric max 12 characters | |
| <a name="customer.currency"></a>currency | <span style="color:orange">**Optional** </span> <br />Your customer's currency <br /><br />**Example** <br /> <span style="color:green">EUR</span><br /><br /> **Syntax** <br /> 3 character currency code (ISO 4217) | |
| <a name="customer.language"></a>language | <span style="color:orange">**Optional** </span> <br />Your customer's preferred language <br /><br />**Example** <br /> <span style="color:green">en</span><br /><br /> **Syntax** <br /> 2 character language code (ISO 639-1) |<ul><li>Sets the default language in which the apps are initially displayed</li><li>Can be overridden by the customer accounts</li></ul>|
| <a name="customer.blocked"></a>blocked | <span style="color:orange">**Optional** </span> <br />Indicates the customer is  blocked <br /><br />**Example** <br /> <span style="color:green">true</span><br/><br /> **Syntax** <br /> <span style="color:green">true ; false</span><br/><span style="color:green">1 ; 0</span> |<ul><li>Blocked customers are not allowed to login or create user accounts</li></ul>|
| <a name="customer.showprices"></a>showprices | <span style="color:orange">**Optional** </span> <br />Indicates the customer is allowed to see prices<br /><br />**Example** <br /> <span style="color:green">true</span><br/><br /> **Syntax** <br /> <span style="color:green">true ; false</span><br/><span style="color:green">1 ; 0</span> |<ul><li>For (potential) customers that are allowed to view the products without prices or the ability place orders</li></ul>|
| <a name="customer.minOrderValue"></a>minOrderValue | <span style="color:orange">**Optional** </span> <br />Minimum order value <br /><br />**Example** <br /> <span style="color:green">360</span><br/><br /> **Syntax** <br /> Numeric |<ul><li>Orders below this value can not be submitted</li></ul>|
| <a name="customer.customergroups"></a>customergroups | <span style="color:orange">**Optional** </span> <br />The customer group(s) of the customer<br /><br />**Example** <br /> <span style="color:green">["country_10", "customergroup_9999"] </span><br/><br /> **Syntax** <br /> Max 50 characters per customergroup ||
| <a name="customer.pricegroups"></a>pricegroups | <span style="color:orange">**Optional** </span> <br />The price group(s) of the customer<br /><br />**Example** <br /> <span style="color:green">["retail_eu", "export"] </span><br/><br /> **Syntax** <br /> Max 50 characters per pricegroup |<ul><li>Pricegroups can be applied to any number of customers</li></ul>|

## Producten
Productdata bestaat uit een aantal standaard gegevens

| Attribute | Format | Remarks |
| --- | --- | --- |
| <a name="product.code"></a>code | <span style="color:red">**Required** </span> <br />Your product’s unique identifier <br /><br />**Example** <br /> <span style="color:green">12345</span><br /><br /> **Syntax** <br /> Max 50 characters |<ul><li>Use a unique value for each product. Use the product's SKU where possible</li><li>Keep the code the same when updating your data</li><li>Use only valid unicode characters. Avoid invalid characters like control, function, or private area characters</li><li>Use the same code for the same product - across countries or languages</li></ul> |
| <a name="product.name"></a>name | <span style="color:red">**Required** </span> <br />Your product’s name <br /><br />**Example** <br /> <span style="color:green">Demo Guitar Deluxe</span><br /><br /> **Syntax** <br /> Max 150 characters |<ul><li>Accurately describe your product</li></ul> |
| <a name="product.desc"></a>desc | <span style="color:orange">**Optional** </span> <br />Your product’s description <br /><br />**Example** <br /> <span style="color:green">The Demo Guitar Deluxe has a solid mahogany body with maple top and a rounded 50's-style mahogany neck with a rosewood fingerboard and trapezoid inlays.</span><br /><br /> **Syntax** <br /> Max 5000 characters |<ul><li>Accurately describe your product</li><li>Don’t include promotional text like "free shipping," all capital letters, or gimmicky foreign characters</li><li>Include only information about the product</li></ul> |
| <a name="product.facets"></a>facets | <span style="color:orange">**Optional** </span> <br />Characteristics of your product <br /><br />**Example** <br /> <span style="color:green">["color=green","height=12","safety-class=S3","brand=10","producttype=12"]</span><br /><br /> **Syntax** <br /> Max 50 characters per facet |<ul><li>Include one value per facet</li><li>Can be used to create (catalogue) filters on characteristics like brand or category</li><li>Can be displayed on the item details screen</li><li>Can be used for search</li></ul> |
| <a name="product.barcode"></a>barcode | <span style="color:orange">**Optional** </span> <br />The barcode of your product<br /><br />**Example** <br /> <span style="color:green">8717847129192</span><br /><br /> **Syntax** <br /> Max 50 numeric characters |<ul><li>Exclude dashes and spaces</li><li>Supported values include EAN, JAN, UPC, ISBN, ITF-14</li><li>Different barcodes for multipacks or bundles are supported</li><li>Can be used for scanning</li></ul> |



## Prijzen

Prijzen kunnen worden aangeleverd per product of per product / klant(groep).

| Attribute | Format | Remarks |
| --- | --- | --- |
| <a name="price.productcode"></a>productcode | <span style="color:red">**Required** </span> <br />Product code to which the price applies<br /><br />**Example** <br /> <span style="color:green">12345</span><br /><br /> **Syntax** <br />Max 50 characters |<ul><li>The product code should match one product</li></ul>|
| <a name="price.prices"></a> prices| <span style="color:red">**Required** </span> <br />Price(s) of your product<br /><br />**Example** <br /> <span style="color:green">[ "price" : 1.6, "currency" : "EUR", "minQuantity" : 1]</span><br /><br /> **Syntax** <br /> <span style="color:green">prices</span> uses 3 sub-attributes:<br/><ul><li><span style="color:green">price</span> (required)<br/>Numeric</li><li><span style="color:green">currency</span> (optional)<br/>ISO 4217</li><li><span style="color:green">minQuantity</span> (optional)<br/>Numeric</li> |<ul><li>Multi currency is supported</li></ul> |
| <a name="price.pricegroup"></a>pricegroup | <span style="color:orange">**Optional** </span> <br />Price group to which the price applies <br /><br />**Example** <br /> <span style="color:green">pricegroup=ALL</span><br /><br /> **Syntax** <br />Max 50 characters |<ul><li>Price groups link customers to prices</li></ul>|
| <a name="price.minQuantity"></a>minQuantity | <span style="color:orange">**Optional** </span> <br />Minimum quantity <br /><br />**Example** <br /> <span style="color:green">120</span><br /><br /> **Syntax** <br />Numeric |<ul><li>The minimum quantity that can be ordered</li>|
| <a name="price.stepping"></a>stepping | <span style="color:orange">**Optional** </span> <br />Number of products per sales unit <br /><br />**Example** <br /> <span style="color:green">12</span><br /><br /> **Syntax** <br />Numeric |<ul><li>Is used when a product ships in bundles of more than one piece per sales unit (e.g. 12 pieces in a box)</li><li>Can be used for pricing per sales unit</li></ul>|