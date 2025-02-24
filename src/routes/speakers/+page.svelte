<script>
    const speakers = [
      { name: "Narayana Murthy", title: "Founder, Infosys", image: "/images/murthy.jpg", bio: "Pioneering entrepreneur who transformed Infosys into a global IT leader." },
      { name: "Sundar Pichai", title: "CEO, Google", image: "/images/pichai.jpg", bio: "Leading Google’s innovation in AI, cloud, and search technologies." },
      { name: "Nandan Nilekani", title: "Co-founder, Aadhaar & Infosys", image: "/images/nilekani.jpg", bio: "Driving India's digital transformation through Aadhaar and fintech innovations." },
      { name: "Kiran Mazumdar-Shaw", title: "Founder, Biocon", image: "/images/kiran.jpg", bio: "India’s biotech leader, focusing on affordable healthcare innovations." },
      { name: "Dr. Vishal Sikka", title: "Former CEO, Infosys", image: "/images/sikka.jpg", bio: "AI researcher and tech entrepreneur focused on business transformation." },
      { name: "Satya Nadella", title: "CEO, Microsoft", image: "/images/nadella.jpg", bio: "Transforming Microsoft into a cloud-first AI-driven company." }
    ];
  </script>
  
  <div class="container py-5">
    <h2 class="text-center mb-4">Meet Our Keynote Speakers</h2>
    <div class="row">
      {#each speakers as speaker}
        <div class="col-md-4 text-center">
          <img src={speaker.image} alt={speaker.name} class="speaker-img">
          <h4>{speaker.name}</h4>
          <p><strong>{speaker.title}</strong></p>
          <p>{speaker.bio}</p>
        </div>
      {/each}
    </div>
  </div>
  
  <style>
    .speaker-img {
      width: 150px;
      height: 150px;
      object-fit: cover;
      border-radius: 50%;
      margin-bottom: 10px;
    }
  </style>