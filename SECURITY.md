# Security Policy

## Supported versions

Only the latest code on `main` is supported.

## Reporting a vulnerability

**Please don't open a public issue.** Use the repo's **Security** tab → **Report a vulnerability**, or contact [@swapnilchaudhari007](https://github.com/swapnilchaudhari007).

Include a description, the impact, steps to reproduce and any suggested fix. You'll get an acknowledgement within 72 hours and an initial assessment within 7 days. Reporters are credited unless they'd rather stay anonymous.

## What we especially care about in PinchPlan

- **Camera / passthrough data:** any code that captures or sends room or hand-tracking data off the device
- **XSS:** task text rendered without escaping
- **Comfort issues:** changes that could cause motion sickness (forced camera movement, flicker)

## For contributors

- Never commit secrets: use `.env` files (git-ignored) or GitHub Actions secrets
- Keep real personal data out of code, tests, issues and screenshots
- Treat all user input, and anything passed to an AI model, as untrusted
