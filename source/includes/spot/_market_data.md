# t(:marketdata)
t(:market_para_auth)

### t(:orderbook)
> t(:codequote_curlExample)

```console
```

```python
```

> t(:codequote_responseExample)

```javascript
{
    "ret_code": 0,
    "ret_msg": null,
    "result": {
        "time": 1620886105740,
        "bids": [
            [
                "50005.12",
                "403.0416"
            ]
        ],
        "asks": [
            [
                "50006.34",
                "0.2297"
            ]
        ]
    },
    "ext_code": null,
    "ext_info": null
}
```


<p class="fake_header">t(:httprequest)</p>
GET
<code><span id=vpOrder>/spot/quote/v1/depth</span></code>
<button class="clipboard_button" data-clipboard-action="copy" data-clipboard-target="#vpOrder"><img src="/images/copy_to_clipboard.png" height=15 width=15></img></button>

<p class="fake_header">t(:requestparameters)</p>
|t(:column_parameter)|t(:column_required)|t(:column_type)|t(:column_comments)|
|:----- |:-------|:-----|----- |
|symbol|true|string|t(:spotSymbol)|
|limit| false | integer | t(:spot_depth_limit)


<p class="fake_header">t(:responseparameters)</p>
|t(:column_parameter)|t(:column_type)|t(:column_comments)|
|:----- |:-----|----- |
| time | long | t(:spot_depth_time) |
| bids | string | t(:spot_depth_bids) |
| asks | string | t(:spot_depth_asks) |

### t(:mergedOrderBook)

> t(:codequote_curlExample)

```console
```

```python
```

> t(:codequote_responseExample)

```javascript
{
    "ret_code": 0,
    "ret_msg": null,
    "result": {
        "time": 1620891567679,
        "bids": [
            [
                "50008",
                "1.8501"
            ]
        ],
        "asks": [
            [
                "70000",
                "1"
            ]
        ]
    },
    "ext_code": null,
    "ext_info": null
}
```


<p class="fake_header">t(:httprequest)</p>
GET
<code><span id=vpOrder>/spot/quote/v1/depth/merged</span></code>
<button class="clipboard_button" data-clipboard-action="copy" data-clipboard-target="#vpOrder"><img src="/images/copy_to_clipboard.png" height=15 width=15></img></button>

<p class="fake_header">t(:requestparameters)</p>
|t(:column_parameter)|t(:column_required)|t(:column_type)|t(:column_comments)|
|:----- |:-------|:-----|----- |
|symbol|true|string|t(:spotSymbol)|
|limit| false | integer | t(:spot_depth_limit)


<p class="fake_header">t(:responseparameters)</p>
|t(:column_parameter)|t(:column_type)|t(:column_comments)|
|:----- |:-----|----- |
| time | long | t(:spot_depth_time) |
| bids | string | t(:spot_depth_bids) |
| asks | string | t(:spot_depth_asks) |

### t(:spot_trades)
> t(:codequote_curlExample)

```console
```

```python
```

> t(:codequote_responseExample)

```javascript
{
    "ret_code": 0,
    "ret_msg": null,
    "result": [
        {
            "price": "50005.12",
            "time": 1620822657672,
            "qty": "0.0001",
            "isBuyerMaker": true
        },
        {
            "price": "50008.34",
            "time": 1620891050659,
            "qty": "0.0001",
            "isBuyerMaker": true
        },
        {
            "price": "50008.34",
            "time": 1620891093266,
            "qty": "0.0001",
            "isBuyerMaker": true
        }
    ],
    "ext_code": null,
    "ext_info": null
}
```


<p class="fake_header">t(:httprequest)</p>
GET
<code><span id=vpOrder>/spot/quote/v1/trades</span></code>
<button class="clipboard_button" data-clipboard-action="copy" data-clipboard-target="#vpOrder"><img src="/images/copy_to_clipboard.png" height=15 width=15></img></button>

<p class="fake_header">t(:requestparameters)</p>
|t(:column_parameter)|t(:column_required)|t(:column_type)|t(:column_comments)|
|:----- |:-------|:-----|----- |
|symbol|true|string|t(:spotSymbol)|
|limit| false | integer | t(:spot_trades_limit)


<p class="fake_header">t(:responseparameters)</p>
|t(:column_parameter)|t(:column_type)|t(:column_comments)|
|:----- |:-----|----- |
| price | float | t(:spot_OrderPrice) |
| time | long | t(:spot_trade_time) |
| qty | float | t(:spotQuantity) |
| isBuyerMaker | bool | t(:spot_is_buyer_maker) |


### t(:spot_klines)
> t(:codequote_curlExample)

```console
```

```python
```

> t(:codequote_responseExample)

```javascript
{
    "ret_code": 0,
    "ret_msg": null,
    "result": [
        [
            1620917160000,
            "50008",
            "50008",
            "50008",
            "50008",
            "0",
            0,
            "0",
            0,
            "0",
            "0"
        ]
    ],
    "ext_code": null,
    "ext_info": null
}
```


<p class="fake_header">t(:httprequest)</p>
GET
<code><span id=vpOrder>/spot/quote/v1/kline</span></code>
<button class="clipboard_button" data-clipboard-action="copy" data-clipboard-target="#vpOrder"><img src="/images/copy_to_clipboard.png" height=15 width=15></img></button>

