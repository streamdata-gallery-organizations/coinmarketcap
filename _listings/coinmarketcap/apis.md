---
name: CoinMarketCap
x-slug: coinmarketcap
description: Cryptocurrency market cap rankings, charts, and more
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
x-kinRank: "7"
x-alexaRank: "276"
tags: CoinMarketCap
created: "2018-08-29"
modified: "2018-08-29"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/apis.md
specificationVersion: "0.14"
apis:
- name: CoinMarketCap Professional API Documentation - Get metadata
  x-api-slug: v1cryptocurrencyinfo-get
  description: |-
    Returns all static metadata for one or more cryptocurrencies including name, symbol, logo, and its various registered URLs.

    **This endpoint is available on the following API plans:**
    - Starter
    - Hobbyist
    - Standard
    - Professional
    - Enterprise

    **Cache / Update frequency:** Static data is updated only as needed, every 30 seconds.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencyinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencyinfo-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get CoinMarketCap ID map
  x-api-slug: v1cryptocurrencymap-get
  description: |-
    Returns a paginated list of all cryptocurrencies by CoinMarketCap ID. We recommend using this convenience endpoint to lookup and utilize our unique cryptocurrency `id` across all endpoints as typical identifiers like ticker symbols can match multiple cryptocurrencies and change over time. As a convenience you may pass a comma-separated list of cryptocurrency symbols as `symbol` to filter this list to only those you require.


      **This endpoint is available on the following API plans:**
      - Starter
      - Hobbyist
      - Standard
      - Professional
      - Enterprise

    **Cache / Update frequency:** Mapping data is updated only as needed, every 30 seconds.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencymap-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencymap-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get metadata
  x-api-slug: v1exchangeinfo-get
  description: |-
    Returns all static metadata for one or more exchanges including logo and homepage URL.

      **This endpoint is available on the following API plans:**
      - ~~Starter~~
      - Hobbyist
      - Standard
      - Professional
      - Enterprise

    **Cache / Update frequency:** Static data is updated only as needed, every 30 seconds.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangeinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangeinfo-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get CoinMarketCap ID map
  x-api-slug: v1exchangemap-get
  description: |-
    Returns a paginated list of all cryptocurrency exchanges by CoinMarketCap ID. We recommend using this convenience endpoint to lookup and utilize our unique exchange `id` across all endpoints as typical exchange identifiers may change over time. As a convenience you may pass a comma-separated list of exchanges by `slug` to filter this list to only those you require.

    **This endpoint is available on the following API plans:**
      - ~~Starter~~
      - Hobbyist
      - Standard
      - Professional
      - Enterprise

    **Cache / Update frequency:** Mapping data is updated only as needed, every 30 seconds.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangemap-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangemap-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Price conversion tool
  x-api-slug: v1toolspriceconversion-get
  description: |-
    Convert an amount of one currency into up to 32 other cryptocurrency or fiat currencies at the same time using latest exchange rates. Optionally pass a historical timestamp to convert values based on historic averages.

    **Note:** Historical fiat conversions aren't yet available and the latest fiat rates will be used as noted by the `last_updated` timestamp included in the market quote. Historical fiat rates will be coming soon.

    **This endpoint is available on the following API plans:**
    - ~~Starter~~
    - Hobbyist
    - Standard
    - Professional
    - Enterprise

    **Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1toolspriceconversion-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1toolspriceconversion-get-openapi.md
- name: CoinMarketCap Professional API Documentation - List all cryptocurrencies (historical)
  x-api-slug: v1cryptocurrencylistingshistorical-get
  description: |-
    **This endpoint is not yet available. It is slated for release in Q3 2018.**


    Get a paginated list of all cryptocurrencies with market data for a given historical time. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencylistingshistorical-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencylistingshistorical-get-openapi.md
