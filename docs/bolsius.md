---
id: bolsius
title: Bolsius
sidebar_label: Bolsius
---

## Lead times per country

[Lead times](customergroups.md#deliveryDateOptions) are defined in customergroups _country_ch_ and _country_at_. The sort order of these customer groups is lower than the default customer groups; the customer group with the lowest sort order will be applied.

These customer groups are not added to the customers via the connector yet.

As a work around, use the manual update process below:

1. Check if all customers per countrycode have been added to the right customer group

```
db.getCollection('bolsius__customers').find({'addresses.countryCode': 'BG','customergroups' : { $not : /country_bg/}})
```

2. If result = 1 or more, add them to the customer group
```
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'BG','customergroups' : { $not : /country_bg/}}, { $push: { 'customergroups': 'country_bg'}}, { multi: true})
```

3. Check again

**ToDo**
- Automatically add customer group _country_xx_ to customers -> connector

**Bulk update**
```
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'BE','customergroups' : { $not : /country_be/}}, { $push: { 'customergroups': 'country_be'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'BG','customergroups' : { $not : /country_bg/}}, { $push: { 'customergroups': 'country_bg'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'CZ','customergroups' : { $not : /country_cz/}}, { $push: { 'customergroups': 'country_cz'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'GR','customergroups' : { $not : /country_gr/}}, { $push: { 'customergroups': 'country_gr'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'HR','customergroups' : { $not : /country_hr/}}, { $push: { 'customergroups': 'country_hr'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'HU','customergroups' : { $not : /country_hu/}}, { $push: { 'customergroups': 'country_hu'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'NL','customergroups' : { $not : /country_nl/}}, { $push: { 'customergroups': 'country_nl'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'PL','customergroups' : { $not : /country_pl/}}, { $push: { 'customergroups': 'country_pl'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'RO','customergroups' : { $not : /country_ro/}}, { $push: { 'customergroups': 'country_ro'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'SI','customergroups' : { $not : /country_si/}}, { $push: { 'customergroups': 'country_si'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'LU','customergroups' : { $not : /country_lu/}}, { $push: { 'customergroups': 'country_lu'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'SK','customergroups' : { $not : /country_sk/}}, { $push: { 'customergroups': 'country_sk'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'DE','customergroups' : { $not : /country_de/}}, { $push: { 'customergroups': 'country_de'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'AT','customergroups' : { $not : /country_at/}}, { $push: { 'customergroups': 'country_at'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'CH','customergroups' : { $not : /country_ch/}}, { $push: { 'customergroups': 'country_ch'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'DK','customergroups' : { $not : /country_dk/}}, { $push: { 'customergroups': 'country_dk'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'GB','customergroups' : { $not : /country_gb/}}, { $push: { 'customergroups': 'country_gb'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'FI','customergroups' : { $not : /country_fi/}}, { $push: { 'customergroups': 'country_fi'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'IE','customergroups' : { $not : /country_ie/}}, { $push: { 'customergroups': 'country_ie'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'IT','customergroups' : { $not : /country_it/}}, { $push: { 'customergroups': 'country_it'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'NO','customergroups' : { $not : /country_no/}}, { $push: { 'customergroups': 'country_no'}}, { multi: true})
db.getCollection('bolsius__customers').update({'addresses.countryCode': 'SE','customergroups' : { $not : /country_se/}}, { $push: { 'customergroups': 'country_se'}}, { multi: true})
```