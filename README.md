<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Sale4u Flipkart Deals</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 font-sans">

  <!-- Header -->
  <header class="bg-blue-600 text-white py-4 shadow">
    <div class="max-w-7xl mx-auto px-4 text-center">
      <h1 class="text-3xl font-bold">Sale4u - Flipkart Affiliate Deals</h1>
      <p class="text-sm mt-1">Top Verified Offers • 100% Secure Checkout</p>
    </div>
  </header>

  <!-- Product Section -->
  <main class="max-w-4xl mx-auto py-10 px-4">
    <div class="bg-white rounded-2xl shadow-lg p-6">

      <!-- Product Image -->
      <div class="w-full flex justify-center mb-6">
        <img src="https://chat.openai.com/cdn-cgi/imagedelivery/0bLEkZyPp1jPE_7zRJpQzw/s-442906536/public" alt="Stylish Sneakers" class="w-72 rounded-xl shadow-md" />
      </div>

      <!-- Product Details -->
      <h2 class="text-2xl font-bold text-gray-800 mb-2 text-center">Stylish Casual Sneakers for Men</h2>
      <p class="text-green-600 text-center font-semibold text-lg">28% Off - Now ₹500 <span class="line-through text-gray-400 text-sm">(MRP ₹700)</span></p>
      <p class="text-gray-700 text-center mt-2">Product delivered by <span class="font-semibold text-blue-600">Flipkart Group</span></p>
      <p class="text-sm text-center text-gray-600 mt-1">📦 Estimated Delivery: 3–5 Days</p>
      <p class="text-sm text-center text-gray-600 mt-1">🔁 Replace in 4 Days</p>

      <!-- Order Form -->
      <div class="mt-8 bg-yellow-50 border border-yellow-300 rounded-xl p-6">
        <h3 class="text-xl font-semibold text-yellow-600 mb-4 text-center">Order Now Form</h3>

        <form onsubmit="sendToWhatsApp(); return false;">
          <div class="mb-4">
            <label for="name" class="block text-gray-700 font-medium mb-1">Full Name</label>
            <input type="text" id="name"
                   class="w-full border border-gray-300 p-2 rounded focus:outline-none focus:ring-2 focus:ring-yellow-400"
                   required />
          </div>

          <div class="mb-4">
            <label for="mobile" class="block text-gray-700 font-medium mb-1">Mobile Number</label>
            <input type="tel" id="mobile"
                   class="w-full border border-gray-300 p-2 rounded focus:outline-none focus:ring-2 focus:ring-yellow-400"
                   required />
          </div>

          <div class="mb-4">
            <label for="address" class="block text-gray-700 font-medium mb-1">Delivery Address</label>
            <textarea id="address" rows="3"
                      class="w-full border border-gray-300 p-2 rounded focus:outline-none focus:ring-2 focus:ring-yellow-400"
                      required></textarea>
          </div>

          <!-- Payment Options -->
          <div class="mb-6">
            <label class="block text-gray-700 font-medium mb-2">Payment Option</label>
            <div class="flex gap-4">
              <label class="flex items-center">
                <input type="radio" name="payment" value="Cash on Delivery" class="mr-2" checked onchange="toggleQRCode()" />
                Cash on Delivery
              </label>
              <label class="flex items-center">
                <input type="radio" name="payment" value="Pay Now" class="mr-2" onchange="toggleQRCode()" />
                Pay Now
              </label>
            </div>
          </div>

          <!-- Pay Now QR Code -->
          <div id="qrSection" class="hidden mb-6 text-center">
            <p class="text-sm text-gray-700 mb-2 font-medium">Scan this UPI QR to Pay Now</p>
            <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=upi://pay?pa=9667302392-2@ybl&pn=Sale4u%20Flipkart%20Deals&am=500" alt="Pay Now QR Code" class="w-40 mx-auto rounded-lg border" />
            <p class="text-xs text-gray-500 mt-1">After payment, complete the form and place your order.</p>
          </div>

          <button type="submit"
                  class="bg-yellow-500 text-white w-full py-2 rounded hover:bg-yellow-600 transition duration-200">
            Send Order via WhatsApp
          </button>
        </form>

        <p class="text-xs text-center text-gray-500 mt-4">We never share your information. 100% safe ordering on WhatsApp.</p>
      </div>
    </div>
  </main>

  <!-- Footer -->
  <footer class="bg-gray-800 text-white text-center py-4 mt-10 rounded-t-lg">
    <p class="text-sm">&copy; 2025 Sale4u | Flipkart Affiliate Partner</p>
    <p class="text-xs mt-1">All brand names are property of their respective owners.</p>
  </footer>

  <!-- Success Sound -->
  <audio id="successSound" src="https://www.soundjay.com/buttons/sounds/button-3.mp3" preload="auto"></audio>

  <!-- Script Section -->
  <script>
    function sendToWhatsApp() {
      const name = document.getElementById("name").value.trim();
      const mobile = document.getElementById("mobile").value.trim();
      const address = document.getElementById("address").value.trim();
      const payment = document.querySelector('input[name="payment"]:checked').value;

      const message = `*New Order Details*%0A👤 *Name:* ${encodeURIComponent(name)}%0A📞 *Mobile:* ${encodeURIComponent(mobile)}%0A🏠 *Address:* ${encodeURIComponent(address)}%0A💳 *Payment:* ${encodeURIComponent(payment)}`;
      const phoneNumber = "919667302392";
      const whatsappURL = `https://wa.me/${phoneNumber}?text=${message}`;

      window.open(whatsappURL, "_blank");
      setTimeout(() => {
        document.getElementById("successSound").play();
        alert("Your order details have been sent on WhatsApp!");
      }, 500);
    }

    function toggleQRCode() {
      const qr = document.getElementById("qrSection");
      const paymentMethod = document.querySelector('input[name="payment"]:checked').value;
      qr.classList.toggle("hidden", paymentMethod !== "Pay Now");
    }
  </script>

</body>
</html>
