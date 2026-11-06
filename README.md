# Tax Signal Screen

**Live demo:** https://lulumypb-eng.github.io/tax-signal-screen/

A research prototype that ranks US public companies' latest 10-K filings for misstatement risk against similar-size peers, using public SEC data. Each company shows its percentile rank, its rank history since fiscal 2019, and the reported numbers that moved its rank, including tax signals such as the book–tax gap.

**This is a screening aid, not an allegation.** A high rank means a company's numbers resemble those of companies the SEC later charged with misstating accounts. Most highly ranked companies have done nothing wrong.

## Accuracy
Tested out of sample on fiscal 2015–2020: AUC 0.67. The top 10% of scores contained 22% of later SEC enforcement cases (18 of 81). Useful for deciding where to look first, not a substitute for audit judgment.

## Data and method
- SEC Financial Statement Data Sets (XBRL), 10-K filings, fiscal 2009–2024
- Labels: SEC Accounting and Auditing Enforcement Releases
- Model: RUSBoost on reported line items, accounting and tax ratios, and Beneish M-score indexes; reasons via a surrogate model and SHAP values

## Author
Pelumi K. Bello, based on her working paper "Do Tax Signals Improve Machine-Learning Detection of Accounting Fraud?" Feedback and pilot partners welcome: [bellopelumi@gmail.com] · [linkendin.com/pelumibello]
