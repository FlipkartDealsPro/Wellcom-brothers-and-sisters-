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
    <div class="max-w-7xl mx-auto px-4">
      <h1 class="text-2xl font-bold">Sale4u - Flipkart Affiliate Deals</h1>
      <p class="text-sm mt-1">Top Verified Offers • 100% Secure Checkout</p>
    </div>
  </header>

  <!-- Product Section -->
  <main class="max-w-4xl mx-auto py-8 px-4">
    <div class="bg-white rounded-lg shadow p-6">

      <!-- YouTube Video -->
      <div class="w-full aspect-w-16 aspect-h-9 mb-6">
        <iframe class="w-full rounded-lg"
          height="315"
          src="https://www.youtube.com/embed/lQJcAx68wYg?si=FdMEK7o1TWF4eSFA"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
      </div>

      <!-- Product Details -->
      <h2 class="text-xl font-semibold text-gray-800">EVRGLOW EVR-001 Analog Watch - For Women</h2>
      <p class="text-green-600 font-bold mt-2">85% Off - Now ₹220 <span class="line-through text-gray-400 text-sm">(MRP ₹1499)</span></p>
      <p class="text-gray-700 mt-2">Color: Gold Strap, Green Dial</p>
      <p class="text-sm text-gray-600 mt-1">★ 4.0 | 8,453 Verified Ratings</p>

      <!-- Flipkart Button -->
      <div class="mt-4">
        <a href="https://fktr.in/1mivEup" target="_blank"
           class="inline-block bg-indigo-600 text-white font-semibold px-5 py-2 rounded hover:bg-indigo-700 transition">
          Buy Now on Flipkart
        </a>
      </div>

      <!-- First Website Button -->
      <div class="mt-6 p-4 bg-gray-50 border border-dashed rounded-lg">
        <p class="text-sm text-gray-700 mb-2">Get this product under ₹240 with trusted service.</p>
        <a href="https://fktr.in/1mivEup" target="_blank"
           class="inline-block bg-yellow-500 text-white font-semibold px-5 py-2 rounded hover:bg-yellow-600 transition">
          Buy on Website under ₹240
        </a>
      </div>

      <!-- Second Website Button: WhatsApp Order Form -->
      <div class="mt-6 bg-gray-100 border rounded-lg p-4">
        <h3 class="text-lg font-semibold text-green-600 mb-4 text-center">Secure WhatsApp Order</h3>

        <form onsubmit="sendToWhatsApp(); return false;">
          <div class="mb-3">
            <label for="name" class="block text-gray-700 font-medium mb-1">Full Name</label>
            <input type="text" id="name"
                   class="w-full border border-gray-300 p-2 rounded focus:outline-none focus:ring-2 focus:ring-green-400"
                   required />
          </div>

          <div class="mb-3">
            <label for="mobile" class="block text-gray-700 font-medium mb-1">Mobile Number</label>
            <input type="tel" id="mobile"
                   class="w-full border border-gray-300 p-2 rounded focus:outline-none focus:ring-2 focus:ring-green-400"
                   required />
          </div>

          <div class="mb-3">
            <label for="address" class="block text-gray-700 font-medium mb-1">Delivery Address</label>
            <textarea id="address" rows="3"
                      class="w-full border border-gray-300 p-2 rounded focus:outline-none focus:ring-2 focus:ring-green-400"
                      required></textarea>
          </div>

          <button type="submit"
                  class="bg-green-500 text-white w-full py-2 rounded hover:bg-green-600 transition duration-200">
            Send Order via WhatsApp
          </button>
        </form>

        <!-- Trust Message -->
        <p class="text-xs text-center text-gray-500 mt-3">We never share your information. 100% safe ordering on WhatsApp.</p>
      </div>
    </div>
  </main>

  <!-- Footer -->
  <footer class="bg-gray-800 text-white text-center py-4 mt-10">
    <p class="text-sm">&copy; 2025 Sale4u | Flipkart Affiliate Partner</p>
    <p class="text-xs mt-1">All brand names are property of their respective owners.</p>
  </footer>

  <!-- WhatsApp Script -->
  <script>
    function sendToWhatsApp() {
      const name = document.getElementById("name").value.trim();
      const mobile = document.getElementById("mobile").value.trim();
      const address = document.getElementById("address").value.trim();

      const message = `*New Order Details*%0A👤 *Name:* ${encodeURIComponent(name)}%0A📞 *Mobile:* ${encodeURIComponent(mobile)}%0A🏠 *Address:* ${encodeURIComponent(address)}`;
      const phoneNumber = "919667302392";
      const whatsappURL = `https://wa.me/${phoneNumber}?text=${message}`;
      window.open(whatsappURL, "_blank");
    }
  </script>

</body>
</html>
