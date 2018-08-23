---
swagger: "2.0"
x-collection-name: CoinMarketCap
x-complete: 0
info:
  title: CoinMarketCap Get metadata
  description: |-
    Returns all static metadata for one or more cryptocurrencies including name, symbol, logo, and its various registered URLs.

    **This endpoint is available on the following API plans:**
    - Starter
    - Hobbyist
    - Standard
    - Professional
    - Enterprise

    **Cache / Update frequency:** Static data is updated only as needed, every 30 seconds.
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