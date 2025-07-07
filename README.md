# Wellcom-brothers-and-sisters-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Sale4u Flipkart Deals</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f3f4f6;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #2563eb;
      color: white;
      padding: 20px;
      text-align: center;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    main {
      max-width: 800px;
      margin: 30px auto;
      padding: 20px;
      background: white;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.05);
    }
    iframe {
      width: 100%;
      border-radius: 8px;
      margin-bottom: 20px;
    }
    h2 {
      font-size: 22px;
      margin-bottom: 10px;
    }
    .price {
      color: green;
      font-weight: bold;
    }
    .info {
      margin: 5px 0;
      color: #333;
    }
    .ratings {
      font-size: 14px;
      color: #777;
    }
    .btn {
      display: inline-block;
      padding: 10px 20px;
      border-radius: 5px;
      text-align: center;
      text-decoration: none;
      font-weight: bold;
      margin-top: 10px;
      cursor: pointer;
    }
    .btn-blue {
      background-color: #4f46e5;
      color: white;
    }
    .btn-blue:hover {
      background-color: #4338ca;
    }
    .btn-yellow {
      background-color: #f59e0b;
      color: white;
    }
    .btn-yellow:hover {
      background-color: #d97706;
    }
    .btn-green {
      background-color: #22c55e;
      color: white;
      width: 100%;
    }
    .btn-green:hover {
      background-color: #16a34a;
    }
    .form-container {
      margin-top: 30px;
      background: #f9fafb;
      padding: 20px;
      border: 1px solid #ddd;
      border-radius: 8px;
    }
    .form-group {
      margin-bottom: 15px;
    }
    label {
      font-weight: bold;
      display: block;
      margin-bottom: 5px;
    }
    input, textarea {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    footer {
      background: #1f2937;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 50px;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <h1>Sale4u - Flipkart Affiliate Deals</h1>
    <p>Top Verified Offers • 100% Secure Checkout</p>
  </header>

  <!-- Product Section -->
  <main>
    <!-- YouTube Video -->
    <iframe height="315" src="https://www.youtube.com/embed/lQJcAx68wYg?si=FdMEK7o1TWF4eSFA" 
      title="YouTube video player" frameborder="0" allowfullscreen></iframe>

    <!-- Product Info -->
    <h2>EVRGLOW EVR-001 Analog Watch - For Women</h2>
    <p class="price">85% Off - Now ₹220 <span style="text-decoration: line-through; color: gray;">(MRP ₹1499)</span></p>
    <p class="info">Color: Gold Strap, Green Dial</p>
    <p class="ratings">★ 4.0 | 8,453 Ratings</p>

    <!-- Button 1: Flipkart -->
    <a href="https://fktr.in/1mivEup" target="_blank" class="btn btn-blue">Buy Now on Flipkart</a>

    <!-- Button 2: Scroll to Form -->
    <div style="margin-top: 20px;">
      <p style="font-size: 14px; color: #555;">Want to order under ₹240 on website?</p>
      <button class="btn btn-yellow" onclick="scrollToForm()">Buy on Website under ₹240</button>
    </div>

    <!-- Form Container -->
    <div class="form-container" id="orderForm">
      <h3 style="text-align: center; color: #16a34a; margin-bottom: 15px;">Order via WhatsApp</h3>
      <form onsubmit="sendToWhatsApp(); return false;">
        <div class="form-group">
          <label for="name">Full Name</label>
          <input type="text" id="name" required />
        </div>
        <div class="form-group">
          <label for="mobile">Mobile Number</label>
          <input type="tel" id="mobile" required />
        </div>
        <div class="form-group">
          <label for="address">Delivery Address</label>
          <textarea id="address" rows="3" required></textarea>
        </div>
        <button type="submit" class="btn btn-green">Send Order via WhatsApp</button>
      </form>
      <p style="font-size: 12px; text-align: center; color: #666; margin-top: 10px;">We never share your information. 100% safe ordering on WhatsApp.</p>
    </div>
  </main>

  <!-- Footer -->
  <footer>
    &copy; 2025 Sale4u | Flipkart Affiliate Partner<br />
    All brand names are property of their respective owners.
  </footer>

  <!-- JavaScript -->
  <script>
    function sendToWhatsApp() {
      const name = document.getElementById("name").value.trim();
      const mobile = document.getElementById("mobile").value.trim();
      const address = document.getElementById("address").value.trim();

      if (!name || !mobile || !address) {
        alert("Please fill all fields.");
        return;
      }

      const message = `*New Order Details*%0A👤 *Name:* ${encodeURIComponent(name)}%0A📞 *Mobile:* ${encodeURIComponent(mobile)}%0A🏠 *Address:* ${encodeURIComponent(address)}`;
      const phoneNumber = "919667302392";
      const whatsappURL = `https://wa.me/${phoneNumber}?text=${message}`;
      window.open(whatsappURL, "_blank");

      // ✅ Confirmation message
      alert("✅ Your order form is ready! Please send it on WhatsApp.");
    }

    function scrollToForm() {
      document.getElementById("orderForm").scrollIntoView({ behavior: "smooth" });
    }
  </script>

</body>
</html>
