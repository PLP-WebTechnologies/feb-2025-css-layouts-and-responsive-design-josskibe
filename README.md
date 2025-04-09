# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨



html file - index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Responsive CSS Layout</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <nav class="navbar">
    <div class="logo">MySite</div>
    <ul class="nav-links">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <main class="main-container">
    <section class="sidebar">
      <h2>Sidebar</h2>
      <p>This is a sidebar with some links or info.</p>
    </section>
    <section class="content">
      <h1>Welcome to Responsive Design</h1>
      <p>This layout adjusts across screen sizes using Flexbox and media queries.</p>
    </section>
  </main>

  <footer class="footer">
    <p>Made with 💻✨</p>
  </footer>
</body>
</html>




css external file - style.css

/* Reset & Base Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: 'Segoe UI', sans-serif;
  line-height: 1.6;
}

/* Navigation Bar */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  padding: 1rem 2rem;
  color: white;
}
.logo {
  font-size: 1.5rem;
}
.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}
.nav-links li a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}
.nav-links li a:hover {
  text-decoration: underline;
}

/* Layout using Flexbox */
.main-container {
  display: flex;
  padding: 2rem;
  gap: 2rem;
}
.sidebar {
  flex: 1;
  background-color: #f0f0f0;
  padding: 1rem;
}
.content {
  flex: 3;
  padding: 1rem;
  background-color: #e6f7ff;
}

/* Footer */
.footer {
  text-align: center;
  padding: 1rem;
  background-color: #333;
  color: white;
}

/* Responsive Design */
@media (max-width: 768px) {
  .main-container {
    flex-direction: column;
  }

  .nav-links {
    flex-direction: column;
    gap: 0.5rem;
  }

  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }
}

@media (max-width: 480px) {
  .logo {
    font-size: 1.2rem;
  }
  .nav-links li a {
    font-size: 0.9rem;
  }
}

