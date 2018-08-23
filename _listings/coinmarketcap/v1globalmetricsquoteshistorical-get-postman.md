{
  "info": {
    "name": "CoinMarketCap Get aggregate market metrics (historical)",
    "_postman_id": "b797f583-bf34-49ba-9adf-3b57c00919ed",
    "description": "Get an interval of aggregate 24 hour volume and market cap data globally based on time and interval parameters.\n\n**Technical Details**\nA historic quote for every \"interval\" period between your \"time_start\" and \"time_end\" will be returned.\nIf a \"time_start\" is not supplied, the \"interval\" will be applied in reverse from \"time_end\".\nIf \"time_end\" is not supplied, it defaults to the current time.\nAt each \"interval\" period, the historic quote that is closest in time to the requested time will be returned.\nIf no historic quotes are available in a given \"interval\" period up until the next interval period, it will be skipped.\n\n**Interval Options**\nThere are 2 types of time interval formats that may be used for \"interval\".\n\nThe first are calendar year and time constants in UTC time:\n**\"hourly\"** - Get the first quote available at the beginning of each calendar hour.\n**\"daily\"** - Get the first quote available at the beginning of each calendar day.\n**\"weekly\"** - Get the first quote available at the beginning of each calendar week.\n**\"monthly\"** - Get the first quote available at the beginning of each calendar month.\n**\"yearly\"** - Get the first quote available at the beginning of each calendar year.\n\nThe second are relative time intervals.\n**\"m\"**: Get the first quote available every \"m\" minutes (60 second intervals). Supported minutes are: \"5m\", \"10m\", \"15m\", \"30m\", \"45m\".\n**\"h\"**: Get the first quote available every \"h\" hours (3600 second intervals). Supported hour intervals are: \"1h\", \"2h\", \"3h\", \"6h\", \"12h\".\n**\"d\"**: Get the first quote available every \"d\" days (86400 second intervals). Supported day intervals are: \"1d\", \"2d\", \"3d\", \"7d\", \"14d\", \"15d\", \"30d\", \"60d\", \"90d\", \"365d\".\n\n**This endpoint is available on the following API plans:**\n- ~~Starter~~\n- ~~Hobbyist~~\n- Standard (1 month)\n- Professional (12 months)\n- Enterprise (Up to 5 years)\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Blockchain",
      "item": [
        {
          "id": "1e401950-dfb7-4e2d-89ad-b0760bd860da",
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
              "id": "95332f16-9ab8-4d09-9d19-b9ed3a4a042c"
            }
          ]
        },
        {
          "id": "8694b7a4-3d34-4ae1-a932-cd0fb53a1c56",
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
              "id": "574ad7fe-1444-4f6f-9700-947dc5e5dfe7"
            }
          ]
        },
        {
          "id": "f92ebd67-4cd3-41ae-b9a9-e62f293acc19",
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
              "id": "3749bec8-6d67-4e9a-b64c-4c2f93126d71"
            }
          ]
        },
        {
          "id": "deee378f-1642-48c6-b118-3c18eb0604ee",
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
              "id": "9fcc3587-bc90-46fb-b014-ab12ac22226b"
            }
          ]
        },
        {
          "id": "627fc57e-c0ed-46ca-ab4c-5796169f1613",
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
              "id": "cdb6ab3c-6fbd-4430-8f60-02b50f2a0850"
            }
          ]
        },
        {
          "id": "81e70bb6-6e06-4b03-a88f-7ebac9ecad8f",
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
              "id": "f2657a52-fa29-44a9-9104-198fdf896073"
            }
          ]
        },
        {
          "id": "a22eb1c0-ee81-4e35-9dcc-2cc86f33156b",
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
              "id": "8783ed1e-4bf0-46ce-9427-a3ee5b5e8ab2"
            }
          ]
        },
        {
          "id": "d8940334-e7b5-4a60-a890-04343b8c64fd",
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
              "id": "034300bc-2fde-4711-972b-37a0bf28254e"
            }
          ]
        },
        {
          "id": "9bbd5547-6b8d-483b-9e18-2395658930e2",
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
              "id": "ec07e02e-b004-4948-9fc9-c75184ebdfd7"
            }
          ]
        },
        {
          "id": "ca81d512-f6dc-480f-9c09-6fd96cac377a",
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
              "id": "502a46cf-1fbd-4650-a927-05f3051d29d8"
            }
          ]
        },
        {
          "id": "c31c7dc0-285c-4596-833b-0a39d0e30f61",
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
              "id": "c39916fa-87b0-4946-85f8-871a4bf00bf7"
            }
          ]
        },
        {
          "id": "202a5e00-7b0f-4947-ad91-233efb1836d1",
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
              "id": "1ae5da1d-1ef7-41da-b4ed-e4362bd1e925"
            }
          ]
        },
        {
          "id": "87becb32-490d-432a-a0bf-ba3e7e8bcfb8",
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
              "id": "82b03aaf-991c-4d86-b404-1851897fcc21"
            }
          ]
        },
        {
          "id": "22374c96-59f1-466c-b536-8a32b3bc0385",
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
              "id": "f164ef20-6d10-42cc-a395-3d1a2ea7cb3c"
            }
          ]
        },
        {
          "id": "e6b8ea1e-a9e8-4438-95f5-faaf43b42d0e",
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
              "id": "51167824-405b-4516-a95a-38013041cbb1"
            }
          ]
        },
        {
          "id": "0ba0a87a-b706-42f1-a8a8-cefd35e511fa",
          "name": "getV1ExchangeQuotesLatest",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/exchange/quotes/latest?convert=%7B%7D&id=%7B%7D&slug=%7B%7D",
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
            "description": "Get the latest 24 hour volume quote for 1 or more exchanges. Additional market data fields will be available in the future. Use the \"convert\" option to return market values in multiple fiat and cryptocurrency conversions in the same call.\n\n**This endpoint is available on the following API plans:**\n- ~~Starter~~\n- ~~Hobbyist~~\n- Standard\n- Professional\n- Enterprise\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "92364bdc-0a67-4cfd-b6b1-8538d58e285d"
            }
          ]
        },
        {
          "id": "f39dfe71-c9ea-48b3-b668-560c1d294ba0",
          "name": "getV1GlobalmetricsQuotesHistorical",
          "request": {
            "url": "http://pro-api.coinmarketcap.com/v1/global-metrics/quotes/historical?convert=%7B%7D&count=%7B%7D&interval=%7B%7D&time_end=%7B%7D&time_start=%7B%7D",
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
            "description": "Get an interval of aggregate 24 hour volume and market cap data globally based on time and interval parameters.\n\n**Technical Details**\nA historic quote for every \"interval\" period between your \"time_start\" and \"time_end\" will be returned.\nIf a \"time_start\" is not supplied, the \"interval\" will be applied in reverse from \"time_end\".\nIf \"time_end\" is not supplied, it defaults to the current time.\nAt each \"interval\" period, the historic quote that is closest in time to the requested time will be returned.\nIf no historic quotes are available in a given \"interval\" period up until the next interval period, it will be skipped.\n\n**Interval Options**\nThere are 2 types of time interval formats that may be used for \"interval\".\n\nThe first are calendar year and time constants in UTC time:\n**\"hourly\"** - Get the first quote available at the beginning of each calendar hour.\n**\"daily\"** - Get the first quote available at the beginning of each calendar day.\n**\"weekly\"** - Get the first quote available at the beginning of each calendar week.\n**\"monthly\"** - Get the first quote available at the beginning of each calendar month.\n**\"yearly\"** - Get the first quote available at the beginning of each calendar year.\n\nThe second are relative time intervals.\n**\"m\"**: Get the first quote available every \"m\" minutes (60 second intervals). Supported minutes are: \"5m\", \"10m\", \"15m\", \"30m\", \"45m\".\n**\"h\"**: Get the first quote available every \"h\" hours (3600 second intervals). Supported hour intervals are: \"1h\", \"2h\", \"3h\", \"6h\", \"12h\".\n**\"d\"**: Get the first quote available every \"d\" days (86400 second intervals). Supported day intervals are: \"1d\", \"2d\", \"3d\", \"7d\", \"14d\", \"15d\", \"30d\", \"60d\", \"90d\", \"365d\".\n\n**This endpoint is available on the following API plans:**\n- ~~Starter~~\n- ~~Hobbyist~~\n- Standard (1 month)\n- Professional (12 months)\n- Enterprise (Up to 5 years)\n\n**Cache / Update frequency:** Every ~5 minutes. This endpoint will be migrated to ~1 minute updates shortly."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8c37fefa-001c-48d1-a004-85edded613e3"
            }
          ]
        }
      ]
    }
  ]
}