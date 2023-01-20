# Entity model

We should have: Operation, Account, Users, (AnalysisResult).

Operation should have :
 - a linked account (acc number col: 0 + acc name: 2)
 - a linked counterpart Account (acc number col: 12 + acc name col: 14)
 - a date (col: 5)
 - a description (col: 6)
 - an amount (col: 8)
 - a communication (col: 16 OR 17)

Account should have :
- a name
- an account number

Users should have :
 - a username
 - a password
 - (permissions?)
 - ref to file repository


