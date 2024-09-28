# Task-Fifteen: SQL Injection Vulnerabilities in DVWA

## Overview

This repository contains the setup steps, exploitation process, and solutions for SQL Injection vulnerabilities at various security levels (low, medium, and high) in Damn Vulnerable Web Application (DVWA). The task was completed as part of an educational project aimed at understanding and demonstrating SQL Injection attacks.

## Contents

1.SQL Injection Vulnerabilities Report

A detailed report explaining the process of setting up DVWA using PentestLab, and solving the SQL Injection labs at different security levels (low, medium, and high). The report includes:

 - Steps for cloning and starting DVWA
   
 - Exploitation techniques for SQL Injection vulnerabilities
   
 - Screenshots and code snippet

2.Steps to Install and Start DVWA
Instructions on how to clone and use the pentestlab repository to set up DVWA, including accessing the web application, logging in, and adjusting security levels.

## Installation

To set up DVWA and start testing for SQL Injection vulnerabilities, follow these steps:

1.Clone the PentestLab Repository:

`git clone https://github.com/eystsen/pentestlab.git`

2.Navigate to the PentestLab Directory:

`cd pentestlab`

3.List Available Labs:

`./pentestlab.sh list`

4.Start DVWA:

`./pentestlab.sh start dvwa`

5.Access DVWA:

Open your browser and go to:
`http://127.8.0.1`

6.Login to DVWA:

Use the following credentials:

 Username: admin
 
 Password: password
 
7.Set the Security Level:

Adjust the security level (low, medium, or high) in the DVWA Security tab.

## Exploitation Techniques

1.Low Security Level:

Simple SQL Injection techniques were used to retrieve user data by injecting payloads like` 1' OR '1'='1'#`.

2.Medium Security Level:

Burp Suite was used to intercept and modify requests, allowing for SQL Injection by altering POST requests with payloads like `1 UNION SELECT user, password FROM users`.

3.High Security Level:

More advanced SQL Injection techniques were employed using payloads like `1' UNION SELECT user,password from users #` to bypass security filters and extract sensitive information.

