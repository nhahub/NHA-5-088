# Contributing to FlightLens

How the team works in this repository. Every change goes through a branch and a pull request, so `main` always holds reviewed, working work.

---

## 1. Workflow

1. **Update `main`:** `git checkout main` then `git pull`
2. **Create a branch** for one task (see the naming rules below)
3. **Commit** your work in small, clear steps
4. **Push the branch:** `git push -u origin <branch-name>`
5. **Open a pull request** into `main` and fill in the description
6. **Review:** another team member reviews and approves it
7. **Merge** after approval, then delete the branch

Nobody pushes directly to `main`.

---

## 2. Branch names

Format: `<type>/<short-description>` in lowercase with hyphens.

| Type | Use for | Example |
|---|---|---|
| `feature/` | new functionality | `feature/silver-cleaning` |
| `fix/` | a bug fix | `fix/overnight-arrival-date` |
| `docs/` | documents and READMEs | `docs/design-phase` |
| `test/` | tests only | `test/gold-quality-checks` |
| `chore/` | setup and configuration | `chore/docker-compose` |

---

## 3. Commit messages

* Start with a verb in the imperative: **Add, Fix, Update, Remove, Rename, Refactor**
* Keep the first line under about 50 characters, with no period at the end
* Say **what changed**, not just which file: `Fix 2400 departure time conversion`, not `Update main.py`
* For bigger changes, leave a blank line and list the details as bullet points

Examples:

```text
Add monthly BTS download script
Fix cancelled flights counted as on time
Add star schema DDL for the Gold layer
```

---

## 4. Pull requests

* **Title:** same style as a commit message
* **Description:** what the change does, how it was tested, and which requirement it covers (for example `FR-03`)
* **Size:** one task per pull request, so it is easy to review
* **Reviewer:** at least one other team member

---

## 5. Folder ownership

| Folder | Owner |
|---|---|
| `ingestion/` | Asmaa Adel Ali |
| `spark/` | Mosaab Mohamed Mohamed |
| `warehouse/`, `dashboard/` | Nepal Adel Ali |
| `ml/` | Omar Emad Hamdy |
| `assistant/` | Abdelrahman Mahmoud Mohamed |
| `tests/`, `docs/` | All members |

Changes in another member's folder should be reviewed by that member.

---

## 6. Never commit

* **Data files** (`.csv`, `.parquet`, `.zip`): keep them in the local `data/` folder
* **Secrets:** passwords and API keys live in `.env`, which is ignored; share an `.env.example` without real values instead
* **Generated files:** `__pycache__/`, `.ipynb_checkpoints/`, logs, MLflow runs

`.gitignore` already blocks these, but check `git status` before every commit.
