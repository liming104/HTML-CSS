# HTML-CSS
##一个具体例子清楚解释 select、radio、text、number、date、checkbox、tel、textarea 用法。
>来自《Head First HTML&CSS》14章


```
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>pratice</title>
	<link rel="stylesheet" href="copy.css">
</head>
<body>

	<h1>The Starbuzz Bean Machine</h1>
	<h2>Fill out the form below and click "order now" to order</h2>

	<form action="" method="post">
		<fieldset>
			<legend>Order details</legend>
			<div class="tableRow">
				<label for="beans">Choose your beans:</label>
				<select id="beans" name="beans">
					<option value="House Blend">House Blend</option>
					<option value="Bolivia">Shade Grown Bolivia Supremo</option>
					<option value="Guatemala">Organic Guatemala</option>
					<option value="Kenya">Kenya</option>
				</select>
			</div>

			<div class="tableRow">
				<label>Type:</label>
				<p>
					
					<input type="radio" id="whole_beantype" name="beantype" value="whole" >
						<label for="whole_beantype">Whole bean</label><br>		
					<input type="radio" id="ground_beantype" name="beantype" value="ground">
						<label for="ground_beantype">Ground</label>
				</p>
			</div>

			<div class="tableRow">
				<label for="bags">Number of bags:</label>
				<input type="Number" name="bags" id="bags" min="1" max="10">
			</div>

			<div class="tableRow">
				<label for="date">Must arrive by date:</label>
				<input type="date" name="date">
			</div>

			<div class="tableRow">
				<label>Extras:</label>
				<p>
					<input type="checkbox" id="giftwrap_extras">
						<label for="giftwrap_extras">Gift wrap</label>
					<input type="checkbox" id="catalog_extras">
						<label for="catalog_extras">Include catalog with order</label>
				</p>
			</div>
		</fieldset>

		<fieldset>
			<legend>Ship to</legend>
			<div class="tableRow">
				<label for="name">Name:</label>
				<input type="text" name="name" placeholder="liming" required>
			</div>

			<div class="tableRow">
				<label for="address">Address:</label>
				<input type="text" id="address" placeholder="zhengzhou" required>
			</div>

			<div class="tableRow">
				<label for="city">City:</label>
				<input type="text" id="city" placeholder="henan" required>
			</div>

			<div class="tableRow">
				<label for="state">State:</label>
				<input type="text" id="state" placeholder="China" >
			</div>

			<div class="tableRow">
				<label for="zip">Zip:</label>
				<input type="text" id="zip" placeholder="450000" required>
			</div>

			<div class="tableRow">
				<label for="phone">Phone:</label>
				<input type="tel" id="phone" placeholder="12332112345" required>
			</div>

			<div class="tableRow">
				<label for="comments">Customer Comments:</label>
				<textarea id="comments" name="comments"></textarea>
			</div>

			<div class="tableRow">
				<label></label>
				<input type="submit" value="Order Now">
			</div>
		</fieldset>
	</form>
</body>
</html>

/* CSS */
body {
	background: #efe5d0 url(images/background.gif) top left;
	margin: 20px;
}

form {
	display: table;
	padding: 10px;
	border: thin dotted #7e7e7e;
	background-color: #e1ceb8;
}

div.tableRow {
	display: table-row;
}

div.tableRow > p, div.tableRow > label, div.tableRow > input {
	display: table-cell;
	vertical-align: top;
	padding: 5px;
}
div.tableRow label:first-child {
	text-align: right;
}
form textarea {
	display: table-cell;
	width: 300px;
	height:50px;
}
legend {
	font-weight: bold;
}
```

