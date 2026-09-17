<!DOCTYPE html>
<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>SAKLEZ — Search. Verify. Understand.</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: white;
      color: #222;
      text-align: center;
    }

    header {
      padding: 22px;
      font-size: 28px;
      font-weight: bold;
    }

    main {
      max-width: 750px;
      margin: 70px auto;
      padding: 20px;
    }

    h1 {
      font-size: 55px;
      margin-bottom: 10px;
    }

    p {
      color: #666;
      font-size: 17px;
    }

    .search {
      display: flex;
      border: 1px solid #ccc;
      border-radius: 35px;
      padding: 6px;
      margin-top: 35px;
    }

    input {
      flex: 1;
      border: none;
      outline: none;
      padding: 15px;
      font-size: 17px;
      border-radius: 30px;
    }

    button {
      border: none;
      background: #111;
      color: white;
      padding: 14px 24px;
      border-radius: 30px;
      cursor: pointer;
    }

    #result {
      text-align: left;
      margin-top: 40px;
    }

    .box {
      border-bottom: 1px solid #ddd;
      padding: 20px 0;
    }

    .source {
      color: green;
      font-size: 14px;
    }
  </style>
</head>

<body>

<header>SAKLEZ</header>

<main>

  <h1>SAKLEZ</h1>

  <p>Search. Verify. Understand.</p>

  <div class="search">
    <input id="query" placeholder="Search anything...">
    <button onclick="search()">Search</button>
  </div>

  <div id="result"></div>

</main>

<script>

function search() {

  const query = document.getElementById("query").value.trim();

  if (!query) {
    document.getElementById("result").innerHTML =
      "<p>Please enter a search.</p>";
    return;
  }

  const googleSearch =
    "https://www.google.com/search?q=" +
    encodeURIComponent(query);

  document.getElementById("result").innerHTML = `

    <div class="box">

      <h2>SAKLEZ Search</h2>

      <div class="source">
        Web Search
      </div>

      <p>
        Your search is ready.
      </p>

      <p>
        <a href="${googleSearch}" target="_blank">
          Open web results for "${query}"
        </a>
      </p>

    </div>

  `;
}

</script>

</body>
</html>
