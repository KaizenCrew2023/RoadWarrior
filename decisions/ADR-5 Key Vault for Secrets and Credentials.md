# ADR 5: Key Vault for Secrets and Credentials

## Context

Road Warrior's users can authorise it to access their email accounts and scan travel-related emails for new reservations. They can also share trip information with people directly from the Road Warrior app and trip dashboard via messaging and social media platforms. Safeguarding access to its users' accounts and sensitive information is critical to Road Warrior's long-term success. 

## Decision

We will use key vaults for securing and managing secrets and credentials.

## Status

Accepted

## Consequences

Positive:

* **Security** - provides a secure and centralised location to store sensitive data, such as secrets and credentials for integrating third-party services and storing authentication/authorsation tokens for users' email accounts.
* **Access controls** - fine-grained access control to ensure only authorsed individuals or systems can read, write and manage secrets and access sensitive information.
* **Scalable** - key vaults are scalable and many cloud-based providers offer multi-region replication.
* **Simplifies secrets management** - most providers offer programmable APIs and tools for simple secret retrieval and management.

Negative: 

* **Incurs cost (if using a cloud service)** - considered to be an acceptable trade-off to safeguard users' accounts.  
