# Functions - Request (request.*)

---

## request.security()

Requests data from another symbol or timeframe.

### Returns
Requested value (or tuple).

### Syntax
```pine
request.security(symbol, timeframe, expression, lookahead, gaps)
```

### Parameters
- **symbol**: Symbol ID (e.g., "BTCUSD")
- **expression**: Value to request
- **timeframe**: Timeframe (e.g., "1H", "D", "W")
- **lookahead**: barmerge.lookahead_off or barmerge.lookahead_on
- **gaps**: barmerge.gaps_on or barmerge.gaps_off

### Code Example
```pine
//@version=6
indicator("Security Example")
// Request daily close
dClose = request.security(syminfo.tickerid, "D", close)
plot(dClose)

// Request with lookahead off (recommended for strategies)
dCloseSafe = request.security(syminfo.tickerid, "D", close[1], lookahead=barmerge.lookahead_off)
plot(dCloseSafe)
```

### Important Notes
- Use `lookahead=barmerge.lookahead_off` for strategies to avoid repainting
- `request.security` creates a new context - variables are not shared
- Maximum 40 unique securities allowed

---

## request.security_lower_tf()

Requests lower timeframe data.

### Returns
Array of values.

### Syntax
```pine
request.security_lower_tf(symbol, timeframe, expression)
```

### Code Example
```pine
//@version=6
indicator("Lower TF")
// Get 1-minute data on 5-minute chart
lowTFClose = request.security_lower_tf(syminfo.tickerid, "1", close)
plot(lowTFClose.last())
```

### Important Notes
- Returns arrays of data
- Can be memory-intensive for long histories
- Use only when necessary

---

## request.dividends()

Requests dividend data.

### Returns
Dividend value.

### Syntax
```pine
request.dividends(symbol, dividends_type)
```

### Parameters
- **symbol**: Symbol ID
- **dividends_type**: dividends.gross or dividends.net

### Code Example
```pine
//@version=6
indicator("Dividends")
div = request.dividends(syminfo.tickerid, dividends.net)
plot(div)
```

---

## request.earnings()

Requests earnings data.

### Returns
Earnings value.

### Syntax
```pine
request.earnings(symbol, earnings_type)
```

### Parameters
- **symbol**: Symbol ID
- **earnings_type**: earnings.actual, earnings.estimate, or earnings.standardized

### Code Example
```pine
//@version=6
indicator("Earnings")
eps = request.earnings(syminfo.tickerid, earnings.actual)
plot(eps)
```

---

## request.quarterly()

Requests quarterly financial data.

### Returns
Quarterly value.

### Syntax
```pine
request.quarterly(symbol, expression)
```

### Code Example
```pine
//@version=6
indicator("Quarterly Revenue")
rev = request.quarterly(syminfo.tickerid, financial.financial_revenue)
plot(rev)
```

---

## request.financial()

Requests financial statement data.

### Returns
Financial value.

### Syntax
```pine
request.financial(symbol, financial_item, period, inventory)
```

### Parameters
- **symbol**: Symbol ID
- **financial_item**: e.g., "FINANCIAL_REVENUE"
- **period**: "TTM", "FY", "FQ", "1Y", "2Y", etc.
- **inventory**: "FIFO", "LIFO", etc.

### Code Example
```pine
//@version=6
indicator("Financial")
rev = request.financial(syminfo.tickerid, "FINANCIAL_REVENUE", "TTM")
plot(rev)
```

---

## request.splits()

Requests stock split data.

### Returns
Split ratio.

### Syntax
```pine
request.splits(symbol, splits_type)
```

### Parameters
- **symbol**: Symbol ID
- **splits_type**: splits.numerator or splits.denominator

### Code Example
```pine
//@version=6
indicator("Splits")
ratio = request.splits(syminfo.tickerid, splits.denominator)
plot(ratio)
```

---

## request.currency()

Requests currency conversion rate.

### Returns
Conversion rate.

### Syntax
```pine
request.currency(symbol, expression)
```

### Code Example
```pine
//@version=6
indicator("USD Conversion")
// Convert to USD if not USD
rate = request.currency("USD", 1)
plot(rate)
```

---

## request.seed()

Requests seed data for reproducibility.

### Returns
Seed value.

### Syntax
```pine
request.seed(symbol, expression)
```

### Important Notes
- Used for reproducible random values
- Helps with debugging

---

## ticker.new()

Creates custom ticker ID.

### Returns
Ticker ID.

### Syntax
```pine
ticker.new(prefix, ticker, adjustment)
```

### Parameters
- **prefix**: Exchange prefix (e.g., "BATS")
- **ticker**: Symbol ticker
- **adjustment**: adjustment.none, adjustment.splits, adjustment.dividends

### Code Example
```pine
//@version=6
indicator("Custom Ticker")
t = ticker.new("BATS", "AAPL", adjustment.dividends)
plot(request.security(t, "D", close))
```

---

## ticker.modify()

Modifies existing ticker ID.

### Returns
Modified ticker ID.

### Syntax
```pine
ticker.modify(ticker, prefix, ticker, adjustment)
```

---

## ticker.heikinashi()

Creates Heikin-Ashi ticker.

### Returns
Heikin-Ashi ticker ID.

### Syntax
```pine
ticker.heikinashi(symbol)
```

### Code Example
```pine
//@version=6
indicator("Heikin-Ashi")
t = ticker.heikinashi(syminfo.tickerid)
haClose = request.security(t, "D", close)
plot(haClose)
```

---

## ticker.renko()

Creates Renko ticker.

### Returns
Renko ticker ID.

### Syntax
```pine
ticker.renko(symbol, brick_size)
```

---

## ticker.kagi()

Creates Kagi ticker.

### Returns
Kagi ticker ID.

### Syntax
```pine
ticker.kagi(symbol, reversal_amount)
```

---

## ticker.linebreak()

Creates Line Break ticker.

### Returns
Line Break ticker ID.

### Syntax
```pine
ticker.linebreak(symbol, line_count)
```

---

## ticker.pnf()

Creates Point & Figure ticker.

### Returns
P&F ticker ID.

### Syntax
```pine
ticker.pnf(symbol, box_size, reversal)
```

---

## syminfo.tickerid

Current symbol ticker ID.

### Type
const string

### Code Example
```pine
//@version=6
indicator("Current Ticker")
plot(0, title=syminfo.tickerid)
```

---

## syminfo.prefix

Exchange prefix.

### Type
const string

---

## syminfo.root

Root symbol name.

### Type
const string

---

## syminfo.currency

Symbol currency.

### Type
const string

---

## syminfo.basecurrency

Base currency.

### Type
const string

---

## syminfo.type

Symbol type (stock, futures, forex, crypto, etc.).

### Type
const string

---

## syminfo.pointvalue

Point value.

### Type
const float

---

## syminfo.mintick

Minimum tick size.

### Type
const float

---

## syminfo.pricescale

Price scale factor.

### Type
const int

---

## syminfo.session

Trading session type.

### Type
const string

---

## syminfo.timezone

Symbol timezone.

### Type
const string

---

## barmerge.gaps_off

Merge data without gaps (fill with previous).

### Type
const barmerge_gaps

---

## barmerge.gaps_on

Allow gaps in merged data.

### Type
const barmerge_gaps

---

## barmerge.lookahead_off

Disable lookahead (recommended for strategies).

### Type
const barmerge_lookahead

---

## barmerge.lookahead_on

Enable lookahead (can cause repainting).

### Type
const barmerge_lookahead

---
