---
swagger: "2.0"
x-collection-name: CoinMarketCap
x-complete: 0
info:
  title: CoinMarketCap Price conversion tool
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