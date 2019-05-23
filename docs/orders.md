---
id: orders
title: Orders
sidebar_label: Orders
---

Orders kunnen op verschillende manieren worden aangeboden aan het ERP systeem. De meest gangbare methoden zijn via een API / Webservice of via uitwisseling van files.

Ondersteunde formaten zijn o.a. JSON, XML, TXT en CSV

Hieronder enkele voorbeelden.

## TXT - Microsoft Dynamics NAV

```
HH99
OO10708203853600120190509015EUR00.0060004100.00JJ        00002370.2420190509
RR1070822019050955002800072001.75000.0000000000000100082322 
RR1070822019050962073000192000.80000.0003684200600100082322 
RR1070822019050962075200144000.55000.0003691500400100082322 
RR1070822019050962072900144000.85000.0003680800500100082322 
RR1070822019050962050500192001.25000.0000000000000100082322 
RR1070822019050962046700096000.99000.0003695300100100082322 
RR1070822019050964006700012004.25000.0000000000000100082322 
RR1070822019050961020900048001.75000.0003680900200100082322 
RR1070822019050972027800012011.50000.0000000000000100082322 
RR1070822019050962039000192000.55000.0003687001100100082322 
RR1070822019050972169700036001.25000.0003701400200100082322 
RR1070822019050961006300012004.10000.0003671800400100082322 
RR1070822019050962013800144000.95000.0000000000000100082322 
RR1070822019050952009000036004.65000.0000000000000100082322 
RR1070822019050954020000096002.15000.0003692500100100082322 
RR1070822019050962065600192000.95000.0003672000200100082322 
RR1070822019050962071000036000.85000.0003684000200100082322 
RR1070822019050957021000048002.95000.0000000000000100082322 
RR1070822019050955002700144001.50000.0000000000000100082322 
```

> NB. Koppeling met Microsoft Dynamics NAV gaat meestal op basis van de [OData Web Service](https://docs.microsoft.com/en-us/dynamics-nav/odata-web-services) 

## TXT - Xlenz

```
ORDHDR	Website	210916-	20190509								82586778.0567200000				82586781.0567200000							20190509														
ORDPOS	1	954626.0567200000|954644.0567200000	1												20190509	
ORDPOS	2	72249793.0567200000|74047419.0567200000	1												20190509	
ORDPOS	3	72249793.0567200000|72249796.0567200000	1												20190509	
ORDPOS	4	72249793.0567200000|72249802.0567200000	4												20190509	
ORDPOS	5	72249793.0567200000|72249805.0567200000	1												20190509	
ORDPOS	6	79716597.0567200000|79716579.0567200000	2												20190509	
ORDPOS	7	67376949.0567200000|67376961.0567200000	1												20190509	
ORDPOS	8	49574661.0567200000|49574670.0567200000	1												20190509	
ORDPOS	9	49574661.0567200000|49574676.0567200000	2												20190509	
ORDPOS	10	49574661.0567200000|49574679.0567200000	3												20190509	
ORDPOS	11	67140490.0567200000|67140496.0567200000	2												20190509	
ORDPOS	12	67140490.0567200000|67140499.0567200000	1												20190509	
ORDPOS	13	67140490.0567200000|67140502.0567200000	2												20190509	
ORDPOS	14	93653465.0567200000|93653448.0567200000	1												20190509	
ORDPOS	15	93653556.0567200000|93653559.0567200000	2												20190509	
ORDPOS	16	93653556.0567200000|93653565.0567200000	1												20190509	
ORDPOS	17	93653556.0567200000|93653568.0567200000	1												20190509	
ORDPOS	18	93653781.0567200000|93653747.0567200000	1												20190509	
ORDPOS	19	93653781.0567200000|93653750.0567200000	1												20190509	
ORDPOS	20	93653828.0567200000|93653807.0567200000	1												20190509	
ORDPOS	21	93653828.0567200000|93653809.0567200000	1	
```

## XML - Xlenz ESB

```
<Orders>
<OrderHeader>
<WebOrderNr>ORDER_12345</WebOrderNr>
<ProviderCode>Testcustomer</ProviderCode>
<Company_obj>374.33961000</Company_obj>
<OrderDate>2019-05-07</OrderDate>
<CustomerCode>00703</CustomerCode>
<WarehouseCode>1</WarehouseCode>
<OrderOriginCode>09</OrderOriginCode>
<OrderTypeCode>8</OrderTypeCode>
<CustomerReference>823027</CustomerReference>
<AdditionalInformation/>
<OrderLines>
<OrderLine>
<WebOrderLineSeq>1</WebOrderLineSeq>
<CustomerItemOrder>823027:1</CustomerItemOrder>
<ItemDimension_obj>35695.33961000</ItemDimension_obj>
<ItemDimensionSize_obj>35698.33961000</ItemDimensionSize_obj>
<ItemCode>21</ItemCode>
<OrderedQty>100</OrderedQty>
<SalesPriceAmt>0.59</SalesPriceAmt>
<SalesPriceAmtFromWebsite>0.59</SalesPriceAmtFromWebsite>
<SalesPricePer>1</SalesPricePer>
<EarliestDeliveryDate>2019-05-07</EarliestDeliveryDate>
<OrderLineTexts/>
<OrderLineCustomFields/>
</OrderLine>
<OrderLine>
<WebOrderLineSeq>2</WebOrderLineSeq>
<CustomerItemOrder>823027:2</CustomerItemOrder>
<ItemDimension_obj>186881502.33961000</ItemDimension_obj>
<ItemDimensionSize_obj>186889517.33961000</ItemDimensionSize_obj>
<ItemCode>31343</ItemCode>
<OrderedQty>1</OrderedQty>
<SalesPriceAmt>49.95</SalesPriceAmt>
<SalesPriceAmtFromWebsite>49.95</SalesPriceAmtFromWebsite>
<SalesPricePer>1</SalesPricePer>
<EarliestDeliveryDate>2019-05-07</EarliestDeliveryDate>
<OrderLineTexts/>
<OrderLineCustomFields/>
</OrderLine>
</OrderLines>
<DeliveryAddresses>
<DeliveryAddress>
<DeliveryAddress_obj>26723.33961000</DeliveryAddress_obj>
</DeliveryAddress>
</DeliveryAddresses>
<CustomerAddress>
<Name>Test Customer</Name>
<Street>Test street</Street>
<HouseNr>32</HouseNr>
<HouseNrExt/>
<ZipCode>1000 AA</ZipCode>
<City>TESTCITY</City>
<CountryIsoCode>NL</CountryIsoCode>
<Phone>0201234567</Phone>
<Email>test@testcustomer.nl</Email>
</CustomerAddress>
<OrderHeaderTexts/>
<OrderHeaderCustomFields/>
</OrderHeader>
</Orders>
```

## XML - Oracle JD Edwards

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<Order>
  <OrderHeader>
    <Customer>
      <AddressNumber>999996</AddressNumber>
      <Name>Test Customer</Name>
    </Customer>
    <OrderDate format="yyyymmdd">20190305</OrderDate>
    <DeliveryDate format="yyyymmdd">20190308</DeliveryDate>
    <CustomerPO>Customer reference</CustomerPO>
    <WebshopPO>98</WebshopPO>
    <Remarks/>
    <OrderTakenBy>WEB</OrderTakenBy>
  </OrderHeader>
  <OrderDetail>
    <OrderLine>
      <Item>102025330463</Item>
      <OrderedQuantity>1</OrderedQuantity>
    </OrderLine>
  </OrderDetail>
</Order>
```

