<!DOCTYPE html>
<html>
<head>
  <title>SAKLEZ — Search. Verify. Understand.</title>
</head>
<body>
  <h1>SAKLEZ</h1>
  <p>Search. Verify. Understand.</p>

  <input id="search" placeholder="Search anything...">
  <button onclick="search()">Search</button>

  <div id="result"></div>

  <script>
    function search() {
      let q = document.getElementById("search").value;
      document.getElementById("result").innerHTML =
        "You searched for: " + q;
    }
  </script>
</body>
</html>
