# Functions - Collections (array, map, matrix)

---

## array.new()

Creates a new array.

### Returns
Array ID.

### Syntax
```pine
array.new<T>(size, initial_value)
```

### Parameters
- **T**: Type (float, int, bool, string, color)
- **size**: Initial size (optional)
- **initial_value**: Initial value for all elements (optional)

### Code Example
```pine
//@version=6
indicator("Array Example")
arr = array.new<float>(5, 0)
array.set(arr, 0, 100)
plot(array.get(arr, 0))
```

---

## array.size()

Returns array size.

### Returns
Size as int.

### Syntax
```pine
array.size(id)
```

---

## array.get()

Gets element at index.

### Returns
Element value.

### Syntax
```pine
array.get(id, index)
```

---

## array.set()

Sets element at index.

### Returns
Void.

### Syntax
```pine
array.set(id, index, value)
```

---

## array.push()

Adds element to end.

### Returns
Void.

### Syntax
```pine
array.push(id, value)
```

---

## array.pop()

Removes and returns last element.

### Returns
Last element.

### Syntax
```pine
array.pop(id)
```

---

## array.insert()

Inserts element at index.

### Returns
Void.

### Syntax
```pine
array.insert(id, index, value)
```

---

## array.remove()

Removes element at index.

### Returns
Removed element.

### Syntax
```pine
array.remove(id, index)
```

---

## array.slice()

Returns slice of array.

### Returns
New array.

### Syntax
```pine
array.slice(id, from_index, to_index)
```

---

## array.contains()

Checks if array contains value.

### Returns
True if contains.

### Syntax
```pine
array.contains(id, value)
```

---

## array.indexof()

Returns index of value.

### Returns
Index or -1.

### Syntax
```pine
array.indexof(id, value)
```

---

## array.last()

Returns last element.

### Returns
Last element.

### Syntax
```pine
array.last(id)
```

---

## array.first()

Returns first element.

### Returns
First element.

### Syntax
```pine
array.first(id)
```

---

## array.sum()

Returns sum of all elements.

### Returns
Sum value.

### Syntax
```pine
array.sum(id)
```

---

## array.avg()

Returns average of all elements.

### Returns
Average value.

### Syntax
```pine
array.avg(id)
```

---

## array.min()

Returns minimum value.

### Returns
Minimum value.

### Syntax
```pine
array.min(id)
```

---

## array.max()

Returns maximum value.

### Returns
Maximum value.

### Syntax
```pine
array.max(id)
```

---

## array.sort()

Sorts array.

### Returns
Sorted array ID.

### Syntax
```pine
array.sort(id, order)
```

### Parameters
- **order**: order.ascending or order.descending

---

## array.reverse()

Reverses array.

### Returns
Reversed array ID.

### Syntax
```pine
array.reverse(id)
```

---

## array.copy()

Copies array.

### Returns
New array.

### Syntax
```pine
array.copy(id)
```

---

## array.clear()

Clears all elements.

### Returns
Void.

### Syntax
```pine
array.clear(id)
```

---

## array.fill()

Fills array with value.

### Returns
Void.

### Syntax
```pine
array.fill(id, value, from_index, to_index)
```

---

## array.join()

Joins array to string.

### Returns
String.

### Syntax
```pine
array.join(id, separator)
```

---

## array.concat()

Concatenates two arrays.

### Returns
New array.

### Syntax
```pine
array.concat(id1, id2)
```

---

## array.unshift()

Adds element to beginning.

### Returns
Void.

### Syntax
```pine
array.unshift(id, value)
```

---

## array.shift()

Removes and returns first element.

### Returns
First element.

### Syntax
```pine
array.shift(id)
```

---

## array.duplicate()

Duplicates array.

### Returns
New array.

### Syntax
```pine
array.duplicate(id)
```

---

## array.covariance()

Returns covariance between two arrays.

### Returns
Covariance.

### Syntax
```pine
array.covariance(id1, id2)
```

