Documentation and Handover:

* Create a brief document or README file that explains your approach, component structure, and how the automation aligns with the PDD.
* Explain how your solution would fit into an agile sprint (e.g., "This automation would be the output of a single sprint, with initial user story mapping and testing done in the sprint."). (PA0702, IAC0705)

======================================================================================================
RPA Fraud Detection Dataset - README
* Generated: 2025-09-15 20:45:45 UTC
* 
* Contents of this package:
* \- Daily\_Transactions.xlsx      : Main dataset of rapid transfers to be processed by the RPA bot.
* &#x20; Columns: TransactionID, Date, SenderAccount, RecipientAccount, Amount, Currency, TransferType, Country, Verified, Description
* &#x20; Notes: Amounts are in ZAR. Several rows intentionally meet 'high-risk' criteria:
* &#x20;   - Amount > R10,000
* &#x20;   - TransferType == 'International'
* &#x20;   - Verified == 'No'
* &#x20;   - RecipientAccount is included in Suspicious\_Accounts.csv
* 
* \- Suspicious\_Accounts.csv      : List of recipient account numbers flagged for suspicious activity. Use this list to check whether a transaction's recipient is suspicious.
* 
* \- Transaction\_Report\_Template.pdf : PDF template with placeholders (e.g., {TransactionID}). Bots should replace placeholders and save per-transaction PDFs named Report\_<TransactionID>.pdf
* 
* Usage suggestions for the assessment:
* \- Read Daily\_Transactions.xlsx as the input source.
* \- Cross-check RecipientAccount values against Suspicious\_Accounts.csv.
* \- Flag transactions where any of the following are true:
* &#x20;   \* Amount > 10000
* &#x20;   \* TransferType == 'International'
* &#x20;   \* Verified == 'No'
* &#x20;   \* RecipientAccount in Suspicious\_Accounts.csv
* &#x20; Concatenate reasons into the 'Reason' field in the summary CSV, e.g., 'Amount > R10,000 | International | Not Verified'.
* 
* \- For compliance, mask account numbers in logs and generated PDFs (e.g., 62000\*\*\*\*\*1234).
* 
* Files in this folder were created for educational use and do NOT contain any real personal data.
==================================================================================================
* 

