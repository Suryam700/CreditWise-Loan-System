# CreditWise-Loan-System
### A Loan Approval System
<hr>
<b>My First Mini M.L. Project.</b>

* ## Problem Statement:
  A mid-sized financial company named <b>Secure Trust Bank</b> offers personal and home loans to customers across urban and rural regions of India. Every day, hundreds of customers apply for loans through online and branch applications.
  
  Until now, <b>Secure Trust Bank</b> has been using a manual verification process where loan officers evaluate applications by checking income proofs, employment details, credit history, and other documents. This process is time-consuming, biased & inconsistent.
  As a result, the bank faces two major challenges:
  
  1. Good customers sometimes get rejected, leading to loss of business.
  2. High-risk customers sometimes get approved, leading to financial losses.
  
  To solve this problem, the bank wants to introduce an intelligent loan approval system powered by Machine Learning that can automatically analyse applicant details and predict whether a loan should be Approved or Rejected before final human verification.

* ## Dataset Description:
  Each row in the dataset represents a <b>Loan applicant</b> and contains multiple attributes describing their personal, financial, and credit information.
  
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
        <tr><td class="col-name">Marital_Status</td><td><span class="badge">Married</span><span class="badge"> Single</span></td></tr>
        <tr><td class="col-name">Dependents</td><td>Number of dependents</td></tr>
        <tr><td class="col-name">Credit_Score</td><td>Credit bureau score</td></tr>
        <tr><td class="col-name">Existing_Loans</td><td>Number of already running loans</td></tr>
        <tr><td class="col-name">DTI_Ratio</td><td>Debt-to-Income ratio</td></tr>
        <tr><td class="col-name">Savings</td><td>Savings balance</td></tr>
        <tr><td class="col-name">Collateral_Value</td><td>Value of collateral provided</td></tr>
        <tr><td class="col-name">Loan_Amount</td><td>Loan amount requested</td></tr>
        <tr><td class="col-name">Loan_Term</td><td>Loan duration (months)</td></tr>
        <tr><td class="col-name">Loan_Purpose</td><td><span class="badge">Home</span><span class="badge">, Education</span><span class="badge">, Personal</span><span class="badge">, Business</span></td></tr>
        <tr><td class="col-name">Property_Area</td><td><span class="badge">Urban</span><span class="badge">, Semi-Urban</span><span class="badge">, Rural</span></td></tr>
        <tr><td class="col-name">Education_Level</td><td><span class="badge">Graduate</span><span class="badge">, Postgraduate</span><span class="badge">, Undergraduate</span></td></tr>
        <tr><td class="col-name">Gender</td><td><span class="badge">Male</span><span class="badge">, Female</span></td></tr>
        <tr><td class="col-name">Employer_Category</td><td><span class="badge">Govt</span><span class="badge">, Private</span><span class="badge">Self</span></td></tr>
        <tr>
          <td class="col-name">Loan_Approved <span style="font-size:11px;font-weight:400;color:#888">(Target)</span></td>
          <td><span class="badge badge-target">1 = Approved</span><span class="badge badge-target">, 0 = Rejected</span></td>
        </tr>
      </tbody>
    </table>
  </div>


* ## Solution using ML model:
  * In this project i built end-to-end Supervised ML model using kNN, Logistic Regression, Naive Baye's and Decision Tree to predict loan approval. Implemented Binary classification along with EDA, feature engineering & model evaluation using Precision, Recall and f1-score.
  * After applying `GridSearchCV()` on all model we have got this summary:
    </br></br>
    <table>
      <thead>
          <tr>
              <th>Model</th>
              <th>Best Score</th>
              <th>Best Std</th>
              <th>Best Params</th>
          </tr>
      </thead>
      <tbody>
          <tr>
              <td>logistic_regression</td>
              <td>0.717110</td>
              <td>0.040591</td>
              <td>{'C': 100}</td>
          </tr>
          <tr>
              <td>knn</td>
              <td>0.547961</td>
              <td>0.061539</td>
              <td>{'n_neighbors': 3}</td>
          </tr>
          <tr>
              <td>naive</td>
              <td>0.729699</td>
              <td>0.068350</td>
              <td>{'var_smoothing': 0.1}</td>
          </tr>
          <tr>
              <td>decision_tree</td>
              <td>0.982979</td>
              <td>0.015922</td>
              <td>{'ccp_alpha': 0.007291666666666665}</td>
          </tr>
      </tbody>
    </table>
  * The Decision Tree model achieved the highest cross-validation score (0.983) among all evaluated models and was therefore selected as the final model.
  * Recall is prioritized because missing a true defaulter (false negative) leads to direct financial loss for the bank, which is far more costly than wrongly rejecting a creditworthy applicant.
  * - Best Model: Decision Tree
    - Training Accuracy: 99.2%
    - Testing Accuracy: 93.4%
    - Training Recall: 95.5%
    - Testing Recall: 91.5%
  * The model generalizes reasonably well with a testing accuracy of 93.4%, though a small gap between training and testing performance indicates mild overfitting. However, visually, the decision tree look well pruned.
  </br>
  <img width="1790" height="889" alt="image" src="https://github.com/user-attachments/assets/62f6f1aa-f783-49ef-ba29-8425ffb83171" />
