# open-address-format

## Data

All files are in `/data` and named with country/region code in **ISO 3166-1 alpha-3**, the country/region name should also follow this standard.

If postcode exist, the match between with provincal level administration and postcode may need validation.

We imported a `basicInfo` key as metadata, Let describe order, special syntax and display format can be stored in one place. Because those data are not relevent to admin_level.

DisplayFormat is intended for `replace(key, data)`. And describe order is for culture influenced address written order between western and eastern. More Eastern country use `L2S` order because they usually written higher-evel part first.

## Hoped Usage

Like [this](https://github.com/openstreetmap/iD/blob/344a9031701f81e18b731974478d04e9f01c9ae9/modules/services/nsi.js#L43-L64), who want to use those data should load a index.json and then find countries/regions wanted.

Currently, when request https://cdn.jsdelivr.net/npm/open-address-format it will give a message:

> Couldn't find the requested file /index.min.js in open-address-format.

## Related Project

FYI

### Inspired by

+ https://github.com/yuiseki/osm-address-editor-vite

### Convert from country code with geojson

+ https://github.com/ideditor/country-coder
+ https://github.com/ideditor/location-conflation

### Editor that have address support

+ https://github.com/openstreetmap/iD/blob/develop/data/address_formats.json
+ https://github.com/streetcomplete/StreetComplete/blob/master/res/country_metadata/additionalValidHousenumberRegex.yml
+ https://github.com/JOSM/josm/blob/master/src/org/openstreetmap/josm/data/validation/tests/Addresses.java
+ https://github.com/JOSM/josm/blob/master/resources/data/validator/addresses.mapcss

### Faker package in different language

+ **JS**: https://github.com/faker-js/faker/blob/main/src/locales/zh_CN/address/index.ts
+ **Python**: https://github.com/joke2k/faker/blob/master/faker/providers/address/zh_CN/__init__.py
+ **Java**: https://github.com/DiUS/java-faker/blob/master/src/main/resources/zh-CN.yml
+ **C#**: https://github.com/slashdotdash/faker-cs/blob/master/src/Faker/Address.cs
+ **Golang**: https://github.com/bxcodec/faker/blob/master/address_test.go
+ **Rust**: https://github.com/cksac/fake-rs/blob/b897246bbe99a158977a03236c393c8d7b476823/fake/src/faker/impls/address.rs
+ **PHP**: https://github.com/fzaninotto/Faker/blob/master/src/Faker/Provider/zh_CN/Address.php
+ **Ruby**: https://github.com/faker-ruby/faker/blob/aa31845ed54c25eb2638d716bfddf59771b502aa/lib/faker/default/address.rb
+ **Swift**: https://github.com/vadymmarkov/Fakery/blob/71cb3bf36a808534659d1248780c2bf3c4c4fc91/Sources/Fakery/Generators/Address.swift
+ **Elixir**: https://github.com/elixirs/faker/blob/master/lib/faker/address/en.ex

## Reference

There will list some document and resource that can be seen knowledge in JSON format.

## Note

This project have no relevence with https://openaddresses.io/
