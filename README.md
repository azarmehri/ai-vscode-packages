# ai-vscode-packages

This repository includes a GitHub Actions workflow that downloads the latest VSIX packages and publishes them to the repository release page.

## Workflow

- File: `.github/workflows/download-vscode-packages.yml`
- Triggers:
  - Manual run (`workflow_dispatch`)
- Downloads:
  - OpenAI ChatGPT extension package
  - Anthropic Claude Code extension package
- Publishes assets to a release tag: `vscode-packages-latest`

## Notes

- The workflow requires `contents: write` permission so it can create/update releases.
- Existing release assets with the same names are replaced on each run.
