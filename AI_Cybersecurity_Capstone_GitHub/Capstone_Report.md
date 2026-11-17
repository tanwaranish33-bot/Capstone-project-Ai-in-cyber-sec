# Mini AI Cybersecurity Assistant – Capstone Report

**Course:** ENSP355 – AI in Cyber Security  
**Institution:** K.R. Mangalam University  
**Experiment:** Capstone – Mini AI Cybersecurity Assistant in Google Colab  
**Student:** ____________________  **Roll No.:** ____________________  
**Faculty:** ____________________  **Date:** ____________________

## 1. Aim and problem statement
The aim is to build a guided AI-assisted cybersecurity prototype that accepts a sample message and a login-activity record. It checks suspicious keywords, uses a Decision Tree and a small neural network, explains the results, masks sensitive identifiers, assigns a risk level and recommends a safe action with human-review guidance.

The implementation follows the capstone workflow: input and privacy, rule-based threat detection, Decision Tree, neural network, explanation, and response. All data included with this submission is synthetic and intended only for classroom use.

## 2. Dataset and preparation
Two CSV files are provided: `messages.csv` contains sample messages and their teaching categories; `login_activity.csv` contains sanitized account identifiers, IP addresses, email addresses, four numeric login features and a Normal/Suspicious target label. The notebook checks missing values, converts numeric fields, fills missing numeric values with medians and constrains hour/device values to valid ranges.

The notebook masks email addresses, IP addresses and account IDs before presenting results. Raw identifiers are retained only in the local synthetic source CSV to demonstrate masking and should never be replaced with real personal or institutional records.

## 3. Methodology
### Rule-based module
A transparent keyword detector checks for phishing, malware and ransomware indicators. It returns a category, matched words and a keyword score. The rule output is evidence for review, not proof of an attack.

### Decision Tree
A Decision Tree is trained using `failed_logins`, `login_hour`, `new_device` and `download_mb`. The data is split into training and testing subsets. The notebook reports test accuracy, a classification report, confusion matrix and feature-importance chart.

### Neural network
A small feed-forward MLP neural network is trained on standardized numeric features. Its class prediction and probability are compared with the Decision Tree. The comparison is useful because model disagreement can indicate uncertainty and trigger human review.

### Integrated response
The assistant combines the rule category, tree prediction, neural prediction and numeric warning thresholds. Numeric reasons include at least five failed logins, a new device, login before 06:00 or after 22:00, and a download of at least 500 MB. Risk is assigned as Low, Medium or High. Human review is requested for High risk, disagreement between the two models or confidence below 0.70. The recommended action is cautious and does not automatically block or punish a user.

## 4. Demonstration scenarios and observations
Five scenarios are run in the notebook:
1. Normal message and normal login.
2. Urgent account-verification message, demonstrating phishing indicators.
3. Repeated failed logins on a new device.
4. Large download at an unusual time.
5. A baseline/low-warning case used to demonstrate confidence and model-agreement checks.

The executed notebook contains the detailed comparison table for every scenario, including matched keywords, Decision Tree and neural predictions, confidence values, numeric reasons, risk, recommended action and human-review status. It also generates a risk-level chart and feature-importance chart. Refer to those live notebook outputs when completing the lab-file screenshots.

## 5. Privacy, responsible use and human review
- Use only synthetic or sanitized data.
- Mask email, IP and account identifiers in screenshots and exports.
- Do not open suspicious links, execute malware, scan networks or test live accounts.
- Treat all model outputs as decision support rather than proof.
- Escalate high-risk, conflicting or low-confidence cases to an authorized analyst.
- Do not take automatic punitive action based on this classroom prototype.

## 6. Limitations
The datasets are small synthetic examples and cannot represent the diversity of real cybersecurity events. Accuracy on this sample is not a measure of production readiness. Keyword rules may miss new phishing language or flag harmless text. A small neural network may overfit, and confidence values are not guarantees. Feature importance describes model behaviour but does not establish causation. The prototype has no access to threat intelligence, identity verification or live telemetry.

## 7. Conclusion
The capstone integrates a rule-based detector, a supervised Decision Tree, a small neural network, feature explanations, privacy masking and a responsible response workflow. The five scenarios demonstrate how multiple sources of evidence can support a cautious risk assessment. The system is for educational demonstration only; real security incidents require validated systems and authorized human investigation.

**Submission note:** Run all cells in `Mini_AI_Cybersecurity_Assistant.ipynb`, save the executed notebook, and include its screenshots and shareable Colab link in the final lab submission.
