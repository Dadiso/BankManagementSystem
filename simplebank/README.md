# Simple Bank

- Create and manage bank accounts.
- Record all balance changes to each of the accounts.
- Perform a money transfer between 2 accounts.

The programming language we will use to develop the service is mainly Golang. The goals are divided into 3 parts:

1. Design a database, generate codes to talk to the DB in a consistent and reliable way using transactions, understand the DB isolation levels, and how to use it correctly in production. I will also use docker for local development, use Git to manage codes, and use Github Action to run unit tests automatically.

2. Build a set of RESTful HTTP APIs using Gin 

3. Build the app with Docker and deploy it to a production Kubernetes cluster on AWS. 

## Simple bank service

The service is a simple bank. It will provide APIs for the frontend to do following things:

1. Create and manage bank accounts, which are composed of owner’s name, balance, and currency.
2. Record all balance changes to each of the account. So every time some money is added to or subtracted from the account, an account entry record will be created.
3. Perform a money transfer between 2 accounts. This should happen within a transaction, so that either both accounts’ balance are updated successfully or none of them are.

