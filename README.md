# email-deliverability-setup  — thukool.online


## Project Overview
Configured professional business email for a custom domain with full DNS authentication to ensure inbox delivery and protect against email spoofing.

## What i Configured
- *MX Records* - 3 Zoho Mail servers with priority failover (priority 10, 20, 50)
- *SPF Record* - authorized Zoho Mail servers to send on behalf of the domain
- *DKIM* - digital signature added to verify email authenticity in transit
- *DMARC* - monitoring policy configured to track and report authentication failures

## Tools i Used
- Zoho Mail - business email provider
- Namecheap - domain registrar and DNS management
- MXToolbox - DNS record verification and testing
- mail-tester.com - email deliverability scoring

## Results
- mail-tester.com score: 8.2/10
- SPF, DKIM and DMARC all verified and passing
- Domain not blocklisted
- Emails landing in inbox not spam

## Key Learnings
- Multiple MX records provide failover redundancy for email delivery
- Only one SPF record is allowed per domain multiple SPF records break deliverability
- DKIM uses public/private key cryptography to verify email content integrity
- DMARC ties SPF and DKIM together and defines policy for failed authentication
- Cheaper TLDs like .online have lower trust scores with some spam filters .com recommended for production

## Screenshots

![MX Records](screenshots/Screenshot 2026-05-20 021143.png)
![SPF Record](screenshots/Screenshot 2026-05-20 022604.png)
![DKIM Record](screenshots/Screenshot 2026-05-20 023119.png)
![DMARC Record](screenshots/Screenshot 2026-05-20 024725.png)
