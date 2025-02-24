<script>
    import Countdown from "$lib/Countdown.svelte";
  
    const speakers = [
      { name: "Sundar Pichai", title: "CEO, Google", image: "/images/pichai.jpg" },
      { name: "Satya Nadella", title: "CEO, Microsoft", image: "/images/nadella.jpg" },
      { name: "Narayana Murthy", title: "Founder, Infosys", image: "/images/murthy.jpg" }
    ];
  </script>
  
  <div class="hero">
    <img src="/favicon.png" alt="India Tech Conference Logo" class="hero-logo" style="display: block; margin: 0 auto; width: 100px; height: auto; "/>
    <h1>India Tech Conference 2025</h1>
    <p>"Innovate, Connect, and Transform the Future of Technology"</p>
    <Countdown />
    <a href="/register" class="btn btn-primary mt-3" style="padding: 10px 20px; font-size: 1rem; border-radius: 5px;"> Register Now</a>
  </div>
  
  <!-- Featured Keynote Speakers Section -->
  <div class="speakers-section">
    <h2 class="section-title">Keynote Speakers</h2>
    <div class="speakers-grid">
      {#each speakers as speaker}
        <div class="speaker-card">
          <img src={speaker.image} alt={speaker.name} class="speaker-img" />
          <h3>{speaker.name}</h3>
          <p class="speaker-title">{speaker.title}</p>
        </div>
      {/each}
    </div>
  </div>
  
  <style>
    .hero {
      background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), 
                  url("/images/hero-background.jpg");
      background-size: cover;
      background-position: center;
      color: white;
      text-align: center;
      padding: 100px 20px;
    }
  
    .hero-logo {
      width: 120px;
      margin-bottom: 15px;
    }
  
    /* Keynote Speakers Section */
    .speakers-section {
      text-align: center;
      padding: 60px 20px;
      background: #f8f9fa;
    }
  
    .section-title {
      font-size: 2rem;
      margin-bottom: 20px;
    }
  
    .speakers-grid {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }
  
    .speaker-card {
      background: white;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      text-align: center;
      width: 250px;
    }
  
    .speaker-img {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 10px;
    }
  
    .speaker-title {
      font-weight: bold;
      color: #555;
    }
  </style>
  