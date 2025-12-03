Self-hosted contact form (Express + Nodemailer)

What this adds
- `server.js`: Express server that exposes POST /send and forwards the message to your email via SMTP (nodemailer).
- `package.json`: dependencies and start script.
- `.env.example`: environment variables required for SMTP credentials and recipient email.

Quick start (local)
1. Copy `.env.example` to `.env` and fill in your SMTP details and desired recipient email.
2. Install dependencies:

```bash
npm install
```

3. Start the server:

```bash
npm start
```

4. Open the site in your browser:

http://localhost:3000/portfolio_website.html

Notes and security
- For Gmail, you must use an App Password (if using 2FA) and set SMTP_HOST=smtp.gmail.com, SMTP_PORT=465 and SMTP_SECURE=true.
- Keep your `.env` out of version control. Do not commit credentials.
- Consider using a transactional email provider (SendGrid, Mailgun) with an API key for better deliverability.

If you want, I can update the repo to serve the site from a `public/` folder and move `portfolio_website.html` there.
