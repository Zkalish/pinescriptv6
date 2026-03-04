# Functions - General (math, str, time, type conversion)

---

## math.abs()

Returns the absolute value of a number.

### Returns
Absolute value.

### Syntax
```pine
math.abs(number)
```

### Code Example
```pine
//@version=6
indicator("math.abs")
plot(math.abs(-10))  // Returns 10
```

---

## math.avg()

Returns the average of all arguments.

### Returns
Average value.

### Syntax
```pine
math.avg(number1, number2, ...)
```

### Code Example
```pine
//@version=6
indicator("math.avg")
plot(math.avg(close, open, high))  // Returns average of 3 values
```

---

## math.ceil()

Returns the smallest integer greater than or equal to x.

### Returns
Ceiling value.

### Syntax
```pine
math.ceil(number)
```

### Code Example
```pine
//@version=6
indicator("math.ceil")
plot(math.ceil(10.3))  // Returns 11
```

---

## math.cos()

Returns the cosine of a number (in radians).

### Returns
Cosine value (-1 to 1).

### Syntax
```pine
math.cos(number)
```

---

## math.exp()

Returns the exponential value of x (e^x).

### Returns
Exponential value.

### Syntax
```pine
math.exp(number)
```

---

## math.floor()

Returns the largest integer less than or equal to x.

### Returns
Floor value.

### Syntax
```pine
math.floor(number)
```

### Code Example
```pine
//@version=6
indicator("math.floor")
plot(math.floor(10.7))  // Returns 10
```

---

## math.log()

Returns the natural logarithm of a number.

### Returns
Natural logarithm.

### Syntax
```pine
math.log(number)
```

---

## math.log10()

Returns the base-10 logarithm of a number.

### Returns
Logarithm base 10.

### Syntax
```pine
math.log10(number)
```

---

## math.max()

Returns the maximum value among arguments.

### Returns
Maximum value.

### Syntax
```pine
math.max(number1, number2, ...)
```

### Code Example
```pine
//@version=6
indicator("math.max")
plot(math.max(high, close))  // Returns highest of the two
```

---

## math.min()

Returns the minimum value among arguments.

### Returns
Minimum value.

### Syntax
```pine
math.min(number1, number2, ...)
```

### Code Example
```pine
//@version=6
indicator("math.min")
plot(math.min(low, close))  // Returns lowest of the two
```

---

## math.mod()

Returns the remainder of dividing x by y.

### Returns
Remainder.

### Syntax
```pine
math.mod(x, y)
```

---

## math.nan()

Checks if value is NaN.

### Returns
True if NaN.

### Syntax
```pine
math.nan(value)
```

---

## math.pow()

Returns x raised to the power of y.

### Returns
Power value.

### Syntax
```pine
math.pow(base, exponent)
```

### Code Example
```pine
//@version=6
indicator("math.pow")
plot(math.pow(2, 8))  // Returns 256
```

---

## math.random()

Returns a random number between min and max.

### Returns
Random number.

### Syntax
```pine
math.random(min, max)
```

---

## math.round()

Returns the rounded value of x.

### Returns
Rounded value.

### Syntax
```pine
math.round(number)
```

### Code Example
```pine
//@version=6
indicator("math.round")
plot(math.round(10.5))  // Returns 11
plot(math.round(10.4))  // Returns 10
```

---

## math.sign()

Returns the sign of a number (-1, 0, or 1).

### Returns
Sign value.

### Syntax
```pine
math.sign(number)
```

---

## math.sin()

Returns the sine of a number (in radians).

### Returns
Sine value (-1 to 1).

### Syntax
```pine
math.sin(number)
```

---

## math.sqrt()

Returns the square root of a number.

### Returns
Square root.

### Syntax
```pine
math.sqrt(number)
```

### Code Example
```pine
//@version=6
indicator("math.sqrt")
plot(math.sqrt(16))  // Returns 4
```

