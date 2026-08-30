# PASTA Threat Modeling – Sneaker Marketplace Application

## Overview

This project demonstrates a threat modeling analysis of a sneaker marketplace application using the **PASTA (Process for Attack Simulation and Threat Analysis)** framework.

The analysis identifies the application's business objectives, technologies, potential threats, vulnerabilities, attack paths, and security controls.

## PASTA Stages

### Stage I – Business and Security Objectives

* Protect users' personal and payment information.
* Provide secure account sign-up and login.
* Follow industry regulations for protecting payment and personal information.

### Stage II – Technical Scope

The application uses:

* Application Programming Interface (API)
* Public Key Infrastructure (PKI)
* SHA-256
* Structured Query Language (SQL)

**Priority:** SQL and SHA-256 were prioritized because they are directly involved in storing and protecting sensitive user information. SQL injection could expose database information, while weaknesses in password hashing could expose user credentials.

### Stage III – Application Decomposition

The application processes information between users, the mobile application, APIs, encryption systems, and the SQL database.

Sensitive information should be protected during transmission and storage, while database access should require proper authentication and authorization.

### Stage IV – Threat Analysis

Identified threats include:

1. SQL injection attacks targeting the application database.
2. Credential theft or phishing used to gain unauthorized access to user accounts.

### Stage V – Vulnerability Analysis

Identified vulnerabilities include:

1. Poor input validation that could allow SQL injection.
2. Weak password storage or authentication controls.

### Stage VI – Attack Modeling

**Primary attack goal:** Gain unauthorized access to sensitive user information.

Possible attack paths include:

* Exploit SQL injection → access database → steal user data.
* Steal user credentials → access account → obtain personal information.

### Stage VII – Risk Analysis and Security Controls

Recommended security controls:

1. **Parameterized SQL queries** to help prevent SQL injection.
2. **Strong password hashing** to protect user credentials.
3. **Encryption** to protect sensitive information.
4. **Access controls and least privilege** to limit unauthorized access.

## Skills Demonstrated

* PASTA threat modeling
* Threat identification
* Vulnerability analysis
* Attack modeling
* Risk analysis
* Application security
* Database security
* Access control
* Data protection

## Disclaimer

This project was completed as part of cybersecurity coursework and is intended for educational and portfolio purposes.
