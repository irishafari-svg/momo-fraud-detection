# Mobile Money Fraud Detection

Problem: Mobile money fraud causes losses for users, telcos, and banks in Ghana.

Data: Data: Synthetic MoMo-style transactions, 20,000 rows, PaySim-style. Used due to data bundle limits, same columns and fraud patterns as PaySim.

Model: Random Forest classifier to flag fraud. Focus on recall for fraud, not just accuracy.

Status: In progress. Building in Google Colab as part of my Master of AI and Applied Data Science at GEM Alpine Business School, Batch 7.

## What I am building

1. Load and explore PaySim data
2. Find which transaction types have the highest fraud rate
3. Train a baseline model
4. Evaluate with confusion matrix and feature importance
5. Share results and chart here

## Results

## Results

Test set: 4000 transactions, 38 frauds.

Confusion matrix:
- Legit correctly called legit: 3962
- Legit wrongly called fraud: 0
- Fraud missed: 19
- Fraud correctly caught: 19

Fraud precision: 1.00, Fraud recall: 0.50, Fraud F1: 0.67

What I found:
1. Fraud is concentrated in TRANSFER at 2.07% and CASH_OUT at 1.87%.
2. Amount alone does not catch fraud. The top signals are sender_emptied at 26.7% and newbalanceOrig at 25.3%. Fraud empties the sender account.
3. Model has perfect precision with zero false alarms, but only catches 50% of frauds. Next step is to improve recall.
![Fraud rate by transaction type](fraud_rate.png)

## Author

Irish Mintah-Afari | GEM Alpine Business School | Batch 7
