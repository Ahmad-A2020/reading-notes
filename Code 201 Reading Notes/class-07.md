### Summarized from the Duckett HTML book:
#### Chapter 6: “Tables” (pp.126-145)
- `<table>`: the `<table>` element is used to create a table. The contents of the table are written out row
by row.The row in the table create using `<tr>` tag, and it is followed by one or more `<td> `elements (one for each cell
in that row).At the end of the row you use a closing `</tr>` tag.`<td>` is used to create each cell of the table.
- The `<th>` element is used just like the `<td> `element but its purpose is to represent the heading for either a column or a row.
- To stretch the table cell across more than one column, the *colspan attribute* can be used on a `<th>` or `<td>` element
and indicates how many columns that cell should run across. Take an example of `<td colspan="2">Geography</td>`.
- To stretch down across more than one row.The rowspan attribute can be used on a `<th>` or `<td>` element to indicate how many rows a cell should span down the table.Take an example of `<td rowspan="2">Movie</td>`.
- For Long Tables; there are three elements that help distinguish between the main content of the table and the first and last rows: 
    - `<thead>`: the headings of the table should sit inside the `<thead>` element.
    - `<tbody>`: the body should sit inside the `<tbody>` element.
    - `<tfoot>`: the footer belongs inside the `<tfoot>` element.

### Summarized from the Duckett JS Book:

### Chapter 3: “Functions, Methods, and Objects” (pp.106-144)
Create & Access Oblects Constructor Notation: 
- new Object() keyword: it create new blank, and after that you start appending the properitries and mehods to the object. 
- Creating Many Objects: Sometimes you will want several objects to represent similar things. Object constructors can use a function as a template for creating objects. 
  - First, create the template with the object's properties and methods. Take the following example:
    `function Hotel (name, rooms, booked) {
    this .name = name;
    this.rooms = rooms;
    this.booked = booked;
    this.checkAvailability = function()
    return this.rooms - this.booked;
    } ;`
  - created instances of these objects, you can then access their properties and methods using the same dot notation that you use with all other objects.
 ` var quayHotel = new Hotel('Quay', 40, 25); 
  var parkHotel = new Hotel( ' Park', 120, 77);`
- Built-in Objects: an example of that is Math object. 