---

## array.stdev()

Returns standard deviation.

### Returns
Standard deviation.

### Syntax
```pine
array.stdev(id)
```

---

## array.variance()

Returns variance.

### Returns
Variance.

### Syntax
```pine
array.variance(id)
```

---

## array.median()

Returns median.

### Returns
Median value.

### Syntax
```pine
array.median(id)
```

---

## array.mode()

Returns mode (most common value).

### Returns
Mode value.

### Syntax
```pine
array.mode(id)
```

---

## array.percentile_linear_interpolation()

Returns percentile.

### Returns
Percentile value.

### Syntax
```pine
array.percentile_linear_interpolation(id, percent)
```

---

## array.percentile_nearest_rank()

Returns percentile (nearest rank).

### Returns
Percentile value.

### Syntax
```pine
array.percentile_nearest_rank(id, percent)
```

---

## array.ranks()

Returns ranks of elements.

### Returns
Array of ranks.

### Syntax
```pine
array.ranks(id, order)
```

---

## arraycorrelation()

Returns correlation between arrays.

### Returns
Correlation.

### Syntax
```pine
array.correlation(id1, id2)
```

---

## array.removeall()

Removes all elements matching value.

### Returns
Number removed.

### Syntax
```pine
array.removeall(id, value)
```

---

## array.replace()

Replaces all occurrences.

### Returns
Number replaced.

### Syntax
```pine
array.replace(id, old_value, new_value)
```

---

## map.new()

Creates a new map.

### Returns
Map ID.

### Syntax
```pine
map.new<T1, T2>()
```

### Parameters
- **T1**: Key type
- **T2**: Value type

### Code Example
```pine
//@version=6
indicator("Map Example")
m = map.new<string, float>()
map.set(m, "key1", 100)
plot(map.get(m, "key1"))
```

---

## map.size()

Returns map size.

### Returns
Size as int.

### Syntax
```pine
map.size(id)
```

---

## map.get()

Gets value by key.

### Returns
Value or na.

### Syntax
```pine
map.get(id, key)
```

---

## map.set()

Sets key-value pair.

### Returns
Void.

### Syntax
```pine
map.set(id, key, value)
```

---

## map.contains()

Checks if key exists.

### Returns
True if contains.

### Syntax
```pine
map.contains(id, key)
```

---

## map.remove()

Removes key-value pair.

### Returns
Removed value or na.

### Syntax
```pine
map.remove(id, key)
```

---

## map.keys()

Returns array of keys.

### Returns
Array of keys.

### Syntax
```pine
map.keys(id)
```

---

## map.values()

Returns array of values.

### Returns
Array of values.

### Syntax
```pine
map.values(id)
```

---

## map.clear()

Removes all entries.

### Returns
Void.

### Syntax
```pine
map.clear(id)
```

---

## map. entries()

Returns array of [key, value] pairs.

### Returns
Array of tuples.

### Syntax
```pine
map.entries(id)
```

---

## matrix.new()

Creates a new matrix.

### Returns
Matrix ID.

### Syntax
```pine
matrix.new<T>(rows, columns, initial_value)
```

### Parameters
- **T**: Type
- **rows**: Number of rows
- **columns**: Number of columns
- **initial_value**: Initial value (optional)

### Code Example
```pine
//@version=6
indicator("Matrix Example")
m = matrix.new<float>(3, 3, 0)
matrix.set(m, 0, 0, 100)
plot(matrix.get(m, 0, 0))
```

---

## matrix.rows()

Returns number of rows.

### Returns
Row count.

### Syntax
```pine
matrix.rows(id)
```

---

## matrix.columns()

Returns number of columns.

### Returns
Column count.

### Syntax
```pine
matrix.columns(id)
```

---

## matrix.size()

Returns total elements.

### Returns
Total count.

### Syntax
```pine
matrix.size(id)
```

---

## matrix.get()

Gets element at row, col.

### Returns
Element value.

