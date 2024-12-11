<template>
  <footer class="footer">  <!-- footer class -->
      <div class="footer-content">
        <p class="contact-info">
          <strong>Contact Us:</strong> 
          <a href="mailto:sharath@bookhaven.com">sharath@bookhaven.com</a>

        </p>
        <p>&copy; 2024 Book Haven. All Rights Reserved.</p>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: "MyFooter",
  };
  </script>
  
  <style scoped>
  .footer {
    background-color: #324c62;
    color: white;
    padding: 20px;
    text-align: center;
    position: relative;
    bottom: 0;
    width: 100%;
    font-size: 14px;
    height: 5rem;
  }
  
  .footer-content {
    max-width: 1200px;
    margin: 0 auto;
  }
  
  .contact-info {
    margin: 5px 0;
  }
  
  .contact-info a {
    color: #ffffff;
    text-decoration: none;
  }
  
  .contact-info a:hover {
    text-decoration: underline;
  }
  </style>
  