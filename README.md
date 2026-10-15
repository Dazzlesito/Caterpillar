# Caterpillar

**English** | [Español](README.es.md)

A collaborative project maintained by a small team using a **simplified GitHub Flow** workflow.

## Team

| Member | GitHub | Role |
| --- | --- | --- |
| Andrés Cortés | [@Dazzlesito](https://github.com/Dazzlesito) | Maintainer |
| Robinson Bastidas | [@Xavyer77](https://github.com/Xavyer77) | Collaborator |
| Daniela Peña | [@danilops018](https://github.com/danilops018) | Collaborator |

---

## Workflow: Simplified GitHub Flow

GitHub Flow is a lightweight, branch-based workflow. With a small team of three, we keep it as simple as possible:

- **`main` is always deployable and stable.** Never commit directly to `main`.
- **All work happens in short-lived feature branches.**
- **All changes reach `main` through a Pull Request (PR)** reviewed by at least one teammate.

### Step by step

#### 1. Sync your local `main`

Always start from the latest version of the project:

```bash
git checkout main
git pull origin main
```

#### 2. Create a feature branch

Give your branch a short, descriptive name. Use one of these prefixes:

- `feature/` — new functionality (e.g. `feature/login-page`)
- `fix/` — bug fixes (e.g. `fix/navbar-overflow`)
- `docs/` — documentation only (e.g. `docs/setup-guide`)
- `chore/` — maintenance, tooling, config (e.g. `chore/update-dependencies`)

```bash
git checkout -b feature/login-page
```

#### 3. Commit your changes

Make small, focused commits following our [commit convention](#commit-message-convention):

```bash
git add <files>
git commit -m "feat: add login form validation"
```

#### 4. Push your branch to GitHub

```bash
git push -u origin feature/login-page
```

#### 5. Open a Pull Request

1. Go to the repository on GitHub and open a **Pull Request** from your branch into `main`.
2. Use a clear title and describe **what** changed and **why**. Link any related issue.
3. Request a review from one of your teammates. **A PR must be reviewed and approved by at least one other team member before merging** — even if it is a small change.

> Tip: open the PR as a *Draft* if your work is not finished yet, so teammates can see your progress and leave early feedback.

#### 6. Review and address feedback

- The reviewer leaves comments, approves, or requests changes.
- Push additional commits to the **same branch** to address the feedback — the PR updates automatically.
- Keep the conversation kind and concrete: comment on the code, not the person.

#### 7. Merge and clean up

- Once approved and the CI checks pass (if any), **squash and merge** into `main` so each PR becomes a single clean commit.
- **Delete the branch** after merging (GitHub offers this button right after merging).
- Update your local copy:

```bash
git checkout main
git pull origin main
git branch -d feature/login-page
```

### Quick rules

1. `main` is protected — no direct pushes.
2. One branch per task/feature.
3. At least **1 approval** required to merge.
4. Squash and merge; delete branches after merging.
5. Pull before you start, and pull before you push.

---

## Commit Message Convention

We follow the **Conventional Commits** style. Every commit message has this structure:

```
<type>(<optional scope>): <short description in imperative mood>

<optional body>

<optional footer(s)>
```

### Types

| Type | When to use it |
| --- | --- |
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation only changes |
| `style` | Changes that do not affect the meaning of the code (formatting, spaces, etc.) |
| `refactor` | A code change that neither fixes a bug nor adds a feature |
| `perf` | A code change that improves performance |
| `test` | Adding or correcting tests |
| `chore` | Maintenance tasks, dependencies, tooling, config |

### Examples

```bash
feat: add user authentication API
feat(auth): support OAuth login with GitHub
fix: prevent crash when cart is empty
docs: explain PR review process in README
chore: configure ESLint and Prettier
```

### Rules of thumb

- Use the **imperative mood**: "add", not "added" or "adds" ("add feature", as if giving an order).
- Keep the description **lowercase** and without a trailing period.
- Limit the first line to **~50 characters**; use the body for extra detail.
- Reference issues in the footer when relevant, e.g. `Closes #12`.

---

## Getting started (local setup)

```bash
# Clone the repository
git clone https://github.com/Dazzlesito/Caterpillar.git
cd Caterpillar

# Create your first branch and start working
git checkout -b feature/my-first-task
```
