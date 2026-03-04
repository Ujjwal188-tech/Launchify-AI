<!DOCTYPE html>
<html>
<head>
    <title>AI Website Generator</title>
</head>
<body>

<h2>Create Your Website</h2>

<input type="text" id="businessName" placeholder="Business Name"><br><br>
<input type="text" id="service" placeholder="Your Service"><br><br>

<button onclick="generateWebsite()">Generate Website</button>

<h3>Generated Code:</h3>
<textarea id="output" rows="15" cols="80"></textarea>

<script>
function generateWebsite() {
    let name = document.getElementById("businessName").value;
    let service = document.getElementById("service").value;

    let code = `
<!DOCTYPE html>
<html>
<head>
<title>${name}</title>
<style>
body { font-family: Arial; text-align: center; }
header { background: black; color: white; padding: 20px; }
</style>
</head>
<body>
<header>
<h1>${name}</h1>
</header>
<h2>Our Service</h2>
<p>${service}</p>
</body>
</html>
`;

    document.getElementById("output").value = code;
}
</script>

</body>
</html>
