Problem statement (real-world):
Banks want to flag potentially fraudulent transactions in real-time. This simplified app loads a small
transaction stream from stdin, computes basic user-level features (avg txn amount, txn frequency, time-of-day patterns)
and applies a lightweight rule-based + statistical anomaly detector to rank suspicious transactions.

Input: lines of transactions: tx_id user_id timestamp(ISO8601) amount merchant_category
Output: for each transaction, print score (0-1) and reason summary for top suspects.

Sample:
1 user1 2025-09-01T10:02:00 120.50 electronics
2 user1 2025-09-01T10:03:00 5000.00 jewelry

How to run:

ython3 fraud_detector.py < tx_stream.txt.
