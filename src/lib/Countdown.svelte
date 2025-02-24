<script>
    import { onMount } from "svelte";
  
    let days = 0, hours = 0, minutes = 0, seconds = 0;
    const eventDate = new Date("2025-06-15T09:00:00").getTime(); // Set event date
  
    function updateCountdown() {
      const now = new Date().getTime();
      const timeLeft = eventDate - now;
  
      if (timeLeft > 0) {
        days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
        hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
        seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
      } else {
        days = hours = minutes = seconds = 0;
      }
    }
  
    onMount(() => {
      updateCountdown();
      const interval = setInterval(updateCountdown, 1000);
      return () => clearInterval(interval); // Cleanup on unmount
    });
  </script>
  
  <div class="countdown text-center">
    <h3>Countdown to Event:</h3>
    <p class="display-4">{days}d {hours}h {minutes}m {seconds}s</p>
  </div>
  