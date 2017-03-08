#TheMole

The Mole is a command line interface SQL Injection exploitation tool.
This application, developed in python, is able to exploit both union-based and blind boolean-based injections.

Every action The Mole can execute is triggered by a specific command. All this application requires in order to exploit a SQL Injection is the URL(including the parameters) and a needle(a string) that appears in the server's response whenever the injection parameter generates a valid query, and does not appear otherwise. Note that the vulnerable parameter must be the last one on the URL.

So far, The Mole supports Mysql, Mssql and Postgres, but we expect to include other DBMSs.

https://sourceforge.net/projects/themole/
