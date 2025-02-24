<div class="contact-container">
    <h1>Contact Us</h1>
    <p>Have questions or need more information? Feel free to reach out to us.</p>

    <form class="contact-form">
        <div class="input-group">
            <input type="text" class="form-control" placeholder="Your Name" required />
        </div>
        
        <div class="input-group">
            <input type="email" class="form-control" placeholder="Your Email" required />
        </div>
        
        <div class="input-group">
            <textarea class="form-control" placeholder="Your Message" rows="5" required></textarea>
        </div>
        
        <button type="submit" class="btn-submit">Send Message</button>
    </form>
</div>

<style>
  /* Contact Section Styling */
  .contact-container {
    max-width: 700px;
    margin: 50px auto;
    padding: 40px;
    background: #ffffff;
    border-radius: 12px;
    box-shadow: 0px 5px 20px rgba(0, 0, 0, 0.1);
    text-align: center;
  }

  .contact-container h1 {
    font-size: 2rem;
    margin-bottom: 10px;
    color: #333;
  }

  .contact-container p {
    font-size: 1.1rem;
    color: #666;
    margin-bottom: 20px;
  }

  .contact-form {
    display: flex;
    flex-direction: column;
    gap: 15px;
  }

  .input-group {
    position: relative;
  }

  .form-control {
    width: 100%;
    padding: 12px 15px;
    font-size: 1rem;
    border: 1px solid #ccc;
    border-radius: 8px;
    transition: border 0.3s ease-in-out;
  }

  .form-control:focus {
    border-color: #007bff;
    outline: none;
    box-shadow: 0px 0px 8px rgba(0, 123, 255, 0.2);
  }

  .btn-submit {
    background: #007bff;
    color: white;
    border: none;
    padding: 12px 18px;
    font-size: 1rem;
    font-weight: bold;
    border-radius: 8px;
    cursor: pointer;
    transition: background 0.3s ease-in-out;
  }

  .btn-submit:hover {
    background: #0056b3;
  }

  /* Responsive Design */
  @media (max-width: 768px) {
    .contact-container {
      padding: 30px;
    }
  }
</style>
