<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Wolf Capital - Access Capital Built for Growth</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
<style>

* { margin:0; padding:0; box-sizing:border-box; font-family:'Inter', sans-serif; }

body {
    background: #f7f9fc;
    color:#0a2540;
}

header {
    background: linear-gradient(135deg,#0a2540,#1a3d7c);
    color:white;
    padding:100px 20px;
    text-align:center;
}

header h1 {
    font-size:48px;
    font-weight:700;
}

header p {
    margin-top:15px;
    font-size:18px;
    opacity:0.9;
}

.btn {
    display:inline-block;
    padding:14px 28px;
    margin:15px 10px;
    background:#635bff;
    color:white;
    border-radius:8px;
    text-decoration:none;
    font-weight:600;
    transition:0.3s;
}

.btn:hover {
    background:#4f46e5;
}

.section {
    padding:80px 20px;
    text-align:center;
}

.section h2 {
    font-size:32px;
    margin-bottom:40px;
}

.grid {
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:25px;
    max-width:1100px;
    margin:auto;
}

.card {
    background:white;
    padding:30px;
    border-radius:12px;
    box-shadow:0 10px 30px rgba(0,0,0,0.05);
    text-align:left;
}

.form-wrapper {
    max-width:600px;
    margin:50px auto;
    background:white;
    padding:40px;
    border-radius:12px;
    box-shadow:0 15px 40px rgba(0,0,0,0.08);
}

.progress {
    height:6px;
    background:#e5e7eb;
    border-radius:5px;
    margin-bottom:30px;
}

.progress-bar {
    height:6px;
    width:20%;
    background:#635bff;
    border-radius:5px;
    transition:0.3s;
}

input, select {
    width:100%;
    padding:14px;
    margin:12px 0;
    border-radius:8px;
    border:1px solid #ddd;
    font-size:15px;
}

button {
    padding:14px;
    width:100%;
    background:#635bff;
    color:white;
    border:none;
    border-radius:8px;
    font-size:16px;
    font-weight:600;
    cursor:pointer;
}

button:hover {
    background:#4f46e5;
}

.step { display:none; }
.step.active { display:block; }

footer {
    background:#0a2540;
    color:white;
    text-align:center;
    padding:30px;
    font-size:14px;
}

/* OTP Modal */
.modal {
    display:none;
    position:fixed;
    inset:0;
    background:rgba(0,0,0,0.5);
    justify-content:center;
    align-items:center;
}

.modal-content {
    background:white;
    padding:40px;
    border-radius:12px;
    text-align:center;
    width:90%;
    max-width:400px;
}

</style>
</head>
<body>

<header>
    <h1>Wolf Capital</h1>
    <p>Access capital built for growth.</p>
    <p>Fast Digital Loans. Apply in Minutes. Get Funded Quickly.</p>
    <a href="#apply" class="btn">Check Eligibility</a>
</header>

<section class="section">
    <h2>How It Works</h2>
    <div class="grid">
        <div class="card">
            <h3>Apply Online</h3>
            <p>Complete a secure 5-minute digital application.</p>
        </div>
        <div class="card">
            <h3>Instant Review</h3>
            <p>Automated affordability & eligibility assessment.</p>
        </div>
        <div class="card">
            <h3>Get Funded</h3>
            <p>Approved funds sent directly to your bank.</p>
        </div>
    </div>
</section>

<section id="apply" class="section">
<h2>Loan Application</h2>

<div class="form-wrapper">
<div class="progress"><div class="progress-bar" id="progressBar"></div></div>

<form id="loanForm">

<div class="step active">
<h3>Basic Details</h3>
<input type="text" placeholder="Full Legal Name" required>
<input type="tel" placeholder="Mobile Number" id="phoneInput" required>
<input type="email" placeholder="Email Address" required>
<button type="button" onclick="nextStep()">Continue</button>
</div>

<div class="step">
<h3>Identity Information</h3>
<input type="date" required>
<input type="text" placeholder="National ID / Passport" required>
<input type="text" placeholder="Residential Address" required>
<button type="button" onclick="nextStep()">Continue</button>
</div>

<div class="step">
<h3>Loan Details</h3>
<input type="number" placeholder="Loan Amount" required>
<select required>
<option value="">Repayment Period</option>
<option>3 Months</option>
<option>6 Months</option>
<option>12 Months</option>
</select>
<button type="button" onclick="nextStep()">Continue</button>
</div>

<div class="step">
<h3>Employment Details</h3>
<select required>
<option value="">Employment Status</option>
<option>Employed</option>
<option>Self-Employed</option>
</select>
<input type="number" placeholder="Monthly Income" required>
<button type="button" onclick="sendOTP()">Verify & Submit</button>
</div>

</form>
</div>
</section>

<!-- OTP Modal -->
<div class="modal" id="otpModal">
<div class="modal-content">
<h3>Phone Verification</h3>
<p>Enter the 6-digit code sent to your phone.</p>
<input type="text" id="otpInput" placeholder="Enter OTP">
<button onclick="verifyOTP()">Verify</button>
</div>
</div>

<footer>
© 2026 Wolf Capital | Privacy Policy | Terms & Conditions
</footer>

<script>

let currentStep = 0;
const steps = document.querySelectorAll(".step");
const progressBar = document.getElementById("progressBar");
let generatedOTP = "";

function nextStep() {
    steps[currentStep].classList.remove("active");
    currentStep++;
    steps[currentStep].classList.add("active");
    progressBar.style.width = ((currentStep+1)/steps.length)*100 + "%";
}

function sendOTP() {
    generatedOTP = Math.floor(100000 + Math.random() * 900000);
    alert("Simulation OTP: " + generatedOTP); // For demo only
    document.getElementById("otpModal").style.display = "flex";
}

function verifyOTP() {
    const entered = document.getElementById("otpInput").value;
    if(entered == generatedOTP) {
        alert("Application Submitted Successfully ✅");
        document.getElementById("otpModal").style.display = "none";
    } else {
        alert("Invalid OTP. Try again.");
    }
}

</script>

</body>
</html>

