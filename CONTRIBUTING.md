# Contributing to PinchPlan

Thanks for helping improve **PinchPlan**, a hands-first mixed-reality focus desk for Meta Quest, built with WebXR.

## Ways to contribute

- Report a bug or suggest an idea in [Issues](https://github.com/swapnilchaudhari007/pinchplan/issues/new/choose)
- Pick up an issue labelled `good first issue` or `help wanted`
- Improve docs, examples or translations
- Review open pull requests

## Local setup

```bash
git clone https://github.com/<your-username>/pinchplan.git
cd pinchplan
# No build step
npx serve .   # WebXR needs a secure context: use localhost or HTTPS
# Open the URL in the Meta Quest Browser and enter mixed reality
```

## Workflow

1. Fork the repo and create a branch: `git checkout -b feat/short-description`
2. Keep each PR focused on one change
3. Use [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `refactor:`, `chore:`
4. Open a PR against `main` and fill in the template

## Areas you can work on

- Hand tracking & pinch gestures
- Passthrough / mixed reality
- Focus timer & tasks
- Desktop (non-XR) fallback
- Performance / comfort

## AI-assisted contributions

AI tools are welcome. You are responsible for every line you submit: review it, test it and say in the PR if AI helped.

## Code of conduct

By taking part you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md).

## Security

Please don't report vulnerabilities in public issues. See [SECURITY.md](SECURITY.md).
