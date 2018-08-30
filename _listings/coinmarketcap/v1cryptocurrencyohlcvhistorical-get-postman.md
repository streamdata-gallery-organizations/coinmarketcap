{
  "info": {
    "name": "CoinMarketCap Get OHLCV values (historical)",
    "_postman_id": "58d367bf-764e-4dec-bc68-63889b190745",
    "description": "Return an interval of historic OHLCV (Open, High, Low, Close, Volume) market quotes for a cryptocurrency.\n\n**Technical Details**\nOne OHLCV quote will be returned for every \"time_period\" between your \"time_start\" and \"time_end\".\nIf a \"time_start\" is not supplied, the \"time_period\" will be applied in reverse from \"time_end\".\nIf \"time_end\" is not supplied, it defaults to the current time.\nIf you don't need every \"time_period\" between your dates you may adjust the frequency that \"time_period\" is sampled using the \"interval\" parameter. For example with \"time_period\" set to \"daily\" you may set \"interval\" to \"2d\" to get the daily OHLCV for every other day. You could set \"interval\" to \"monthly\" to get the first daily OHLCV for each month, or set it to \"yearly\" to get the daily OHLCV value against the same date every year.\n\n**Interval Options**\nThere are 2 types of time interval formats that may be used for \"time_period\" and \"interval\" parameters. For \"time_period\" these return aggregate OHLCV data from the beginning to end of each interval period. Apply these time intervals to \"interval\" to adjust how frequently \"time_period\" is sampled.\n\nThe first are calendar year and time constants in UTC time:\n**\"daily\"** - Calendar day intervals for each UTC day.\n**\"weekly\"** - Calendar week intervals for each calendar week.\n**\"monthly\"** - Calendar month intervals for each calendar month.\n**\"yearly\"** - Calendar year intervals for each calendar year.\n\nThe second format is relative time:\n**\"d\"**: Time periods that repeat every \"d\" days (86400 second intervals). Supported day intervals are: \"1d\", \"2d\", \"3d\", \"7d\", \"14d\", \"15d\", \"30d\", \"60d\", \"90d\", \"365d\".\n\n**Note:** \"time_period\" currently only supports the \"daily\" option. \"interval\" supports all interval options.\n\n**This endpoint is available on the following API plans:**\n- ~~Starter~~\n- ~~Hobbyist~~\n- Standard (1 month)\n- Professional (12 months)\n- Enterprise (Up to 5 years)\n\n**Cache / Update frequency:** Every 24 hours for 1 day OHLCV ranges. Additional OHLCV ranges will be available in the near-term.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Blockchain",
      "item": [
        {
          "id": "ba1507c7-ef9f-462d-aaaf-80daca6c8720",
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
              "id": "fe71e452-eeea-40b2-a969-b74ffcbd0997"
            }
          ]
        },
        {
          "id": "8be15abc-1356-48e8-9b41-dba37fcbf687",
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
              "id": "9d629d8a-467f-40e8-a8f1-2d87404662aa"
            }
          ]
        },
        {
          "id": "2057d5fc-f32d-4380-b08b-15864b182356",
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
              "id": "4412f9c0-2f3e-432b-91a7-72131e6abe83"
            }
          ]
        },
        {
          "id": "6ae792c6-654d-44fe-95e2-fb2821857866",
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
              "id": "71f25abb-001f-441b-aef2-4be93a8c4156"
            }
          ]
        },
        {
          "id": "1793ecc5-38d3-44c5-a798-08d9963a84c4",
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
              "id": "9fde78d5-84be-47e0-8692-d1bf51cf533f"
            }
          ]
        },
        {
          "id": "ad3e3de1-4354-4e38-84f3-dfd9a3baf25b",
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
              "id": "d92ed299-6b5e-4d77-99bd-5f058293a838"
            }
          ]
        },
        {
          "id": "be793bfe-636c-404b-971c-1e6c970482a2",
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
              "id": "f9ee7722-f92c-4a18-8f29-72057a6cc71e"
            }
          ]
        },
        {
          "id": "0c75b96e-b410-4c9b-9c3e-a9413675f797",
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
              "id": "7c20d79d-3200-4d81-a0d4-5204c980e7b5"
            }
          ]
        },
        {
          "id": "f6179bf8-fb75-4561-98ea-af0b9a16886a",
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
              "id": "1bdbfe6e-3f2d-4bbf-95e1-449d8c0b6ea8"
            }
          ]
        }
      ]
    }
  ]
}