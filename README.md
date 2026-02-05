<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Wolf Capital — Capital That Moves With You</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background-color: #f4f6f9;
      color: #333;
      line-height: 1.6;
    }

    header {
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: #ffffff;
      padding: 70px 20px;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 38px;
    }

    header p {
      margin-top: 10px;
      font-size: 18px;
      opacity: 0.95;
    }

    .container {
      max-width: 1100px;
      margin: auto;
      padding: 25px 20px;
    }

    .section {
      background: #ffffff;
      padding: 30px;
      margin-bottom: 25px;
      border-radius: 10px;
      box-shadow: 0 6px 16px rgba(0,0,0,0.08);
    }

    h2 {
      margin-top: 0;
      color: #203a43;
    }

    h3 {
      margin-bottom: 10px;
      color: #2c5364;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 16px;
    }

    input,
    select,
    textarea {
      width: 100%;
      padding: 13px;
      border-radius: 6px;
      border: 1px solid #ccc;
      font-size: 14px;
      margin-bottom: 15px;
    }

    button {
      width: 100%;
      padding: 15px;
      background-color: #2c5364;
      color: #ffffff;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      font-weight: bold;
      cursor: pointer;
    }

    button:hover {
      background-color: #203a43;
    }

    ul {
      padding-left: 20px;
    }

    .checkbox {
      display: flex;
      gap: 10px;
      font-size: 14px;
      margin-bottom: 15px;
    }

    footer {
      text-align: center;
      padding: 25px;
      font-size: 13px;
      color: #666;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 26px;
      }

      header p {
        font-size: 16px;
      }
    }
  </style>
</head>

<body>

  <!-- HERO -->
  <header>
    <h1>Wolf Capital — Capital That Moves With You</h1>
    <p>Access capital built for growth.</p>
  </header>

  <div class="container">

    <!-- HOW IT WORKS -->
    <div class="section">
      <h2>How It Works</h2>
      <div class="grid">
        <div>🐺 Apply digitally in minutes</div>
        <div>⚡ Fast review and approval</div>
        <div>🏦 Funds sent directly to your bank</div>
      </div>
    </div>

    <!-- FEATURES -->
    <div class="section">
      <h2>Why Wolf Capital</h2>
      <ul>
        <li>Flexible capital for individuals and businesses</li>
        <li>Transparent pricing with no hidden fees</li>
        <li>100% digital application process</li>
        <li>Early repayment supported</li>
      </ul>
    </div>

    <!-- APPLICATION FORM -->
    <div class="section">
      <h2>Apply for Capital</h2>

      <form>

        <h3>Personal Information</h3>
        <div class="grid">
          <input type="text" placeholder="Full Legal Name" required />
          <input type="date" required />
          <input type="text" placeholder="National ID / Passport Number" required />
          <input type="text" placeholder="Residential Address" required />
          <input type="tel" placeholder="Mobile Number" required />
          <input type="email" placeholder="Email Address" required />
        </div>

        <h3>Loan Details</h3>
        <div class="grid">
          <input type="number" placeholder="Loan Amount Requested (TZS)" required />
          <select required>
            <option value="">Loan Purpose</option>
            <option>Business Expansion</option>
            <option>Working Capital</option>
            <option>Personal Use</option>
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
          <input type="text" placeholder="Employer / Business Name" required />
          <input type="number" placeholder="Average Monthly Income (TZS)" required />
        </div>

        <h3>Bank Details</h3>
        <div class="grid">
          <input type="text" placeholder="Bank Name" required />
          <input type="text" placeholder="Account Holder Name" required />
          <input type="text" placeholder="Account Number" required />
        </div>

        <div class="checkbox">
          <input type="checkbox" required />
          <label>
            I confirm that all information provided is true and accurate and I agree to the
            <strong>Wolf Capital Terms & Conditions</strong>.
          </label>
        </div>

        <div class="checkbox">
          <input type="checkbox" required />
          <label>
            I consent to credit checks, electronic communication, and processing of my personal data.
          </label>
        </div>

        <input type="text" placeholder="Type Full Legal Name as Digital Signature" required />

        <button type="submit">Submit Application</button>

      </form>
    </div>

    <!-- TERMS & CONDITIONS -->
    <div class="section">
      <h2>Wolf Capital – Terms & Conditions (Tanzania)</h2>

      <p><strong>1. Binding Agreement</strong><br>
      By submitting this application, the Applicant enters into a legally binding agreement with Wolf Capital governed by the laws of the United Republic of Tanzania.</p>

      <p><strong>2. Eligibility</strong><br>
      The Applicant confirms that they are at least eighteen (18) years of age, legally competent, and resident in Tanzania.</p>

      <p><strong>3. Accuracy of Information</strong><br>
      All information provided must be true, accurate, and complete. Any misrepresentation may result in rejection or legal action.</p>

      <p><strong>4. Credit Assessment</strong><br>
      Wolf Capital may obtain and share credit information with Credit Reference Bureaus licensed by the Bank of Tanzania.</p>

      <p><strong>5. Repayment Obligation</strong><br>
      The Applicant agrees to repay the loan amount together with applicable interest, fees, and penalties as per the agreed repayment schedule.</p>

      <p><strong>6. Default & Recovery</strong><br>
      In the event of default, Wolf Capital may pursue lawful recovery actions including legal proceedings and credit reporting.</p>

      <p><strong>7. Data Protection</strong><br>
      Personal data shall be processed in accordance with the Tanzania Personal Data Protection Act, 2022.</p>

      <p><strong>8. Electronic Acceptance</strong><br>
      Digital consent, electronic signatures, timestamps, and system records shall constitute valid legal evidence.</p>

      <p><strong>9. Governing Law</strong><br>
      This agreement shall be governed by and construed in accordance with the laws of the United Republic of Tanzania.</p>
    </div>

  </div>

  <footer>
    © 2026 Wolf Capital • Capital That Moves With You
  </footer>

</body>
</html>

