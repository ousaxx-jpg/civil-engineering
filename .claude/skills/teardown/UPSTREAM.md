# Upstream

Vendored from https://github.com/elvarofficial/teardown (MIT) at commit `a91262ac1109051e014662d42ecb0b7bc1f113b1`.

- `docs/` (14 MB of demo GIFs) is not vendored; README image links point to the upstream copies.
- `node_modules/` is not committed. Run `npm install` in this folder before first use.
- In Claude Code on the web, Chromium is pre-installed: skip `npx playwright install chromium` and set
  `CHROMIUM=/opt/pw-browsers/chromium` if capture complains about a missing browser.