- name: CoinMarketCap Professional API Documentation - List all cryptocurrencies (latest)
  x-api-slug: v1cryptocurrencylistingslatest-get
  description: "Get a paginated list of all cryptocurrencies with latest market data.
    You can configure this call to sort by market cap or another market ranking field.
    Use the \"convert\" option to return market values in multiple fiat and cryptocurrency
    conversions in the same call.   \n\n\nCryptocurrencies are listed by CoinMarketCap
    Rank by default. You may optionally sort against any of the following:\n**name**:
    The cryptocurrency name.\n**symbol**: The cryptocurrency symbol.\n**date_added**:
    Date cryptocurrency was added to the system.\n**market_cap**: market cap (latest
    trade price x circulating supply).\n**price**: latest average trade price across
    markets.\n**circulating_supply**: approximate number of coins currently in circulation.\n**total_supply**:
    approximate total amount of coins in existence right now (minus any coins that
    have been verifiably burned).\n**max_supply**: our best approximation of the maximum
    amount of coins that will ever exist in the lifetime of the currency.\n**num_market_pairs**:
    number of market pairs across all exchanges trading each currency.\n**volume_24h**:
    24 hour trading volume for each currency.\n**percent_change_1h**: 1 hour trading
    price percentage change for each currency.\n**percent_change_24h**: 24 hour trading
    price percentage change for each currency.\n**percent_change_7d**: 7 day trading
    price percentage change for each currency.\n\n  **This endpoint is available on
    the following API plans:**\n  - Starter\n  - Hobbyist\n  - Standard\n  - Professional\n
    \ - Enterprise\n\n**Cache / Update frequency:** Every ~1 minute. \n  \n*NOTE:
    Use this endpoint if you need a sorted and paginated list of cryptocurrencies.
    If you want to query for market data on a few specific cryptocurrencies use /v1/cryptocurrency/quotes/latest
    which is optimized for that purpose. The response data between these endpoints
    is otherwise the same.*"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencylistingslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencylistingslatest-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get market pairs (latest)
  x-api-slug: v1cryptocurrencymarketpairslatest-get
  description: |-
    Lists all market pairs for the specified cryptocurrency with associated stats. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.


      **This endpoint is available on the following API plans:**
      - ~~Starter~~
      - ~~Hobbyist~~
      - Standard
      - Professional
      - Enterprise

    **Cache / Update frequency:** Every ~1 minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencymarketpairslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencymarketpairslatest-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get OHLCV values (historical)
  x-api-slug: v1cryptocurrencyohlcvhistorical-get
  description: |-
    Return an interval of historic OHLCV (Open, High, Low, Close, Volume) market quotes for a cryptocurrency.

    **Technical Details**
    One OHLCV quote will be returned for every "time_period" between your "time_start" and "time_end".
    If a "time_start" is not supplied, the "time_period" will be applied in reverse from "time_end".
    If "time_end" is not supplied, it defaults to the current time.
    If you don't need every "time_period" between your dates you may adjust the frequency that "time_period" is sampled using the "interval" parameter. For example with "time_period" set to "daily" you may set "interval" to "2d" to get the daily OHLCV for every other day. You could set "interval" to "monthly" to get the first daily OHLCV for each month, or set it to "yearly" to get the daily OHLCV value against the same date every year.

    **Interval Options**
    There are 2 types of time interval formats that may be used for "time_period" and "interval" parameters. For "time_period" these return aggregate OHLCV data from the beginning to end of each interval period. Apply these time intervals to "interval" to adjust how frequently "time_period" is sampled.

    The first are calendar year and time constants in UTC time:
    **"daily"** - Calendar day intervals for each UTC day.
    **"weekly"** - Calendar week intervals for each calendar week.
    **"monthly"** - Calendar month intervals for each calendar month.
    **"yearly"** - Calendar year intervals for each calendar year.

    The second format is relative time:
    **"d"**: Time periods that repeat every "d" days (86400 second intervals). Supported day intervals are: "1d", "2d", "3d", "7d", "14d", "15d", "30d", "60d", "90d", "365d".

    **Note:** "time_period" currently only supports the "daily" option. "interval" supports all interval options.

    **This endpoint is available on the following API plans:**
    - ~~Starter~~
    - ~~Hobbyist~~
    - Standard (1 month)
    - Professional (12 months)
    - Enterprise (Up to 5 years)

    **Cache / Update frequency:** Every 24 hours for 1 day OHLCV ranges. Additional OHLCV ranges will be available in the near-term.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencyohlcvhistorical-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencyohlcvhistorical-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get market quotes (historical)
  x-api-slug: v1cryptocurrencyquoteshistorical-get
  description: |-
    Returns an interval of historic market quotes for any cryptocurrency based on time and interval parameters.

    **Technical Details**
    A historic quote for every "interval" period between your "time_start" and "time_end" will be returned.
    If a "time_start" is not supplied, the "interval" will be applied in reverse from "time_end".
    If "time_end" is not supplied, it defaults to the current time.
    At each "interval" period, the historic quote that is closest in time to the requested time will be returned.
    If no historic quotes are available in a given "interval" period up until the next interval period, it will be skipped.

    **Interval Options**
    There are 2 types of time interval formats that may be used for "interval".

    The first are calendar year and time constants in UTC time:
    **"hourly"** - Get the first quote available at the beginning of each calendar hour.
    **"daily"** - Get the first quote available at the beginning of each calendar day.
    **"weekly"** - Get the first quote available at the beginning of each calendar week.
    **"monthly"** - Get the first quote available at the beginning of each calendar month.
    **"yearly"** - Get the first quote available at the beginning of each calendar year.

    The second are relative time intervals.
    **"m"**: Get the first quote available every "m" minutes (60 second intervals). Supported minutes are: "5m", "10m", "15m", "30m", "45m".
    **"h"**: Get the first quote available every "h" hours (3600 second intervals). Supported hour intervals are: "1h", "2h", "3h", "6h", "12h".
    **"d"**: Get the first quote available every "d" days (86400 second intervals). Supported day intervals are: "1d", "2d", "3d", "7d", "14d", "15d", "30d", "60d", "90d", "365d".

    **This endpoint is available on the following API plans:**
    - ~~Starter~~
    - ~~Hobbyist~~
    - Standard (1 month)
    - Professional (12 months)
    - Enterprise (Up to 5 years)

    **Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencyquoteshistorical-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencyquoteshistorical-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get market quotes (latest)
  x-api-slug: v1cryptocurrencyquoteslatest-get
  description: |-
    Get the latest market quote for 1 or more cryptocurrencies. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.

    **This endpoint is available on the following API plans:**
    - Starter
    - Hobbyist
    - Standard
    - Professional
    - Enterprise

    **Cache / Update frequency:** Every ~1 minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencyquoteslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1cryptocurrencyquoteslatest-get-openapi.md
