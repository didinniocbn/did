
<!DOCTYPE html>
<html>
<head>
	<title>Contact Form</title>
	<style>
		body {
			font-family: Arial, sans-serif;
			background-color: #f2f2f2;
		}
		form {
			background-color: #fff;
			max-width: 500px;
			margin: 0 auto;
			padding: 20px;
			border-radius: 5px;
			box-shadow: 0px 0px 10px rgba(0,0,0,0.1);
		}
		input[type=text], textarea {
			width: 100%;
			padding: 12px;
			border: 1px solid #ccc;
			border-radius: 4px;
			resize: vertical;
		}
		label {
			display: block;
			font-weight: bold;
			margin-bottom: 10px;
		}
		button[type=submit] {
			background-color: #4CAF50;
			color: white;
			padding: 12px 20px;
			border: none;
			border-radius: 4px;
			cursor: pointer;
		}
		button[type=submit]:hover {
			background-color: #45a049;
		}
		.error-message {
			color: red;
			margin-bottom: 10px;
		}
	</style>
</head>
<body>
	<form action="#" method="post">
		<label for="name">Name</label>
		<input type="text" id="name" name="name" placeholder="Your name.." required>

		<label for="email">Email</label>
		<input type="text" id="email" name="email" placeholder="Your email.." required>

		<label for="subject">Subject</label>
		<input type="text" id="subject" name="subject" placeholder="Subject.." required>

		<label for="message">Message</label>
		<textarea id="message" name="message" placeholder="Write something.." required></textarea>

		<div class="error-message"></div>

		<button type="submit">Submit</button>
	</form>

	<script>
		const form = document.querySelector('form');
		const errorMessage = document.querySelector('.error-message');

		form.addEventListener('submit', (event) => {
			event.preventDefault();

			const name = document.querySelector('#name').value.trim();
			const email = document.querySelector('#email').value.trim();
			const subject = document.querySelector('#subject').value.trim();
			const message = document.querySelector('#message').value.trim();

			if (!name || !email || !subject || !message) {
				errorMessage.textContent = 'Please fill in all fields.';
				return;
			}

			// Send the form data to a server using AJAX or fetch

			errorMessage.textContent = '';
			form.reset();
		});
	</script>
</body>
</html>
