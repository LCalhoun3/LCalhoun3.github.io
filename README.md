<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Cream Background Website Layout</title>
    <!-- Use Google Fonts for a professional look -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap" rel="stylesheet">
    <style>
        body {
            background: #D1C7C0;
            color: #111;
            font-family: 'Roboto', Arial, sans-serif;
            margin: 0;
            padding: 0;
            overflow-x: hidden;
        }
        header {
            background: #6C63FF;
            color: #FFFDD0;
            padding: 2rem 1rem;
            text-align: center;
            border-radius: 0 0 2px 2px;
            box-shadow: 0 4px 16px rgba(108,99,255,0.10);
        }
        nav {
            background: #FFD700;
            padding: 1rem;
            text-align: center;
            border-radius: 0 0 24px 24px;
            box-shadow: 0 2px 8px rgba(108,99,255,0.08);
        }
        nav a {
            color: #111;
            text-decoration: none;
            margin: 0 1rem;
            font-weight: 500;
            padding: 0.5rem 1rem;
            border-radius: 18px;
            transition: background 0.2s, color 0.2s, transform 0.2s;
            display: inline-block;
            font-family: inherit;
        }
        nav a:hover {
            background: #6C63FF;
            color: #FFFDD0;
            transform: scale(1.08);
        }
        #pages-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 400px;
            position: relative;
        }
        .page {
            width: 95%;
            max-width: 700px;
            margin: 2rem 0;
            background: #fffbe6;
            padding: 2rem;
            border-radius: 32px;
            box-shadow: 0 4px 24px rgba(108,99,255,0.10);
            opacity: 0;
            transform: translateY(40px) scale(0.98);
            pointer-events: none;
            position: absolute;
            left: 50%;
            top: 0;
            translate: -50% 0;
            transition: opacity 0.6s, transform 0.6s;
            font-family: inherit;
            z-index: 1;
        }
        .page.active {
            opacity: 1;
            transform: translateY(0) scale(1);
            pointer-events: auto;
            position: relative;
            left: 0;
            top: 0;
            translate: none;
            z-index: 2;
        }
        h1, h2 {
            margin-top: 0;
            font-family: inherit;
        }
        button {
            background: #6C63FF;
            color: #FFFDD0;
            border: none;
            padding: 0.75rem 1.5rem;
            border-radius: 18px;
            cursor: pointer;
            font-size: 1rem;
            margin-top: 1rem;
            box-shadow: 0 2px 8px rgba(108,99,255,0.08);
            transition: background 0.2s, transform 0.2s;
            font-family: inherit;
        }
        button:hover {
            background: #FFD700;
            color: #111;
            transform: scale(1.07);
        }
        footer {
            background: #FFD700;
            color: #111;
            text-align: center;
            padding: 1rem;
            margin-top: 2rem;
            border-radius: 8px 8px 8px 8px;
            box-shadow: 0 -2px 2px rgba(108,99,255,0.08);
            font-family: inherit;
        }
        @media (max-width: 800px) {
            .page {
                width: 98%;
                padding: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Lorem Ipsum Website</h1>
        <p>Where I live stream my crash-outs.</p>
    </header>
    <nav>
        <a href="#" data-page="home">Home</a>
        <a href="#" data-page="about">About</a>
        <a href="#" data-page="services">Services</a>
        <a href="#" data-page="contact">Contact</a>
    </nav>
    <div id="pages-container">
        <section class="page active" id="home">
            <h2>Welcome, User</h2>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, urna eu tincidunt consectetur, nisi nisl aliquam eros, a facilisis enim leo nec urna.
            </p>
            <button>Learn More</button>
        </section>
        <section class="page" id="about">
            <h2>About Us</h2>
            <p>
                We are passionate about creating beautiful, interactive web experiences. Our team loves design, code, and coffee!
            </p>
            <button>Meet the Team</button>
        </section>
        <section class="page" id="services">
            <h2>Our Services</h2>
            <p>
                From web design to development, we offer a range of services to help you build your dream website.
            </p>
            <button>See Pricing</button>
        </section>
        <section class="page" id="contact">
            <h2>Contact Us</h2>
            <p>
                Have questions or want to work with us? Reach out and we'll get back to you soon!
            </p>
            <button>Send Message</button>
        </section>
    </div>
    <footer>
        &copy; 2025 Cream Layout. All rights reserved.
    </footer>
    <script>
        // Page transition logic
        const navLinks = document.querySelectorAll('nav a');
        const pages = document.querySelectorAll('.page');
        navLinks.forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const pageId = link.getAttribute('data-page');
                pages.forEach(page => {
                    if(page.id === pageId) {
                        page.classList.add('active');
                    } else {
                        page.classList.remove('active');
                    }
                });
            });
        });
    </script>
</body>
</html>
