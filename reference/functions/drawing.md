# Functions - Drawing (plot, line, box, label, table)

---

## plot()

Plots a series on chart.

### Syntax
```pine
plot(series, title, color, linewidth, style, trackprice, transp, offset, display)
```

### Parameters
- **series**: Value to plot
- **title**: Plot name
- **color**: Plot color
- **linewidth**: Line width
- **style**: Plot style

### Code Example
```pine
//@version=6
indicator("Plot Example")
plot(ta.sma(close, 14), color=color.blue, linewidth=2)
```

---

## plotarrow()

Plots arrows on chart.

### Syntax
```pine
plotarrow(series, title, colorup, colordown, offset, transp, display)
```

---

## plotbar()

Plots bars on chart.

### Syntax
```pine
plotbar(open, high, low, close, title, colorup, colordown, transp, display)
```

---

## plotcandle()

Plots candles on chart.

### Syntax
```pine
plotcandle(open, high, low, close, title, colorup, colordown, wickup, wickdown, transp, display)
```

---

## plotchar()

Plots character on chart.

### Syntax
```pine
plotchar(series, title, text, char, textcolor, color, size, location, offset, transp, display)
```

---

## plotshape()

Plots shape on chart.

### Syntax
```pine
plotshape(series, title, text, style, color, size, location, offset, transp, display)
```

### Code Example
```pine
//@version=6
indicator("Shape Example")
plotshape(ta.crossover(ta.sma(20), ta.sma(50)), "Buy", shape.triangleup, location.belowbar, color.lime)
```

---

## hline()

Plots horizontal line.

### Syntax
```pine
hline(price, title, color, linestyle, linewidth, lineextend)
```

### Code Example
```pine
//@version=6
indicator("HLine Example")
hline(100, "Level", color=color.red, linestyle=hline.style_dashed)
```

---

## fill()

Fills area between lines.

### Syntax
```pine
fill(hline1, hline2, title, color, transp)
fill(plot1, plot2, title, color, transp)
```

---

## line.new()

Creates a new line.

### Syntax
```pine
line.new(x1, y1, x2, y2, xloc, extend, color, style, width)
```

### Parameters
- **x1, y1**: Start point
- **x2, y2**: End point
- **xloc**: xloc.bar_index or xloc.bar_time
- **extend**: extend.none, extend.right, extend.left, extend.both

### Code Example
```pine
//@version=6
indicator("Line Example")
line.new(bar_index[10], close[10], bar_index, close, xloc=bar_index, color=color.blue)
```

---

## line.delete()

Deletes a line.

### Syntax
```pine
line.delete(id)
```

---

## line.set_x1()

Sets start x coordinate.

### Syntax
```pine
line.set_x1(id, x)
```

---

## line.set_y1()

Sets start y coordinate.

### Syntax
```pine
line.set_y1(id, y)
```

---

## line.set_x2()

Sets end x coordinate.

### Syntax
```pine
line.set_x2(id, x)
```

---

## line.set_y2()

Sets end y coordinate.

### Syntax
```pine
line.set_y2(id, y)
```

---

## line.set_color()

Sets line color.

### Syntax
```pine
line.set_color(id, color)
```

---

## line.set_width()

Sets line width.

### Syntax
```pine
line.set_width(id, width)
```

---

## line.set_style()

Sets line style.

### Syntax
```pine
line.set_style(id, style)
```

---

## line.get_x1()

Gets start x coordinate.

### Syntax
```pine
line.get_x1(id)
```

---

## line.get_y1()

Gets start y coordinate.

### Syntax
```pine
line.get_y1(id)
```

---

## line.get_x2()

Gets end x coordinate.

### Syntax
```pine
line.get_x2(id)
```

---

## line.get_y2()

Gets end y coordinate.

### Syntax
```pine
line.get_y2(id)
```

---

## label.new()

Creates a new label.

### Syntax
```pine
label.new(x, y, text, xloc, yloc, color, style, textcolor, size, textalign)
```

### Parameters
- **x**: X coordinate
- **y**: Y coordinate
- **text**: Label text
- **xloc**: xloc.bar_index or xloc.bar_time
- **yloc**: yloc.price, yloc.abovebar, yloc.belowbar

### Code Example
```pine
//@version=6
indicator("Label Example")
label.new(bar_index, high, "High", xloc=bar_index, yloc=price, color=color.red)
```

---

## label.delete()

Deletes a label.

### Syntax
```pine
label.delete(id)
```

---

## label.set_text()

Sets label text.

### Syntax
```pine
label.set_text(id, text)
```

---

## label.set_x()

Sets label x coordinate.

### Syntax
```pine
label.set_x(id, x)
```

---

## label.set_y()

Sets label y coordinate.

### Syntax
```pine
label.set_y(id, y)
```

---

## label.set_color()

Sets label color.

### Syntax
```pine
label.set_color(id, color)
```

---

## label.set_textcolor()

Sets label text color.

### Syntax
```pine
label.set_textcolor(id, color)
```

---

## label.set_size()

Sets label size.

### Syntax
```pine
label.set_size(id, size)
```

---

## label.set_style()

Sets label style.

### Syntax
```pine
label.set_style(id, style)
```

---

## box.new()

Creates a new box.

### Syntax
```pine
box.new(left, top, right, bottom, border_color, border_width, border_style, fill_color, text, text_size, text_color, text_halign, text_valign)
```

### Code Example
```pine
//@version=6
indicator("Box Example")
box.new(bar_index[10], high[10], bar_index, low, border_color=color.blue, fill_color=color.new(color.blue, 90))
```

---

## box.delete()

Deletes a box.

### Syntax
```pine
box.delete(id)
```

---

