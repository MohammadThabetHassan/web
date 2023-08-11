<!DOCTYPE html>
<html>
<head>
  <title>My Blog</title>
  <link rel="stylesheet" href="style.css">
  <script src="script.js"></script>
</head>
<body>
  <div id="container">
    <header>
      <h1>My Blog</h1>
    </header>
    <main>
      <section id="posts">
        <h2>Posts</h2>
        <ul>
          <li>
            <a href="#">This is my first post</a>
          </li>
          <li>
            <a href="#">This is my second post</a>
          </li>
          <li>
            <a href="#">This is my third post</a>
          </li>
        </ul>
      </section>
      <section id="about">
        <h2>About</h2>
        <p>This is my blog, where I share my thoughts and experiences.</p>
      </section>
    </main>
    <footer>
      <p>&copy; 2023 My Blog</p>
    </footer>
  </div>

  <script>
    function readMore(event) {
      event.preventDefault();

      var postId = event.target.dataset.postId;
      var url = "post.html?id=" + postId;

      window.open(url, "_blank");
    }

    function about(event) {
      event.preventDefault();

      var url = "about.html";

      window.open(url, "_blank");
    }

    document.querySelectorAll(".read-more").forEach(function(button) {
      button.addEventListener("click", readMore);
    });

    document.querySelector(".about").addEventListener("click", about);
  </script>
</body>
</html>
