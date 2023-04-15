# Entity model

We should have: Operation, Account, Users, (AnalysisResult).

Operation should have :
 - an id
 - a linked user (the user currently connected)
 - a linked counterpart Account (acc number col: 12 + acc name col: 14)
 - a date (col: 5)
 - an operation type (col: 6)
 - an amount (col: 8)
 - a communication (col: 16 OR 17)

Account should have :
- an id
- a name
- an account number
- a list of Operation

Users should have :
 - an id
 - a username
 - a password
 - an Account
 - (permissions?)
 - ref to file directory


