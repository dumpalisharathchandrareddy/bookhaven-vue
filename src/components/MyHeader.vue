<template>
    <div class="tophead">
      <h1 class="appName">{{ appName }}</h1>
      <h2 class="Welcome">Welcome to Book Haven</h2>
      <h1 class="apptagline">DISCOVER YOUR NEXT FAV READ TO HEART</h1>
  
      <!-- Nav Bar -->
      <!-- Took reference from W3 schools menu bar creation -->
      <div class="nav-bar">
        <ul class="nav">
          <li class="nav-item"><a href="#home">Home</a></li>
          <li class="nav-item"><a href="#genre">Genre</a></li>
          <li class="nav-item"><a href="#bestsellers">Best Sellers</a></li>
          <li class="nav-item"><a href="#contact">Contact</a></li>

          <!-- Menu icon -->
          <li class="icon-menu" @click="toggleMenu">
            <div class="bar1"></div>
            <div class="bar2"></div>
            <div class="bar3"></div>
          </li>
        </ul>
        <!-- Dropdown for Hidden Items (Visible Only on Small Screens) -->
        <div class="dropdown" :class="{ show: isMenuVisible }">
          <a href="#bestsellers">Best Sellers</a>
          <a href="#contact">Contact</a>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "MyHeader",
    props: {
      appName: String,
    },
    data() {
      return {
        isMenuVisible: false, // Tracks the visibility of the dropdown menu
      };
    },
    methods: {
      toggleMenu() {
        this.isMenuVisible = !this.isMenuVisible; // Toggle dropdown menu visibility
      },
    },
  };
  </script>
  
  <style scoped>
  div {
    text-align: center;
  }
  
  .tophead {
    text-align: center;
    padding: 2rem;
    margin: 0.5rem 0;
    background: linear-gradient(135deg, #1b9a92, #103dc2);
    border-radius: 8px;
    box-shadow: 0 4px 6px #0000001a;
    color: #FFF;
  }
  
  .appName {
    padding: 1rem 0;
    margin: 0.5rem 0;
    background-color: rgba(255, 255, 255, 0.2);
    color: #FFF;
    border-radius: 5px;
    font-size: 2.5rem;
    letter-spacing: 3px;
    font-weight: bold;
  }
  
  .Welcome {
    color: #FFF;
    font-size: 1.5rem;
    margin: 0.5rem 0;
    letter-spacing: 1px;
    text-decoration: underline;
  }
  
  .apptagline {
    color: #FFF;
    font-size: 1.75rem;
    margin-top: 1rem;
    font-style: italic;
  }
  
  .nav-bar {
    margin-top: 1.5rem;
    background-color: rgba(255, 255, 255, 0.1);
    padding: 0.5rem 1rem;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    position: relative; /* For dropdown positioning */
  }
  
  .nav {
    list-style: none;
    display: grid;
    grid-template-columns: repeat(4, auto); /* All items visible */
    align-items: center;
    justify-content: center;
    padding: 0;
    margin: 0;
  }
  
  .nav-bar li {
    margin: 0 1rem;
  }
  
  .nav-bar a {
    text-decoration: none;
    color: #ffffff;
    font-size: 1rem;
    font-weight: bold;
    padding: 0.5rem 1rem;
    border-radius: 5px;
  }
  
  .nav-bar a:hover {
    background-color: rgba(255, 255, 255, 0.2);
    color: #ffdd45;
  }
  
  /* Menu Icon Styling */
  .icon-menu {
    cursor: pointer;
    display: none; /* Hidden on larger screens */
  }
  
  .bar1, .bar2, .bar3 {
    width: 25px;
    height: 3px;
    background-color: white;
    margin: 3px 0;
    transition: 0.4s;
  }
  
  /* Dropdown Menu */
  .dropdown {
    display: none;
    position: absolute;
    top: 100%;
    right: 0;
    background-color: #444;
    padding: 10px;
    border-radius: 5px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    z-index: 10;
  }
  
  .dropdown a {
    color: white;
    padding: 10px;
    text-decoration: none;
    display: block;
  }
  
  .dropdown a:hover {
    background-color: #555;
  }
  .dropdown.show {
    display: grid;
  }
  
  /* Responsive Design */
  @media screen and (max-width: 680px) {
    .appName {
      font-size: 1.5rem;
    }
  
    .Welcome {
      font-size: 1rem;
    }
  
    .apptagline {
      font-size: 0.75rem;
    }
  
    .nav {
      grid-template-columns: repeat(3, auto); /* Home, Genre, and Menu Icon */
    }
  
    .icon-menu {
      display: grid; 
      justify-items: center;
    }
  
    /* Hide normal nav items on small screens */
    .nav .nav-item:nth-child(n+3) {
    display: none; /* Hide items after first two */
  }
  
    .dropdown {
      display: none;
    }
  }
  </style>
  