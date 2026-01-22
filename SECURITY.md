# 🔐 Security Policy

## Supported Versions

This repository is a **demonstration project** intended for architectural and educational purposes.

Security practices shown here reflect **real-world production standards**.

---

## 🔒 Security Principles Applied

- **Webhook Authentication**
  - All inbound requests require a shared secret via HTTP header:
    ```
    x-webhook-secret
    ```

- **Early Rejection**
  - Unauthorized requests are rejected before any processing occurs.

- **Least Privilege**
  - Only required fields are extracted and passed downstream.

- **Isolation of External Calls**
  - External APIs are only called after validation and classification.

---

## 🔑 Secrets Management

- All secrets in this repository are **DEMO ONLY**
- In production, secrets should be stored using:
  - n8n Credentials Manager
  - Environment Variables
  - Secret Vaults (AWS / GCP / Azure)

🚫 **Never commit real secrets to GitHub**

---

## 🌐 External Endpoints

The following external endpoint is used **only for testing visibility**:

https://webhook.site/6b880026-c28f-4983-b465-c6a84963e1a7


This endpoint does not store sensitive data and is used solely to demonstrate outbound payloads.

---

## 📣 Reporting Security Issues

If this were a real production system, security issues should be reported via a private channel.

For demo purposes, no vulnerability submissions are required.

---

## ✅ Best Practices Reminder

- Rotate secrets regularly
- Use HTTPS only
- Enable rate limiting in production
- Monitor webhook traffic
- Log rejected requests
