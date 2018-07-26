## &#x1F4D7; Selecting DOM elements in D3

You can refer the below section to select HTML dom elements in D3. Selecting an element is provided by default in D3 and it is not necessary to use JQuery selector to select elements in D3

```
<body>

<div class="container">
	<h2>D3 Graphic</h2>
	<section id="chart">
		<div class="item">John</div>
		<div class="item">James</div>
		<div class="item">Jeril</div>
		<div class="item">Jose</div>
		<div class="item">Jany</div>
	</section>
</div>

<script src="https://d3js.org/d3.v5.min.js"></script>

<script>
	

</script>
</body>
```

## D3 DOM selector

Refer the below documentation on how to select DOM elements in D3

> :fire: [Selecting DOM elements in D3](https://github.com/d3/d3/blob/master/API.md#selecting-elements)

You can use the below methods to select a DOM element using D3

```Javascript
d3.select - select an element from the document.
d3.selectAll - select multiple elements from the document.
```

### Example:

//this will pick the first item i.e "John" and change the text "John" to "George"

```Javascript
 d3.select('.item').text('George')
 ```

//if you want to select all the items having the class "item" then you can use selectall

```Javascript
 d3.selectAll('.item').text('select')
 ```
 
// using id -> the below code selects "item" under "#chart"

```Javascript
d3.select('#chart .item').text('select')
d3.selectAll('#chart .item').text('select')
```

//the below code will select the second element which has the class name "item"
// to know more about nth child selector you can [click here](https://css-tricks.com/how-nth-child-works/)

```Javascript
d3.select('.item:nth-child(2)').text('select')
```

//this will select every other odd elements

```Javascript
d3.select('.item:nth-child(odd)').text('select')
```
//this will select every element after the 3rd element including the 3rd element

```Javascript
d3.select('.item:nth-child(n+3)').text('select')
```

//this will select the 2nd element and every other element after that

```Javascript
d3.select('.item:nth-child(2n)').text('select')
```

---

## Working with HTML DOM Elements using D3(Inserting, appending, removing HTML elements)

So how do you insert HTML elements like ```<div>```, ```<span>``` inside the DOM?

```
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

<div class="container">
	<h2>D3 Graphic</h2>
	<section id="chart">
		<div class="item">John</div>
		<div class="item">James</div>
		<div class="item">Jeril</div>
		<div class="item">Jose</div>
		<div class="item">Jany</div>
	</section>
</div>
<script src="https://d3js.org/d3.v5.min.js"></script>

<script> 

//write code to insert, append or remove here

</script>

```

:fire: Using the append functionality

```Javascript
<script>
d3.select('.item')   //selects the element with the class name .item, similiarly you can use #chart
  .append('div')
  .html('<strong>selection</strong>')
</script>

</body>
</html>
```

:fire: Using the insert functionality - To Insert a DOM element in-between another DOM element

```Javacript
d3.select('#chart')   
  .insert('span', ':nth-child(3)')
  .html('<strong>selection</strong>')
```

:fire: Using the remove functionality - To Delete a DOM element

```Javascript
d3.select('#chart .item:nth-child(3)')
  .remove()
```

### BROWSER OUTPUT: 

A new element named selection is added

* John
* **selection**
* James
* Jeril
* Jose
* Jany

### HTML OUTPUT for APPEND: 

The above code selects the first item and creates a ```<div>``` under it and then creates a ```<strong>``` element under the ```<div>```

```
  <div class="item">John</div>  
  <div>
   	 <strong>selection</strong>
  </div>
  <div class="item">James</div>
  <div class="item">Jeril</div>
  <div class="item">Jose</div>
  <div class="item">Jany</div>
```

---

## Working with CSS and styling - 

You can style elements using the ```attr()``` method of D3. You can also control any element using ATTR method

```Javascript
d3.selectAll('.item')
  .attr('class', 'highlight')
```

```Javascript
d3.selectAll('.item:nth-child(3)')
  .attr('class', 'highlight')
```

#### CSS

```
.highlight{
  color: #C64C6F
  font-weight: 600;
}
```

You can also style directly like shown below.
//style is an object {}

```Javascript
d3.selectAll('.item:nth-child(3)')
  .style({
     'background': '#268BD2',
     'padding' : '10px',
     'margin' : '5px',
     'color' : '#EEE8D5'
  })
```

---
