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

* `Naam`
* `Klantnummer`
* `Factuuradres`
* `Afleveradres(sen)`
* `Telefoonnummer`
* `Status` - actief / niet actief

[Bekijk alle klantproperties](#)

## Producten
Productdata bestaat uit een aantal standaard gegevens

| Attribute | Format | Remarks |
| --- | --- | --- |
| id | <span style="color:red">**Required** </span> <br />Your product’s unique identifier <br /><br />**Example** <br /> <span style="color:green">12345</span><br /><br /> **Syntax** <br /> Max 50 characters |<ul><li>Use a unique value for each product. Use the product's SKU where possible</li><li>Keep the ID the same when updating your data</li><li>Use only valid unicode characters. Avoid invalid characters like control, function, or private area characters</li><li>Use the same ID for the same product - across countries or languages</li></ul> |
| title | <span style="color:red">**Required** </span> <br />Your product’s name <br /><br />**Example** <br /> <span style="color:green">Demo Guitar Deluxe</span><br /><br /> **Syntax** <br /> Max 150 characters |<ul><li>Accurately describe your product</li></ul> |
| description | <span style="color:orange">**Optional** </span> <br />Your product’s description <br /><br />**Example** <br /> <span style="color:green">Demo Guitar Deluxe</span><br /><br /> **Syntax** <br /> Max 5000 characters |<ul><li>Accurately describe your product</li><li>Don’t include promotional text like "free shipping," all capital letters, or gimmicky foreign characters</li><li>Include only information about the product. Don’t include links to your store, sales information, details about competitors, other products, or accessories</li></ul> |
| facets | <span style="color:orange">**Optional** </span> <br />Array with characteristics of your product <br /><br />**Example** <br /> <span style="color:green">["color:green","height:12","safety-class:S3"]</span><br /><br /> **Syntax** <br /> Max 50 characters per facet |<ul><li>Include one value per facet</li><li>Can be used to create (catalogue) filters</li><li>Can be displayed on the item details screen</li><li>Can be used for search</li></ul> |


## Prijzen

Prijzen kunnen worden aangeleverd per product of per klant.
| Attribute | Format | Remarks |
| --- | --- | --- |
| price | <span style="color:red">**Required** </span> <br />The price of your product <br /><br />**Example** <br /> <span style="color:green">12</span><br /><br /> **Syntax** <br /> Numeric |<ul><li>Accurately submit the product's price and currency</li></ul> |