```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>My Website</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            min-height: 100vh;

            /* Website background */
            background-image: url("website background.avif");
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            background-attachment: fixed;

            color: white;
        }

        /* Dark overlay over background */
        body::before {
            content: "";
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.35);
            z-index: -1;
        }

        /* Top navigation */
        header {
            width: 100%;
            height: 75px;
            display: flex;
            justify-content: flex-end;
            align-items: center;
            padding: 0 30px;
        }

        /* Menu button */
        .menu-button {
            width: 50px;
            height: 50px;
            border: none;
            border-radius: 10px;
            background: rgba(0, 0, 0, 0.55);
            cursor: pointer;

            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            gap: 6px;
        }

        .menu-button span {
            width: 28px;
            height: 3px;
            background: white;
            border-radius: 5px;
            transition: 0.3s;
        }

        /* Menu panel */
        .menu {
            position: absolute;
            top: 75px;
            right: 30px;
            width: 220px;

            background: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(10px);

            border-radius: 12px;
            padding: 10px;

            display: none;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.5);
        }

        .menu.active {
            display: block;
        }

        .menu a {
            display: block;
            color: white;
            text-decoration: none;

            padding: 15px;
            border-radius: 8px;

            font-size: 16px;
            transition: 0.25s;
        }

        .menu a:hover {
            background: rgba(255, 255, 255, 0.15);
            padding-left: 20px;
        }

        /* Main content */
        main {
            min-height: calc(100vh - 75px);

            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;

            padding: 30px;
        }

        .content {
            max-width: 800px;
            padding: 45px;

            background: rgba(0, 0, 0, 0.35);
            backdrop-filter: blur(5px);

            border-radius: 20px;
        }

        .content h1 {
            font-size: 50px;
            margin-bottom: 15px;
        }

        .content p {
            font-size: 19px;
            line-height: 1.6;
        }

        /* Sections */
        section {
            min-height: 100vh;
            padding: 100px 30px;
            text-align: center;
        }

        section h2 {
            font-size: 40px;
            margin-bottom: 20px;
        }

        section p {
            max-width: 700px;
            margin: auto;
            font-size: 18px;
            line-height: 1.7;
        }

        /* Mobile */
        @media (max-width: 600px) {

            header {
                padding: 0 15px;
            }

            .menu {
                right: 15px;
                width: 200px;
            }

            .content {
                padding: 30px 20px;
            }

            .content h1 {
                font-size: 36px;
            }

            .content p {
                font-size: 16px;
            }

            section h2 {
                font-size: 32px;
            }
        }
    </style>
</head>

<body>

    <!-- Top Header -->
    <header>

        <!-- Triple-line menu button -->
        <button class="menu-button" onclick="toggleMenu()">
            <span></span>
            <span></span>
            <span></span>
        </button>

        <!-- Menu -->
        <nav class="menu" id="menu">

            <a href="#home" onclick="closeMenu()">Home</a>

            <a href="#about-website" onclick="closeMenu()">
                About Website
            </a>

            <a href="#about-creator" onclick="closeMenu()">
                About Creator
            </a>

        </nav>

    </header>


    <!-- Home -->
    <main id="home">

        <div class="content">

            <h1>Welcome</h1>

            <p>
                Welcome to my website.
                Explore the website using the menu in the top-right corner.
            </p>

        </div>

    </main>


    <!-- About Website -->
    <section id="about-website">

        <h2>About Website</h2>

        <p>
            Welcome to my website. This section contains information
            about the purpose, features and other details of this website.
        </p>

    </section>


    <!-- About Creator -->
    <section id="about-creator">

        <h2>About Creator</h2>

        <p>
            This website was created by Kush Neupane.
            More information about the creator can be added here.
        </p>

    </section>


    <!-- JavaScript for menu -->
    <script>

        function toggleMenu() {
            const menu = document.getElementById("menu");
            menu.classList.toggle("active");
        }

        function closeMenu() {
            const menu = document.getElementById("menu");
            menu.classList.remove("active");
        }

    </script>

</body>
</html>
```
