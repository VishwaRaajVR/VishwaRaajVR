<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Vishwa Raaj eBook Store - Premium Digital Books Collection">
    <meta name="keywords" content="eBooks, Digital Books, Vishwa Raaj, Free Download">
    <meta name="author" content="Vishwa Raaj eBook Store">
    <title>Vishwa Raaj eBook Store | Premium Digital Books</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #1e88e5;
            --secondary-color: #263238;
            --highlight-color: #ffca28;
            --text-color: #455a64;
            --bg-color: #f7f9fc;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        /* Header */
        .header {
            background: var(--secondary-color);
            color: #fff;
            padding: 1rem 2rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        /* Site Title Division */
        .site-title {
            background: linear-gradient(45deg, var(--secondary-color), var(--primary-color));
            padding: 0.5rem 1rem;
            border-radius: 8px;
            transition: transform 0.3s ease;
        }

        .site-title h1 {
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: 1.5px;
        }

        .site-title h1 span {
            color: var(--highlight-color);
            text-shadow: 1px 1px 2px rgba(0,0,0,0.2);
        }

        .site-title:hover {
            transform: scale(1.02);
        }

        /* Navigation Bar Division */
        .nav-bar {
            display: flex;
            align-items: center;
            gap: 2rem;
        }

        .nav-bar a {
            color: #fff;
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            position: relative;
            transition: all 0.3s ease;
        }

        .nav-bar a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--highlight-color);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            transition: width 0.3s ease;
        }

        .nav-bar a:hover::after {
            width: 70%;
        }

        .nav-bar a:hover {
            color: var(--highlight-color);
            background: rgba(255,255,255,0.1);
        }

        /* Container */
        .container {
            max-width: 1200px;
            margin: 2rem auto;
            padding: 0 1.5rem;
        }

        /* Book Grid */
        .book-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            padding: 1rem 0;
        }

        .book-card {
            background: #fff;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 6px 20px rgba(0,0,0,0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .book-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 30px rgba(0,0,0,0.15);
        }

        .book-cover {
            width: 100%;
            height: 320px;
            object-fit: cover;
            border-bottom: 4px solid var(--primary-color);
        }

        .book-details {
            padding: 1.5rem;
        }

        .book-title {
            color: var(--secondary-color);
            font-size: 1.3rem;
            font-weight: 500;
            margin-bottom: 0.5rem;
        }

        .book-author {
            color: var(--text-color);
            font-size: 0.95rem;
            margin-bottom: 1rem;
        }

        .book-price {
            color: var(--primary-color);
            font-size: 1.4rem;
            font-weight: 700;
        }

        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background: var(--primary-color);
            color: #fff;
            text-decoration: none;
            border-radius: 25px;
            margin-top: 1rem;
            transition: background 0.3s ease, transform 0.2s ease;
        }

        .btn:hover {
            background: #1565c0;
            transform: scale(1.05);
        }

        /* Legal Sections */
        .legal-section {
            background: #fff;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.08);
            margin: 2rem 0;
        }

        .legal-section h2 {
            color: var(--secondary-color);
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .legal-section p {
            margin-bottom: 1rem;
        }

        /* Contact Form */
        .contact-section {
            background: #fff;
            padding: 2rem;
            border-radius: 12px;
            box-shadow: 0 6px 20px rgba(0,0,0,0.08);
            margin: 2rem 0;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 1.2rem;
        }

        .contact-form label {
            font-weight: 500;
            color: var(--secondary-color);
        }

        .contact-form input,
        .contact-form textarea {
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            border-color: var(--primary-color);
            outline: none;
        }

        .contact-form textarea {
            resize: vertical;
            min-height: 120px;
        }

        /* Footer */
        .footer {
            background: var(--secondary-color);
            color: #fff;
            text-align: center;
            padding: 2rem 1rem;
            margin-top: 3rem;
        }

        .footer-links {
            margin-top: 1rem;
        }

        .footer-links a {
            color: #fff;
            margin: 0 1.5rem;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--highlight-color);
        }

        /* Media Queries */
        @media (max-width: 768px) {
            .header {
                flex-direction: column;
                padding: 1rem;
            }
            .site-title h1 {
                font-size: 1.8rem;
            }
            .nav-bar {
                margin-top: 1rem;
                gap: 1rem;
                flex-wrap: wrap;
                justify-content: center;
            }
            .book-grid {
                grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            }
        }

        @media (max-width: 480px) {
            .book-title {
                font-size: 1.1rem;
            }
            .book-price {
                font-size: 1.2rem;
            }
            .btn {
                padding: 0.6rem 1rem;
            }
            .nav-bar a {
                font-size: 1rem;
                padding: 0.4rem 0.8rem;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="site-title">
            <h1>Vishwa <span>Raaj</span> eBook Store</h1>
        </div>
        <nav class="nav-bar">
            <a href="#home">Home</a>
            <a href="#terms">Terms</a>
            <a href="#privacy">Privacy</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <main class="container">
        <section class="book-grid" id="home">
            <article class="book-card">
                <img src="https://via.placeholder.com/300x400.png?text=FIRE+Book+Cover" 
                     alt="Financial Independence Retire Early (FIRE) Book Cover" 
                     class="book-cover" 
                     loading="lazy">
                <div class="book-details">
                    <h3 class="book-title">Financial Independence Retire Early (FIRE)</h3>
                    <p class="book-author">Author: Sandeep Shende</p>
                    <p class="book-price">Free Download</p>
                    <a href="#" class="btn" aria-label="Download FIRE Book">Download Now</a>
                </div>
            </article>

            <article class="book-card">
                <img src="https://via.placeholder.com/300x400.png?text=Teeth+Whitening+Cover" 
                     alt="7 Days to Whiter Teeth Book Cover" 
                     class="book-cover" 
                     loading="lazy">
                <div class="book-details">
                    <h3 class="book-title">7 Days to Whiter Teeth</h3>
                    <p class="book-author">Author: Natural Methods Guide</p>
                    <p class="book-price">$2.99</p>
                    <a href="#" class="btn" aria-label="Buy 7 Days to Whiter Teeth Book">Buy Now</a>
                </div>
            </article>
        </section>

        <!-- Terms and Conditions -->
        <section class="legal-section" id="terms">
            <h2>Terms and Conditions</h2>
            <p>Welcome to Vishwa Raaj eBook Store. Please read the following terms before using our website:</p>
            <p>1. All content is the property of Vishwa Raaj eBook Store. Unauthorized copying is prohibited.</p>
            <p>2. Free and paid eBooks require compliance with our terms.</p>
            <p>3. Disputes will be governed by Indian law.</p>
            <p>4. We reserve the right to modify these terms at any time.</p>
        </section>

        <!-- Privacy Policy -->
        <section class="legal-section" id="privacy">
            <h2>Privacy Policy</h2>
            <p>We respect your privacy. This policy explains how we handle your information:</p>
            <p>1. We collect name, email, and payment details for order processing only.</p>
            <p>2. Your information will not be shared with third parties, except as required by law.</p>
            <p>3. We implement reasonable security measures to protect your data.</p>
            <p>4. Contact us with any questions.</p>
        </section>

        <!-- Contact Form -->
        <section class="contact-section" id="contact">
            <h2>Contact Us</h2>
            <form class="contact-form">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required placeholder="Enter your name">

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required placeholder="Enter your email">

                <label for="message">Message:</label>
                <textarea id="message" name="message" required placeholder="Your message"></textarea>

                <button type="submit" class="btn">Send Message</button>
            </form>
            <p style="margin-top: 1rem;">Or email us at: <a href="mailto:support@vishwaraaj.com">support@vishwaraaj.com</a></p>
        </section>
    </main>

    <footer class="footer">
        <p>© 2025 Vishwa Raaj eBook Store. All Rights Reserved.</p>
        <div class="footer-links">
            <a href="#contact">Contact Us</a>
            <a href="#terms">Terms</a>
            <a href="#privacy">Privacy</a>
        </div>
    </footer>
</body>
</html>