### Syntax
```pine
matrix.get(id, row, column)
```

---

## matrix.set()

Sets element at row, col.

### Returns
Void.

### Syntax
```pine
matrix.set(id, row, column, value)
```

---

## matrix.add_row()

Adds new row.

### Returns
Void.

### Syntax
```pine
matrix.add_row(id, row_index, values)
```

---

## matrix.add_column()

Adds new column.

### Returns
Void.

### Syntax
```pine
matrix.add_column(id, column_index, values)
```

---

## matrix.remove_row()

Removes row.

### Returns
Removed row as array.

### Syntax
```pine
matrix.remove_row(id, row_index)
```

---

## matrix.remove_column()

Removes column.

### Returns
Removed column as array.

### Syntax
```pine
matrix.remove_column(id, column_index)
```

---

## matrix.getrow()

Returns row as array.

### Returns
Row array.

### Syntax
```pine
matrix.getrow(id, row_index)
```

---

## matrix.getcol()

Returns column as array.

### Returns
Column array.

### Syntax
```pine
matrix.getcol(id, column_index)
```

---

## matrix.setrow()

Sets entire row.

### Returns
Void.

### Syntax
```pine
matrix.setrow(id, row_index, values)
```

---

## matrix.setcol()

Sets entire column.

### Returns
Void.

### Syntax
```pine
matrix.setcol(id, column_index, values)
```

---

## matrix.copy()

Copies matrix.

### Returns
New matrix.

### Syntax
```pine
matrix.copy(id)
```

---

## matrix.transpose()

Returns transposed matrix.

### Returns
Transposed matrix.

### Syntax
```pine
matrix.transpose(id)
```

---

## matrix.sum()

Returns sum of all elements.

### Returns
Sum value.

### Syntax
```pine
matrix.sum(id)
```

---

## matrix.min()

Returns minimum value.

### Returns
Minimum value.

### Syntax
```pine
matrix.min(id)
```

---

## matrix.max()

Returns maximum value.

### Returns
Maximum value.

### Syntax
```pine
matrix.max(id)
```

---

## matrix.avg()

Returns average of all elements.

### Returns
Average value.

### Syntax
```pine
matrix.avg(id)
```

---

## matrix.fill()

Fills matrix with value.

### Returns
Void.

### Syntax
```pine
matrix.fill(id, value)
```

---

## matrix.clear()

Clears all elements.

### Returns
Void.

### Syntax
```pine
matrix.clear(id)
```

---

## matrix.flatten()

Flattens matrix to array.

### Returns
Array.

### Syntax
```pine
matrix.flatten(id)
```

---

## matrix.diag()

Creates diagonal matrix.

### Returns
Diagonal matrix.

### Syntax
```pine
matrix.diag(id)
```

---

## matrix.inv()

Returns inverse matrix.

### Returns
Inverse matrix.

### Syntax
```pine
matrix.inv(id)
```

---

## matrix.det()

Returns determinant.

### Returns
Determinant.

### Syntax
```pine
matrix.det(id)
```

---

## matrix.dot()

Returns dot product of matrices.

### Returns
Result matrix.

### Syntax
```pine
matrix.dot(id1, id2)
```

---

## matrix.e()

Returns eigenvalues.

### Returns
Eigenvalues array.

### Syntax
```pine
matrix.e(id)
```

---

## matrix.pinv()

Returns pseudo-inverse matrix.

### Returns
Pseudo-inverse matrix.

### Syntax
```pine
matrix.pinv(id)
```

---

## matrix.cov()

Returns covariance matrix.

### Returns
Covariance matrix.

### Syntax
```pine
matrix.cov(id)
```

---

## matrix.correlation()

Returns correlation matrix.

### Returns
Correlation matrix.

### Syntax
```pine
matrix.correlation(id)
```

---

## order.ascending

Sort order - smallest to largest.

### Type
const sort_order

---

## order.descending

Sort order - largest to smallest.

### Type
const sort_order

---
