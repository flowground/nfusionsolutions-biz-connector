# ![LOGO](logo.png) nFusion Solutions Market Data API v1 **flow**ground Connector

## Description

A generated **flow**ground connector for the nFusion Solutions Market Data API v1 API (version 1).

Generated from: https://api.apis.guru/v2/specs/nfusionsolutions.biz/1/swagger.json<br/>
Generated at: 2019-05-07T17:43:15+03:00

## API Description

[nFusion Solutions](https://nfusionsolutions.com) provides [REST and streaming APIs](https://nfusionsolutions.com/data-feeds/) that deliver enterprise-grade financial data. Data sets include real-time and historical pricing for Spot prices of precious metals such as Gold, Silver, Platinum, and Palladium, exchange rates for major currency pairs, exchange rates for Crypto Currencies such as BTC, ETH, and LTC. All API access requires authentication. In order to be issued access credentials you must first enter into a service agreement with nFusion Solutions and acquire a commercial license. For information on how to obtain a licence [take a tour of our products](https://nfusionsolutions.com/nfusion-solutions-metals-gold-price-feed-tour/) or email sales@nfusionsolutions.com.

## Authorization

This API does not require authorization.

## Actions

### Get historical prices for requested currency pairs

> Historical OHLC data for the specified period and interval size<br/>
> <br/>
> The combination of the interval parameter and start and end dates can result in results<br/>
> being truncated to conform to result size limits. See comments on interval parameter for details on valid interval values.

*Tags:* `Currencies`

#### Input Parameters
* `token` - _required_ - auth token
* `pairs` - _required_ - comma separated list of currency pairs. For example: USD/CAD,USD/EUR,USD/AUD
* `start` - _required_ - start date of time period. format is <i>yyyy-mm-dd</i>
* `end` - _optional_ - end date of time period. format is <i>yyyy-mm-dd</i>. Default is current date.
* `interval` - _optional_ - aggregation interval. Composed of an optional integer value (which defaults to 1 when not specified), 
followed by a type string which must be one of the following values:
y=year,
m=month,
w=week,
d=day,
h=hour,
mi=minute

For example, a yearly interval can be specified as "y" and 6 month interval as "6m". 

If not specified the interval parameter default is 1 Day.
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get list of currency pairs supported by the history endpoint

> Only the currency pairs in the direction noted can be used with the history endpoint.<br/>
> For example: USD/CAD is not the same as CAD/USD

*Tags:* `Currencies`

#### Input Parameters
* `token` - _required_ - auth token
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get latest mid rate for requested currency pairs

> Current Mid Rate

*Tags:* `Currencies`

#### Input Parameters
* `token` - _required_ - auth token
* `pairs` - _required_ - comma separated list of currency pairs. For example: USD/CAD,USD/EUR,USD/AUD
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get list of currencies supported by the rate endpoint

> Any of the currencies in this list can be paired with any other currency in this list when supplied to the Rate endpoint.<br/>
> For example: USD/CAD,CAD/USD,USD/EUR,EUR/CAD

*Tags:* `Currencies`

#### Input Parameters
* `token` - _required_ - auth token
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get latest Summary for requested currency pairs

> Current and daily summary information combined into a single quote

*Tags:* `Currencies`

#### Input Parameters
* `token` - _required_ - auth token
* `pairs` - _required_ - comma separated list of currency pairs. For example: USD/CAD,USD/EUR,USD/AUD
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get list of currency pairs supported by the Summary endpoint

> Only the currency pairs in the direction noted can be used with the Summary endpoint.<br/>
> For example: USD/CAD is not the same as CAD/USD

*Tags:* `Currencies`

#### Input Parameters
* `token` - _required_ - auth token
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get historical benchmark prices for requested metals

> Historical OHLC data for the specified period and interval size<br/>
> <br/>
> The combination of the interval parameter and start and end dates can result in results<br/>
> being truncated to conform to result size limits. See comments on interval parameter for details on valid interval values.<br/>
> <br/>
> The historicalfx flag is used to determine whether to apply today's fx rates to a historical period, or to apply the historical rates from that same time frame.

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `metals` - _required_ - comma separated list of metals
* `start` - _required_ - start date of time period. format is <i>yyyy-mm-dd</i>
* `end` - _optional_ - end date of time period. format is <i>yyyy-mm-dd</i>. Default is current date.
* `interval` - _optional_ - aggregation interval. Composed of an optional integer value (which defaults to 1 when not specified), 
followed by a type string which must be one of the following values:
y=year,
m=month,
w=week,
d=day,
h=hour,
mi=minute

For example, a yearly interval can be specified as "y" and 6 month interval as "6m". 

If not specified the interval parameter default is 1 Day.
* `historicalfx` - _optional_ - if true use historical currency rates otherwise current currency rates. Defaults to false.
* `currency` - _optional_ - comma separated list of conversion currencies, defaults to USD
* `unitofmeasure` - _optional_ - unit of meaure, defaults to troy ounces. allowed values are:
mg=milligram
g=gram
kg=kilogram
gr=grain
oz=ounce
toz=troy ounce
ct=carat
dwt=pennyweight
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get latest Benchmark prices for requested metals

> Benchmark price information

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `metals` - _required_ - comma separated list of metals
* `currency` - _optional_ - comma separated list of conversion currencies, defaults to USD
* `unitofmeasure` - _optional_ - unit of meaure, defaults to troy ounces. allowed values are:
mg=milligram
g=gram
kg=kilogram
gr=grain
oz=ounce
toz=troy ounce
ct=carat
dwt=pennyweight
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get list of symbols supported by the benchmark endpoints

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get historical Spot prices for requested metals

> Historical OHLC data for the specified period and interval size<br/>
> <br/>
> The combination of the interval parameter and start and end dates can result in results<br/>
> being truncated to conform to result size limits. See comments on interval parameter for details on valid interval values.<br/>
> <br/>
> The historicalfx flag is used to determine whether to apply today's fx rates to a historical period, or to apply the historical rates from that same time frame.

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `metals` - _required_ - comma separated list of metals
* `start` - _required_ - start date of time period. format is <i>yyyy-mm-dd</i>
* `end` - _optional_ - end date of time period. format is <i>yyyy-mm-dd</i>. Default is current date.
* `interval` - _optional_ - aggregation interval. Composed of an optional integer value (which defaults to 1 when not specified), 
followed by a type string which must be one of the following values:
y=year,
m=month,
w=week,
d=day,
h=hour,
mi=minute

For example, a yearly interval can be specified as "y" and 6 month interval as "6m". 

If not specified the interval parameter default is 1 Day.
* `historicalfx` - _optional_ - if true use historical currency rates otherwise current currency rates. Defaults to false.
* `currency` - _optional_ - comma separated list of conversion currencies, defaults to USD
* `unitofmeasure` - _optional_ - unit of meaure, defaults to troy ounces. allowed values are:
mg=milligram
g=gram
kg=kilogram
gr=grain
oz=ounce
toz=troy ounce
ct=carat
dwt=pennyweight
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get Historical Performance for requested metals

> Historical Performance information

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `metals` - _required_ - comma separated list of metals
* `currency` - _optional_ - comma separated list of conversion currencies, defaults to USD
* `unitofmeasure` - _optional_ - unit of meaure, defaults to troy ounces. allowed values are:
mg=milligram
g=gram
kg=kilogram
gr=grain
oz=ounce
toz=troy ounce
ct=carat
dwt=pennyweight
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get Historical Annual Performance for requested metals

> Annual Historical Performance information

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `metals` - _required_ - comma separated list of metals
* `currency` - _optional_ - comma separated list of conversion currencies, defaults to USD
* `unitofmeasure` - _optional_ - unit of meaure, defaults to troy ounces. allowed values are:
mg=milligram
g=gram
kg=kilogram
gr=grain
oz=ounce
toz=troy ounce
ct=carat
dwt=pennyweight
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `years` - _optional_ - Number of years of history to return. Defaults to 10.
* `version` - _required_ - The requested API version

### Get historical Spot Ratio prices for requested metals

> Historical data for the specified period and interval size<br/>
> <br/>
> The combination of the interval parameter and start and end dates can result in results<br/>
> being truncated to conform to result size limits. See comments on interval parameter for details on valid interval values.

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `pairs` - _required_ - comma separated list of metals
* `start` - _required_ - start date of time period. format is <i>yyyy-mm-dd</i>
* `end` - _optional_ - end date of time period. format is <i>yyyy-mm-dd</i>. Default is current date.
* `interval` - _optional_ - aggregation interval. Composed of an optional integer value (which defaults to 1 when not specified), 
followed by a type string which must be one of the following values:
y=year,
m=month,
w=week,
d=day,
h=hour,
mi=minute

For example, a yearly interval can be specified as "y" and 6 month interval as "6m". 

If not specified the interval parameter default is 1 Day.
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get latest Spot Summary for requested metal ratios

> Ratios between prices of two metals

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `pairs` - _required_ - comma separated list of metal pairs. For example: gold/silver,gold/platinum,silver/palladium
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get latest Spot Summary for requested metals

> Current and daily summary information combined into a single quote

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `metals` - _required_ - comma separated list of metals
* `currency` - _optional_ - comma separated list of conversion currencies, defaults to USD
* `unitofmeasure` - _optional_ - unit of meaure, defaults to troy ounces. allowed values are:
mg=milligram
g=gram
kg=kilogram
gr=grain
oz=ounce
toz=troy ounce
ct=carat
dwt=pennyweight
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `adjust` - _optional_ - apply global and per-tenant spot price adjustments. Defaults to true.
* `version` - _required_ - The requested API version

### Get list of symbols supported by the spot endpoints

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

### Get list of currencies supported by metals endpoints for currency conversion

*Tags:* `Metals`

#### Input Parameters
* `token` - _required_ - auth token
* `format` - _optional_ - to override content negotiation specify a value of json or xml
* `version` - _required_ - The requested API version

## License

**flow**ground :- Telekom iPaaS / nfusionsolutions-biz-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
