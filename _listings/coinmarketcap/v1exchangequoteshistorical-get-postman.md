{
  "info": {
    "name": "CoinMarketCap Get market quotes (historical)",
    "_postman_id": "73623d7a-4950-462b-9c8b-92d84b51750a",
    "description": "Returns an interval of historic quotes for any exchange based on time and interval parameters.\n\nHistorical exchange quotes currently include:\nvolume_24: Combined 24 hour volume for all market pairs at each historical interval.\nnum_market_pairs: Number of market pairs available at each historical interval.\nQuotes are returned in USD. Additional currency conversion options and additional fields will be available in the future.\n\n**Technical Details**\nA historic quote for every \"interval\" period between your \"time_start\" and \"time_end\" will be returned.\nIf a \"time_start\" is not supplied, the \"interval\" will be applied in reverse from \"time_end\".\nIf \"time_end\" is not supplied, it defaults to the current time.\nAt each \"interval\" period, the historic quote that is closest in time to the requested time will be returned.\nIf no historic quotes are available in a given \"interval\" period up until the next interval period, it will be skipped.\n\n**Interval Options**\nThere are 2 types of time interval formats that may be used for \"interval\".\n\nThe first are calendar year and time constants in UTC time:\n**\"hourly\"** - Get the first quote available at the beginning of each calendar hour.\n**\"daily\"** - Get the first quote available at the beginning of each calendar day.\n**\"weekly\"** - Get the first quote available at the beginning of each calendar week.\n**\"monthly\"** - Get the first quote available at the beginning of each calendar month.\n**\"yearly\"** - Get the first quote available at the beginning of each calendar year.\n\nThe second are relative time intervals.\n**\"m\"**: Get the first quote available every \"m\" minutes (60 second intervals). Supported minutes are: \"5m\", \"10m\", \"15m\", \"30m\", \"45m\".\n**\"h\"**: Get the first quote available every \"h\" hours (3600 second intervals). Supported hour intervals are: \"1h\", \"2h\", \"3h\", \"6h\", \"12h\".\n**\"d\"**: Get the first quote available every \"d\" days (86400 second intervals). Supported day intervals are: \"1d\", \"2d\", \"3d\", \"7d\", \"14d\", \"15d\", \"30d\", \"60d\", \"90d\", \"365d\".\n\n**This endpoint is available on the following API plans:**\n  - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard (1 month)\n  - Professional (12 months)\n  - Enterprise (Up to 5 years)\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Blockchain",
      "item": [
        {
          "id": "23ba16e9-2b5e-4c2e-88df-1518cbe00a20",
          "name": "getV1CryptocurrencyInfo",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/cryptocurrency/info?id=%7B%7D&symbol=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns all static metadata for one or more cryptocurrencies including name, symbol, logo, and its various registered URLs.\n\n**This endpoint is available on the following API plans:**\n- Starter\n- Hobbyist\n- Standard\n- Professional\n- Enterprise\n\n**Cache / Update frequency:** Static data is updated only as needed, every 30 seconds."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0fa41f07-98fd-4f1b-8cc1-ff2d813af980"
            }
          ]
        },
        {
          "id": "de9757a5-4898-4cee-9db4-16df85f85ce4",
          "name": "getV1CryptocurrencyMap",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/cryptocurrency/map?limit=%7B%7D&listing_status=%7B%7D&start=%7B%7D&symbol=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a paginated list of all cryptocurrencies by CoinMarketCap ID. We recommend using this convenience endpoint to lookup and utilize our unique cryptocurrency `id` across all endpoints as typical identifiers like ticker symbols can match multiple cryptocurrencies and change over time. As a convenience you may pass a comma-separated list of cryptocurrency symbols as `symbol` to filter this list to only those you require.\n\n\n  **This endpoint is available on the following API plans:**\n  - Starter\n  - Hobbyist\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:** Mapping data is updated only as needed, every 30 seconds."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dae13e33-a70c-4998-8b17-1b1d0cb05f07"
            }
          ]
        },
        {
          "id": "9b44e22f-b234-4f80-9ce7-88eb1c141941",
          "name": "getV1ExchangeInfo",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/exchange/info?id=%7B%7D&slug=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns all static metadata for one or more exchanges including logo and homepage URL.\n\n  **This endpoint is available on the following API plans:**\n  - ~~Starter~~\n  - Hobbyist\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:** Static data is updated only as needed, every 30 seconds."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cdfc4a24-0d76-4f03-9d64-8dc3da17df50"
            }
          ]
        },
        {
          "id": "d30d4707-bfd2-4c84-9292-09016ef6c7c5",
          "name": "getV1ExchangeMap",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/exchange/map?limit=%7B%7D&listing_status=%7B%7D&slug=%7B%7D&start=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a paginated list of all cryptocurrency exchanges by CoinMarketCap ID. We recommend using this convenience endpoint to lookup and utilize our unique exchange `id` across all endpoints as typical exchange identifiers may change over time. As a convenience you may pass a comma-separated list of exchanges by `slug` to filter this list to only those you require.\n\n**This endpoint is available on the following API plans:**\n  - ~~Starter~~\n  - Hobbyist\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:** Mapping data is updated only as needed, every 30 seconds."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5b354faa-cc8a-4758-b099-aba0ab1a7ac3"
            }
          ]
        },
        {
          "id": "4317f6cd-c5b9-4b0c-982e-7b2fc6ad40c0",
          "name": "getV1ToolsPriceconversion",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/tools/price-conversion?amount=%7B%7D&convert=%7B%7D&id=%7B%7D&symbol=%7B%7D&time=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Convert an amount of one currency into up to 32 other cryptocurrency or fiat currencies at the same time using latest exchange rates. Optionally pass a historical timestamp to convert values based on historic averages.\n\n**Note:** Historical fiat conversions aren't yet available and the latest fiat rates will be used as noted by the `last_updated` timestamp included in the market quote. Historical fiat rates will be coming soon.\n\n**This endpoint is available on the following API plans:**\n- ~~Starter~~\n- Hobbyist\n- Standard\n- Professional\n- Enterprise\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5275cec0-7893-4898-9b9a-3a889198aebd"
            }
          ]
        },
        {
          "id": "28ee39f1-3c47-46b4-bf96-600ff7a8ac29",
          "name": "getV1CryptocurrencyListingsHistorical",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/cryptocurrency/listings/historical?convert=%7B%7D&cryptocurrency_type=%7B%7D&limit=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&start=%7B%7D&timestamp=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "**This endpoint is not yet available. It is slated for release in Q3 2018.**\n\n\nGet a paginated list of all cryptocurrencies with market data for a given historical time. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "38b192d7-57e2-4861-948f-80a7675dfcc9"
            }
          ]
        },
        {
          "id": "9fcfe3c2-9fb8-4d74-9d99-3776792c5f3f",
          "name": "getV1CryptocurrencyListingsLatest",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/cryptocurrency/listings/latest?convert=%7B%7D&cryptocurrency_type=%7B%7D&limit=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&start=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a paginated list of all cryptocurrencies with latest market data. You can configure this call to sort by market cap or another market ranking field. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call.   \n\n\nCryptocurrencies are listed by CoinMarketCap Rank by default. You may optionally sort against any of the following:\n**name**: The cryptocurrency name.\n**symbol**: The cryptocurrency symbol.\n**date_added**: Date cryptocurrency was added to the system.\n**market_cap**: market cap (latest trade price x circulating supply).\n**price**: latest average trade price across markets.\n**circulating_supply**: approximate number of coins currently in circulation.\n**total_supply**: approximate total amount of coins in existence right now (minus any coins that have been verifiably burned).\n**max_supply**: our best approximation of the maximum amount of coins that will ever exist in the lifetime of the currency.\n**num_market_pairs**: number of market pairs across all exchanges trading each currency.\n**volume_24h**: 24 hour trading volume for each currency.\n**percent_change_1h**: 1 hour trading price percentage change for each currency.\n**percent_change_24h**: 24 hour trading price percentage change for each currency.\n**percent_change_7d**: 7 day trading price percentage change for each currency.\n\n  **This endpoint is available on the following API plans:**\n  - Starter\n  - Hobbyist\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:** Every ~1 minute. \n  \n*NOTE: Use this endpoint if you need a sorted and paginated list of cryptocurrencies. If you want to query for market data on a few specific cryptocurrencies use /v1/cryptocurrency/quotes/latest which is optimized for that purpose. The response data between these endpoints is otherwise the same.*"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ae14d96-4ebf-47ad-a839-4dfb9b757cad"
            }
          ]
        },
        {
          "id": "775ed54a-b848-49f2-82b4-526df93bf4d7",
          "name": "getV1CryptocurrencyMarketpairsLatest",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/cryptocurrency/market-pairs/latest?convert=%7B%7D&id=%7B%7D&limit=%7B%7D&start=%7B%7D&symbol=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Lists all market pairs for the specified cryptocurrency with associated stats. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call.\n\n\n  **This endpoint is available on the following API plans:**\n  - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:** Every ~1 minute."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de745f63-f50f-4067-b7f0-b93a90eca10f"
            }
          ]
        },
        {
          "id": "fa55b715-2c6a-49b8-a2c5-8efd21a38ca8",
          "name": "getV1CryptocurrencyOhlcvHistorical",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/cryptocurrency/ohlcv/historical?convert=%7B%7D&count=%7B%7D&id=%7B%7D&interval=%7B%7D&symbol=%7B%7D&time_end=%7B%7D&time_period=%7B%7D&time_start=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Return an interval of historic OHLCV (Open, High, Low, Close, Volume) market quotes for a cryptocurrency.\n\n**Technical Details**\nOne OHLCV quote will be returned for every \"time_period\" between your \"time_start\" and \"time_end\".\nIf a \"time_start\" is not supplied, the \"time_period\" will be applied in reverse from \"time_end\".\nIf \"time_end\" is not supplied, it defaults to the current time.\nIf you don't need every \"time_period\" between your dates you may adjust the frequency that \"time_period\" is sampled using the \"interval\" parameter. For example with \"time_period\" set to \"daily\" you may set \"interval\" to \"2d\" to get the daily OHLCV for every other day. You could set \"interval\" to \"monthly\" to get the first daily OHLCV for each month, or set it to \"yearly\" to get the daily OHLCV value against the same date every year.\n\n**Interval Options**\nThere are 2 types of time interval formats that may be used for \"time_period\" and \"interval\" parameters. For \"time_period\" these return aggregate OHLCV data from the beginning to end of each interval period. Apply these time intervals to \"interval\" to adjust how frequently \"time_period\" is sampled.\n\nThe first are calendar year and time constants in UTC time:\n**\"daily\"** - Calendar day intervals for each UTC day.\n**\"weekly\"** - Calendar week intervals for each calendar week.\n**\"monthly\"** - Calendar month intervals for each calendar month.\n**\"yearly\"** - Calendar year intervals for each calendar year.\n\nThe second format is relative time:\n**\"d\"**: Time periods that repeat every \"d\" days (86400 second intervals). Supported day intervals are: \"1d\", \"2d\", \"3d\", \"7d\", \"14d\", \"15d\", \"30d\", \"60d\", \"90d\", \"365d\".\n\n**Note:** \"time_period\" currently only supports the \"daily\" option. \"interval\" supports all interval options.\n\n**This endpoint is available on the following API plans:**\n- ~~Starter~~\n- ~~Hobbyist~~\n- Standard (1 month)\n- Professional (12 months)\n- Enterprise (Up to 5 years)\n\n**Cache / Update frequency:** Every 24 hours for 1 day OHLCV ranges. Additional OHLCV ranges will be available in the near-term."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "74d05237-245a-4986-8655-59407ef2e198"
            }
          ]
        },
        {
          "id": "ee9f1569-7a0c-4245-9726-d451b44ebbcf",
          "name": "getV1CryptocurrencyQuotesHistorical",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/cryptocurrency/quotes/historical?convert=%7B%7D&count=%7B%7D&id=%7B%7D&interval=%7B%7D&symbol=%7B%7D&time_end=%7B%7D&time_start=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns an interval of historic market quotes for any cryptocurrency based on time and interval parameters.\n\n**Technical Details**\nA historic quote for every \"interval\" period between your \"time_start\" and \"time_end\" will be returned.\nIf a \"time_start\" is not supplied, the \"interval\" will be applied in reverse from \"time_end\".\nIf \"time_end\" is not supplied, it defaults to the current time.\nAt each \"interval\" period, the historic quote that is closest in time to the requested time will be returned.\nIf no historic quotes are available in a given \"interval\" period up until the next interval period, it will be skipped.\n\n**Interval Options**\nThere are 2 types of time interval formats that may be used for \"interval\".\n\nThe first are calendar year and time constants in UTC time:\n**\"hourly\"** - Get the first quote available at the beginning of each calendar hour.\n**\"daily\"** - Get the first quote available at the beginning of each calendar day.\n**\"weekly\"** - Get the first quote available at the beginning of each calendar week.\n**\"monthly\"** - Get the first quote available at the beginning of each calendar month.\n**\"yearly\"** - Get the first quote available at the beginning of each calendar year.\n\nThe second are relative time intervals.\n**\"m\"**: Get the first quote available every \"m\" minutes (60 second intervals). Supported minutes are: \"5m\", \"10m\", \"15m\", \"30m\", \"45m\".\n**\"h\"**: Get the first quote available every \"h\" hours (3600 second intervals). Supported hour intervals are: \"1h\", \"2h\", \"3h\", \"6h\", \"12h\".\n**\"d\"**: Get the first quote available every \"d\" days (86400 second intervals). Supported day intervals are: \"1d\", \"2d\", \"3d\", \"7d\", \"14d\", \"15d\", \"30d\", \"60d\", \"90d\", \"365d\".\n\n**This endpoint is available on the following API plans:**\n- ~~Starter~~\n- ~~Hobbyist~~\n- Standard (1 month)\n- Professional (12 months)\n- Enterprise (Up to 5 years)\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "75529317-8db0-4e6c-9b82-4d72f8f06ce0"
            }
          ]
        },
        {
          "id": "a5cb2cc5-e189-4805-8e15-951db45f9471",
          "name": "getV1CryptocurrencyQuotesLatest",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/cryptocurrency/quotes/latest?convert=%7B%7D&id=%7B%7D&symbol=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get the latest market quote for 1 or more cryptocurrencies. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call.\n\n**This endpoint is available on the following API plans:**\n- Starter\n- Hobbyist\n- Standard\n- Professional\n- Enterprise\n\n**Cache / Update frequency:** Every ~1 minute."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "317b77be-8b2e-4dcb-b47f-202f00adf0b3"
            }
          ]
        },
        {
          "id": "a4b731cf-ad9e-4d1a-9a7c-0949a132b964",
          "name": "getV1ExchangeListingsHistorical",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/exchange/listings/historical?convert=%7B%7D&limit=%7B%7D&market_type=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&start=%7B%7D&timestamp=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "**This endpoint is not yet available. It is slated for release in Q3 2018.**\n\n\nGet a paginated list of all cryptocurrency exchanges with historical market data for a given point in time. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "19dacbf3-b79f-42a2-a66e-7f89dfa531cb"
            }
          ]
        },
        {
          "id": "d83f95e2-8591-4c4e-a822-b5b84db42e70",
          "name": "getV1ExchangeListingsLatest",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/exchange/listings/latest?convert=%7B%7D&limit=%7B%7D&market_type=%7B%7D&sort=%7B%7D&sort_dir=%7B%7D&start=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a paginated list of all cryptocurrency exchanges with 24 hour volume. Additional market data fields will be available in the future. You can configure this call to sort by 24 hour volume or another field. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call.  \n  \n**This endpoint is available on the following API plans:**\n  - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.  \n  \n  *NOTE: Use this endpoint if you need a sorted and paginated list of exchanges. If you want to query for market data on a few specific exchanges use /v1/exchange/quotes/latest which is optimized for that purpose. The response data between these endpoints is otherwise the same.*"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "41f59d5d-a73f-405f-8c32-b94c05e59d89"
            }
          ]
        },
        {
          "id": "6a8ab0af-5d0f-44b0-a313-440d4bcaf8c0",
          "name": "getV1ExchangeMarketpairsLatest",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/exchange/market-pairs/latest?convert=%7B%7D&id=%7B%7D&limit=%7B%7D&slug=%7B%7D&start=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of active market pairs for an exchange. Active means the market pair is open for trading. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call.'\n\n  **This endpoint is available on the following API plans:**\n  - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d0ab0111-3a5e-4f79-a82b-b436a1c2a054"
            }
          ]
        },
        {
          "id": "6d613b1d-d668-46cc-a740-4c78cafc4fd9",
          "name": "getV1ExchangeQuotesHistorical",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/exchange/quotes/historical?convert=%7B%7D&count=%7B%7D&id=%7B%7D&interval=%7B%7D&slug=%7B%7D&time_end=%7B%7D&time_start=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns an interval of historic quotes for any exchange based on time and interval parameters.\n\nHistorical exchange quotes currently include:\nvolume_24: Combined 24 hour volume for all market pairs at each historical interval.\nnum_market_pairs: Number of market pairs available at each historical interval.\nQuotes are returned in USD. Additional currency conversion options and additional fields will be available in the future.\n\n**Technical Details**\nA historic quote for every \"interval\" period between your \"time_start\" and \"time_end\" will be returned.\nIf a \"time_start\" is not supplied, the \"interval\" will be applied in reverse from \"time_end\".\nIf \"time_end\" is not supplied, it defaults to the current time.\nAt each \"interval\" period, the historic quote that is closest in time to the requested time will be returned.\nIf no historic quotes are available in a given \"interval\" period up until the next interval period, it will be skipped.\n\n**Interval Options**\nThere are 2 types of time interval formats that may be used for \"interval\".\n\nThe first are calendar year and time constants in UTC time:\n**\"hourly\"** - Get the first quote available at the beginning of each calendar hour.\n**\"daily\"** - Get the first quote available at the beginning of each calendar day.\n**\"weekly\"** - Get the first quote available at the beginning of each calendar week.\n**\"monthly\"** - Get the first quote available at the beginning of each calendar month.\n**\"yearly\"** - Get the first quote available at the beginning of each calendar year.\n\nThe second are relative time intervals.\n**\"m\"**: Get the first quote available every \"m\" minutes (60 second intervals). Supported minutes are: \"5m\", \"10m\", \"15m\", \"30m\", \"45m\".\n**\"h\"**: Get the first quote available every \"h\" hours (3600 second intervals). Supported hour intervals are: \"1h\", \"2h\", \"3h\", \"6h\", \"12h\".\n**\"d\"**: Get the first quote available every \"d\" days (86400 second intervals). Supported day intervals are: \"1d\", \"2d\", \"3d\", \"7d\", \"14d\", \"15d\", \"30d\", \"60d\", \"90d\", \"365d\".\n\n**This endpoint is available on the following API plans:**\n  - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard (1 month)\n  - Professional (12 months)\n  - Enterprise (Up to 5 years)\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1921f1f3-5cec-4ed9-baa6-d97ee5675fe7"
            }
          ]
        }
      ]
    }
  ]
}