## Selecting DOM elements in D3

You can refer the below section to select HTML dom elements in D3. Selecting an element is provided by default in D3 and it is not necessary to use JQuery selector to select elements in D3

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

## D3 DOM selector

[Selecting DOM elements in D3](https://github.com/d3/d3/blob/master/API.md#selecting-elements)

You can use the below methods to select a DOM element using D3

d3.select - select an element from the document.
d3.selectAll - select multiple elements from the document.

### Example:

//this will pick the first item i.e "John" and change the text "John" to "George"

 d3.select('.item').text('George')

//if you want to select all the items having the class "item" then you can use selectall

 d3.selectAll('.item').text('select')
 
// using id -> the below code selects "item" under "#chart"

d3.select('#chart .item').text('select')

d3.selectAll('#chart .item').text('select')

//the below code will select the second element which has the class name "item"
// to know more about nth child selector you can [click here](https://css-tricks.com/how-nth-child-works/)
d3.select('.item:nth-child(2)').text('select')

//this will select every other odd elements

d3.select('.item:nth-child(odd)').text('select')

//this will select every element after the 3rd element including the 3rd element
d3.select('.item:nth-child(n+3)').text('select')

//this will select the 2nd element and every other element after that
d3.select('.item:nth-child(2n)').text('select')
