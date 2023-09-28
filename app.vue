<template>
  <div>
    <header>
      <nav>
        <ul>
          <li><router-link to="/">Home</router-link></li>
          <li><router-link to="/about">About</router-link></li>
          <li><router-link to="/contact">Contact</router-link></li>
        </ul>
      </nav>
    </header>

    <main>
      <div id="app">
        <!-- Mount the Vue 3 component here -->
        <my-vue-component></my-vue-component>
      </div>

      <!-- Home Section -->
      <section class="home-section">
        <h1>Welcome to Vue 3 App</h1>
        <p>Experience the power of Vue 3 and the Composition API in building dynamic web applications. Our app showcases various Vue features.</p>
      </section>

      <!-- Features Section -->
      <section class="features-section">
        <h2>Key Features</h2>
        <ul>
          <li>Reactive data binding using Vue 3</li>
          <li>Component-based architecture</li>
          <li>Single File Components (SFC)</li>
          <li>Routing with Vue Router</li>
          <li>Form handling with Vue Forms</li>
        </ul>
      </section>

      <!-- About Section -->
      <section class="about-section">
        <h2>About Us</h2>
        <p>We are a passionate team of developers dedicated to creating amazing web experiences. Our Vue 3 app is a showcase of our skills and commitment to modern web development.</p>
      </section>

      <!-- Contact Section -->
      <section class="contact-section">
        <h2>Contact Us</h2>
        <p>If you have any questions or would like to get in touch with us, feel free to reach out:</p>
        <ul>
          <li>Email: <a href="mailto:contact@example.com">jijincherianjose@gmail.com</a></li>
          <li>Phone: +61413209640</li>
          <li>Address: Geelong, Australia</li>
        </ul>
      </section>
    </main>

    <footer>
      <p>&copy; 2023 Cj. All rights reserved.</p>
      <p>Contact us at <a href="mailto:contact@example.com">jijincherianjose@gmail.com</a></p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style scoped>
/* Include your CSS styles here */
/* Reset some default styles */
body, h1, h2, h3, p, ul, li {
    margin: 0;
    padding: 0;
  }
  
  /* Set a background color and font for the entire page */
  body {
    font-family: 'Helvetica Neue', sans-serif;
    background-color: #f4f4f4;
    color: #333;
    line-height: 1.6;
  }
  
  /* Style the header with a background color, padding, and a navigation bar */
  header {
    background-color: #333;
    color: #fff;
    padding: 1rem 0;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  /* Style the navigation menu with a list and links */
  nav ul {
    list-style: none;
    text-align: center;
    padding: 10px;
  }
  
  nav ul li {
    display: inline;
    margin-right: 20px;
  }
  
  nav a {
    text-decoration: none;
    color: #fff;
    font-weight: bold;
    font-size: 16px;
  }
  
  /* Style the main content area with padding and a light background */
  main {
    padding: 2rem;
    background-color: #fff;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  /* Style sections with padding and a border */
  section {
    padding: 1.5rem;
    border: 1px solid #ccc;
    margin-bottom: 1.5rem;
    background-color: #fff;
    border-radius: 5px;
  }
  
  /* Style headings */
  h1, h2, h3 {
    color: #333;
    margin-bottom: 10px;
  }
  
  /* Style the footer with a background color and padding */
  footer {
    background-color: #333;
    color: #fff;
    padding: 1rem 0;
    text-align: center;
  }
  
  /* Style links in the footer */
  footer a {
    color: #fff;
    text-decoration: none;
    font-weight: bold;
  }
  
  /* Add hover effect to navigation links */
  nav a:hover {
    text-decoration: underline;
  }
  
  /* Style the key features list */
  .features-section ul {
    list-style-type: disc;
    margin-left: 20px;
  }
  
  /* Add a border radius to sections */
  section {
    border-radius: 5px;
  }
  
  /* Style buttons */
  button {
    background-color: #007bff;
    color: #fff;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    transition: background-color 0.3s ease;
  }
  
  /* Add a hover effect to buttons */
  button:hover {
    background-color: #0056b3;
  }
  
  /* Style links */
  a {
    color: #007bff;
    text-decoration: none;
    font-weight: bold;
  }
  
  /* Add hover effect to links */
  a:hover {
    text-decoration: underline;
  }
  
  /* Style the main content area */
  #app {
    max-width: 800px;
    margin: 0 auto;
  }
</style>