---

## math.sum()

Returns the sum of all arguments.

### Returns
Sum value.

### Syntax
```pine
math.sum(number1, number2, ...)
```

---

## math.tan()

Returns the tangent of a number (in radians).

### Returns
Tangent value.

### Syntax
```pine
math.tan(number)
```

---

## math.atan()

Returns the arc tangent of a number (in radians).

### Returns
Arc tangent value.

### Syntax
```pine
math.atan(number)
```

---

## math.atan2()

Returns the arc tangent of y/x (in radians).

### Returns
Arc tangent value.

### Syntax
```pine
math.atan2(y, x)
```

---

## math.pi

Constant for π (3.141592653589793).

### Type
const float

---

## math.phi

Constant for golden ratio (1.6180339887498948).

### Type
const float

---

## math.e

Constant for Euler's number (2.718281828459045).

### Type
const float

---

## math.rphi

Constant for golden ratio conjugate (0.6180339887498948).

### Type
const float

---

## str.format_time()

Formats a timestamp to string.

### Returns
Formatted time string.

### Syntax
```pine
str.format_time(timestamp, format, timezone)
```

### Code Example
```pine
//@version=6
indicator("str.format_time")
plot(str.format_time(timenow, "dd.MM.yyyy HH:mm", "UTC+3"))
```

---

## str.length()

Returns the length of a string.

### Returns
Length as integer.

### Syntax
```pine
str.length(string)
```

---

## str.lower()

Converts string to lowercase.

### Returns
Lowercase string.

### Syntax
```pine
str.lower(string)
```

---

## str.upper()

Converts string to uppercase.

### Returns
Uppercase string.

### Syntax
```pine
str.upper(string)
```

---

## str.replace()

Replaces substring in string.

### Returns
New string.

### Syntax
```pine
str.replace(source, target, replacement)
```

---

## str.substring()

Returns substring.

### Returns
Substring.

### Syntax
```pine
str.substring(source, begin, end)
```

### Code Example
```pine
//@version=6
indicator("str.substring")
plotstring(str.substring("Hello", 0, 3), "test", 0, location.top)
```

---

## str.contains()

Checks if string contains substring.

### Returns
True if contains.

### Syntax
```pine
str.contains(source, target)
```

---

## str.startswith()

Checks if string starts with substring.

### Returns
True if starts with.

### Syntax
```pine
str.startswith(source, target)
```

---

## str.endswith()

Checks if string ends with substring.

### Returns
True if ends with.

### Syntax
```pine
str.endswith(source, target)
```

---

## str.tostring()

Converts value to string.

### Returns
String representation.

### Syntax
```pine
str.tostring(value, format)
```

### Code Example
```pine
//@version=6
indicator("str.tostring")
plotstring(str.tostring(close, "#.00"), "price", 0, location.top)
```

---

## str.format()

Formats values into string.

### Returns
Formatted string.

### Syntax
```pine
str.format("format", value1, value2, ...)
```

---

## timestamp()

Creates timestamp from date/time components.

### Returns
Timestamp in milliseconds.

### Syntax
```pine
timestamp(year, month, day, hour, minute, second)
```

### Code Example
```pine
//@version=6
indicator("timestamp")
start = timestamp(2023, 1, 1)
plot(time >= start ? 1 : 0)
```

---

## year

Returns current year.

### Returns
Year (int).

### Syntax
```pine
year
```

---

## month

Returns current month (1-12).

### Returns
Month (int).

### Syntax
```pine
month
```

---

## dayofmonth

Returns current day of month (1-31).

### Returns
Day of month (int).

### Syntax
```pine
dayofmonth
```

---

## dayofweek

Returns current day of week (1-7, Sunday=1).

### Returns
Day of week (int).

### Syntax
```pine
dayofweek
```

---

## hour

Returns current hour (0-23).

### Returns
Hour (int).

