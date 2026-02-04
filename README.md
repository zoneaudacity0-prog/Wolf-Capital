<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Digital Loan Application</title>

  <style>
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background: #f5f7fa;
      color: #333;
    }

    header {
      background: #0a3cff;
      color: white;
      padding: 40px 20px;
      text-align: center;
    }

    header h1 {
      margin-bottom: 10px;
    }

    .container {
      max-width: 1000px;
      margin: auto;
      padding: 20px;
    }

    .section {
      background: white;
      padding: 25px;
      margin-bottom: 20px;
      border-radius: 8px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.08);
    }

    h2 {
      margin-top: 0;
      color: #0a3cff;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 15px;
    }

    input, select, textarea, button {
      width: 100%;
      padding: 12px;
      margin-top: 8px;
      margin-bottom: 15px;
      border-radius: 5px;
      border: 1px solid #ccc;
      font-size: 14px;
    }

    button {
      background: #0a3cff;
      color: white;
      border: none;
      cursor: pointer;
      font-weight: bold;
    }

    button:hover {
      background: #062dbf;
    }

    .checkbox {
      display: flex;
      align-items: flex-start;
      gap: 10px;
      font-size: 14px;
      margin-bottom: 15px;
    }

    footer {
      text-align: center;
      font-size: 13px;
      padding: 20px;
      color: #666;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 24px;
      }
    }
  </style>
</head>

<body>

<header>
  <h1>Fast Digital Loans</h1>
  <p>Apply online • Get approved • Funds sent directly to your bank</p>
</header>

<div class="container">

  <!-- HOW IT WORKS -->
  <div class="section">
    <h2>How It Works</h2>
    <div class="grid">
      <div>1️⃣ Apply online in minutes</div>
      <div>2️⃣ We review your application</div>
      <div>3️⃣ Funds sent to your bank</div>
    </div>
  </div>

  <!-- LOAN FEATURES -->
  <div class="section">
    <h2>Loan Features</h2>
    <ul>
      <li>Flexible loan amounts</li>
      <li>Transparent interest rates</li>
      <li>No physical paperwork</li>
      <li>Early repayment allowed</li>
    </ul>
  </div>

  <!-- APPLICATION FORM -->
  <div class="section">
    <h2>Loan Application Form</h2>

    <form>

      <h3>Personal Information</h3>
      <div class="grid">
        <input type="text" placeholder="Full Legal Name" required>
        <input type="date" placeholder="Date of Birth" required>
        <input type="text" placeholder="National ID / Passport Number" required>
        <input type="text" placeholder="Residential Address" required>
        <input type="tel" placeholder="Mobile Number" required>
        <input type="email" placeholder="Email Address" required>
      </div>

      <h3>Loan Details</h3>
      <div class="grid">
        <input type="number" placeholder="Loan Amount Requested" required>
        <select required>
          <option value="">Loan Purpose</option>
          <option>Business</option>
          <option>Personal</option>
          <option>Education</option>
          <option>Emergency</option>
        </select>
        <select required>
          <option value="">Repayment Period</option>
          <option>3 Months</option>
          <option>6 Months</option>
          <option>12 Months</option>
          <option>24 Months</option>
        </select>
      </div>

      <h3>Employment & Financial Information</h3>
      <div class="grid">
        <select required>
          <option value="">Employment Status</option>
          <option>Employed</option>
          <option>Self-Employed</option>
          <option>Business Owner</option>
        </select>
        <input type="text" placeholder="Employer / Business Name" required>
        <input type="number" placeholder="Monthly Income (TZS)" required>
      </div>

      <h3>Bank Details</h3>
      <div class="grid">
        <input type="text" placeholder="Bank Name" required>
        <input type="text" placeholder="Account Holder Name" required>
        <input type="text" placeholder="Account Number" required>
      </div>

      <!-- CONSENT -->
      <div class="checkbox">
        <input type="checkbox" required>
        <label>
          I confirm that all information provided is true and correct and I agree to the
          <strong>Terms & Conditions</strong>.
        </label>
      </div>

      <div class="checkbox">
        <input type="checkbox" required>
        <label>
          I consent to credit checks, data processing, and electronic communication.
        </label>
      </div>

      <input type="text" placeholder="Type Full Legal Name as Digital Signature" required>

      <button type="submit">Submit Application</button>
    </form>
  </div>

  <!-- TERMS AND CONDITIONS -->
  <div class="section">
    <h2>Terms & Conditions (Tanzania)</h2>

    <p><strong>1. Legal Agreement</strong><br>
    By submitting this application, the Applicant enters into a legally binding agreement governed by the laws of the United Republic of Tanzania.</p>

    <p><strong>2. Eligibility</strong><br>
    The Applicant confirms they are at least 18 years old, legally competent, and a resident of Tanzania.</p>

    <p><strong>3. Accuracy of Information</strong><br>
    All information provided must be accurate and complete. Any false declaration may result in rejection of the loan or legal action.</p>

    <p><strong>4. Credit Assessment</strong><br>
    The Lender reserves the right to conduct credit reference checks with Credit Reference Bureaus licensed by the Bank of Tanzania.</p>

    <p><strong>5. Repayment Obligation</strong><br>
    The Applicant agrees to repay the loan in full, including interest, fees, and penalties, according to the agreed repayment schedule.</p>

    <p><strong>6. Default</strong><br>
    In case of default, the Lender may pursue recovery actions including deductions, legal proceedings, or reporting to credit bureaus.</p>

    <p><strong>7. Data Protection</strong><br>
    Personal data will be processed in accordance with the Tanzania Personal Data Protection Act, 2022.</p>

    <p><strong>8. Electronic Consent</strong><br>
    The Applicant agrees that electronic acceptance, digital signature, timestamps, and IP records constitute valid legal evidence.</p>

    <p><strong>9. Governing Law</strong><br>
    This agreement shall be governed and interpreted in accordance with the laws of the United Republic of Tanzania.</p>
  </div>

</div>

<footer>
  © 2026 Digital Loan Platform • Tanzania
</footer>

</body>
</html>
