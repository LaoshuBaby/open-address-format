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

### Convert from country code with geojson

+ https://github.com/ideditor/country-coder
+ https://github.com/ideditor/location-conflation

### Editor that have address support

+ https://github.com/openstreetmap/iD/blob/develop/data/address_formats.json
+ https://github.com/streetcomplete/StreetComplete/blob/master/res/country_metadata/additionalValidHousenumberRegex.yml
+ https://github.com/JOSM/josm/blob/master/src/org/openstreetmap/josm/data/validation/tests/Addresses.java
+ https://github.com/JOSM/josm/blob/master/resources/data/validator/addresses.mapcss


## Note

This project have no relevence with https://openaddresses.io/