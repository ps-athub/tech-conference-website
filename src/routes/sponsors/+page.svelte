<script>
    const sponsors = {
      gold: [
        { name: "Google", logo: "/images/google.png", link: "https://www.google.com" },
        { name: "Microsoft", logo: "/images/microsoft.png", link: "https://www.microsoft.com" },
        { name: "Apple", logo: "/images/apple.png", link: "https://www.apple.com" },
        { name: "Reliance Jio", logo: "/images/jio.png", link: "https://www.jio.com" }
      ],
      silver: [
        { name: "Amazon Web Services", logo: "/images/aws.png", link: "https://aws.amazon.com" },
        { name: "IBM", logo: "/images/ibm.png", link: "https://www.ibm.com" },
        { name: "HCL Technologies", logo: "/images/hcl.png", link: "https://www.hcltech.com" },
        { name: "Dell", logo: "/images/dell.png", link: "https://www.dell.com" }
      ],
      bronze: [
        { name: "TCS", logo: "/images/tcs.png", link: "https://www.tcs.com" },
        { name: "Wipro", logo: "/images/wipro.png", link: "https://www.wipro.com" },
        { name: "Infosys", logo: "/images/infosys.png", link: "https://www.infosys.com" },
        { name: "Tech Mahindra", logo: "/images/techmahindra.png", link: "https://www.techmahindra.com" }
      ]
    };
</script>

<div class="sponsors-section">
  <h2>Our Sponsors</h2>

  <div class="sponsor-category gold">
    <h3>🏆 Gold Sponsors</h3>
    <div class="sponsor-grid">
      {#each sponsors.gold as sponsor}
        <a href={sponsor.link} target="_blank" class="sponsor-card">
          <img src={sponsor.logo} alt={sponsor.name} />
          <p>{sponsor.name}</p>
        </a>
      {/each}
    </div>
  </div>

  <div class="sponsor-category silver">
    <h3>🥈 Silver Sponsors</h3>
    <div class="sponsor-grid">
      {#each sponsors.silver as sponsor}
        <a href={sponsor.link} target="_blank" class="sponsor-card">
          <img src={sponsor.logo} alt={sponsor.name} />
          <p>{sponsor.name}</p>
        </a>
      {/each}
    </div>
  </div>

  <div class="sponsor-category bronze">
    <h3>🥉 Bronze Sponsors</h3>
    <div class="sponsor-grid">
      {#each sponsors.bronze as sponsor}
        <a href={sponsor.link} target="_blank" class="sponsor-card">
          <img src={sponsor.logo} alt={sponsor.name} />
          <p>{sponsor.name}</p>
        </a>
      {/each}
    </div>
  </div>
</div>

<style>
  .sponsors-section {
    text-align: center;
    padding: 60px 20px;
    background-color: #f9f9f9;
  }

  .sponsors-section h2 {
    font-size: 2.5rem;
    font-weight: bold;
    margin-bottom: 30px;
  }

  .sponsor-category {
    margin-bottom: 50px;
    padding: 20px;
    border-radius: 10px;
  }

  .gold { background: linear-gradient(135deg, #ffd700, #ffcc00); }
  .silver { background: linear-gradient(135deg, #c0c0c0, #a8a8a8); }
  .bronze { background: linear-gradient(135deg, #cd7f32, #b87333); }

  .sponsor-category h3 {
    font-size: 1.8rem;
    color: white;
    padding: 15px 0;
    margin-bottom: 20px;
  }

  .sponsor-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 20px;
    justify-items: center;
    padding: 20px;
  }

  .sponsor-card {
    background: white;
    padding: 15px;
    border-radius: 10px;
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    text-decoration: none;
    color: black;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .sponsor-card img {
    width: 100px;
    height: auto;
    margin-bottom: 10px;
    transition: transform 0.3s ease;
  }

  .sponsor-card p {
    font-size: 1.1rem;
    font-weight: bold;
    margin: 0;
  }

  .sponsor-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }

  .sponsor-card:hover img {
    transform: scale(1.1);
  }
</style>
