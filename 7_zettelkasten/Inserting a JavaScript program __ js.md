# Meta
2025-01-29 18:56
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed

# The “script” tag
JavaScript programs can be inserted almost anywhere into an HTML document using the `<script>` tag.
```HTML title:example.html
<!DOCTYPE HTML>
<html>

<body>
	<p>Before the script...</p>

	<script>
		alert('Hello, world!');
	</script>
</body>

</html>
```

# Inline External Scripts
```HTML title:example.html
<!DOCTYPE HTML>
<html>

<body>
	<p>Before the script...</p>

	<script src="/js/script1.js"></script>
</body>

</html>
```

>[!warning]
>A single `<script>` tag can’t have both the `src` attribute and code inside.

# ✅ → Best Practice
```HTML title:example.html
<!DOCTYPE HTML>
<html>
<head>
	<script src="path/to/script.js"></script>
</head>

<body>

</body>

</html>
```

# 📑 → Further Reading
[[Non-blocking JavaScript: defer and async __ js]]
