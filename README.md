# CreditWise-Loan-System
#### A Loan Approval System
<hr>
My First Mini M.L. Project.

### Problem Statement
A mid-sized financial company named <b>Secure Trust Bank</b> offers personal and home loans to customers across urban and rural regions of India. Every day, hundreds of customers apply for loans through online and branch applications.

Until now, <b>Secure Trust Bank</b> has been using a manual verification process where loan officers evaluate applications by checking income proofs, employment details, credit history, and other documents. This process is time-consuming, biased & inconsistent.
As a result, the bank faces two major challenges:

1. Good customers sometimes get rejected, leading to loss of business.
2. High-risk customers sometimes get approved, leading to financial losses.

To solve this problem, the bank wants to introduce an intelligent loan approval system powered by Machine Learning that can automatically analyse applicant details and predict whether a loan should be Approved or Rejected before final human verification.


### Solution using ML model
In this project i built end-to-end Supervised ML pipeline using kNN, Logistic Regression, and Naive Baye's to predict loan approval. Implemented Binary classification along with EDA, feature engineering & model evaluation using Precision, Recall and f1-score.

### Dataset Description
Each row in the dataset represents a <b>Loan applicant</b> and contains multiple attributes describing their personal, financial, and credit information.

<style>
  .schema-table { width: 100%; border-collapse: collapse; font-size: 14px; font-family: sans-serif; }
  .schema-table thead tr { background: #f5f5f5; }
  .schema-table th { text-align: left; padding: 10px 16px; font-weight: 500; font-size: 13px; color: #666; border-bottom: 1px solid #ddd; }
  .schema-table td { padding: 9px 16px; border-bottom: 1px solid #eee; color: #111; vertical-align: middle; }
  .schema-table tbody tr:last-child td { border-bottom: none; }
  .schema-table tbody tr:hover td { background: #fafafa; }
  .col-name { font-weight: 600; white-space: nowrap; }
  .badge { display: inline-block; font-size: 11px; padding: 2px 7px; border-radius: 4px; margin-right: 4px; background: #e8f0fe; color: #1a56db; }
  .badge-target { background: #e3f9e5; color: #1a7a2e; }
  .wrapper { border: 1px solid #ddd; border-radius: 10px; overflow: hidden; }
</style>

<div class="wrapper">
  <table class="schema-table">
    <thead>
      <tr>
        <th style="width:40%">Column</th>
        <th>Description</th>
      </tr>
    </thead>
    <tbody>
      <tr><td class="col-name">Applicant_ID</td><td>Unique applicant ID</td></tr>
      <tr><td class="col-name">Applicant_Income</td><td>Monthly income of applicant</td></tr>
      <tr><td class="col-name">Coapplicant_Income</td><td>Monthly income of co-applicant</td></tr>
      <tr><td class="col-name">Employment_Status</td><td><span class="badge">Salaried</span><span class="badge">Self-Employed</span><span class="badge">Business</span></td></tr>
      <tr><td class="col-name">Age</td><td>Applicant age</td></tr>
      <tr><td class="col-name">Marital_Status</td><td><span class="badge">Married</span><span class="badge">Single</span></td></tr>
      <tr><td class="col-name">Dependents</td><td>Number of dependents</td></tr>
      <tr><td class="col-name">Credit_Score</td><td>Credit bureau score</td></tr>
      <tr><td class="col-name">Existing_Loans</td><td>Number of already running loans</td></tr>
      <tr><td class="col-name">DTI_Ratio</td><td>Debt-to-Income ratio</td></tr>
      <tr><td class="col-name">Savings</td><td>Savings balance</td></tr>
      <tr><td class="col-name">Collateral_Value</td><td>Value of collateral provided</td></tr>
      <tr><td class="col-name">Loan_Amount</td><td>Loan amount requested</td></tr>
      <tr><td class="col-name">Loan_Term</td><td>Loan duration (months)</td></tr>
      <tr><td class="col-name">Loan_Purpose</td><td><span class="badge">Home</span><span class="badge">Education</span><span class="badge">Personal</span><span class="badge">Business</span></td></tr>
      <tr><td class="col-name">Property_Area</td><td><span class="badge">Urban</span><span class="badge">Semi-Urban</span><span class="badge">Rural</span></td></tr>
      <tr><td class="col-name">Education_Level</td><td><span class="badge">Graduate</span><span class="badge">Postgraduate</span><span class="badge">Undergraduate</span></td></tr>
      <tr><td class="col-name">Gender</td><td><span class="badge">Male</span><span class="badge">Female</span></td></tr>
      <tr><td class="col-name">Employer_Category</td><td><span class="badge">Govt</span><span class="badge">Private</span><span class="badge">Self</span></td></tr>
      <tr>
        <td class="col-name">Loan_Approved <span style="font-size:11px;font-weight:400;color:#888">(Target)</span></td>
        <td><span class="badge badge-target">1 = Approved</span><span class="badge badge-target">0 = Rejected</span></td>
      </tr>
    </tbody>
  </table>
</div>