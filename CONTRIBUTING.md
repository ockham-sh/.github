# Contributing to Ockham

Thanks for your interest in contributing. This guide covers the workflow shared across the Ockham repositories. Some repos add their own `CONTRIBUTING.md` with project-specific setup (dev environment, test commands, architecture rules); when one is present, follow it for the details and treat this as the common baseline.

## Ground rules

- Be respectful. All participation is covered by our [Code of Conduct](https://github.com/ockham-sh/.github/blob/main/CODE_OF_CONDUCT.md).
- Search existing issues and discussions before opening a new one.
- Keep changes focused: one logical change per pull request.

## Workflow

1. Fork the repository and create a feature branch.
2. Make your change, with tests where it makes sense.
3. Run the repo's checks locally (lint, type check, tests) before pushing. The same checks run in CI and must pass.
4. Use clear, conventional commit messages (`feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`).
5. Open a pull request describing what changed and why. A maintainer will review it.

## Licensing of contributions

- The **parsimony** data stack (`parsimony-core`, `parsimony-connectors`, `parsimony-agents`) is Apache-2.0. By contributing, you agree your contribution is licensed under Apache-2.0.
- **Ockham Terminal** is open-core (an AGPL-3.0 core plus a separately-licensed enterprise edition) and requires accepting a Contributor License Agreement before a contribution can be merged. See that repository's `CONTRIBUTING.md` and `CLA.md`.

## Security

Please do not report security issues in public issues. See our [security policy](https://github.com/ockham-sh/.github/blob/main/SECURITY.md) or email security@ockham.sh.

## Questions

Open a GitHub Discussion on the relevant repository. We are happy to help.
