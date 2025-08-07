[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/KWCswwQh)
# 🧠 Assignment: Interactive Web Pages with JavaScript

Welcome to the exciting world of interactivity! This assignment is all about **making your web pages feel alive**. You’ll learn how to respond to user actions, build engaging components, and validate form input—without reloading the page. This is where JavaScript gets fun, practical, and powerful. 🚀

---

## 🎉 Part 1: JavaScript Event Handling and Interactive Elements

Let’s start with the basics of **event handling**. You'll set up JavaScript to listen for user actions like clicks, mouseovers, keyboard input, and more—and respond to them in meaningful ways.

**Goal:** Use event listeners to react to user behavior and trigger changes on the page (e.g., showing messages, toggling classes, hiding/showing content).

---

## 🎮 Part 2: Building Interactive Elements

Now it’s time to apply what you’ve learned by creating your own mini interactive features. You can build things like:

* A light/dark mode toggle
* A counter or button game
* A collapsible FAQ section
* A simple dropdown menu
* A tabbed interface

**Goal:** Use DOM manipulation + events to make the page dynamic and engaging. Be creative!

---

## 📋✅ Part 3: Form Validation with JavaScript

Forms are essential to the web—and validating them properly is key to good user experience. You’ll build a form with multiple input fields (name, email, password, etc.) and write JavaScript to validate each field when the user submits or types.

**Goal:** Prevent incorrect form submissions by writing custom validation logic using conditions and regular expressions. Show user-friendly error messages and success feedback.

---

## Deliverables

* `index.html`: Your structured web page with at least one form and several interactive sections
* `script.js`: Your JavaScript file with:

  * Event handling for buttons, inputs, or links
  * At least 2 interactive features created from scratch
  * A fully functioning custom form validation (no HTML5-only validation)
* `style.css` (optional but encouraged): To style your interactive elements

Each section of your JavaScript should be commented to explain its purpose.

---

## Outcome

* Use of event listeners and appropriate event types
* Creativity and functionality of interactive elements
* Form validation accuracy and helpfulness of feedback
* Clear, modular, and well-commented JavaScript code
* A clean and functional user experience

index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive JavaScript Project</title>
    <link rel="stylesheet" href="style.css">
    <!-- Font Awesome for the expand/collapse icon -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>

    <div class="container">
        <h1>Interactive JavaScript Demo</h1>

        <!-- Part 1: Event Handling - Color Change Button -->
        <section class="section-card">
            <h2>Color Changer</h2>
            <p>Click the button to change its color randomly.</p>
            <button id="color-btn" class="interactive-btn">Change Color</button>
        </section>

        <!-- Part 2: Interactive Element - Collapsible FAQ -->
        <section class="section-card">
            <h2>FAQ Section</h2>
            <div class="faq-item">
                <button class="faq-toggle">
                    What is JavaScript?
                    <i class="fas fa-chevron-down icon"></i>
                </button>
                <div class="faq-answer">
                    <p>JavaScript is a programming language that makes webpages interactive. It's used for everything from simple animations to complex web applications.</p>
                </div>
            </div>

            <div class="faq-item">
                <button class="faq-toggle">
                    What is the DOM?
                    <i class="fas fa-chevron-down icon"></i>
                </button>
                <div class="faq-answer">
                    <p>The DOM (Document Object Model) is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content.</p>
                </div>
            </div>
        </section>

        <!-- Part 3: Form Validation -->
        <section class="section-card">
            <h2>User Registration</h2>
            <form id="registration-form">
                <div class="form-group">
                    <label for="name">Name:</label>
                    <input type="text" id="name" name="name">
                    <small class="error-message"></small>
                </div>
                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email">
                    <small class="error-message"></small>
                </div>
                <div class="form-group">
                    <label for="password">Password:</label>
                    <input type="password" id="password" name="password">
                    <small class="error-message"></small>
                </div>
                <button type="submit" class="interactive-btn">Register</button>
            </form>
            <div id="form-feedback"></div>
        </section>
    </div>

    <script src="script.js"></script>
</body>
</html>

styles.css

body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    background-color: #f0f2f5;
    color: #333;
    line-height: 1.6;
    margin: 0;
    padding: 20px;
}

.container {
    max-width: 800px;
    margin: auto;
    display: flex;
    flex-direction: column;
    gap: 30px;
}

