<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Wolf Capital — Capital That Moves With You</title>

<style>
* { box-sizing: border-box; margin: 0; padding: 0; }

body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  background: #f5f7fb;
  color: #1a1a1a;
}

header {
  background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
  color: white;
  padding: 80px 20px;
  text-align: center;
}

header h1 {
  font-size: 38px;
  margin-bottom: 10px;
}

header p {
  font-size: 18px;
  opacity: 0.9;
}

.container {
  max-width: 1000px;
  margin: -40px auto 40px;
  padding: 0 20px;
}

.card {
  background: white;
  padding: 40px;
  border-radius: 14px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.08);
}

h2 {
  margin-bottom: 20px;
  color: #203a43;
}

.progress-bar {
  height: 6px;
  background: #e0e6ed;
  border-radius: 4px;
  margin-bottom: 30px;
  overflow: hidden;
}

.progress {
  height: 100%;
  width: 25%;
  background: #2c5364;
  transition: 0.3s ease;
}

.step { display: none; }
.step.active { display: block; }

input, select {
  width: 100%;
  padding: 14px;
  margin-bottom: 15px;
  border: 1px solid #ccc;
  border-radius: 8px;
  font-size: 14px;
}

button {
  padding: 14px 20px;
  border-radius: 8px;
  border: none;
  font-weight: 600;
  cursor: pointer;
  font-size: 15px;
}

.btn-primary {
  background: #2c5364;
  color: white;
}

.btn-secondary {
  background: #e0e6ed;
}

.button-group {
  display: flex;
  justify-content: space-between;
  gap: 10px;
}

.checkbox {
  display: flex;
  align-items: flex-start;
  gap: 8px;
  font-size: 13px;
  margin-bottom: 15px;
}

.success-message {
  text-align: center;
  padding: 40px;
  display: none;
}

.success-message h2 {
  color: #2c5364;
}

footer {
  text-align: center;
  padding: 30px;
  font-size: 13px;
  color: #777;
}

@media(max-width: 600px) {
  header h1 { font-size: 26px; }
  .card { padding: 25px; }
}
</style>
</head>

<body>

<header>
  <h1>Wolf Capital — Capital That Moves With You</h1>
  <p>Access capital built for growth.</p>
</header>

<div class="container">
  <div class="card">

    <div class="progress-bar">
      <div class="progress" id="progress"></div>
    </div>

    <form id="loanForm">

      <!-- STEP 1 -->
      <div class="step active">
        <h2>Personal Information</h2>
        <input type="text" placeholder="Full Legal Name" required>
        <input type="date" required>
        <input type="text" placeholder="National ID Number" required>
      </div>

      <!-- STEP 2 -->
      <div class="step">
        <h2>Loan Details</h2>
        <input type="number" placeholder="Loan Amount (TZS)" required>
        <select required>
          <option value="">Loan Purpose</option>
          <option>Business Expansion</option>
          <option>Working Capital</option>
          <option>Personal Use</option>
        </select>
        <select required>
          <option value="">Repayment Period</option>
          <option>3 Months</option>
          <option>6 Months</option>
          <option>12 Months</option>
        </select>
      </div>

      <!-- STEP 3 -->
      <div class="step">
        <h2>Employment Information</h2>
        <select required>
          <option value="">Employment Status</option>
          <option>Employed</option>
          <option>Self-Employed</option>
          <option>Business Owner</option>
        </select>
        <input type="number" placeholder="Monthly Income (TZS)" required>
      </div>

      <!-- STEP 4 -->
      <div class="step">
        <h2>Consent & Declaration</h2>

        <div class="checkbox">
          <input type="checkbox" required>
          <label>I confirm the information provided is accurate.</label>
        </div>

        <div class="checkbox">
          <input type="checkbox" required>
          <label>I agree to Wolf Capital Terms & Conditions and credit checks under Tanzanian law.</label>
        </div>

        <input type="text" placeholder="Type Full Legal Name as Digital Signature" required>
      </div>

      <div class="button-group">
        <button type="button" class="btn-secondary" id="prevBtn">Previous</button>
        <button type="button" class="btn-primary" id="nextBtn">Next</button>
      </div>

    </form>

    <div class="success-message" id="successMessage">
      <h2>Application Submitted Successfully</h2>
      <p>Thank you for applying with Wolf Capital. Our team will review your application and contact you shortly.</p>
    </div>

  </div>
</div>

<footer>
© 2026 Wolf Capital • Capital That Moves With You
</footer>

<script>
const steps = document.querySelectorAll(".step");
const progress = document.getElementById("progress");
const nextBtn = document.getElementById("nextBtn");
const prevBtn = document.getElementById("prevBtn");
const form = document.getElementById("loanForm");
const successMessage = document.getElementById("successMessage");

let currentStep = 0;

function updateStep() {
  steps.forEach((step, index) => {
    step.classList.toggle("active", index === currentStep);
  });

  progress.style.width = ((currentStep + 1) / steps.length) * 100 + "%";

  prevBtn.style.display = currentStep === 0 ? "none" : "inline-block";
  nextBtn.textContent = currentStep === steps.length - 1 ? "Submit" : "Next";
}

nextBtn.addEventListener("click", () => {
  const inputs = steps[currentStep].querySelectorAll("input, select");
  for (let input of inputs) {
    if (!input.checkValidity()) {
      input.reportValidity();
      return;
    }
  }

  if (currentStep < steps.length - 1) {
    currentStep++;
    updateStep();
  } else {
    form.style.display = "none";
    successMessage.style.display = "block";
  }
});

prevBtn.addEventListener("click", () => {
  if (currentStep > 0) {
    currentStep--;
    updateStep();
  }
});

updateStep();
</script>

</body>
</html>
