# Functions - Strategy (strategy.*)

---

## strategy()

Declares a strategy.

### Syntax
```pine
strategy(title, overlay, default_qty_type, default_qty_value, initial_capital, currency, commission_type, commission_value, slippage, calc_on_every_tick, ...)
```

### Parameters
- **title**: Strategy name
- **overlay**: Display on chart
- **default_qty_type**: Quantity type (strategy.fixed, strategy.cash, strategy.percent_of_equity)
- **default_qty_value**: Default quantity
- **initial_capital**: Starting capital
- **commission_value**: Commission percent

### Code Example
```pine
//@version=6
strategy("My Strategy", overlay=true, default_qty_type=strategy.fixed, default_qty_value=1)
```

---

## strategy.entry()

Places an entry order.

### Syntax
```pine
strategy.entry(id, direction, qty, limit, stop, when)
```

### Parameters
- **id**: Order ID
- **direction**: strategy.long or strategy.short
- **qty**: Quantity
- **limit**: Limit price (optional)
- **stop**: Stop price (optional)
- **when**: Condition

### Code Example
```pine
//@version=6
strategy("Entry Example")
if ta.crossover(ta.sma(close, 14), ta.sma(close, 28))
    strategy.entry("Long", strategy.long)
```

---

## strategy.order()

Places a pending order.

### Syntax
```pine
strategy.order(id, direction, qty, limit, stop, oca_type, oca_name, when)
```

---

## strategy.exit()

Places an exit order.

### Syntax
```pine
strategy.exit(id, from_entry, qty, limit, stop, profit, loss, when)
```

### Parameters
- **from_entry**: Entry order ID to exit
- **profit**: Profit target (in points)
- **loss**: Stop loss (in points)

### Code Example
```pine
//@version=6
strategy("Exit Example")
if ta.crossover(ta.sma(close, 14), ta.sma(close, 28))
    strategy.entry("Long", strategy.long)

strategy.exit("Exit", from_entry="Long", profit=100, loss=50)
```

---

## strategy.close()

Closes a position.

### Syntax
```pine
strategy.close(id, when)
```

### Code Example
```pine
//@version=6
strategy("Close Example")
if ta.crossover(ta.sma(close, 14), ta.sma(close, 28))
    strategy.entry("Long", strategy.long)

if ta.crossunder(ta.sma(close, 14), ta.sma(close, 28))
    strategy.close("Long")
```

---

## strategy.cancel()

Cancels an order.

### Syntax
```pine
strategy.cancel(id)
```

---

## strategy.cancel_all()

Cancels all orders.

### Syntax
```pine
strategy.cancel_all()
```

---

## strategy.position_size()

Current position size.

### Returns
Position size.

### Type
series int

---

## strategy.position_avg_price()

Average entry price.

### Returns
Average price.

### Type
series float

---

## strategy.openprofit

Current open profit.

### Type
series float

---

## strategy.closedtrades

Number of closed trades.

### Type
series int

---

## strategy.opentrades

Number of open trades.

### Type
series int

---

## strategy.wintrades

Number of winning trades.

### Type
series int

---

## strategy.losstrades

Number of losing trades.

### Type
series int

---

## strategy.grossprofit

Total gross profit.

### Type
series float

---

## strategy.grossloss

Total gross loss.

### Type
series float

---

## strategy.netprofit

Total net profit.

### Type
series float

---

## strategy.max_drawdown

Maximum drawdown.

### Type
series float

---

## strategy.max_runup

Maximum run-up.

### Type
series float

---

## strategy.initial_capital

Initial capital setting.

### Type
const float

---

## strategy.equity

Current equity.

### Type
series float

---

## strategy.account_currency

Account currency.

### Type
const string

---

## strategy.risk.allow_entry_in()

Controls direction.

### Syntax
```pine
strategy.risk.allow_entry_in(direction)
```

### Code Example
```pine
// Only allow long entries
strategy.risk.allow_entry_in(strategy.direction.long)
```

---

## strategy.risk.max_intraday_filled_loss()

Max intraday loss.

### Syntax
```pine
strategy.risk.max_intraday_filled_loss(value)
```

---

## strategy.risk.max_position_size()

Max position size.

### Syntax
```pine
strategy.risk.max_position_size(value)
```

---

## strategy.close_all()

Closes all positions.

### Syntax
```pine
strategy.close_all(when)
```

---

## alert()

Creates alert.

### Syntax
```pine
alert(message, freq)
```

---

## alert.freq_all

Alert on every condition.

---

## alert.freq_once_per_bar

Alert once per bar.

---

## alert.freq_once_per_bar_close

Alert once per bar close.

---

## strategy.long

Long direction constant.

---

## strategy.short

Short direction constant.

---

## strategy.fixed

Fixed quantity type.

---

## strategy.cash

Cash quantity type.

---

## strategy.percent_of_equity

Percent of equity type.

---

## strategy.direction.all

Allow both directions.

---

## strategy.direction.long

Allow long only.

---

## strategy.direction.short

Allow short only.

---

## strategy.oca.cancel

OCA cancel type.

---

## strategy.oca.none

OCA none type.

---

## strategy.oca.reduce

OCA reduce type.

---

## strategy.commission.percent

Commission percent type.

---

## strategy.commission.cash_per_contract

Commission per contract.

---

## strategy.commission.cash_per_order

Commission per order.
