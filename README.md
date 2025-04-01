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

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox and Grid</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navigation Bar -->
    <nav class="navbar">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>

    <!-- Main Content Section -->
    <main>
        <section class="grid-container">
            <article class="content-item">Section 1</article>
            <article class="content-item">Section 2</article>
            <article class="content-item">Section 3</article>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 Your Company</p>
    </footer>

</body>
</html>



/* Basic reset and font setup */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body {
    font-family: 'Arial', sans-serif;
    background-color: #f4f4f4;
}

/* Navigation Bar */
.navbar {
    background-color: #4CAF50;
    padding: 15px;
}
.navbar ul {
    display: flex;
    justify-content: center;
    list-style-type: none;
}
.navbar ul li {
    margin: 0 15px;
}
.navbar ul li a {
    color: white;
    text-decoration: none;
    font-size: 18px;
    transition: color 0.3s;
}
.navbar ul li a:hover {
    color: #ddd;
}

/* Main Grid Layout */
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    padding: 20px;
}
.content-item {
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

/* Footer */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: 30px;
}

/* Media Queries */

/* Tablet View (max-width: 768px) */
@media (max-width: 768px) {
    .navbar ul {
        flex-direction: column;
        align-items: center;
    }
    .grid-container {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Mobile View (max-width: 480px) */
@media (max-width: 480px) {
    .navbar ul {
        flex-direction: column;
        align-items: center;
    }
    .grid-container {
        grid-template-columns: 1fr;
    }
}
