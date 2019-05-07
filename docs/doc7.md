---
id: doc7
title: XML - JD Edwards
sidebar_label: XML - JD Edwards
---

Voorbeeld XML tbv JD Edwards

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