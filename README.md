<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>LGBTQ+ Wiki</title>
  <style>
    body {
      font-family: "Georgia", serif;
      margin: 0;
      display: flex;
      background: #f6f6f6;
    }

    .sidebar {
      width: 280px;
      background: #fff;
      border-right: 1px solid #ccc;
      padding: 20px;
      height: 100vh;
      box-sizing: border-box;
      overflow-y: auto;
    }

    .sidebar h1 {
      font-size: 20px;
      margin-bottom: 15px;
      color: #d63384;
    }

    .sidebar h2 {
      font-size: 16px;
      margin-top: 20px;
      margin-bottom: 10px;
      color: #333;
    }

    .sidebar input {
      width: 100%;
      padding: 8px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 3px;
    }

    .results {
      list-style: none;
      padding: 0;
      margin: 0;
    }

    .results li {
      padding: 8px;
      margin-bottom: 5px;
      background: #f8f9fa;
      border-radius: 3px;
      cursor: pointer;
      font-size: 14px;
    }

    .results li:hover {
      background: #e2e2e2;
    }

    .content {
      flex: 1;
      padding: 40px;
      background: #fff;
      border-left: 1px solid #ccc;
      min-height: 100vh;
    }

    .top-articles {
      margin-bottom: 40px;
    }

    .article-card {
      display: flex;
      align-items: center;
      background: #f8f9fa;
      padding: 25px;
      border-radius: 5px;
      margin-bottom: 25px;
      box-shadow: 0 1px 3px rgba(0,0,0,0.1);
    }

    .article-card img {
      width: 125px;
      height: 125px;
      margin-right: 50px;
    }

    .article-card h3 {
      margin: 0;
      font-size: 16px;
      color: #333;
    }

    .article-card p {
      margin: 5px 0 0;
      font-size: 14px;
      color: #666;
    }

    .article-card span {
      margin-left: auto;
      font-size: 20px;
      color: #d63384;
      cursor: pointer;
    }

    .article {
      display: none;
      max-width: 800px;
      margin: auto;
    }

    .article.active {
      display: block;
    }

    h2 {
      border-bottom: 1px solid #ccc;
      padding-bottom: 5px;
      color: #d63384;
    }

    p {
      line-height: 1.6;
    }
  </style>
</head>
<body>

  <div class="sidebar">
    <h1>🌈 Rainbow Wiki</h1>
    <input type="text" id="searchInput" placeholder="Search articles...">
    
    <h2>Articles</h2>
    <ul id="resultsList" class="results">
      <li data-article="home">Home</li>
      <li data-article="stonewall">Stonewall Riots</li>
      <li data-article="marsha">Marsha P. Johnson</li>
      <li data-article="harvey">Harvey Milk</li>
      <li data-article="pride">History of Pride</li>
      <li data-article="discrimination">Ending Discrimination</li>
      <li data-article="contact">Contact Information</li>
    </ul>

    <h2>Top Contributors</h2>
    <ul class="results">
      <li>Lorem Ipsum</li>
      <li>Dolor Sit</li>
      <li>Amet Et</li>
    </ul>
  </div>

  <div class="content">
    <div class="top-articles">
      <h2>Top Articles</h2>
      <div class="article-card">
        <img src="fiona_3.jpg" alt="icon">
        <div>
          <h3>I am gay</h3>
          <p>Placeholder text for a sample article preview...</p>
        </div>
        <span>❤️</span>
      </div>
      <div class="article-card">
        <img src="download (2).jpg" alt="icon">
        <div>
          <h3>I am GAY</h3>
          <p>Another preview of a popular article...</p>
        </div>
        <span>❤️</span>
      </div>
    </div>

    <div id="home" class="article active">
      <h2>Welcome</h2>
      <h3>
      <p>
        This website addresses discrimination against the LGBTQ+ community and provides solutions.  
        Discrimination in any form is unacceptable, and in recent years it has been at an all-time high, especially for LGBTQ+ individuals.  
        This wiki is a place where everyone can submit articles about historical figures and events regarding the LGBTQ+.  
        The goal of this site is to educate as many people as possible about the LGBTQ+ community. 🌈
      </p>
      </h3>
    </div>

    <div id="stonewall" class="article">
      <h2>Stonewall Riots</h2>
      <p>
        The Stonewall Riots of 1969 in New York City were a series of protests by members of the LGBTQ+ community against police harassment.  
        They are widely considered the spark that ignited the modern LGBTQ+ rights movement.
      </p>
    </div>

    <div id="marsha" class="article">
      <h2>Marsha P. Johnson</h2>
      <p>
        Marsha P. Johnson was a Black transgender activist and drag queen who played a major role in the Stonewall Riots.  
        She became a symbol of resistance and an important figure in LGBTQ+ history.
      </p>
    </div>

    <div id="harvey" class="article">
      <h2>Harvey Milk</h2>
      <p>
        Harvey Milk was the first openly gay elected official in California, serving as a San Francisco city supervisor in 1977.  
        His courage and leadership inspired countless LGBTQ+ people worldwide.
      </p>
    </div>

    <div id="pride" class="article">
      <h2>History of Pride</h2>
      <p>
        Pride Month is celebrated in June to honor the Stonewall Riots and the fight for LGBTQ+ rights.  
        Pride parades and events are held worldwide to promote equality, love, and acceptance.
      </p>
    </div>

    <div id="discrimination" class="article">
      <h2>Ending Discrimination</h2>
      <p>
        Ending discrimination requires education, awareness, and activism.  
        Laws must protect LGBTQ+ people, and communities must support inclusion and respect for all identities.  
        By working together, society can move towards equality and acceptance for everyone.
      </p>
    </div>

    <div id="contact" class="article">
      <h2>Contact Information</h2>
      <p>
        For more information or to contribute to this wiki, please contact us at: rainbowwiki@example.com
      </p>
    </div>
  </div>

  <script>
    const searchInput = document.getElementById("searchInput");
    const results = document.querySelectorAll("#resultsList li");
    const articles = document.querySelectorAll(".article");

    // 🔎 Filter search
    searchInput.addEventListener("keyup", () => {
      const searchText = searchInput.value.toLowerCase();
      results.forEach(item => {
        item.style.display = item.textContent.toLowerCase().includes(searchText) ? "block" : "none";
      });
    });

    // 🖱️ Show article on click
    results.forEach(item => {
      item.addEventListener("click", () => {
        const articleId = item.getAttribute("data-article");

        // hide all
        articles.forEach(article => article.classList.remove("active"));

        // show selected
        document.getElementById(articleId).classList.add("active");
      });
    });
  </script>

</body>
