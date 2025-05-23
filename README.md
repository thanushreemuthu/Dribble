# Project Responsive Web Design using Bootstrap
## Date:19-05-2025

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
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Dribbble</title>
    
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        
        .navbar {
            background-color: black;
        }
        
        .navbar-brand {
            font-weight: 700;
            color: white !important;
        }
        
        .nav-link {
            color: rgba(255, 255, 255, 0.85) !important;
        }
        
        .nav-link:hover {
            color: white !important;
        }
        
        .hero-section {
            background-color: #f5f5f5;
            padding: 100px 0;
            text-align: center;
        }
        
        .shot-card {
            border-radius: 8px;
            overflow: hidden;
            margin-bottom: 20px;
            transition: transform 0.3s ease;
            border: none;
        }
        
        .shot-card:hover {
            transform: translateY(-5px);
        }
        
        .shot-image {
            height: 200px;
            object-fit: cover;
            width: 100%;
        }
        
        .user-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            object-fit: cover;
        }
        
        .section-title {
            font-weight: 700;
            margin-bottom: 40px;
            position: relative;
            display: inline-block;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            width: 50%;
            height: 3px;
            background-color: black;
            bottom: -10px;
            left: 25%;
        }
        
        footer {
            background-color: #333;
            color: white;
            padding: 30px 0;
            margin-top: 50px;
        }
        
        .btn-primary {
            background-color: black;
            border-color: black;
        }
        
        .btn-primary:hover {
            background-color:black;
            border-color: black;
        }
        
        .btn-outline-primary {
            color:black;
            border-color: black;
        }
        
        .btn-outline-primary:hover {
            background-color: black;
            border-color: black;
        }
        
        
        .auth-modal .modal-content {
            border-radius: 10px;
            border: none;
        }
        
        .auth-modal .modal-header {
            border-bottom: none;
            padding-bottom: 0;
        }
        
        .auth-modal .modal-body {
            padding-top: 0;
        }
        
        .auth-modal .form-control {
            padding: 12px 15px;
            margin-bottom: 15px;
        }
        
        .auth-modal .btn-submit {
            padding: 12px;
            font-weight: 600;
        }
        
        .auth-toggle {
            text-align: center;
            margin-top: 20px;
        }
        
        .auth-toggle a {
            color: black;
            font-weight: 600;
            text-decoration: none;
        }
    </style>
