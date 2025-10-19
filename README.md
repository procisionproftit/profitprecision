# profitprecision
Maximize your profits with expert-vetted parlay picks, confidence percentages, and potential payouts—all in one easy-to-use PDF.
Profit-Precison/
├── index.html
├── tos.html
└── assets/
    ├── logo.png
    └── ProfitPrecisionGuide.pdf
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Profit Precision</title>
  <link rel="icon" href="assets/logo.png">
  <style>
    body { margin:0; font-family:'Segoe UI', Tahoma, sans-serif; background:#0f1724; color:white; }
    header, main, footer { max-width:900px; margin:auto; padding:20px; }
    a { color:#38b2ac; text-decoration:none; }
  </style>
</head>
<body>

  <!-- === AGE VERIFICATION MODAL === -->
  <div id="ageModal" style="
      position:fixed; top:0; left:0; width:100%; height:100%;
      background:rgba(15,23,36,0.95); display:flex; justify-content:center; align-items:center;
      z-index:10000; font-family: 'Segoe UI', Tahoma, sans-serif; padding:20px;
      opacity:0; animation:fadeIn 0.5s forwards;">
    <div style="
        background:#0f1724; color:white; padding:40px; border-radius:15px;
        text-align:center; max-width:450px; width:100%;
        box-shadow:0 0 30px rgba(0,0,0,0.7); border:2px solid #38b2ac;
        box-sizing:border-box;
        transform:translateY(30px); animation:slideUp 0.5s forwards;">
      <img src="assets/logo.png" alt="Profit Precision Logo" style="width:25%; max-width:120px; height:auto; margin-bottom:20px;">
      <h1 style="font-size:2em; margin-bottom:10px; color:#38b2ac;">Profit Precision</h1>
      <p style="font-size:1.1em; font-style:italic; margin-bottom:20px; color:#cbd5e1;">Maximize Your Winning Potential</p>
      <p style="font-size:1em; margin-bottom:25px;">
        You must be at least <strong>18 years old</strong> to access this site. Please confirm your age.
      </p>
      <div style="display:flex; flex-direction:column; gap:10px;">
        <button onclick="acceptAge()" style="padding:12px 0; background:#38b2ac; border:none; border-radius:8px; color:white; font-weight:bold; font-size:1em; cursor:pointer; transition:0.3s;"
          onmouseover="this.style.background='#2c7a7b'" onmouseout="this.style.background='#38b2ac'">
          I am 18+
        </button>
        <button onclick="denyAge()" style="padding:12px 0; background:#e53e3e; border:none; border-radius:8px; color:white; font-weight:bold; font-size:1em; cursor:pointer; transition:0.3s;"
          onmouseover="this.style.background='#c53030'" onmouseout="this.style.background='#e53e3e'">
          I am under 18
        </button>
      </div>
    </div>
  </div>

  <style>
    @keyframes fadeIn { from {opacity:0;} to {opacity:1;} }
    @keyframes slideUp { from {transform:translateY(30px);} to {transform:translateY(0);} }
  </style>

  <script>
    function acceptAge() {
      localStorage.setItem('ageVerified', 'true');
      document.getElementById('ageModal').style.display = 'none';
    }
    function denyAge() {
      alert("Sorry, you must be at least 18 to access Profit Precision.");
      window.location.href = "https://www.google.com";
    }
    document.addEventListener("DOMContentLoaded", function() {
      if(localStorage.getItem('ageVerified') === 'true') {
        document.getElementById('ageModal').style.display = 'none';
      }
    });
  </script>

  <!-- === SITE CONTENT === -->
  <header>
    <h1>Profit Precision</h1>
    <p>Your hub for sports betting insights and maximum profit potential.</p>
  </header>

  <main>
    <h2>Today’s Highlights</h2>
    <p>Use our data-driven picks and analytics to make informed betting decisions. Remember, all bets carry risk.</p>

    <!-- BUY NOW BUTTON -->
    <a href="YOUR_STRIPE_PAYMENT_LINK" target="_blank">
      <button style="
          padding:15px 40px; background:#38b2ac; color:white; border:none;
          border-radius:10px; font-size:1.2em; cursor:pointer; transition:0.3s;"
          onmouseover="this.style.background='#2c7a7b'" onmouseout="this.style.background='#38b2ac'">
        Buy Now
      </button>
    </a>

    <p style="margin-top:20px;"><a href="tos.html">Read our Terms of Service</a></p>
  </main>

  <footer style="text-align:center; padding:20px; margin-top:40px;">
    &copy; 2025 Profit Precision | <a href="tos.html">Terms of Service</a>
  </footer>

</body>
</html>
