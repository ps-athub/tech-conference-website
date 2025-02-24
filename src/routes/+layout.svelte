<script>
    import "bootstrap/dist/css/bootstrap.min.css"; // Import Bootstrap globally
    import "../styles/global.css"; // Custom CSS
    import Navbar from "../lib/Navbar.svelte"; // Import Navbar component
    import Footer from "../lib/Footer.svelte"; // Import Footer component
  </script>
  
  <Navbar />
  
  <!-- This ensures that the inner page content is displayed -->
  <slot />
  
  <Footer />
  