.section-card {
    background-color: #fff;
    padding: 30px;
    border-radius: 10px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

h1, h2 {
    color: #1c1e21;
    text-align: center;
    margin-bottom: 20px;
}

p {
    text-align: center;
}

.interactive-btn {
    display: block;
    width: 100%;
    padding: 12px 20px;
    background-color: #4267b2;
    color: #fff;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
    transition: background-color 0.3s ease;
}

.interactive-btn:hover {
    background-color: #3b5998;
}

/* Part 2: Collapsible FAQ Styling */
.faq-item {
    border-bottom: 1px solid #dddfe2;
    margin-bottom: 10px;
}

.faq-toggle {
    width: 100%;
    text-align: left;
    background: none;
    border: none;
    padding: 15px 0;
    font-size: 18px;
    font-weight: bold;
    color: #1c1e21;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.faq-answer {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease-out;
}

.faq-answer p {
    padding: 15px 0;
    margin: 0;
    text-align: left;
}

.faq-item.active .faq-answer {
    max-height: 200px; /* A value large enough to accommodate the content */
    transition: max-height 0.4s ease-in;
}

.faq-item.active .icon {
    transform: rotate(180deg);
}

.faq-item .icon {
    transition: transform 0.3s ease;
}

/* Part 3: Form Styling */
.form-group {
    margin-bottom: 20px;
    text-align: left;
}

.form-group label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
}

.form-group input {
    width: 100%;
    padding: 12px;
    border: 1px solid #dddfe2;
    border-radius: 6px;
    font-size: 16px;
    box-sizing: border-box;
}

.form-group input.error {
    border-color: #fa3e3e;
}

.error-message {
    color: #fa3e3e;
    font-size: 12px;
    margin-top: 5px;
    display: none;
}

.form-group.error .error-message {
    display: block;
}

#form-feedback {
    margin-top: 20px;
    padding: 15px;
    border-radius: 6px;
    font-weight: bold;
    text-align: center;
}

.success {
    background-color: #e6f7e8;
    color: #38a169;
}

script.js

document.addEventListener('DOMContentLoaded', () => {

   
    const colorBtn = document.getElementById('color-btn');

    // Attach a click event listener to the button
    colorBtn.addEventListener('click', () => {
        // Generate a random color in hexadecimal format
        const randomColor = '#' + Math.floor(Math.random()*16777215).toString(16);
        
        // Change the button's background color dynamically
        colorBtn.style.backgroundColor = randomColor;
    });

    const faqToggles = document.querySelectorAll('.faq-toggle');

    // Iterate over each toggle button
    faqToggles.forEach(toggle => {
        // Attach a click event listener to each button
        toggle.addEventListener('click', () => {
            // Find the parent .faq-item element
            const faqItem = toggle.closest('.faq-item');
            // Toggle the 'active' class on the parent item.
            // This class will control the visibility of the answer via CSS.
            faqItem.classList.toggle('active');
        });
    });

    
    const form = document.getElementById('registration-form');
    const nameInput = document.getElementById('name');
    const emailInput = document.getElementById('email');
    const passwordInput = document.getElementById('password');
    const formFeedback = document.getElementById('form-feedback');

    // Add a 'submit' event listener to the form itself.
    // This allows us to intercept the submission before it goes to the server.
    form.addEventListener('submit', (e) => {
        // Prevent the form from submitting by default.
        e.preventDefault(); 

        // Run all validation functions and check if any of them failed.
        const isNameValid = validateName();
        const isEmailValid = validateEmail();
        const isPasswordValid = validatePassword();
        
        // If all fields are valid, show a success message.
        if (isNameValid && isEmailValid && isPasswordValid) {
            formFeedback.textContent = 'Registration successful!';
            formFeedback.classList.add('success');
            form.reset(); // Reset the form fields
        } else {
            // If validation failed, the individual error messages will be shown by
            // the validation functions themselves.
            formFeedback.textContent = 'Please fix the errors above.';
            formFeedback.classList.remove('success');
            formFeedback.style.color = '#fa3e3e';
            formFeedback.style.backgroundColor = 'rgba(250, 62, 62, 0.1)';
        }
    });

    
    function showError(input, message) {
        // Find the parent form-group element
        const formGroup = input.parentElement;
        // Add the 'error' class to show the error message.
        formGroup.classList.add('error');
        // Find the small element and set its text content to the error message.
        const errorText = formGroup.querySelector('.error-message');
        errorText.textContent = message;
    }

  
    function clearError(input) {
        // Find the parent form-group element
        const formGroup = input.parentElement;
        // Remove the 'error' class.
        formGroup.classList.remove('error');
        // Clear the error message text.
        const errorText = formGroup.querySelector('.error-message');
        errorText.textContent = '';
    }

 
    function validateName() {
        if (nameInput.value.trim() === '') {
            showError(nameInput, 'Name is required.');
            return false;
        } else {
            clearError(nameInput);
            return true;
        }
    }

  
    function validateEmail() {
        const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        if (emailInput.value.trim() === '') {
            showError(emailInput, 'Email is required.');
            return false;
        } else if (!emailRegex.test(emailInput.value.trim())) {
            showError(emailInput, 'Please enter a valid email address.');
            return false;
        } else {
            clearError(emailInput);
            return true;
        }
    }

 
    function validatePassword() {
        if (passwordInput.value.length < 8) {
            showError(passwordInput, 'Password must be at least 8 characters.');
            return false;
        } else {
            clearError(passwordInput);
            return true;
        }
    }
});
