# Project Responsive Web Design using Bootstrap
## Date: 23-05-2025

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

### Step 5:
Create a HTML file and include the needed Bootstrap components.

### Step 6:
Publish the website in the LocalHost.

## PROGRAM :
home.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Redmi</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"/>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      font-family: 'Outfit', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
    }

    .hero-section {
      position: relative;
      height: 100vh;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    .hero-video {
      position: absolute;
      top: 50%;
      left: 50%;
      width: 100%;
      height: 100%;
      object-fit: cover;
      transform: translate(-50%, -50%);
      z-index: -1;
    }

    .hero-content {
      z-index: 2;
      color: white;
      background: rgba(0, 0, 0, 0.5);
      padding: 2rem;
      border-radius: 15px;
      max-width: 90%;
    }

    .hero-content h1 {
      font-size: 3rem;
      font-weight: 700;
    }

    .hero-content p {
      font-size: 1.25rem;
      margin-bottom: 1rem;
    }

    .products img {
      height: 300px;
      object-fit: cover;
    }

    footer {
      background-color: #000;
      color: #fff;
      padding: 20px 0;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg bg-dark navbar-dark fixed-top">
    <div class="container">
      <a class="navbar-brand" href="#">Redmi</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
        data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item"><a class="nav-link" href="home.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="phones.html">Phones</a></li>
          <li class="nav-item"><a class="nav-link" href="tablets.html">Tablets</a></li>
          <li class="nav-item"><a class="nav-link" href="tv.html">Smart TVs</a></li>
          <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <header class="hero-section">
    <video autoplay muted loop playsinline class="hero-video">
      <source src="10 v.mp4" type="video/mp4" />
    </video>
    <div class="hero-content">
      <h1>Redmi Note 13 Pro+</h1>
      <p>Innovation for Everyone.</p>
      <a href="phones.html" class="btn btn-light">Learn More</a>
    </div>
  </header>

  <!-- Products Section -->
  <section class="products py-5">
    <div class="container">
      <h2 class="text-center mb-5 fw-bold">Featured Products</h2>
      <div class="row g-4">
        <div class="col-md-4">
          <div class="card border-0 shadow text-center">
            <img src="redmi book.jpg" class="card-img-top" alt="Redmi Book">
            <div class="card-body">
              <h5 class="card-title fw-bold">Redmi Book</h5>
              <p class="card-text">Power meets productivity.</p>
              <a href="#" class="btn btn-dark">Buy</a>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card border-0 shadow text-center">
            <img src="vv.webp" class="card-img-top" alt="Redmi Pad SE">
            <div class="card-body">
              <h5 class="card-title fw-bold">Redmi Pad SE</h5>
              <p class="card-text">Entertainment on the go.</p>
              <a href="#" class="btn btn-dark">Buy</a>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card border-0 shadow text-center">
            <img src="redminote 13 pro+.jpg" class="card-img-top" alt="Redmi Note 13 Pro+">
            <div class="card-body">
              <h5 class="card-title fw-bold">Redmi Note 13 Pro+</h5>
              <p class="card-text">Flagship performance. Stunning design.</p>
              <a href="#" class="btn btn-dark">Buy</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="text-center">
    <p class="mb-0">© 2025 Redmi Clone. Designed for educational purposes.</p>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```
phones.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Redmi Phones</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"/>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Outfit', sans-serif;
      background-color: #f8f9fa;
      margin-top: 80px;
    }
    .card img {
      height: 250px;
      object-fit: cover;
    }
    .section-title {
      font-weight: 700;
    }
    footer {
      background-color: #000;
      color: #fff;
      padding: 20px 0;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg bg-dark navbar-dark fixed-top">
    <div class="container">
      <a class="navbar-brand" href="home.html">Redmi</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
        data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item"><a class="nav-link" href="home.html">Home</a></li>
          <li class="nav-item"><a class="nav-link active" href="phones.html">Phones</a></li>
          <li class="nav-item"><a class="nav-link" href="tablets.html">Tablets</a></li>
          <li class="nav-item"><a class="nav-link" href="tv.html">Smart TVs</a></li>
          <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Phone Listings -->
  <div class="container py-5">
    <h2 class="text-center mb-5 section-title">Explore Redmi Phones</h2>
    <div class="row g-4">
      <!-- Phone 1 -->
      <div class="col-md-4">
        <div class="card shadow border-0">
          <img src="ll.jpg" class="card-img-top" alt="Redmi Note 13 Pro+">
          <div class="card-body text-center">
            <h5 class="card-title fw-bold">Redmi Note 13 Pro+</h5>
            <p class="card-text">200MP camera | 120Hz AMOLED | MediaTek Dimensity 7200-Ultra</p>
            <a href="#" class="btn btn-dark">Buy Now</a>
          </div>
        </div>
      </div>

      <!-- Phone 2 -->
      <div class="col-md-4">
        <div class="card shadow border-0">
          <img src="12[[.jpg" class="card-img-top" alt="Redmi 12">
          <div class="card-body text-center">
            <h5 class="card-title fw-bold">Redmi 12</h5>
            <p class="card-text">Crystal Glass Design | 90Hz Display | Helio G88</p>
            <a href="#" class="btn btn-dark">Buy Now</a>
          </div>
        </div>
      </div>

      <!-- Phone 3 -->
      <div class="col-md-4">
        <div class="card shadow border-0">
          <img src="note12-.jpg" class="card-img-top" alt="Redmi Note 12 5G">
          <div class="card-body text-center">
            <h5 class="card-title fw-bold">Redmi Note 12 5G</h5>
            <p class="card-text">Snapdragon 4 Gen 1 | AMOLED display | 5G Ready</p>
            <a href="#" class="btn btn-dark">Buy Now</a>
          </div>
        </div>
      </div>

```
tablets.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Redmi Pad - Details</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"/>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Outfit', sans-serif;
      background-color: #f8f9fa;
      margin-top: 80px;
    }

    .product-image {
      width: 100%;
      max-height: 500px;
      object-fit: contain;
    }

    .price {
      font-size: 1.5rem;
      font-weight: 600;
      color: #dc3545;
    }

    footer {
      background-color: #000;
      color: #fff;
      padding: 20px 0;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg bg-dark navbar-dark fixed-top">
    <div class="container">
      <a class="navbar-brand" href="home.html">Redmi</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
        data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item"><a class="nav-link" href="home.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="phones.html">Phones</a></li>
          <li class="nav-item"><a class="nav-link active" href="tablets.html">Tablets</a></li>
          <li class="nav-item"><a class="nav-link" href="tv.html">Smart TVs</a></li>
          <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Tablet Details Section -->
  <div class="container py-5">
    <div class="row align-items-center g-5">
      <div class="col-md-6">
        <img src="tablet redmi.jpg" alt="Redmi Pad" class="product-image shadow-sm rounded">
      </div>
      <div class="col-md-6">
        <h1 class="fw-bold">Redmi Pad</h1>
        <p class="lead">Premium design, power-packed performance.</p>
        <p class="price">₹12,999</p>
        <ul class="list-group list-group-flush mb-4">
          <li class="list-group-item">📱 10.61" 2K Display, 90Hz refresh rate</li>
          <li class="list-group-item">⚡ MediaTek Helio G99 Octa-core Processor</li>
          <li class="list-group-item">🔋 8000mAh battery with 18W fast charging</li>
          <li class="list-group-item">🔊 Quad speakers with Dolby Atmos</li>
        </ul>
        <a href="#" class="btn btn-danger btn-lg">Buy Now</a>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="text-center">
    <p class="mb-0">© 2025 Redmi Clone. Designed for educational purposes.</p>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>

```
tv.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Redmi Smart TVs</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"/>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Outfit', sans-serif;
      background-color: #f8f9fa;
      margin-top: 80px;
    }

    .card img {
      height: 250px;
      object-fit: cover;
    }

    .section-title {
      font-weight: 700;
    }

    footer {
      background-color: #000;
      color: #fff;
      padding: 20px 0;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg bg-dark navbar-dark fixed-top">
    <div class="container">
      <a class="navbar-brand" href="home.html">Redmi</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
        data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item"><a class="nav-link" href="home.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="phones.html">Phones</a></li>
          <li class="nav-item"><a class="nav-link" href="tablets.html">Tablets</a></li>
          <li class="nav-item"><a class="nav-link active" href="tv.html">Smart TVs</a></li>
          <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Smart TVs Section -->
  <div class="container py-5">
    <h2 class="text-center mb-5 section-title">Explore Redmi Smart TVs</h2>
    <div class="row g-4">

      <!-- TV 1 -->
      <div class="col-md-4">
        <div class="card shadow border-0">
          <img src="tv 32.jpg" class="card-img-top" alt="Redmi Smart TV 32">
          <div class="card-body text-center">
            <h5 class="card-title fw-bold">Redmi Smart TV 32"</h5>
            <p class="card-text">HD Ready | 20W Speakers | Android TV 11</p>
            <a href="#" class="btn btn-dark">Buy Now</a>
          </div>
        </div>
      </div>

      <!-- TV 2 -->
      <div class="col-md-4">
        <div class="card shadow border-0">
          <img src="tv 43.webp" class="card-img-top" alt="Redmi Smart TV 43">
          <div class="card-body text-center">
            <h5 class="card-title fw-bold">Redmi Smart TV 43"</h5>
            <p class="card-text">Full HD | PatchWall | Dolby Audio</p>
            <a href="#" class="btn btn-dark">Buy Now</a>
          </div>
        </div>
      </div>

      <!-- TV 3 -->
      <div class="col-md-4">
        <div class="card shadow border-0">
          <img src="tv 50.jpg" class="card-img-top" alt="Redmi Smart TV 50 4K">
          <div class="card-body text-center">
            <h5 class="card-title fw-bold">Redmi Smart TV 50" 4K</h5>
            <p class="card-text">4K Ultra HD | Dolby Vision | DTS Virtual:X</p>
            <a href="#" class="btn btn-dark">Buy Now</a>
          </div>
        </div>
      </div>

      <!-- Add more TVs if needed -->

    </div>
  </div>

  <!-- Footer -->
  <footer class="text-center">
    <p class="mb-0">© 2025 Redmi Clone. Designed for educational purposes.</p>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>

```
contact.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Contact Us - Redmi</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"/>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Outfit', sans-serif;
      background-color: #f8f9fa;
      margin-top: 80px;
    }

    .form-control:focus {
      box-shadow: none;
      border-color: #dc3545;
    }

    .contact-info {
      background: #000;
      color: #fff;
      padding: 30px;
      border-radius: 8px;
    }

    footer {
      background-color: #000;
      color: #fff;
      padding: 20px 0;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg bg-dark navbar-dark fixed-top">
    <div class="container">
      <a class="navbar-brand" href="home.html">Redmi</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
        data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item"><a class="nav-link" href="home.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="phones.html">Phones</a></li>
          <li class="nav-item"><a class="nav-link" href="tablets.html">Tablets</a></li>
          <li class="nav-item"><a class="nav-link" href="tv.html">Smart TVs</a></li>
          <li class="nav-item"><a class="nav-link active" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Contact Section -->
  <div class="container py-5">
    <div class="row g-5">
      <div class="col-md-6">
        <h2 class="fw-bold mb-4">Get in Touch</h2>
        <form>
          <div class="mb-3">
            <label for="name" class="form-label">Your Name</label>
            <input type="text" id="name" class="form-control" placeholder="Enter your name" required>
          </div>
          <div class="mb-3">
            <label for="email" class="form-label">Your Email</label>
            <input type="email" id="email" class="form-control" placeholder="Enter your email" required>
          </div>
          <div class="mb-3">
            <label for="message" class="form-label">Message</label>
            <textarea id="message" class="form-control" rows="5" placeholder="Your message here..." required></textarea>
          </div>
          <button type="submit" class="btn btn-danger">Send Message</button>
        </form>
      </div>
      <div class="col-md-6">
        <div class="contact-info">
          <h4 class="fw-bold mb-3">Redmi Support</h4>
          <p><strong>Address:</strong> 123 Tech Avenue, Chennai, India</p>
          <p><strong>Email:</strong> support@redmi.in</p>
          <p><strong>Phone:</strong> +91 98765 43210</p>
          <hr class="my-4">
          <p>For product queries, warranty support, or service requests, feel free to reach out using the form or contact details above.</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="text-center">
    <p class="mb-0">© 2025 Redmi Clone. Designed for educational purposes.</p>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>

```

## OUTPUT:
![Screenshot 2025-05-19 175627](https://github.com/user-attachments/assets/7fb78cd0-b7a9-4b71-8f47-dfe05757ba34)
![Screenshot 2025-05-19 175632](https://github.com/user-attachments/assets/5eea58fd-a797-4a04-8b1e-da23c2b160f6)
![Screenshot 2025-05-19 175637](https://github.com/user-attachments/assets/e1990592-2246-4a35-8850-a329675d48b6)
![Screenshot 2025-05-19 175641](https://github.com/user-attachments/assets/ff350b2b-a2da-486f-86c0-4dd73c57d965)
![Screenshot 2025-05-19 175645](https://github.com/user-attachments/assets/a9546da0-7ce5-4eef-95df-76ad057979ab)
![Screenshot 2025-05-19 175649](https://github.com/user-attachments/assets/4c7856c5-dab2-4c84-ac53-4dbc61a74693)


## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
