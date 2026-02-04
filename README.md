<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Wolf Capital — Capital That Moves With You</title>

  <style>
    :root {
      --primary:#0f172a;
      --accent:#16a34a;
      --muted:#64748b;
      --bg:#f8fafc;
      --card:#ffffff;
    }

    * { box-sizing:border-box; font-family: system-ui, -apple-system, BlinkMacSystemFont, sans-serif; }
    body { margin:0; background:var(--bg); color:var(--primary); }

    header, section { padding:60px 20px; max-width:1100px; margin:auto; }

    h1, h2, h3 { margin-bottom:12px; }
    p { color:var(--muted); line-height:1.6; }

    .btn {
      display:inline-block;
      padding:14px 22px;
      border-radius:8px;
      border:none;
      cursor:pointer;
      font-size:16px;
      font-weight:600;
      text-decoration:none;
    }
    .btn-primary { background:var(--accent); color:white; }
    .btn-secondary { background:#e5e7eb; color:#111827; }

    .hero { text-align:center; }
    .hero h1 { font-size:clamp(28px,5vw,46px); }
    .hero .cta { margin-top:24px; display:flex; gap:12px; justify-content:center; flex-wrap:wrap; }

    .trust { display:flex; justify-content:center; gap:20px; margin-top:30px; flex-wrap:wrap; font-size:14px; }

    .grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:24px; }

    .card {
      background:var(--card);
      padding:24px;
      border-radius:14px;
      box-shadow:0 10px 30px rgba(0,0,0,.05);
    }

    /* FORM */
    .form-wrapper { max-width:700px; margin:auto; }
    .progress { height:8px; background:#e5e7eb; border-radius:6px; overflow:hidden; margin-bottom:20px; }
    .progress-bar { height:100%; width:0%; background:var(--accent); transition:.3s; }

    .form-step { display:none; }
    .form-step.active { display:block; }

    label { display:block; font-size:14px; margin:14px 0 6px; }
    input, select, textarea {
      width:100%;
      padding:14px;
      border-radius:8px;
      border:1px solid #d1d5db;
      font-size:16px;
    }

    .form-nav {
      display:flex;
      justify-content:space-between;
      margin-top:24px;
      gap:10px;
    }

    footer {
      background:#020617;
      color:#94a3b8;
      padding:40px 20px;
      font-size:14px;
    }
  </style>
</head>
<body>

<!-- HERO -->
<header class="hero">
  <h1>Wolf Capital — Capital That Moves With You</h1>
  <p><strong>Fast Digital Loans.</strong> Apply in Minutes. Get Funded Quickly.</p>
  <p>Flexible personal and business loans with transparent pricing, no hidden fees, and simple online approval.</p>

  <div class="cta">
    <a href="#apply" class="btn btn-primary">Check Eligibility</a>
    <a href="#features" class="btn btn-secondary">Calculate Your Loan</a>
  </div>

  <div class="trust">
    <span>🔒 Secure & Encrypted</span>
    <span>📜 Regulated Lender</span>
    <span>🛡️ Data Privacy Protected</span>
  </div>
</header>

<!-- HOW IT WORKS -->
<section>
  <h2>How It Works</h2>
  <div class="grid">
    <div class="card">
      <h3>1. Apply Online</h3>
      <p>Complete a short digital application from any device.</p>
    </div>
    <div class="card">
      <h3>2. Get Approved</h3>
      <p>We review your details and assess eligibility quickly.</p>
    </div>
    <div class="card">
      <h3>3. Receive Funds</h3>
      <p>Approved loans are disbursed directly to your bank account.</p>
    </div>
  </div>
</section>

<!-- FEATURES -->
<section id="features">
  <h2>Loan Features</h2>
  <div class="grid">
    <div class="card">💰 $500 – $50,000 Loan Amounts</div>
    <div class="card">📆 3 – 36 Month Repayment Terms</div>
    <div class="card">📉 Competitive Interest Rates</div>
    <div class="card">📄 No Physical Paperwork</div>
    <div class="card">⚡ Early Repayment Allowed</div>
  </div>
  <br/>
  <a href="#apply" class="btn btn-primary">Apply Now</a>
</section>

<!-- ELIGIBILITY -->
<section>
  <h2>Eligibility Snapshot</h2>
  <ul>
    <li>18 years or older</li>
    <li>Valid Government ID</li>
    <li>Regular source of income</li>
    <li>Active bank account</li>
  </ul>
  <a href="#apply" class="btn btn-primary">Start Application</a>
</section>

<!-- APPLICATION FORM -->
<section id="apply">
  <h2>Loan Application</h2>

  <div class="form-wrapper card">
    <div class="progress"><div class="progress-bar" id="progressBar"></div></div>

    <form id="loanForm">

      <!-- STEP 1 -->
      <div class="form-step active">
        <label>Full Legal Name</label>
        <input required />

        <label>Mobile Phone Number</label>
        <input required />

        <label>Email Address</label>
        <input type="email" required />
      </div>

      <!-- STEP 2 -->
      <div class="form-step">
        <label>Date of Birth</label>
        <input type="date" required />

        <label>National ID / Passport Number</label>
        <input required />

        <label>Residential Address</label>
        <textarea required></textarea>
      </div>

      <!-- STEP 3 -->
      <div class="form-step">
        <label>Loan Amount Requested</label>
        <input type="number" required />

        <label>Loan Purpose</label>
        <select>
          <option>Business</option>
          <option>Personal</option>
          <option>Education</option>
          <option>Other</option>
        </select>

        <label>Preferred Repayment Period (Months)</label>
        <input type="number" />
      </div>

      <!-- STEP 4 -->
      <div class="form-step">
        <label>Employment Status</label>
        <select>
          <option>Employed</option>
          <option>Self-Employed</option>
          <option>Business Owner</option>
        </select>

        <label>Employer / Business Name</label>
        <input />

        <label>Monthly Income Range</label>
        <select>
          <option>Below $500</option>
          <option>$500 – $1,000</option>
          <option>$1,000+</option>
        </select>
      </div>

      <!-- STEP 5 -->
      <div class="form-step">
        <label>Bank Name</label>
        <input />

        <label>Account Holder Name</label>
        <input />

        <label>Account Number</label>
        <input />
      </div>

      <!-- STEP 6 -->
      <div class="form-step">
        <label><input type="checkbox" required /> I confirm information is true</label>
        <label><input type="checkbox" required /> I agree to Loan Terms & Conditions</label>
        <label><input type="checkbox" required /> I consent to credit checks & data processing</label>
        <label><input type="checkbox" required /> I authorize automated reminders</label>

        <label>Digital Signature (Type Full Name)</label>
        <input required />

        <p><strong>Date:</strong> <span id="today"></span></p>
      </div>

      <div class="form-nav">
        <button type="button" class="btn btn-secondary" onclick="prevStep()">Back</button>
        <button type="button" class="btn btn-primary" onclick="nextStep()">Continue</button>
      </div>

    </form>
  </div>
</section>

<!-- FOOTER / LEGAL -->
<footer>
  <p><strong>Legal Notice (Tanzania)</strong></p>
  <p>
    By submitting this application, you confirm the accuracy of the information provided and consent to credit assessment,
    data processing, and electronic communication in accordance with Tanzanian law. Providing false information may result
    in rejection or legal action.
  </p>
  <p>© Wolf Capital. All Rights Reserved.</p>
</footer>

<script>
  const steps = document.querySelectorAll(".form-step");
  let currentStep = 0;

  function updateUI() {
    steps.forEach((s,i)=>s.classList.toggle("active", i===currentStep));
    document.getElementById("progressBar").style.width =
      ((currentStep+1)/steps.length*100)+"%";
  }

  function nextStep() {
    if (currentStep < steps.length - 1) currentStep++;
    else alert("Application Submitted Successfully ✅");
    updateUI();
  }

  function prevStep() {
    if (currentStep > 0) currentStep--;
    updateUI();
  }

  document.getElementById("today").textContent =
    new Date().toLocaleDateString();
</script>

</body>
</html>
