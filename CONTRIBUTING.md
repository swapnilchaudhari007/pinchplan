# Contributing to PinchPlan

Thanks for helping improve **PinchPlan**, a hands-first mixed-reality focus desk for Meta Quest, built with WebXR + Three.js. Bug reports, ideas and pull requests are all welcome.

## Ways to contribute

- Report a bug or suggest an idea in [Issues](https://github.com/swapnilchaudhari007/pinchplan/issues/new/choose)
- Pick up an issue labelled `good first issue` or `help wanted`
- Improve docs, examples or translations
- Review open pull requests

### Reporting a bug

Please include:

- Headset model (Quest 2 / 3 / 3S / Pro) and Meta Quest Browser version
- Input used: hands, controllers or mouse
- Mode: mixed reality (`immersive-ar`), VR fallback (`immersive-vr`) or desktop
- Steps to reproduce, expected vs. actual behaviour
- A short video or screenshot if possible

## Local setup

PinchPlan is a single static `index.html` — no build step, no dependencies to install.

```bash
git clone https://github.com/<your-username>/pinchplan.git
cd pinchplan
python3 -m http.server 8000   # or: npx serve .
# Open http://localhost:8000
```

WebXR needs a secure context. `localhost` works on desktop, but a headset needs HTTPS — use a tunnel such as:

```bash
npx localtunnel --port 8000
```

Then open the HTTPS URL in the Meta Quest Browser and tap **Enter Mixed Reality**.

## Workflow

1. Fork the repo and create a branch: `git checkout -b feat/short-description`
2. Keep each PR focused on one change
3. Use [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `refactor:`, `chore:`
4. Test your change (see checklist below)
5. Open a PR against `main` and fill in the template

## Development guidelines

- **Hands first** — every interaction must work with hand tracking alone; controllers and mouse are fallbacks.
- **Stay seated and comfortable** — no forced locomotion, keep UI within easy reach, avoid flashing or fast motion.
- **Keep it static** — single `index.html`, no build tooling or heavy dependencies; Three.js stays pinned (currently r169).
- **Keep the fallbacks** — `immersive-ar` → `immersive-vr` → desktop must keep working.
- **Local data only** — tasks are stored on the device; don't add network calls, analytics or tracking.
- Plain modern JavaScript (ES modules), 2-space indentation; comment non-obvious math (joint poses, pinch thresholds, raycasting).

## Testing checklist

Before opening a PR, check what applies:

- [ ] Loads without console errors on desktop
- [ ] Quick pinch moves a card to the next lane (Next up → Now → Done)
- [ ] Pinch & drag reorders / moves cards; dragging below the board deletes
- [ ] Pinching the orb starts / pauses the focus timer
- [ ] Left palm up opens the wrist menu
- [ ] Tasks persist after reload
- [ ] Tested on a real Quest headset (mention the model in your PR)

## Areas you can work on

- Hand tracking & pinch gestures
- Passthrough / mixed reality
- Focus timer & tasks
- Desktop (non-XR) fallback
- Performance / comfort
- Accessibility (text size, contrast, one-handed use)

## AI-assisted contributions

AI tools are welcome. You are responsible for every line you submit: review it, test it and say in the PR if AI helped.

## Code of conduct

By taking part you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md).

## Security

Please don't report vulnerabilities in public issues. See [SECURITY.md](SECURITY.md).

## License

By contributing, you agree that your contributions will be licensed under the same license as this project — see [LICENSE](LICENSE).
