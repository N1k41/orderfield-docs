---
id: doc1
title: Introductie
sidebar_label: Introductie
---

OrderField  <=> ERP systeem.

* Alle data over bijv. producten, prijzen en klanten wordt beheerd in het ERP systeem.
=> De ERP data wordt geimporteerd in OrderField. 
* Orders worden samengesteld in OrderField
=> De orders worden geimporteerd in het ERP systeem.

## Basis Data (vanuit ERP systeem)

Om klanten toegang te geven en artikelen te laten bestellen zijn minimaal de volgende gegevens nodig:

* Producten (naam, artikelnummer)
* Prijzen
* Klanten (naam, klantnummer, adres)

Optioneel kunnen bijv. voorraden, kortingen en delivery leadtimes worden verwerkt.

[Meer over klantdata](doc3.md)

## Orders
Orders kunnen op verschillende manieren worden aangeboden aan het ERP systeem. De meest gangbare methoden zijn via een API / Webservice of via uitwisseling van files. 

Meest gangbare formaten zijn JSON, XML, TXT en CSV

[Meer over orders](doc4.md)


## Volgende stappen

* [Klantdata](doc3.md) 
* [Productdata](doc4.md)
* [Prijzen](doc4.md)     
* try [demo.orderfield.com](https://demo.orderfield.com)
* [contact us](mailto:info@orderfield.com)