- name: CoinMarketCap Professional API Documentation - List all exchanges (historical)
  x-api-slug: v1exchangelistingshistorical-get
  description: |-
    **This endpoint is not yet available. It is slated for release in Q3 2018.**


    Get a paginated list of all cryptocurrency exchanges with historical market data for a given point in time. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangelistingshistorical-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangelistingshistorical-get-openapi.md
- name: CoinMarketCap Professional API Documentation - List all exchanges (latest)
  x-api-slug: v1exchangelistingslatest-get
  description: "Get a paginated list of all cryptocurrency exchanges with 24 hour
    volume. Additional market data fields will be available in the future. You can
    configure this call to sort by 24 hour volume or another field. Use the \"convert\"
    option to return market values in multiple fiat and cryptocurrency conversions
    in the same call.  \n  \n**This endpoint is available on the following API plans:**\n
    \ - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache
    / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute
    updates shortly.  \n  \n  *NOTE: Use this endpoint if you need a sorted and paginated
    list of exchanges. If you want to query for market data on a few specific exchanges
    use /v1/exchange/quotes/latest which is optimized for that purpose. The response
    data between these endpoints is otherwise the same.*"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangelistingslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangelistingslatest-get-openapi.md
- name: CoinMarketCap Professional API Documentation - List all market pairs (latest)
  x-api-slug: v1exchangemarketpairslatest-get
  description: |-
    Get a list of active market pairs for an exchange. Active means the market pair is open for trading. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.'

      **This endpoint is available on the following API plans:**
      - ~~Starter~~
      - ~~Hobbyist~~
      - Standard
      - Professional
      - Enterprise

    **Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangemarketpairslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangemarketpairslatest-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get market quotes (historical)
  x-api-slug: v1exchangequoteshistorical-get
  description: |-
    Returns an interval of historic quotes for any exchange based on time and interval parameters.

    Historical exchange quotes currently include:
    volume_24: Combined 24 hour volume for all market pairs at each historical interval.
    num_market_pairs: Number of market pairs available at each historical interval.
    Quotes are returned in USD. Additional currency conversion options and additional fields will be available in the future.

    **Technical Details**
    A historic quote for every "interval" period between your "time_start" and "time_end" will be returned.
    If a "time_start" is not supplied, the "interval" will be applied in reverse from "time_end".
    If "time_end" is not supplied, it defaults to the current time.
    At each "interval" period, the historic quote that is closest in time to the requested time will be returned.
    If no historic quotes are available in a given "interval" period up until the next interval period, it will be skipped.

    **Interval Options**
    There are 2 types of time interval formats that may be used for "interval".

    The first are calendar year and time constants in UTC time:
    **"hourly"** - Get the first quote available at the beginning of each calendar hour.
    **"daily"** - Get the first quote available at the beginning of each calendar day.
    **"weekly"** - Get the first quote available at the beginning of each calendar week.
    **"monthly"** - Get the first quote available at the beginning of each calendar month.
    **"yearly"** - Get the first quote available at the beginning of each calendar year.

    The second are relative time intervals.
    **"m"**: Get the first quote available every "m" minutes (60 second intervals). Supported minutes are: "5m", "10m", "15m", "30m", "45m".
    **"h"**: Get the first quote available every "h" hours (3600 second intervals). Supported hour intervals are: "1h", "2h", "3h", "6h", "12h".
    **"d"**: Get the first quote available every "d" days (86400 second intervals). Supported day intervals are: "1d", "2d", "3d", "7d", "14d", "15d", "30d", "60d", "90d", "365d".

    **This endpoint is available on the following API plans:**
      - ~~Starter~~
      - ~~Hobbyist~~
      - Standard (1 month)
      - Professional (12 months)
      - Enterprise (Up to 5 years)

    **Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangequoteshistorical-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangequoteshistorical-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get market quotes (latest)
  x-api-slug: v1exchangequoteslatest-get
  description: |-
    Get the latest 24 hour volume quote for 1 or more exchanges. Additional market data fields will be available in the future. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.

    **This endpoint is available on the following API plans:**
    - ~~Starter~~
    - ~~Hobbyist~~
    - Standard
    - Professional
    - Enterprise

    **Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangequoteslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1exchangequoteslatest-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get aggregate market metrics
    (historical)
  x-api-slug: v1globalmetricsquoteshistorical-get
  description: |-
    Get an interval of aggregate 24 hour volume and market cap data globally based on time and interval parameters.

    **Technical Details**
    A historic quote for every "interval" period between your "time_start" and "time_end" will be returned.
    If a "time_start" is not supplied, the "interval" will be applied in reverse from "time_end".
    If "time_end" is not supplied, it defaults to the current time.
    At each "interval" period, the historic quote that is closest in time to the requested time will be returned.
    If no historic quotes are available in a given "interval" period up until the next interval period, it will be skipped.

    **Interval Options**
    There are 2 types of time interval formats that may be used for "interval".

    The first are calendar year and time constants in UTC time:
    **"hourly"** - Get the first quote available at the beginning of each calendar hour.
    **"daily"** - Get the first quote available at the beginning of each calendar day.
    **"weekly"** - Get the first quote available at the beginning of each calendar week.
    **"monthly"** - Get the first quote available at the beginning of each calendar month.
    **"yearly"** - Get the first quote available at the beginning of each calendar year.

    The second are relative time intervals.
    **"m"**: Get the first quote available every "m" minutes (60 second intervals). Supported minutes are: "5m", "10m", "15m", "30m", "45m".
    **"h"**: Get the first quote available every "h" hours (3600 second intervals). Supported hour intervals are: "1h", "2h", "3h", "6h", "12h".
    **"d"**: Get the first quote available every "d" days (86400 second intervals). Supported day intervals are: "1d", "2d", "3d", "7d", "14d", "15d", "30d", "60d", "90d", "365d".

    **This endpoint is available on the following API plans:**
    - ~~Starter~~
    - ~~Hobbyist~~
    - Standard (1 month)
    - Professional (12 months)
    - Enterprise (Up to 5 years)

    **Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1globalmetricsquoteshistorical-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1globalmetricsquoteshistorical-get-openapi.md
- name: CoinMarketCap Professional API Documentation - Get aggregate market metrics
    (latest)
  x-api-slug: v1globalmetricsquoteslatest-get
  description: |-
    Get the latest quote of aggregate market metrics. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.

    **This endpoint is available on the following API plans:**
    - Starter
    - Hobbyist
    - Standard
    - Professional
    - Enterprise

    **Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28891-pro-coinmarketcap-com.jpg
  humanURL: https://pro.coinmarketcap.com
  baseURL: https://pro-api.coinmarketcap.com//
  tags: Blockchain
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1globalmetricsquoteslatest-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/coinmarketcap/master/_listings/coinmarketcap/v1globalmetricsquoteslatest-get-openapi.md
x-common:
- type: x-github
  url: https://github.com/coinmarketcap
- type: x-openapi
  url: https://pro-api.coinmarketcap.com/swagger.json
- type: x-api-gallery
  url: http://coinfabrik.api.gallery.streamdata.io
- type: x-email
  url: legal@coinmarketcap.com
- type: x-twitter
  url: https://twitter.com/CoinMarketCap
- type: x-website
  url: https://pro.coinmarketcap.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---