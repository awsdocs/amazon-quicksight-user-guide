# `rtrim`<a name="rtrim-function"></a>

`rtrim` removes following whitespace from a string\. 

### Syntax<a name="rtrim-function-syntax"></a>

```
rtrim(expression)
```

### Arguments<a name="rtrim-function-arguments"></a>

 *expression*   
The expression must be a string\. It can be the name of a field that uses the string data type, a literal value like **'12 Main Street'**, or a call to another function that outputs a string\.

### Return Type<a name="rtrim-function-return-type"></a>

String

### Example<a name="rtrim-function-example"></a>

The following example removes the following spaces from a string\.

```
rtrim('Seattle Store #14   ')
```

For these field values, the following values are returned\.

```
Seattle Store #14
```

You can also remote specific characters from at the end of a string field. For example, assuming `customer.address` has the string value `Seatle Store #14`:

```
rtrim(customer.address, '#14')
```

And this will return\.

```
Seattle Store 
```