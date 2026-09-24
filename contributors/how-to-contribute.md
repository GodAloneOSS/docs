# How to Contribute

Every GodAlone Open Source repository follows the same contribution
workflow. This page explains it once; each repo's own `CONTRIBUTING.md`
adds only project-specific setup details on top of this.

```text
Fork
  ↓
Clone
  ↓
Install
  ↓
Create branch
  ↓
Make changes
  ↓
Test
  ↓
Commit
  ↓
Push
  ↓
Create Pull Request
```

## Step by step

1. **Fork** the repository you want to contribute to (top-right "Fork"
   button on its GitHub page).
2. **Clone** your fork:
   ```bash
   git clone https://github.com/YOUR-USERNAME/<repo-name>.git
   cd <repo-name>
   ```
3. **Install** dependencies as described in that repo's README.
4. **Create a branch**: `git checkout -b fix/short-description`
5. **Make your changes.**
6. **Test** your changes — run the test suite if one exists, or verify
   manually per the README.
7. **Commit**: `git commit -m "Fix: short description"`
8. **Push**: `git push origin fix/short-description`
9. **Open a Pull Request** against the original repo's `main` branch,
   filling in the PR template.

## Finding something to work on

Browse issues labeled
[`good first issue`](https://github.com/search?q=org%3AGodAlone+label%3A%22good+first+issue%22+is%3Aopen&type=issues)
across every GodAlone repo — these are picked to be approachable without
deep familiarity with the codebase. Examples of good first contributions:

- Fix a documentation typo
- Improve or add a translation
- Improve accessibility (contrast, alt text, keyboard navigation)
- Add a missing test case
- Improve a README
- Report or fix a broken link

## Code of Conduct

All contributors are expected to follow the
[Code of Conduct](https://github.com/GodAlone/.github/blob/main/CODE_OF_CONDUCT.md)
— respectful, patient, and welcoming, regardless of background or
experience level.

## Questions

Open a GitHub Discussion on the relevant repo, or an issue labeled
`question`. There's no such thing as a silly question.