</head>
<body>
   
    <nav class="navbar navbar-expand-lg navbar-dark sticky-top">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="fas fa-basketball-ball me-2"></i>Dribbble
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Inspiration</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Find Work</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Learn Design</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Go Pro</a>
                    </li>
                    <li class="nav-item ms-lg-3 mt-2 mt-lg-0">
                        <button class="btn btn-outline-light btn-sm" data-bs-toggle="modal" data-bs-target="#signinModal">Sign in</button>
                    </li>
                    <li class="nav-item ms-lg-2 mt-2 mt-lg-0">
                        <button class="btn btn-light btn-sm" data-bs-toggle="modal" data-bs-target="#signupModal">Sign up</button>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    
    <div class="modal fade auth-modal" id="signinModal" tabindex="-1" aria-labelledby="signinModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="signinModalLabel">Sign In to Dribbble</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="signinForm">
                        <div class="mb-3">
                            <label for="signinUsername" class="form-label">Username or Email</label>
                            <input type="text" class="form-control" id="signinUsername" placeholder="Enter your username or email" required>
                        </div>
                        <div class="mb-3">
                            <label for="signinPassword" class="form-label">Password</label>
                            <input type="password" class="form-control" id="signinPassword" placeholder="Enter your password" required>
                        </div>
                        <div class="mb-3 form-check">
                            <input type="checkbox" class="form-check-input" id="rememberMe">
                            <label class="form-check-label" for="rememberMe">Remember me</label>
                            <a href="#" class="float-end">Forgot password?</a>
                        </div>
                        <button type="submit" class="btn btn-primary w-100 btn-submit">Sign In</button>
                    </form>
                    <div class="auth-toggle">
                        <p>Don't have an account? <a href="#" data-bs-toggle="modal" data-bs-target="#signupModal" data-bs-dismiss="modal">Sign up</a></p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    
    <div class="modal fade auth-modal" id="signupModal" tabindex="-1" aria-labelledby="signupModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="signupModalLabel">Join Dribbble</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="signupForm">
                        <div class="row">
                            <div class="col-md-6 mb-3">
                                <label for="firstName" class="form-label">First Name</label>
                                <input type="text" class="form-control" id="firstName" placeholder="First name" required>
                            </div>
                            <div class="col-md-6 mb-3">
                                <label for="lastName" class="form-label">Last Name</label>
                                <input type="text" class="form-control" id="lastName" placeholder="Last name" required>
                            </div>
                        </div>
                        <div class="mb-3">
                            <label for="signupUsername" class="form-label">Username</label>
                            <input type="text" class="form-control" id="signupUsername" placeholder="Choose a username" required>
                        </div>
                        <div class="mb-3">
                            <label for="signupEmail" class="form-label">Email</label>
                            <input type="email" class="form-control" id="signupEmail" placeholder="Enter your email" required>
                        </div>
                        <div class="mb-3">
                            <label for="signupPassword" class="form-label">Password</label>
                            <input type="password" class="form-control" id="signupPassword" placeholder="Create a password (min 8 characters)" required minlength="8">
                        </div>
                        <div class="mb-3">
                            <label for="dateOfBirth" class="form-label">Date of Birth</label>
                            <input type="date" class="form-control" id="dateOfBirth" required>
                        </div>
                        <div class="mb-3">
                            <label for="phoneNumber" class="form-label">Phone Number</label>
                            <input type="tel" class="form-control" id="phoneNumber" placeholder="Enter your phone number">
                        </div>
                        <div class="mb-3 form-check">
                            <input type="checkbox" class="form-check-input" id="termsAgreement" required>
                            <label class="form-check-label" for="termsAgreement">I agree to the <a href="#">Terms of Service</a> and <a href="#">Privacy Policy</a></label>
                        </div>
                        <button type="submit" class="btn btn-primary w-100 btn-submit">Create Account</button>
                    </form>
                    <div class="auth-toggle">
                        <p>Already have an account? <a href="#" data-bs-toggle="modal" data-bs-target="#signinModal" data-bs-dismiss="modal">Sign in</a></p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    
    <section class="hero-section">
        <div class="container">
            <h1 class="display-4 fw-bold mb-4">Discover the world's top designers & creatives</h1>
            <p class="lead mb-5">Shots is the leading destination to find & showcase creative work and home to the world's best design professionals.</p>
            <button class="btn btn-primary btn-lg px-4 me-2" data-bs-toggle="modal" data-bs-target="#signupModal">Sign up</button>
            <a href="#" class="btn btn-outline-primary btn-lg px-4">Learn more</a>
        </div>
    </section>

    
    <section class="py-5">
        <div class="container">
            <h2 class="text-center section-title">Popular Shots</h2>
            <div class="row">
                <div class="col-md-6 col-lg-3">
                    <div class="card shot-card shadow-sm">
                        <img src="download (1).jpeg" class="shot-image" alt="Design shot">
                        <div class="card-body">
                            <div class="d-flex align-items-center">
                                <img src="rafiz.webp" class="user-avatar me-2" alt="User">
                                <div>
                                    <h6 class="mb-0">Rafiz studio</h6>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-lg-3">
                    <div class="card shot-card shadow-sm">
                        <img src="download.png" class="shot-image" alt="Illustration">
                        <div class="card-body">
                            <div class="d-flex align-items-center">
                                <img src="threedee.webp" class="user-avatar me-2" alt="User">
                                <div>
                                    <h6 class="mb-0">ThreeDee</h6>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-lg-3">
                    <div class="card shot-card shadow-sm">
                        <img src="brand.jpeg" class="shot-image" alt="Branding">
                        <div class="card-body">
                            <div class="d-flex align-items-center">
                                <img src="nixito.gif" class="user-avatar me-2" alt="User">
                                <div>
                                    <h6 class="mb-0">Nixito</h6>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-lg-3">
                    <div class="card shot-card shadow-sm">
                        <img src="logo.jpeg" class="shot-image" alt="Branding">
                        <div class="card-body">
                            <div class="d-flex align-items-center">
                                <img src="ziko.webp" class="user-avatar me-2" alt="User">
                                <div>
                                    <h6 class="mb-0">ziko</h6>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-lg-3">
                    <div class="card shot-card shadow-sm">
                        <img src="app.jpeg" class="shot-image" alt="Mobile App">
                        <div class="card-body">
                            <div class="d-flex align-items-center">
                                <img src="showit.webp" class="user-avatar me-2" alt="User">
                                <div>
                                    <h6 class="mb-0">showit</h6>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    
    <section class="py-5">
        <div class="container text-center">
            <h2 class="mb-4">Ready to showcase your creative work?</h2>
            <p class="lead mb-4">Join the world's leading community for creatives</p>
            <button class="btn btn-primary btn-lg px-5" data-bs-toggle="modal" data-bs-target="#signupModal">Get Started</button>
        </div>
    </section>

   
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-md-3 mb-4 mb-md-0">
                    <h5><i class="fas fa-basketball-ball me-2"></i>Dribbble</h5>
                    <p>A Dribbble-inspired platform for designers to showcase their work.</p>
                </div>
                <div class="col-md-3 mb-4 mb-md-0">
                    <h5>For Designers</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="text-white">Go Pro</a></li>
                        <li><a href="#" class="text-white">Explore work</a></li>
                        <li><a href="#" class="text-white">Design blog</a></li>
                    </ul>
                </div>
                <div class="col-md-3 mb-4 mb-md-0">
                    <h5>Hire Designers</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="text-white">Post a job</a></li>
                        <li><a href="#" class="text-white">Search designers</a></li>
                    </ul>
                </div>
                <div class="col-md-3">
                    <h5>Company</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="text-white">About</a></li>
                        <li><a href="#" class="text-white">Careers</a></li>
                        <li><a href="#" class="text-white">Support</a></li>
                    </ul>
                </div>
            </div>
            <hr class="my-4 bg-secondary">
            <div class="row">
                <div class="col-md-6">
                    <p class="mb-0">&copy; All rights reserved</p>
                </div>
                <div class="col-md-6 text-md-end">
                    <p class="mb-0">Created by <strong>S.Dhamini</strong></p>
                </div>
            </div>
        </div>
    </footer>

    
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    
    
    <script>
        
        document.getElementById('signinForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const username = document.getElementById('signinUsername').value;
            const password = document.getElementById('signinPassword').value;
            const rememberMe = document.getElementById('rememberMe').checked;
            
            // Here you would typically send this data to your server
            console.log('Sign In Attempt:', { username, password, rememberMe });
            
            // For demo purposes, just show an alert
            alert('Sign In functionality would be implemented here.\n\nUsername: ' + username + '\nPassword: ' + password);
            
            // Close the modal
            const signinModal = bootstrap.Modal.getInstance(document.getElementById('signinModal'));
            signinModal.hide();
        });
        
        // Sign Up Form Handling
        document.getElementById('signupForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const firstName = document.getElementById('firstName').value;
            const lastName = document.getElementById('lastName').value;
            const username = document.getElementById('signupUsername').value;
            const email = document.getElementById('signupEmail').value;
            const password = document.getElementById('signupPassword').value;
            const dob = document.getElementById('dateOfBirth').value;
            const phone = document.getElementById('phoneNumber').value;
            
            // Here you would typically send this data to your server
            console.log('Sign Up Attempt:', { 
                firstName, 
                lastName, 
                username, 
                email, 
                password, 
                dob, 
                phone 
            });
            
            // For demo purposes, just show an alert
            alert('Sign Up functionality would be implemented here.\n\nName: ' + firstName + ' ' + lastName + 
                  '\nUsername: ' + username + '\nEmail: ' + email + '\nDOB: ' + dob + '\nPhone: ' + phone);
            
            // Close the modal
            const signupModal = bootstrap.Modal.getInstance(document.getElementById('signupModal'));
            signupModal.hide();
        });
        
        // Toggle between sign in and sign up modals
        document.querySelectorAll('[data-bs-toggle="modal"]').forEach(button => {
            button.addEventListener('click', function() {
                const targetModal = this.getAttribute('data-bs-target');
                const currentModal = this.closest('.modal').id;
                
                if (targetModal && currentModal) {
                    const currentModalInstance = bootstrap.Modal.getInstance(document.getElementById(currentModal));
                    const targetModalInstance = new bootstrap.Modal(document.querySelector(targetModal));
                    
                    currentModalInstance.hide();
                    targetModalInstance.show();
                }
            });
        });
    </script>
</body>
</html>
```
## OUTPUT:
![alt text](dhamini/dhamini/static/1.png)
![alt text](dhamini/dhamini/static/2.png)
![alt text](dhamini/dhamini/static/3.png)


## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
