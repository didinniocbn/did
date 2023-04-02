<!DOCTYPE html>
<html>
<head>
	<title>Table with JavaScript</title>
</head>
<body>
	<h1>Table with JavaScript</h1>

	<table id="myTable">
		<thead>
			<tr>
				<th>Name</th>
			</tr>
		</thead>
		<tbody>
		</tbody>
	</table>

	<script>
		// array of names to be added to the table
		var names = ["John", "Mary", "Tom", "Lisa"];

		// select the table body
		var tableBody = document.querySelector("#myTable tbody");

		// loop through the names and create a new row for each name
		for (var i = 0; i < names.length; i++) {
			var name = names[i];

			// create a new row and cell for the name
			var newRow = tableBody.insertRow();
			var cell = newRow.insertCell();

			// add the name to the cell
			cell.innerHTML = name;
		}
	</script>
</body>
</html>
# did
Fidino
