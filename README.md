<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Order Now - Sale4u</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 font-sans flex items-center justify-center min-h-screen">

  <!-- Order Form Only -->
  <div class="max-w-xl w-full bg-white rounded-2xl shadow-xl p-6">
    <h3 class="text-2xl font-bold text-yellow-600 mb-6 text-center">Place Your Order</h3>

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

      <!-- Only Cash on Delivery -->
      <div class="mb-6">
        <label class="block text-gray-700 font-medium mb-2">Payment Option</label>
        <div>
          <label class="flex items-center">
            <input type="radio" name="payment" value="Cash on Delivery" class="mr-2" checked />
            Cash on Delivery
          </label>
        </div>
      </div>

      <button type="submit"
              class="bg-yellow-500 text-white w-full py-2 rounded hover:bg-yellow-600 transition duration-200">
        Send Order via WhatsApp
      </button>

      <p class="text-xs text-center text-gray-500 mt-4">🔁 Replace available in 4 days. 100% Secure Order.</p>
    </form>
  </div>

  <audio id="successSound" src="https://www.soundjay.com/buttons/sounds/button-3.mp3" preload="auto"></audio>

  <script>
    function sendToWhatsApp() {
      const name = document.getElementById("name").value.trim();
      const mobile = document.getElementById("mobile").value.trim();
      const address = document.getElementById("address").value.trim();
      const payment = "Cash on Delivery";

      const message = `*New Order Details*%0A👤 *Name:* ${encodeURIComponent(name)}%0A📞 *Mobile:* ${encodeURIComponent(mobile)}%0A🏠 *Address:* ${encodeURIComponent(address)}%0A💳 *Payment:* ${encodeURIComponent(payment)}`;
      const whatsappURL = `https://wa.me/919667302392?text=${message}`;

      window.open(whatsappURL, "_blank");
      setTimeout(() => {
        document.getElementById("successSound").play();
        alert("Your order details have been sent on WhatsApp!");
      }, 500);
    }
  </script>

</body>
</html>
