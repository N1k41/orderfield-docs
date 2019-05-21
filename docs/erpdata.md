---
id: erpdata
title: ERP Data
sidebar_label: ERP Data
---

Om klanten toegang te geven en producten te laten bestellen zijn minimaal de volgende gegevens nodig:

* [Klanten](#klanten)
* [Producten](#producten)
* [Prijzen](#prijzen)

## Klanten

Klanten hebben doorgaans onderstaande properties

| Attribute | Format | Remarks |
| --- | --- | --- |
| code | <span style="color:red">**Required** </span> <br />Your customers's unique identifier <br /><br />**Example** <br /> <span style="color:green">12345</span><br /><br /> **Syntax** <br /> Max 50 characters |<ul><li>Use a unique value for each customer</li><li>Keep the code the same when updating your data</li><li>Use only valid unicode characters. Avoid invalid characters like control, function, or private area characters</li><li>Use the same code for the same customer - across countries or languages</li></ul> |
| name | <span style="color:red">**Required** </span> <br />Your customer's name <br /><br />**Example** <br /> <span style="color:green">Acme Company</span><br /><br /> **Syntax** <br /> Max 150 characters |<ul><li>Try to keep the name clean (avoid codes, remarks, unnecessary characters)</li></ul> |
| addresses | <span style="color:red">**Required** </span> <br />Array with your customer's address(es) <br /><br />**Example** <br /> <span style="color:green">["isPrimary":true, "code":"123456", "type":"Delivery", "name":"Cantona Olsztyn", "addressLine1":"ul. Kanta 230", "zipCode":"10-691", "city":"Olsztyn", "countryCode":"PL", "country":"Polska"]</span><br /><br /> **Syntax** <br /> <span style="color:green">addresses</span> uses 9 sub-attributes:<ul><li><span style="color:green">isPrimary</span> (optional)<br/>The default address</li><li><span style="color:green">code</span> (optional)<br/>The _unique_ address Id</li><li><span style="color:green">type</span> (optional)<br/>The address type: shipping or delivery</li><li><span style="color:green">name</span> (required)<br/>Name of the company</li><li><span style="color:green">addressLine1</span> (required)<br/>Street and number</li><li><span style="color:green">zipCode</span> (required)<br/>Zip code</li><li><span style="color:green">city</span> (required)<br/>City</li><li><span style="color:green">countryCode</span> (required)<br/>Two character country code</li><li><span style="color:green">country</span> (optional)<br/>Country name</li></ul> |<ul><li>If your customer has one address, that's fine. Just make sure the required sub-attributes are filled.</li></ul>|
| phonenumber | <span style="color:orange">**Optional** </span> <br />Your customer's phone number <br /><br />**Example** <br /> <span style="color:green">061234567</span><br /><br /> **Syntax** <br /> Numeric max 12 characters | |
| currency | <span style="color:orange">**Optional** </span> <br />Your customer's currency <br /><br />**Example** <br /> <span style="color:green">EUR</span><br /><br /> **Syntax** <br /> 3 character currency code (ISO 4217) | |
| language | <span style="color:orange">**Optional** </span> <br />Your customer's preferred language <br /><br />**Example** <br /> <span style="color:green">en</span><br /><br /> **Syntax** <br /> 2 character language code (ISO 639-1) |<ul><li>Sets the default language in which the apps are initially displayed</li><li>Can be overridden by the customer accounts</li></ul>|
| blocked | <span style="color:orange">**Optional** </span> <br />Indication if the customer is still valid <br /><br />**Example** <br /> <span style="color:green">true</span><br/><br /> **Syntax** <br /> <span style="color:green">true ; false</span><br/><span style="color:green">1 ; 0</span> ||
| showprices | <span style="color:orange">**Optional** </span> <br />Determines if the customer is allowed to see prices<br /><br />**Example** <br /> <span style="color:green">true</span><br/><br /> **Syntax** <br /> <span style="color:green">true ; false</span><br/><span style="color:green">1 ; 0</span> ||


## Producten
Productdata bestaat uit een aantal standaard gegevens

| Attribute | Format | Remarks |
| --- | --- | --- |
| code | <span style="color:red">**Required** </span> <br />Your product’s unique identifier <br /><br />**Example** <br /> <span style="color:green">12345</span><br /><br /> **Syntax** <br /> Max 50 characters |<ul><li>Use a unique value for each product. Use the product's SKU where possible</li><li>Keep the code the same when updating your data</li><li>Use only valid unicode characters. Avoid invalid characters like control, function, or private area characters</li><li>Use the same code for the same product - across countries or languages</li></ul> |
| name | <span style="color:red">**Required** </span> <br />Your product’s name <br /><br />**Example** <br /> <span style="color:green">Demo Guitar Deluxe</span><br /><br /> **Syntax** <br /> Max 150 characters |<ul><li>Accurately describe your product</li></ul> |
| description | <span style="color:orange">**Optional** </span> <br />Your product’s description <br /><br />**Example** <br /> <span style="color:green">Demo Guitar Deluxe</span><br /><br /> **Syntax** <br /> Max 5000 characters |<ul><li>Accurately describe your product</li><li>Don’t include promotional text like "free shipping," all capital letters, or gimmicky foreign characters</li><li>Include only information about the product. Don’t include links to your store, sales information, details about competitors, other products, or accessories</li></ul> |
| facets | <span style="color:orange">**Optional** </span> <br />Array with characteristics of your product <br /><br />**Example** <br /> <span style="color:green">["color:green","height:12","safety-class:S3"]</span><br /><br /> **Syntax** <br /> Max 50 characters per facet |<ul><li>Include one value per facet</li><li>Can be used to create (catalogue) filters</li><li>Can be displayed on the item details screen</li><li>Can be used for search</li></ul> |
| barcode | <span style="color:orange">**Optional** </span> <br />The barcode of your product<br /><br />**Example** <br /> <span style="color:green">8717847129192</span><br /><br /> **Syntax** <br /> Max 50 numeric characters |<ul><li>Exclude dashes and spaces</li><li>Supported values include EAN, JAN, UPC, ISBN, ITF-14</li><li>Multipacks and bundles are supported</li><li>Can be used for scanning</li></ul> |



## Prijzen

Prijzen kunnen worden aangeleverd per product of per product / klant(groep).
| Attribute | Format | Remarks |
| --- | --- | --- |
| price | <span style="color:red">**Required** </span> <br />The price of your product <br /><br />**Example** <br /> <span style="color:green">12</span><br /><br /> **Syntax** <br /> Numeric |<ul><li>Accurately submit the product's price</li></ul> |