### Syntax
```pine
hour
```

---

## minute

Returns current minute (0-59).

### Returns
Minute (int).

### Syntax
```pine
minute
```

---

## second

Returns current second (0-59).

### Returns
Second (int).

### Syntax
```pine
second
```

---

## weekofyear

Returns week number of year (1-53).

### Returns
Week of year (int).

### Syntax
```pine
weekofyear
```

---

## timeframe.change()

Detects changes in timeframe.

### Returns
True if timeframe changed.

### Syntax
```pine
timeframe.change(timeframe)
```

### Code Example
```pine
//@version=6
indicator("New Week")
plot(timeframe.change("1W") ? 1 : 0)
```

---

## timeframe.isdaily

True if current timeframe is daily.

### Type
const bool

---

## timeframe.isweekly

True if current timeframe is weekly.

### Type
const bool

---

## timeframe.ismonthly

True if current timeframe is monthly.

### Type
const bool

---

## timeframe.isintraday

True if current timeframe is intraday.

### Type
const bool

---

## timeframe.period

Current timeframe as string.

### Type
const string

---

## timeframe.multiplier

Current timeframe multiplier.

### Type
const int

---

## nz()

Returns value or replacement if na.

### Returns
Value or replacement.

### Syntax
```pine
nz(value, replacement)
```

### Code Example
```pine
//@version=6
indicator("nz")
plot(nz(close[1], close))  // If close[1] is na, use close
```

---

## na()

Checks if value is na.

### Returns
True if na.

### Syntax
```pine
na(value)
```

---

## float()

Converts to float.

### Returns
Float value.

### Syntax
```pine
float(value)
```

---

## int()

Converts to integer.

### Returns
Integer value.

### Syntax
```pine
int(value)
```

---

## bool()

Converts to boolean.

### Returns
Boolean value.

### Syntax
```pine
bool(value)
```

---

## color()

Creates color from RGB/RGBA.

### Returns
Color.

### Syntax
```pine
color(r, g, b, transp)
color.new(color, transp)
```

### Code Example
```pine
//@version=6
indicator("color")
c = color.new(color.red, 50)  // 50% transparent red
plot(close, color=c)
```

---

## input.float()

User input for float value.

### Returns
Float value.

### Syntax
```pine
input.float(defval, title, minval, maxval, step, options)
```

---

## input.int()

User input for integer value.

### Returns
Integer value.

### Syntax
```pine
input.int(defval, title, minval, maxval, step, options)
```

---

## input.string()

User input for string value.

### Returns
String value.

### Syntax
```pine
input.string(defval, title, options)
```

---

## input.bool()

User input for boolean value.

### Returns
Boolean value.

### Syntax
```pine
input.bool(defval, title)
```

---

## input.time()

User input for time value.

### Returns
Time value.

### Syntax
```pine
input.time(defval, title)
```

---

## input.timeframe()

User input for timeframe.

### Returns
Timeframe string.

### Syntax
```pine
input.timeframe(defval, title, options)
```

---

## alert()

Creates an alert.

### Syntax
```pine
alert(message, freq)
```

### Code Example
```pine
//@version=6
strategy("Alert Example")
if ta.crossover(ta.sma(close, 14), ta.sma(close, 28))
    alert("SMA crossover!", alert.freq_once_per_bar)
```

---

## label.new()

Creates a new label.

### Returns
Label ID.

### Syntax
```pine
label.new(x, y, text, xloc, yloc, color, style, textcolor, size, textalign)
```

---

## line.new()

Creates a new line.

### Returns
Line ID.

### Syntax
```pine
line.new(x1, y1, x2, y2, xloc, extend, color, style, width)
```

---

## box.new()

Creates a new box.

### Returns
Box ID.

### Syntax
```pine
box.new(left, top, right, bottom, border_color, border_width, border_style, fill_color, text, text_size, text_color, text_halign, text_valign)
```

---
