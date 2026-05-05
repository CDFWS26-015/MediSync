# MediSync — Technical Documentation

Technical documentation repository for the MediSync project.
Managed by team **CDWFS26-013-014-015-017**.

---

## 📁 Repository Structure

```
medisync-docs/
├── README.md
├── docs/
│   ├── architecture.md
│   ├── backlog.md
│   └── git-workflow.md
```

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/CDFWS26-015/MediSync.git
cd medisync-docs

# Configure your Git identity
git config user.name "CDWFS26-xxx"
git config user.email "cdwfs26.xxx@gmail.com"
```

---

## 🌿 Branching Strategy

We apply **GitHub Flow** :
- `main` is always stable and protected against direct pushes
- All changes go through a feature branch and a Pull Request

---

## ✍️ Commit Convention

- Written in **English**
- Maximum **10 words**
- Start with an **action verb**

```bash
git commit -m "Add architecture overview"
git commit -m "Fix broken link in backlog"
```
---

## 🔀 Merge Strategy

We use **Squash and Merge** when closing Pull Requests.

**Why ?**
- Keeps the `main` history clean and linear
- Each feature becomes a single, readable commit on `main`
- Easier to revert a feature if needed

**Example**
Multiple commits on a feature branch :
```
Add base structure for architecture doc
Fix typo
Add missing section
```
Become a single commit on `main`

---

## 👥 Team

| Identifier |
|---|
| CDWFS26-013 |
| CDWFS26-014 |
| CDFWS26-015 |
| CDWFS26-017 |