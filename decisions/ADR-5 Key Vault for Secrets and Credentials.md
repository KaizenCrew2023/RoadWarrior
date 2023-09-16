# ADR 5: Key Vault for Secrets and Credentials

## Context

Road Warrior's users can authorise it to access their email accounts to scan travel-realted emails for new reservations. They can also share trip information with people directly from the Road Warrior app and trip dashboard via messaging and social media platforms. Safeguarding access to its users' accounts and sensitive information is critical to Road Warrior's long-term success. 

## Decision

We will use key vaults for securing and managing secrets and credentials.

## Status

Proposed

## Consequences

Positive:

* **Security**
* **Access controls**
* **Scalable**
* **Simplifies secrets management**

Negative: 

* **Incurs cost** - considered to be an acceptable trade-off to safeguard users' accounts.  
