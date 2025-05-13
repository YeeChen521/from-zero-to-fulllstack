# HTML Table

Table is a very useful tool in displaying data.
```
<table>
</table>
```

## Row
`<tr></tr>`

## Data
Add data using table data element `<td>`

`<td>73</td>`

```
<table>
    <tr>
        <td>123</td>
        <td>456</td>
    </tr>
    <tr>
    </tr>
</table>
```
In the example above, the table contains two rows and two columns. The first row contains 123 in first column and 456 in second column. The second row is an empty row.

## Heading
To add titles to rows and columns, we can use table heading element `<th>`.
```
<table>
    <tr>
        <th></th>
        <th scope="col">Saturday</th>
        <th scope="col">Sunday</th>
    </tr>
    <tr>
        <th scope="row">Temperature</th>
        <td>73</td>
        <td>81</td>
    </tr>
</table>
```
In the example above, a new row was added to hold the three headings: a blank heading, a `Saturday` heading and a `Sunday` heading. In the second row, one tabole heading was added as a row title:`Temperature`.
<table>
    <tr>
        <th></th>
        <th scope="col">Saturday</th>
        <th scope="col">Sunday</th>
    </tr>
    <tr>
        <th scope="row">Temperature</th>
        <td>73</td>
        <td>81</td>
    </tr>
</table>

The use of `scope` attribute, which can take one of two values:
- `row` : heading for a row
- `col` : heading for a column

## Border
In older versions of HTML, a border can be added to a table using `border` attribute.
```
<table border="1">
    <tr>
        <td>73</td>
    </tr>
</table>
```
However, the code in the example above is deprecated, so please prevent use this way.
Normally, we use CSS to style HTML documents because it help us to seperate the structure of a page from how it looks.
```
table,td{
    border: 1px solid black;
}
```

## Spanning
### Column
Data can span columns using `colspan` attribute. The attribute accepts an integer (>= 1) to denote the number of columns it spans across.
```
<table>
    <tr>
        <th>Monday</th>
        <th>Tuesday</th>
        <th>Wednesday</th>
    </tr>
    <tr>
        <td colspan="2">Out of Town</td>
        <td>Back in Town</td>
    </tr>
</table>
```
<table>
    <tr>
        <th>Monday</th>
        <th>Tuesday</th>
        <th>Wednesday</th>
    </tr>
    <tr>
        <td colspan="2">Out of Town</td>
        <td>Back in Town</td>
    </tr>
</table>

### Row
`rowspan` is used for data that spans multiple rows. It works like `colspan`.

```
<table>
    <tr>
        <th></th>
        <th>Saturday</th>
        <th>Sunday</th>
    </tr>
    <tr>
        <th>Morning</th>
        <td rowspan="2">Work</td>
        <td rowspan="3">Relax</td>
    </tr>
    <tr>
        <th>Afternoon</th>
    </tr>
    <tr>
        <th>Evening</th>
        <th>Dinner</th>
    </tr>
</table>
```
<table>
    <tr>
        <th></th>
        <th>Saturday</th>
        <th>Sunday</th>
    </tr>
    <tr>
        <th>Morning</th>
        <td rowspan="2">Work</td>
        <td rowspan="3">Relax</td>
    </tr>
    <tr>
        <th>Afternoon</th>
    </tr>
    <tr>
        <th>Evening</th>
        <th>Dinner</th>
    </tr>
</table>

## Table Body , Head and Footer
When a table grow to contain a lot of data and become very long, the table can be sectioned off so that it is easier to manage. Long tables can be sectioned off using the table *body* element:`<tbody>`
`<tbody>` contain all of the table's data except the table headings. When a table's body is sectioned off, it also make sense to section off the table's column headings using the `<thead>` element.
Only the column header will go under `<thead>`.
The bottom part of a long table can also be sectioned off using `<tfoot>` element. Footer are often used to contain sums,difference and other data results.
```
<table>
  <thead>
    <tr>
      <th>Quarter</th>
      <th>Revenue</th>
      <th>Costs</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Q1</th>
      <td>$10M</td>
      <td>$7.5M</td>
    </tr>
    <tr>
      <th>Q2</th>
      <td>$12M</td>
      <td>$5M</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Total</th>
      <td>$22M</td>
      <td>$12.5M</td>
    </tr>
  </tfoot>
</table>
```
<table>
  <thead>
    <tr>
      <th>Quarter</th>
      <th>Revenue</th>
      <th>Costs</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Q1</th>
      <td>$10M</td>
      <td>$7.5M</td>
    </tr>
    <tr>
      <th>Q2</th>
      <td>$12M</td>
      <td>$5M</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Total</th>
      <td>$22M</td>
      <td>$12.5M</td>
    </tr>
  </tfoot>
</table>

