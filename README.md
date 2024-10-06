# The database contains 3 SQL tables: 
- CREDITS: Contains information on each credit. This includes:
            - CreditID: ID of the credit
            - CreditAmount: Amount of the credit in USD
            - CreditDurationMonths: Duration of the credit in months
            - DateofFirstDisbursement: Disbursement date of the credit
            - CreditStatus: Current status of the credit (A: active, C: Completed, D: Defaulted)
            - CreditAgent: Credit agent
            - AnnualInterestRate: Annual interest rate of the credit
            -MonthlyInstallment: Monthly installment amount per credit

- CLIENTS: Contains information regarding each client: This includes:
            - ClientID: ID of the client
            - FirstName: Client's first name
            - LastName: Client's last name
            - BirthDate: Client's birth date
            - Client's gender
            - Client's address state

- CREDITSCHEDULE: tracks the historical payment of each credit's installments. This includes:
            - CreditID: ID of the credit
            - InstallmentIndex: index of the installment (1st installment, 2nd installment)
            - InstallmentDate: installment's due date
            - PaymentDate: Actual payment date of the installment amount

# Semantic Relationships: 
- CLIENTS 1 x * CREDITS: column CLIENTID
- CREDIT 1 x 1 CREDITSCHEDULE: column CREDITID
  
The 3 tables are manipulated using SQL queries (in the Dataset Generation.ipynb file) to generate the 3 excel files (Clients.xlsx, Credits.xlsx, Credit Schedule.xlsx).
The Excel files are then imported in the Exploratory Data Analysis.ipynb file for further analysis
