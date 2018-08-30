{
  "info": {
    "name": "CoinMarketCap List all market pairs (latest)",
    "_postman_id": "29fde1c9-4098-425a-8dde-df79a4f102de",
    "description": "Get a list of active market pairs for an exchange. Active means the market pair is open for trading. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call.'\n\n  **This endpoint is available on the following API plans:**\n  - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Blockchain",
      "item": [
        {
          "id": "db83b2c9-becd-44c8-95d1-95af8ed5b3a1",
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
              "id": "7fb5efe2-ed5c-43f2-90b8-76dea0a4c6dc"
            }
          ]
        },
        {
          "id": "3074d82b-25bf-48a2-9f41-dd09915ad12d",
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
              "id": "f1c79c0d-84a7-4cc4-a92e-0d6d3d95cc5f"
            }
          ]
        },
        {
          "id": "51252137-57fb-4b44-b6dc-88fe02a93f8f",
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
              "id": "3da0a5dc-ee5c-4cbf-b22e-f64b608c45af"
            }
          ]
        },
        {
          "id": "edeebfc7-0aba-4297-a273-5bc250a1c2ba",
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
              "id": "5fbc8502-5641-42a4-99f5-a7e438b6254f"
            }
          ]
        },
        {
          "id": "6f2c44d5-49b0-4ea2-90df-afb8c12b4297",
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
              "id": "0d746406-267a-4e0d-a9cf-917fdf073a22"
            }
          ]
        },
        {
          "id": "913eda20-cf4d-4546-8903-9d259cceecc1",
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
              "id": "fb108203-63b0-4da7-a854-2e9ab3836e95"
            }
          ]
        },
        {
          "id": "1e97c42b-05b3-400c-a635-8d838db558a2",
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
              "id": "a4b05b43-c049-446c-acbc-c32874c3956f"
            }
          ]
        },
        {
          "id": "cdfb9fbd-a792-48a7-9b97-7704cc64d5cb",
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
              "id": "63c630ea-2fff-4da7-bc94-f70594a5db14"
            }
          ]
        },
        {
          "id": "f1832295-d902-46da-b150-54d88dc776e9",
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
              "id": "5bd48f95-7471-4081-bcf0-1b3b4ba53ad7"
            }
          ]
        },
        {
          "id": "d9382e94-ed24-4025-8357-c1e0a411efda",
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
              "id": "368dbcf1-c322-490a-ac76-e5024e936317"
            }
          ]
        },
        {
          "id": "9da4643a-0a24-451f-af56-5e4e084e0fe7",
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
              "id": "fda863b1-f125-4e17-a6af-62a066897e7a"
            }
          ]
        },
        {
          "id": "6f92019f-43ee-477f-931b-f5b763c25bc2",
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
              "id": "9420f2f6-1c93-47ef-ac4d-0dbede8eb816"
            }
          ]
        },
        {
          "id": "f38fdbf9-a061-4623-9338-4bf1e2cc9659",
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
              "id": "322accce-66d8-48da-974b-b67102a0ff1b"
            }
          ]
        },
        {
          "id": "109c24e0-2a85-44eb-bba1-eb2aa13281f2",
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
              "id": "13b276cb-e827-43da-87ab-38debc59e04d"
            }
          ]
        }
      ]
    }
  ]
}