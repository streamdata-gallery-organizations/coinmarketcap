---
swagger: "2.0"
x-collection-name: CoinMarketCap
x-complete: 0
info:
  title: CoinMarketCap List all market pairs (latest)
  description: |-
    Get a list of active market pairs for an exchange. Active means the market pair is open for trading. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.'

      **This endpoint is available on the following API plans:**
      - ~~Starter~~
      - ~~Hobbyist~~
      - Standard
      - Professional
      - Enterprise

    **Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.
  termsOfService: https://coinmarketcap.com/terms/
  version: 1.0.0
host: pro-api.coinmarketcap.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/cryptocurrency/info:
    get:
      summary: Get metadata
      description: |-
        Returns all static metadata for one or more cryptocurrencies including name, symbol, logo, and its various registered URLs.

        **This endpoint is available on the following API plans:**
        - Starter
        - Hobbyist
        - Standard
        - Professional
        - Enterprise

        **Cache / Update frequency:** Static data is updated only as needed, every 30 seconds.
      operationId: getV1CryptocurrencyInfo
      x-api-path-slug: v1cryptocurrencyinfo-get
      parameters:
      - in: query
        name: id
        description: One or more comma-separated CoinMarketCap cryptocurrency IDs
      - in: query
        name: symbol
        description: Alternatively pass one or more comma-separated cryptocurrency
          symbols
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Metadata
  /v1/cryptocurrency/map:
    get:
      summary: Get CoinMarketCap ID map
      description: |-
        Returns a paginated list of all cryptocurrencies by CoinMarketCap ID. We recommend using this convenience endpoint to lookup and utilize our unique cryptocurrency `id` across all endpoints as typical identifiers like ticker symbols can match multiple cryptocurrencies and change over time. As a convenience you may pass a comma-separated list of cryptocurrency symbols as `symbol` to filter this list to only those you require.


          **This endpoint is available on the following API plans:**
          - Starter
          - Hobbyist
          - Standard
          - Professional
          - Enterprise

        **Cache / Update frequency:** Mapping data is updated only as needed, every 30 seconds.
      operationId: getV1CryptocurrencyMap
      x-api-path-slug: v1cryptocurrencymap-get
      parameters:
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: listing_status
        description: Only active coins are returned by default
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      - in: query
        name: symbol
        description: Optionally pass a comma-separated list of cryptocurrency symbols
          to return CoinMarketCap IDs for
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - CoinMarketCap
      - ID
      - Map
  /v1/exchange/info:
    get:
      summary: Get metadata
      description: |-
        Returns all static metadata for one or more exchanges including logo and homepage URL.

          **This endpoint is available on the following API plans:**
          - ~~Starter~~
          - Hobbyist
          - Standard
          - Professional
          - Enterprise

        **Cache / Update frequency:** Static data is updated only as needed, every 30 seconds.
      operationId: getV1ExchangeInfo
      x-api-path-slug: v1exchangeinfo-get
      parameters:
      - in: query
        name: id
        description: One or more comma-separated CoinMarketCap cryptocurrency exchange
          ids
      - in: query
        name: slug
        description: Alternatively, one or more comma-separated exchange names in
          URL friendly shorthand slug format (all lowercase, spaces replaced with
          hyphens)
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Metadata
  /v1/exchange/map:
    get:
      summary: Get CoinMarketCap ID map
      description: |-
        Returns a paginated list of all cryptocurrency exchanges by CoinMarketCap ID. We recommend using this convenience endpoint to lookup and utilize our unique exchange `id` across all endpoints as typical exchange identifiers may change over time. As a convenience you may pass a comma-separated list of exchanges by `slug` to filter this list to only those you require.

        **This endpoint is available on the following API plans:**
          - ~~Starter~~
          - Hobbyist
          - Standard
          - Professional
          - Enterprise

        **Cache / Update frequency:** Mapping data is updated only as needed, every 30 seconds.
      operationId: getV1ExchangeMap
      x-api-path-slug: v1exchangemap-get
      parameters:
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: listing_status
        description: Only active cryptocurrency exchanges are returned by default
      - in: query
        name: slug
        description: Optionally pass a comma-separated list of exchange slugs (lowercase
          URL friendly shorthand name with spaces replaced with dashes) to return
          CoinMarketCap IDs for
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - CoinMarketCap
      - ID
      - Map
  /v1/tools/price-conversion:
    get:
      summary: Price conversion tool
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
      operationId: getV1ToolsPriceconversion
      x-api-path-slug: v1toolspriceconversion-get
      parameters:
      - in: query
        name: amount
        description: An amount of currency to convert
      - in: query
        name: convert
        description: Pass up to 32 comma-separated fiat or cryptocurrency symbols
          to convert the source amount to
      - in: query
        name: id
        description: The CoinMarketCap cryptocurrency ID of the base currency to convert
          from
      - in: query
        name: symbol
        description: Alternatively the cryptocurrency symbol of the base currency
          to convert from
      - in: query
        name: time
        description: Optional timestamp (Unix or ISO 8601) to reference historical
          pricing during conversion
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Price
      - Conversion
      - Tool
  /v1/cryptocurrency/listings/historical:
    get:
      summary: List all cryptocurrencies (historical)
      description: |-
        **This endpoint is not yet available. It is slated for release in Q3 2018.**


        Get a paginated list of all cryptocurrencies with market data for a given historical time. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.
      operationId: getV1CryptocurrencyListingsHistorical
      x-api-path-slug: v1cryptocurrencylistingshistorical-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: cryptocurrency_type
        description: The type of cryptocurrency to include
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: sort
        description: What field to sort the list of cryptocurrencies by
      - in: query
        name: sort_dir
        description: The direction in which to order cryptocurrencies against the
          specified sort
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      - in: query
        name: timestamp
        description: Timestamp (Unix or ISO 8601) to return historical cryptocurrency
          listings for
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - List
      - ""
      - Cryptocurrencies
      - (historical)
  /v1/cryptocurrency/listings/latest:
    get:
      summary: List all cryptocurrencies (latest)
      description: "Get a paginated list of all cryptocurrencies with latest market
        data. You can configure this call to sort by market cap or another market
        ranking field. Use the \"convert\" option to return market values in multiple
        fiat and cryptocurrency conversions in the same call.   \n\n\nCryptocurrencies
        are listed by CoinMarketCap Rank by default. You may optionally sort against
        any of the following:\n**name**: The cryptocurrency name.\n**symbol**: The
        cryptocurrency symbol.\n**date_added**: Date cryptocurrency was added to the
        system.\n**market_cap**: market cap (latest trade price x circulating supply).\n**price**:
        latest average trade price across markets.\n**circulating_supply**: approximate
        number of coins currently in circulation.\n**total_supply**: approximate total
        amount of coins in existence right now (minus any coins that have been verifiably
        burned).\n**max_supply**: our best approximation of the maximum amount of
        coins that will ever exist in the lifetime of the currency.\n**num_market_pairs**:
        number of market pairs across all exchanges trading each currency.\n**volume_24h**:
        24 hour trading volume for each currency.\n**percent_change_1h**: 1 hour trading
        price percentage change for each currency.\n**percent_change_24h**: 24 hour
        trading price percentage change for each currency.\n**percent_change_7d**:
        7 day trading price percentage change for each currency.\n\n  **This endpoint
        is available on the following API plans:**\n  - Starter\n  - Hobbyist\n  -
        Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:**
        Every ~1 minute. \n  \n*NOTE: Use this endpoint if you need a sorted and paginated
        list of cryptocurrencies. If you want to query for market data on a few specific
        cryptocurrencies use /v1/cryptocurrency/quotes/latest which is optimized for
        that purpose. The response data between these endpoints is otherwise the same.*"
      operationId: getV1CryptocurrencyListingsLatest
      x-api-path-slug: v1cryptocurrencylistingslatest-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: cryptocurrency_type
        description: The type of cryptocurrency to include
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: sort
        description: What field to sort the list of cryptocurrencies by
      - in: query
        name: sort_dir
        description: The direction in which to order cryptocurrencies against the
          specified sort
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - List
      - ""
      - Cryptocurrencies
      - (latest)
  /v1/cryptocurrency/market-pairs/latest:
    get:
      summary: Get market pairs (latest)
      description: |-
        Lists all market pairs for the specified cryptocurrency with associated stats. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.


          **This endpoint is available on the following API plans:**
          - ~~Starter~~
          - ~~Hobbyist~~
          - Standard
          - Professional
          - Enterprise

        **Cache / Update frequency:** Every ~1 minute.
      operationId: getV1CryptocurrencyMarketpairsLatest
      x-api-path-slug: v1cryptocurrencymarketpairslatest-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: id
        description: A cryptocurrency by CoinMarketCap ID
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      - in: query
        name: symbol
        description: Alternatively pass a cryptocurrency by symbol
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Market
      - Pairs
      - (latest)
  /v1/cryptocurrency/ohlcv/historical:
    get:
      summary: Get OHLCV values (historical)
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
      operationId: getV1CryptocurrencyOhlcvHistorical
      x-api-path-slug: v1cryptocurrencyohlcvhistorical-get
      parameters:
      - in: query
        name: convert
        description: By default market quotes are returned in USD
      - in: query
        name: count
        description: Optionally limit the number of time periods to return results
          for
      - in: query
        name: id
        description: A CoinMarketCap cryptocurrency ID
      - in: query
        name: interval
        description: Optionally adjust the interval that time_period is sampled
      - in: query
        name: symbol
        description: Alternatively a cryptocurrency symbol
      - in: query
        name: time_end
        description: Timestamp (Unix or ISO 8601) to stop returning OHLCV time periods
          for (exclusive)
      - in: query
        name: time_period
        description: Time period to return OHLCV data for
      - in: query
        name: time_start
        description: Timestamp (Unix or ISO 8601) to start returning OHLCV time periods
          for
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - OHLCV
      - Values
      - (historical)
  /v1/cryptocurrency/quotes/historical:
    get:
      summary: Get market quotes (historical)
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
      operationId: getV1CryptocurrencyQuotesHistorical
      x-api-path-slug: v1cryptocurrencyquoteshistorical-get
      parameters:
      - in: query
        name: convert
        description: By default market quotes are returned in USD
      - in: query
        name: count
        description: The number of interval periods to return results for
      - in: query
        name: id
        description: A CoinMarketCap cryptocurrency ID
      - in: query
        name: interval
        description: Interval of time to return data points for
      - in: query
        name: symbol
        description: Alternatively pass a cryptocurrency symbol
      - in: query
        name: time_end
        description: Timestamp (Unix or ISO 8601) to stop returning quotes for (inclusive)
      - in: query
        name: time_start
        description: Timestamp (Unix or ISO 8601) to start returning quotes for
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Market
      - Quotes
      - (historical)
  /v1/cryptocurrency/quotes/latest:
    get:
      summary: Get market quotes (latest)
      description: |-
        Get the latest market quote for 1 or more cryptocurrencies. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.

        **This endpoint is available on the following API plans:**
        - Starter
        - Hobbyist
        - Standard
        - Professional
        - Enterprise

        **Cache / Update frequency:** Every ~1 minute.
      operationId: getV1CryptocurrencyQuotesLatest
      x-api-path-slug: v1cryptocurrencyquoteslatest-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: id
        description: One or more comma-separated cryptocurrency CoinMarketCap IDs
      - in: query
        name: symbol
        description: Alternatively pass one or more comma-separated cryptocurrency
          symbols
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - Market
      - Quotes
      - (latest)
  /v1/exchange/listings/historical:
    get:
      summary: List all exchanges (historical)
      description: |-
        **This endpoint is not yet available. It is slated for release in Q3 2018.**


        Get a paginated list of all cryptocurrency exchanges with historical market data for a given point in time. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.
      operationId: getV1ExchangeListingsHistorical
      x-api-path-slug: v1exchangelistingshistorical-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: market_type
        description: The type of exchange markets to include in rankings
      - in: query
        name: sort
        description: What field to sort the list of exchanges by
      - in: query
        name: sort_dir
        description: The direction in which to order exchanges against the specified
          sort
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      - in: query
        name: timestamp
        description: Timestamp (Unix or ISO 8601) to return historical exchange listings
          for
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - List
      - ""
      - Exchanges
      - (historical)
  /v1/exchange/listings/latest:
    get:
      summary: List all exchanges (latest)
      description: "Get a paginated list of all cryptocurrency exchanges with 24 hour
        volume. Additional market data fields will be available in the future. You
        can configure this call to sort by 24 hour volume or another field. Use the
        \"convert\" option to return market values in multiple fiat and cryptocurrency
        conversions in the same call.  \n  \n**This endpoint is available on the following
        API plans:**\n  - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard\n  - Professional\n
        \ - Enterprise\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint
        will be migrated to ~1 minute updates shortly.  \n  \n  *NOTE: Use this endpoint
        if you need a sorted and paginated list of exchanges. If you want to query
        for market data on a few specific exchanges use /v1/exchange/quotes/latest
        which is optimized for that purpose. The response data between these endpoints
        is otherwise the same.*"
      operationId: getV1ExchangeListingsLatest
      x-api-path-slug: v1exchangelistingslatest-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: market_type
        description: The type of exchange markets to include in rankings
      - in: query
        name: sort
        description: What field to sort the list of exchanges by
      - in: query
        name: sort_dir
        description: The direction in which to order exchanges against the specified
          sort
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - List
      - ""
      - Exchanges
      - (latest)
  /v1/exchange/market-pairs/latest:
    get:
      summary: List all market pairs (latest)
      description: |-
        Get a list of active market pairs for an exchange. Active means the market pair is open for trading. Use the "convert" option to return market values in multiple fiat and cryptocurrency conversions in the same call.'

          **This endpoint is available on the following API plans:**
          - ~~Starter~~
          - ~~Hobbyist~~
          - Standard
          - Professional
          - Enterprise

        **Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.
      operationId: getV1ExchangeMarketpairsLatest
      x-api-path-slug: v1exchangemarketpairslatest-get
      parameters:
      - in: query
        name: convert
        description: Optionally calculate market quotes in up to 32 currencies at
          once by passing a comma-separated list of cryptocurrency or fiat currency
          symbols
      - in: query
        name: id
        description: A CoinMarketCap exchange ID
      - in: query
        name: limit
        description: Optionally specify the number of results to return
      - in: query
        name: slug
        description: Alternatively pass an exchange slug (URL friendly all lowercase
          shorthand version of name with spaces replaced with hyphens)
      - in: query
        name: start
        description: Optionally offset the start (1-based index) of the paginated
          list of items to return
      responses:
        200:
          description: OK
      tags:
      - Blockchain
      - List
      - ""
      - Market
      - Pairs
      - (latest)
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---