{
  "info": {
    "name": "CoinMarketCap List all exchanges (latest)",
    "_postman_id": "8a0b16d2-8e3a-4a43-9a15-680f6b149d97",
    "description": "Get a paginated list of all cryptocurrency exchanges with 24 hour volume. Additional market data fields will be available in the future. You can configure this call to sort by 24 hour volume or another field. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call.  \n  \n**This endpoint is available on the following API plans:**\n  - ~~Starter~~\n  - ~~Hobbyist~~\n  - Standard\n  - Professional\n  - Enterprise\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.  \n  \n  *NOTE: Use this endpoint if you need a sorted and paginated list of exchanges. If you want to query for market data on a few specific exchanges use /v1/exchange/quotes/latest which is optimized for that purpose. The response data between these endpoints is otherwise the same.*",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Blockchain",
      "item": [
        {
          "id": "c40876e4-e055-458d-81f2-e7d2144fa021",
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
              "id": "26288c22-3ef5-4fb9-bb6b-4aba6c6883c7"
            }
          ]
        },
        {
          "id": "0c34e4ab-0d56-4706-8f14-d8a677ad860e",
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
              "id": "6401f22f-4145-412d-a888-54c96df05030"
            }
          ]
        },
        {
          "id": "2a308ac9-0f51-490f-ad7a-99cd38050443",
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
              "id": "08fdecd9-bbe8-4ac4-8b15-9db7d97d8775"
            }
          ]
        },
        {
          "id": "c55f038d-c2f5-479a-b953-d5d594f56e16",
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
              "id": "71cd1165-6c33-46ee-b9d2-c62db9375c62"
            }
          ]
        },
        {
          "id": "f4202815-9319-4576-8159-4d69562ec4a2",
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
              "id": "d1d882d9-4013-4eb5-9b8c-48293fbf1893"
            }
          ]
        },
        {
          "id": "67db3ea0-5535-4b10-8c35-ade07d483451",
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
              "id": "a46b22ec-bb28-4132-b688-31be5f274e8b"
            }
          ]
        },
        {
          "id": "6e1cae34-7eae-4906-a365-316d81e48fbf",
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
              "id": "6ea41851-ae3c-412e-bd86-698650940b23"
            }
          ]
        },
        {
          "id": "c8fa406f-4e59-42e2-a1ac-0a3e1aa369a9",
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
              "id": "438c5d17-5147-4880-a761-bbdf725dc385"
            }
          ]
        },
        {
          "id": "6b40cbdc-e7a6-434a-88bd-7120cdeeaa0b",
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
              "id": "e8078f01-8b2f-4e13-8fd1-5daffe368fde"
            }
          ]
        },
        {
          "id": "2648e140-1dcb-451d-a427-596cf4bd0077",
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
              "id": "5ae1db0e-d3be-4aae-81cb-76320a1acf6a"
            }
          ]
        },
        {
          "id": "6b307f11-a8e5-43cd-a115-c19ff594f595",
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
              "id": "0091cbda-a63f-473c-8899-036cd36ad7a0"
            }
          ]
        },
        {
          "id": "f6b4cf24-5043-4160-a5be-1ecac2b5bb66",
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
              "id": "bed0fd66-f225-4925-8b91-534f92598a9b"
            }
          ]
        },
        {
          "id": "da797802-0628-4d07-b0e3-b31642cbcc9a",
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
              "id": "a7280f4a-e9eb-434e-8047-0a692396fc40"
            }
          ]
        }
      ]
    }
  ]
}