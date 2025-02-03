# Contributing to HabiTrack

Thanks for your interest in contributing to **HabiTrack**! We appreciate your help in improving this project. Please take a moment to review this document before submitting your contributions.

## Table of Contents

1. [Code of Conduct](#code-of-conduct)  
2. [How Can I Contribute?](#how-can-i-contribute)  
   - [Reporting Bugs](#reporting-bugs)  
   - [Suggesting Features or Enhancements](#suggesting-features-or-enhancements)  
   - [Pull Requests](#pull-requests)  
   - [Documentation Improvements](#documentation-improvements)  
3. [Development Workflow](#development-workflow)  
   - [Project Setup](#project-setup)  
   - [Branch Organization](#branch-organization)  
   - [Commit Message Guidelines](#commit-message-guidelines)  
4. [Code Style & Testing](#code-style--testing)  
5. [Licensing](#licensing)  
6. [Community & Support](#community--support)

---

## Code of Conduct

All contributors and participants in this project must abide by our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it to understand the expectations for our community.

---

## How Can I Contribute?

### Reporting Bugs

1. **Check if the issue is already reported**  
   - Look through [open issues](https://github.com/king04aman/HabiTrack/issues) before creating a new one.

2. **Create a new issue**  
   - Provide a clear and descriptive title.  
   - Include steps to reproduce the bug and any relevant logs or screenshots.  
   - Specify your operating system, environment, and version of HabiTrack, if applicable.

### Suggesting Features or Enhancements

We welcome your ideas on how to make HabiTrack better!

1. **Check existing feature requests**  
   - If a similar request exists, add your comments or additional details there.

2. **Open a feature request**  
   - Clearly describe the problem you’re trying to solve.  
   - Suggest how you imagine a solution might look.  
   - If possible, outline potential approaches or relevant technologies.

### Pull Requests

1. **Open an Issue First**  
   - For major changes or new features, please open a discussion issue first. This helps us provide feedback and guide you in the right direction.

2. **Fork the Repo**  
   - Fork [HabiTrack](https://github.com/king04aman/HabiTrack) and create a feature branch on your fork.

3. **Create Your Pull Request**  
   - Ensure your PR title and description clearly indicate the purpose and scope.  
   - Reference any related issues (e.g., “Closes #XX” or “Fixes #XX”).  
   - Provide testing instructions and relevant screenshots.

4. **Code Reviews**  
   - Project maintainers or other contributors will review your code.  
   - Please be open to feedback and be prepared to make revisions.

### Documentation Improvements

- If you spot any typos, grammar issues, or outdated information in the README, Wiki, or other docs, feel free to open a PR directly.  
- For more significant documentation overhauls, consider opening an issue to discuss proposed changes.

---

## Development Workflow

### Project Setup

**Backend**  
```bash
git clone https://github.com/king04aman/HabiTrack.git
cd HabiTrack/backend
npm install
npm run dev
```

**Desktop**  
```bash
cd HabiTrack/desktop/electron-app
npm install
npm start
```

**Mobile**  
```bash
cd HabiTrack/mobile
npm install
npm run android  # or npm run ios
```

*(Adjust accordingly as the project evolves.)*

### Branch Organization

1. **`main`**  
   - Production-ready, stable code.  

2. **`dev`** (or `development`)  
   - Main active development branch where new features are integrated before release.  

3. **Feature Branches**  
   - Create feature branches off `dev` (e.g., `feature/mobile-lock-screen`, `bugfix/activity-logging`).  
   - Merge feature branches back into `dev` via pull requests.

### Commit Message Guidelines

- **Format**:  
  ```
  type(scope): short description

  [optional body describing the commit in detail]

  [optional footer referencing issues]
  ```

- **Examples**:  
  ```
  feat(mobile): add basic phone lock feature
  fix(backend): correct null pointer in user activity handler
  docs: update README installation steps
  ```

- **Types**:
  - **feat**: A new feature  
  - **fix**: A bug fix  
  - **docs**: Documentation-only changes  
  - **style**: Changes that do not affect the code meaning (whitespace, formatting)  
  - **refactor**: Code changes that neither fix a bug nor add a feature  
  - **perf**: Performance improvements  
  - **test**: Adding or updating tests  
  - **chore**: Other changes that do not modify source or test files  

---

## Code Style & Testing

- **Linting & Formatting**:  
  - If using ESLint or Prettier, run them before submitting your PR.  
  - Ensure code is consistent with the project’s established style.

- **Testing**:  
  - Add or update tests (unit, integration, end-to-end) where appropriate.  
  - Make sure existing tests pass before opening a PR.  

*(Testing details may be added or updated as the project grows.)*

---

## Licensing

HabiTrack is licensed under **GPLv3**.  
By contributing to HabiTrack, you agree that your contributions will be licensed under the project’s existing GPLv3 license.

---

## Community & Support

- **Issue Tracker**: [GitHub Issues](https://github.com/king04aman/HabiTrack/issues)  
- **Discussions**: [GitHub Discussions](https://github.com/king04aman/habitrack/discussions)  
- **Contact**: See [README](README.md#support--contact) for direct contact details.

We truly appreciate your time and effort in contributing. Thank you for making **HabiTrack** better for everyone!