## box.set_left()

Sets left coordinate.

### Syntax
```pine
box.set_left(id, left)
```

---

## box.set_top()

Sets top coordinate.

### Syntax
```pine
box.set_top(id, top)
```

---

## box.set_right()

Sets right coordinate.

### Syntax
```pine
box.set_right(id, right)
```

---

## box.set_bottom()

Sets bottom coordinate.

### Syntax
```pine
box.set_bottom(id, bottom)
```

---

## box.set_border_color()

Sets border color.

### Syntax
```pine
box.set_border_color(id, color)
```

---

## box.set_fill_color()

Sets fill color.

### Syntax
```pine
box.set_fill_color(id, color)
```

---

## box.set_text()

Sets box text.

### Syntax
```pine
box.set_text(id, text)
```

---

## box.set_text_color()

Sets text color.

### Syntax
```pine
box.set_text_color(id, color)
```

---

## table.new()

Creates a new table.

### Syntax
```pine
table.new(position, columns, rows, bgcolor, border_color, border_width)
```

### Code Example
```pine
//@version=6
indicator("Table Example")
var table myTable = table.new(position.top_right, 2, 2)
table.cell(myTable, 0, 0, "Hello", bgcolor=color.gray)
```

---

## table.delete()

Deletes a table.

### Syntax
```pine
table.delete(id)
```

---

## table.cell()

Sets table cell.

### Syntax
```pine
table.cell(table_id, column, row, text, bgcolor, text_color, text_size, text_halign, text_valign)
```

### Code Example
```pine
//@version=6
indicator("Table Cell Example")
var table t = table.new(position.top_right, 2, 2)
table.cell(t, 0, 0, "Price:", text_color=color.white)
table.cell(t, 1, 0, str.tostring(close), text_color=color.yellow)
```

---

## table.cell_set_text()

Sets cell text.

### Syntax
```pine
table.cell_set_text(id, column, row, text)
```

---

## table.cell_set_text_color()

Sets cell text color.

### Syntax
```pine
table.cell_set_text_color(id, column, row, color)
```

---

## table.cell_set_bg_color()

Sets cell background color.

### Syntax
```pine
table.cell_set_bg_color(id, column, row, color)
```

---

## table.clear()

Clears table.

### Syntax
```pine
table.clear(id, column, row)
```

---

## polyline.new()

Creates a new polyline.

### Syntax
```pine
polyline.new(points, xloc, closed, line_color, fill_color, line_width)
```

---

## linefill.new()

Creates line fills.

### Syntax
```pine
linefill.new(line1, line2, color)
```

---

## linefill.delete()

Deletes line fill.

### Syntax
```pine
linefill.delete(id)
```

---

## color.new()

Creates color with transparency.

### Syntax
```pine
color.new(color, transp)
```

### Code Example
```pine
//@version=6
indicator("Color New")
c = color.new(color.red, 50)  // 50% transparent
plot(close, color=c)
```

---

## color.rgb()

Creates color from RGB.

### Syntax
```pine
color.rgb(r, g, b, transp)
```

---

## color.from_gradient()

Creates gradient color.

### Syntax
```pine
color.from_gradient(value, min_value, min_color, max_value, max_color)
```

---

## display.all

Display in all locations.

---

## display.data_window

Display in data window only.

---

## display.none

Display nowhere.

---

## display.pane

Display in pane.

---

## display.price_scale

Display in price scale.

---

## display.status_line

Display in status line.

---

## plot.style_area

Area style.

---

## plot.style_areabr

Area with breaks style.

---

## plot.style_circles

Circles style.

---

## plot.style_columns

Columns style.

---

## plot.style_cross

Cross style.

---

## plot.style_histogram

Histogram style.

---

## plot.style_line

Line style.

---

## plot.style_linebr

Line with breaks style.

---

## plot.style_stepline

Stepline style.

---

## plot.style_stepline_diamond

Stepline diamond style.

---

## shape.triangleup

Triangle up shape.

---

## shape.triangledown

Triangle down shape.

---

## shape.square

Square shape.

---

## shape.diamond

Diamond shape.

---

## shape.circle

Circle shape.

---

## shape.cross

Cross shape.

---

## shape.xcross

X-cross shape.

---

## shape.arrowup

Arrow up shape.

---

## shape.arrowdown

Arrow down shape.

---

## shape.labelup

Label up shape.

---

## shape.labeldown

Label down shape.

---

## location.abovebar

Location above bar.

---

## location.belowbar

Location below bar.

---

## location.top

Location top.

---

## location.bottom

Location bottom.

---

## location.absolute

Location absolute.

---

## size.auto

Auto size.

---

## size.tiny

Tiny size.

---

## size.small

Small size.

---

## size.normal

Normal size.

---

## size.large

Large size.

---

## size.huge

Huge size.

---

## text.align_left

Text align left.

---

## text.align_center

Text align center.

---

## text.align_right

Text align right.

---

## text.align_top

Text align top.

---

## text.align_bottom

Text align bottom.

---

## text.format_bold

Bold text format.

---

## text.format_italic

Italic text format.

---

## text.wrap_auto

Auto wrap text.

---

## text.wrap_none

No wrap text.

---

## xloc.bar_index

X location by bar index.

---

## xloc.bar_time

X location by bar time.

---

## yloc.price

Y location by price.

---

## yloc.abovebar

Y location above bar.

---

## yloc.belowbar

Y location below bar.

---

## line.style_solid

Solid line style.

---

## line.style_dashed

Dashed line style.

---

## line.style_dotted

Dotted line style.

---

## extend.none

No extend.

---

## extend.right

Extend right.

---

## extend.left

Extend left.

---

## extend.both

Extend both.
