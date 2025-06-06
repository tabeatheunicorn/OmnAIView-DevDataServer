# Contribution Guide

Thank you for your interest in contributing to **OmnAIView-DevDataServer**!  
This guide outlines the workflow for submitting contributions.

## 1. Fork the Repository

1. Navigate to the [OmnAIView-DevDataServer repository](https://github.com/AI-Gruppe/OmnAIView-DevDataServer).
2. Click the **Fork** button (top right) to create your own copy of the repository.

## 2. Clone Your Fork

Clone your fork to your local machine:

```sh
git clone https://github.com/YOUR-USERNAME/OmnAIView-DevDataServer.git
cd OmnAIView-DevDataServer
```

## 3. Create a Feature Branch

Before making changes, create a new branch:

```sh
git checkout -b feature/your-feature-name
```

Follow the naming convention:
- `feature/your-feature-name` for new features
- `fix/your-fix-description` for bug fixes
- `docs/update-readme` for documentation updates

## 4. Implement Your Changes

- Follow the project's coding standards.
- Ensure your code is properly formatted and linted.
- Write or update tests if applicable.

## 5. Commit Your Changes

Write meaningful commit messages:

```sh
git add .
git commit -m "Add feature: description of changes"
```

## 6. Push to Your Fork

Push your branch to your fork:

```sh
git push origin feature/your-feature-name
```

## 7. Open a Pull Request

1. Go to the original repository on GitHub.
2. Click **New Pull Request**.
3. Select your fork and branch.
4. Provide a **clear description** of your changes.
5. Submit the pull request.

## 8. Review & Approval

- PRs must be reviewed by at least **two maintainers**.
- Address requested changes by updating your branch and pushing updates.
- Once approved, the PR will be merged.

## 9. Keep Your Fork Updated

To stay up to date with the latest changes:

```sh
git checkout main
git fetch upstream
git merge upstream/main
git push origin main
```

## 10. Reporting Issues

If you find a bug or have a feature request, please open an [issue](https://github.com/AI-Gruppe/OmnAIView-DevDataServer/issues) and describe it clearly.

---

🚀 **Happy coding!** If you have any questions, feel free to ask in [Discussions](https://github.com/AI-Gruppe/OmnAIView-DevDataServer/discussions).

