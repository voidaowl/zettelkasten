# Meta
2025-01-29 20:18
**Tags:** [[HTML]]
**Activity:** #learning 
**Status:** #completed   

# 1️⃣ → What does it look like?
```HTML title:example.html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<link rel="stylesheet" href="./styles.css" media="print" on-load="this.media='all'"/>
		<script async src="./script.js"></script>
		<title>My First Webpage</title>
	</head>

	<body>
		...
	</body>

</html>
```

# 2️⃣ → What does it do?
Structures an HTML document.

# 3️⃣ → How it does it.
Every HTML page starts with a doctype declaration, telling the browser what version of HTML it should use to render the document.

The `<html>` element tag represents the root element of the document. All other elements descend from it, and are thus contained within.

The `lang` attribute helps define the language of an element.

The `<head>` element is where we put important meta-information about our webpages. It **should not** contain any content-displaying elements.

Using a `<meta>` element with the charset encoding is **mandatory**.

The `<title>` element specifies our page’s name.

The `<body>` element contains all elements that will be displayed on the page (e.g., text, images, graphs, etc.).

# 4️⃣ → Further reading / Sources
