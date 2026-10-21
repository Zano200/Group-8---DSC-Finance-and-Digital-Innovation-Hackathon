Suspicious Transaction Detection System

🏆 1st Place – DSC Finance & Digital Innovation Hackathon 2026 Sol Plaatje University Data Science Club, sponsored by Standard Bank (July 2026) · Team: Group 8

An end-to-end fraud detection system that flags suspicious mobile money transactions, explains why each one was flagged, and presents the results in a dashboard that a fraud team could act on.

The problem

Mobile money fraud is rare but expensive. In our dataset of 636,262 transactions, only 0.13% were fraudulent, so a model that labels everything as "not fraud" is 99.87% accurate and completely useless. The challenge was to catch as much fraud as possible without burying analysts in false alarms.

Approach
Data cleaning and EDA to understand transaction types, amounts and balance behaviour around fraud cases
Feature engineering on balance changes and transaction patterns
Handling class imbalance with imbalanced-learn
Modelling with XGBoost, evaluated with PR-AUC (better suited than accuracy or ROC-AUC for rare events)
Cost-based decision threshold, chosen by weighing the cost of a missed fraud against the cost of a false alarm
Explainability with SHAP, so every flagged transaction comes with the reasons behind it
Power BI dashboard and a Tkinter app demo to present results to non-technical users
Results
Metric	Result
Fraud cases caught (recall)	91.2%
Missed-fraud rate	8.8%
PR-AUC	0.594 (random baseline ≈ 0.001)
What's in this repo

Group 8 - DSC Finance and Digital Innovation Hackathon.zip contains:

📊 PowerPoint presentation
📈 Power BI dashboard (screenshot, as the .pbix was too large to upload)
📄 Word report
🐍 Python notebook (full analysis and modelling)
🖥️ Tkinter app demo


Tools

Python · Pandas · NumPy · Scikit-learn · XGBoost · imbalanced-learn · SHAP · Matplotlib · Seaborn · Power BI · Tkinter