<p class="fake_header">t(:requestparameters)</p>
|t(:column_parameter)|t(:column_required)|t(:column_type)|t(:column_comments)|
|:----- |:-------|:-----|----- |
|symbol|true|string|t(:spotSymbol)|
| interval | true | string | t(:spot_kline_interval)|
| limit | false | integer | t(:spot_trades_limit) |
| startTime | false | number | t(:spot_orders_start_time) |
| endTime | false | number | t(:spot_orders_end_time) |


<p class="fake_header">t(:responseparameters)</p>

|t(:column_parameter)|t(:column_type)|t(:column_comments)|
|:----- |:-----|----- |
|startTime| long | t(:spot_orders_start_time)|
|open| float | t(:spotOpen) |
|high| float | t(:spotHigh) |
|low| float | t(:spotLow) |
|close| float | t(:spotClose) |
|volume| float | t(:spotVolume) |
|endTime| float | t(:spot_orders_end_time) |
|trades| integer | t(:spotTrades) |
|takerBaseVolume| float | t(:spotTakerBaseVolume) | 
|takerQuoteVolume| float | t(:spotTakerQuoteVolume) |

### t(:spotTicker)
> t(:codequote_curlExample)

```console
```

```python
```

> t(:codequote_responseExample)

```javascript
{
    "ret_code": 0,
    "ret_msg": null,
    "result": {
        "time": 1620918180046,
        "symbol": "ETHUSDT",
        "bestBidPrice": "50005.12",
        "bestAskPrice": "50008",
        "volume": "26.7308",
        "quoteVolume": "1337500.362672",
        "lastPrice": "50008",
        "highPrice": "70000",
        "lowPrice": "50005.12",
        "openPrice": "50005.12"
    },
    "ext_code": null,
    "ext_info": null
}
```


<p class="fake_header">t(:httprequest)</p>
GET
<code><span id=vpOrder>/spot/quote/v1/ticker/24hr</span></code>
<button class="clipboard_button" data-clipboard-action="copy" data-clipboard-target="#vpOrder"><img src="/images/copy_to_clipboard.png" height=15 width=15></img></button>

<p class="fake_header">t(:requestparameters)</p>

|t(:column_parameter)|t(:column_required)|t(:column_type)|t(:column_comments)|
|:----- |:-------|:-----|----- |
|symbol|false|string|t(:spotSymbol)|


<p class="fake_header">t(:responseparameters)</p>

|t(:column_parameter)|t(:column_type)|t(:column_comments)|
|:----- |:-----|----- |
|time| long | t(:spot_trade_time)|
|symbol| string | t(:spotSymbol) |
|bestBidPrice|float|t(:spot_best_bid_price)|
|bestAskPrice|float|t(:spot_best_ask_price)
|lastPrice|float|t(:spot_last_price)|
|openPrice|float|t(:spot_open_price)|
|highPrice|float|t(:spot_high_price)|
|lowPrice|float|t(:spot_low_price)|
|volume|float|t(:spot_volume)|

### t(:spotSymbolPrice)
> t(:codequote_curlExample)

```console
```

```python
```

> t(:codequote_responseExample)

```javascript
{
    "ret_code": 0,
    "ret_msg": null,
    "result": {
        "symbol": "ETHUSDT",
        "price": "50008"
    },
    "ext_code": null,
    "ext_info": null
}
```


<p class="fake_header">t(:httprequest)</p>
GET
<code><span id=vpOrder>/spot/quote/v1/ticker/price</span></code>
<button class="clipboard_button" data-clipboard-action="copy" data-clipboard-target="#vpOrder"><img src="/images/copy_to_clipboard.png" height=15 width=15></img></button>

<p class="fake_header">t(:requestparameters)</p>
|t(:column_parameter)|t(:column_required)|t(:column_type)|t(:column_comments)|
|:----- |:-------|:-----|----- |
|symbol|false|string|t(:spotSymbol)|


<p class="fake_header">t(:responseparameters)</p>
|t(:column_parameter)|t(:column_type)|t(:column_comments)|
|:----- |:-----|----- |
| symbol | string | t(:spotSymbol) |
| price | float | t(:spotPrice) |

### t(:spotBestTicker)
> t(:codequote_curlExample)

```console
```

```python
```

> t(:codequote_responseExample)

```javascript
{
    "ret_code": 0,
    "ret_msg": null,
    "result": {
        "symbol": "ETHUSDT",
        "bidPrice": "50005.12",
        "bidQty": "394",
        "askPrice": "50008",
        "askQty": "0.8001",
        "time": 1620919281808
    },
    "ext_code": null,
    "ext_info": null
}
```


<p class="fake_header">t(:httprequest)</p>
GET
<code><span id=vpOrder>/spot/quote/v1/ticker/book-ticker</span></code>
<button class="clipboard_button" data-clipboard-action="copy" data-clipboard-target="#vpOrder"><img src="/images/copy_to_clipboard.png" height=15 width=15></img></button>

<p class="fake_header">t(:requestparameters)</p>
|t(:column_parameter)|t(:column_required)|t(:column_type)|t(:column_comments)|
|:----- |:-------|:-----|----- |
|symbol|false|string|t(:spotSymbol)|


<p class="fake_header">t(:responseparameters)</p>
|t(:column_parameter)|t(:column_type)|t(:column_comments)|
|:----- |:-----|----- |
| symbol | string | t(:spotSymbol) |
| bidPrice| float | t(:spot_best_bid_price)|
| bidQty | float | t(:spotBidQuantity)|
| askPrice| float | t(:spot_best_ask_price)|
| askQty | float |t(:spotAskQuantity)|

