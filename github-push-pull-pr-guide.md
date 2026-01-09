# GitHub: Push, Pull, and Pull Requests Guide

## Overview
Understanding the difference between push, pull, and pull requests is fundamental to working with GitHub in collaborative projects.

---

## 1. Push vs Pull Request - Key Differences

### Visual Comparison

```mermaid
graph LR
    subgraph Push["🔼 PUSH"]
        P1["Local Commits"] -->|"git push origin branch"| P2["Remote Branch"]
        P2 -->|"Auto-merged"| P3["Main Branch"]
    end
    
    subgraph PR["🔄 PULL REQUEST"]
        PR1["Local Commits"] -->|"git push origin branch"| PR2["Remote Branch"]
        PR2 -->|"Create PR"| PR3["Code Review<br/>Tests Run"]
        PR3 -->|"Approval +<br/>Merge Click"| PR4["Main Branch"]
    end
    
    style Push fill:#f44336,color:#fff
    style PR fill:#4caf50,color:#fff
    style P3 fill:#ffc107,color:#000
    style PR4 fill:#ffc107,color:#000
```

### **Push**
- **Type:** Git command
- **What it does:** Uploads your local commits directly to a remote branch
- **Access requirement:** Requires write access to the branch
- **Review process:** No built-in review
- **When merged:** Automatic (once pushed)
- **Typical use:** Your own branches or direct commits

### **Pull Request (PR)**
- **Type:** GitHub feature (not a Git command)
- **What it does:** Proposes changes for review before merging
- **Access requirement:** Anyone can create (if fork permissions allowed)
- **Review process:** Enables code review, discussion, and checks
- **When merged:** Requires explicit approval + merge
- **Typical use:** Contributing to shared/main branches

---

## 2. When to Use Push and Pull

### **git push** - Upload Local Changes

**When to push:**
- After making commits locally and you're ready to share them
- Before creating a pull request (push your feature branch first)
- To keep your remote branch up-to-date with your work
- Whenever you want others to see your changes

```bash
git push origin feature-branch
```

### **git pull** - Download Remote Changes

**When to pull:**
- Before starting work (to get the latest changes from teammates)
- Before pushing (to avoid conflicts)
- After a PR is merged (to sync with main)
- Regularly during collaborative work to stay current

```bash
git pull origin main
```

---

## 3. Git Workflow Architecture

### Local vs Remote Repository

```mermaid
graph TB
    subgraph Local["💻 YOUR LOCAL MACHINE"]
        LW["Working Directory<br/>(Your files)"]
        LS["Staging Area<br/>(git add)"]
        LR["Local Repository<br/>(git commit)"]
        LW -->|"git add"| LS
        LS -->|"git commit"| LR
    end
    
    subgraph Remote["☁️ GITHUB REMOTE"]
        RB["Remote Branch<br/>(origin/main)"]
    end
    
    LR -->|"git push"| RB
    RB -->|"git pull"| LR
    
    style Local fill:#e3f2fd,color:#0d47a1
    style Remote fill:#f3e5f5,color:#4a148c
    style RB fill:#e8f5e9,color:#1b5e20
```

### Step-by-Step:

```mermaid
graph LR
    A["1️⃣ git pull<br/>origin main"] 
    B["2️⃣ Create &<br/>Edit Files<br/>Feature Branch"]
    C["3️⃣ git add &<br/>git commit"]
    D["4️⃣ git push origin<br/>feature-branch"]
    E["5️⃣ Open Pull<br/>Request"]
    F["6️⃣ Code Review &<br/>Tests"]
    G["7️⃣ Merge to<br/>Main"]
    H["8️⃣ git pull origin<br/>main"]
    
    A --> B --> C --> D --> E --> F --> G --> H
    
    style A fill:#e1f5fe,color:#01579b
    style B fill:#f3e5f5,color:#4a148c
    style C fill:#fff3e0,color:#e65100
    style D fill:#fce4ec,color:#880e4f
    style E fill:#e8f5e9,color:#1b5e20
    style F fill:#f3e5f5,color:#4a148c
    style G fill:#e8f5e9,color:#1b5e20
    style H fill:#e1f5fe,color:#01579b
```

1. **Pull** → Get latest code from remote
   ```bash
   git pull origin main
   ```

2. Create a feature branch and make changes locally
   ```bash
   git checkout -b feature-branch
   # Make changes...
   git add .
   git commit -m "Your changes"
   ```

3. **Push** → Upload your branch to remote
   ```bash
   git push origin feature-branch
   ```

4. Open a Pull Request on GitHub
   - Go to your repository
   - Click "New Pull Request"
   - Select your feature branch and main
   - Add title and description
   - Click "Create Pull Request"

5. **Pull** → After PR is merged, sync your main branch
   ```bash
   git pull origin main
   ```

---

## 4. How Pull Requests Update Main Branch

### The Complete PR Flow

```mermaid
graph TD
    A["👤 Developer<br/>Local Feature Branch"] 
    B["🚀 Push to Remote<br/>origin/feature-branch"]
    C["📝 Create Pull Request<br/>on GitHub"]
    D["👀 Code Review<br/>Feedback & Discussion"]
    E["✅ All Checks Passed<br/>Tests Run Successfully"]
    F["✔️ Approve & Merge<br/>Click Merge Button"]
    G["🎯 Main Branch Updated<br/>Changes Live"]
    
    A -->|"git push"| B
    B --> C
    C --> D
    D -->|"Approved"| E
    E --> F
    F --> G
    
    D -->|"Changes Needed"| A
    
    style A fill:#e3f2fd,color:#0d47a1
    style B fill:#f3e5f5,color:#4a148c
    style C fill:#fff3e0,color:#e65100
    style D fill:#fce4ec,color:#880e4f
    style E fill:#e8f5e9,color:#1b5e20
    style F fill:#e8f5e9,color:#1b5e20
    style G fill:#a5d6a7
```

### Branch Separation & Safety

```mermaid
graph TB
    subgraph Branches["🌳 Git Branches"]
        M["main branch<br/>(Production Ready)"]
        F["feature branch<br/>(Your Work)"]
    end
    
    subgraph Process["🔄 PR Process"]
        code["Code Changes"]
        review["👀 Review"]
        tests["✅ Tests"]
        merge["Merge PR"]
    end
    
    F -->|"Contains"| code
    code --> review
    review --> tests
    tests -->|"Only if approved"| merge
    merge -->|"Updates"| M
    
    style M fill:#fff9c4
    style F fill:#e1f5fe
    style merge fill:#c8e6c9
```

### Why Not Push Directly to Main?

In collaborative projects, **pushing directly to main is restricted** via branch protection rules. You must use a PR instead because:

- ✅ Allows code review before changes reach main
- ✅ Prevents bad code from breaking the project
- ✅ Creates discussion and accountability
- ✅ Runs automated tests before merging
- ✅ Creates audit trail of changes

### Branching Strategy Comparison

```mermaid
graph LR
    subgraph BadPractice["❌ Direct Push to Main<br/>(DANGEROUS)"]
        BP1["Your Code"] -->|"git push<br/>origin main"| BP2["Main Updated<br/>Immediately"]
        BP2 -->|"No Review!"| BP3["🐛 Bugs Enter<br/>Production"]
    end
    
    subgraph GoodPractice["✅ PR Workflow<br/>(SAFE)"]
        GP1["Your Code"] -->|"git push<br/>origin feature"| GP2["PR Created"]
        GP2 -->|"Review &<br/>Test"| GP3["Approval"]
        GP3 -->|"Merge"| GP4["Main Updated<br/>Safely"]
    end
    
    style BadPractice fill:#ffebee
    style GoodPractice fill:#e8f5e9
    style BP3 fill:#ef5350
    style GP4 fill:#66bb6a
```

### Key Point:

**The PR merge (not a direct push) is what updates main.**

The PR itself is a gatekeeper that ensures only reviewed, approved code reaches main.

---

## 5. Quick Reference Summary

| Operation | Command | Purpose |
|-----------|---------|---------|
| **Push** | `git push origin branch` | Upload local commits to remote |
| **Pull** | `git pull origin branch` | Download and merge remote changes |
| **Create PR** | Via GitHub UI | Propose changes for review |
| **Merge PR** | Click "Merge" on GitHub | Update main with reviewed code |

---

## Key Takeaways

1. **Push:** "Here's my work" (upload local → remote)
2. **Pull:** "Give me the latest" (download remote → local)
3. **Pull Request:** "Please review and merge my changes" (gatekeeper for main branch)

Push and pull are the two fundamental Git operations for syncing between your local repository and GitHub.

---

## 6. Quick Cheatsheet

### Essential Commands

```bash
# PULL - Get latest changes from remote
git pull origin main
git pull origin feature-branch

# PUSH - Upload your commits to remote
git push origin feature-branch
git push origin main

# CREATE & COMMIT
git checkout -b new-feature                    # Create new branch
git add .                                      # Stage changes
git commit -m "Your message"                   # Commit changes
git push origin new-feature                    # Push to remote

# SYNC BEFORE WORKING
git pull origin main                           # Get latest from main
git merge main                                 # Merge main into your branch

# AFTER PR MERGE
git checkout main                              # Switch to main
git pull origin main                           # Get merged changes
git branch -d feature-branch                   # Delete old branch (optional)
```

### Decision Tree: Push vs Pull Request?

```mermaid
graph TD
    A{"Are you changing<br/>main branch?"}
    A -->|YES| B{"Do you have<br/>write access?"}
    A -->|NO| C["Use PUSH<br/>directly to<br/>your branch"]
    B -->|NO| D["Create PULL<br/>REQUEST<br/>from fork"]
    B -->|YES<br/>With team| E["Create PULL<br/>REQUEST<br/>for review"]
    B -->|YES<br/>Personal| F["Can use PUSH<br/>if allowed"]
    
    style C fill:#c8e6c9
    style D fill:#fff9c4
    style E fill:#fff9c4
    style F fill:#ffccbc
```

### Common Scenarios Cheatsheet

| Scenario | What To Do | Command |
|----------|-----------|---------|
| **Starting new work** | Pull latest main | `git pull origin main` |
| **Made local changes** | Push to your branch | `git push origin feature-branch` |
| **Ready for merge** | Create PR on GitHub | UI: "New Pull Request" |
| **PR approved** | Merge on GitHub | UI: "Merge Pull Request" |
| **PR rejected** | Fix locally, push again | `git push origin feature-branch` |
| **After PR merged** | Sync your main | `git pull origin main` |
| **Conflict in PR** | Resolve locally, push | `git push origin feature-branch` |
| **Need teammate's code** | Pull their branch | `git pull origin teammate-branch` |

---

## 7. Compare & Contrast: Real-World Scenarios

### Scenario 1: Solo Personal Project (You're the Only Developer)

```mermaid
graph LR
    A["Make Changes<br/>Locally"]
    B["Commit"]
    C{"Ready for<br/>Production?"}
    C -->|YES| D["git push<br/>origin main"]
    C -->|NO| E["git push<br/>origin dev"]
    D --> F["✅ Live!"]
    E --> G["Keep Developing"]
    
    style F fill:#c8e6c9
    style D fill:#a5d6a7
```

**Best Practice:**
- ✅ **Can use direct PUSH** to main (no review needed)
- ✅ Use branches for experimental work
- ✅ Keep main as stable, deployable code
- ⚠️ Still good habit to use feature branches + PRs for learning

---

### Scenario 2: Team Project with Code Review

```mermaid
graph LR
    A["Developer 1<br/>feature-auth"]
    B["Developer 2<br/>feature-api"]
    C["Developer 3<br/>feature-ui"]
    A --> D["Create PR"]
    B --> D
    C --> D
    D --> E["Code Review<br/>by Team Lead"]
    E -->|"Approved"| F["Merge to<br/>main"]
    E -->|"Changes<br/>Needed"| A
    F --> G["Deploy to<br/>Production"]
    
    style G fill:#c8e6c9
    style D fill:#fff9c4
```

**Best Practice:**
- ✅ **ALWAYS use Pull Requests**
- ✅ Require at least 1 approval before merge
- ✅ Branch protection rules on main
- ✅ Automated tests must pass
- ✅ Prevents conflicts & bad code

---

### Scenario 3: Open Source Contribution (You Don't Have Direct Access)

```mermaid
graph LR
    A["Fork Repository"]
    B["Clone to Local"]
    C["Create Feature<br/>Branch"]
    D["git push<br/>origin feature"]
    E["Create Pull<br/>Request to<br/>Main Repo"]
    F["Maintainer<br/>Reviews"]
    G["Merged!<br/>Your code<br/>in official repo"]
    
    A --> B --> C --> D --> E --> F --> G
    
    style G fill:#c8e6c9
    style E fill:#fff9c4
```

**Best Practice:**
- ✅ **Can't push directly** (no write access)
- ✅ **MUST use Pull Requests**
- ✅ Follow project's contribution guidelines
- ✅ Be ready for feedback from maintainers
- ✅ Maintainer decides when/if to merge

---

### Scenario 4: Feature Branch with Parallel Development

```mermaid
graph TB
    M["main<br/>(stable)"]
    F1["feature/auth<br/>(your work)"]
    F2["feature/payments<br/>(teammate)"]
    
    M --> F1
    M --> F2
    
    F1 -->|"PR 1<br/>Merged"| M
    F2 -->|"PR 2<br/>Merged"| M
    
    M -->|"git pull"| F1
    M -->|"git pull"| F2
    
    style M fill:#fff9c4
    style F1 fill:#e1f5fe
    style F2 fill:#f3e5f5
```

**Best Practice:**
- ✅ Each feature gets its own branch
- ✅ **All changes go through PR**
- ✅ Pull latest main before pushing
- ✅ Helps prevent merge conflicts
- ✅ Keeps work organized & trackable

---

### Decision Guide for Exams/Interviews

| Question | Answer | Remember |
|----------|--------|----------|
| "When should I use push?" | To upload your local commits to remote | Push = Upload |
| "When should I use pull?" | Before starting work or to sync changes | Pull = Download |
| "What's the difference?" | Push uploads, Pull downloads | Opposite operations |
| "Why use PR instead of push?" | Code review, tests, gatekeeper for main | Safety & Quality |
| "Can you push to main?" | Only if you have write access & no protection | Not always allowed |
| "Who decides to merge a PR?" | Maintainer/team lead approves then merges | Not automatic |
| "Is PR a Git command?" | No, it's a GitHub feature | Git ≠ GitHub |
| "What happens after PR merge?" | main branch is updated with your changes | Then git pull to sync |
| "What if PR is rejected?" | Fix issues locally, push again to branch | Keeps same PR updated |
| "Workflow for team?" | Branch → Push → PR → Review → Merge → Pull | Always this order |

---

**Created:** January 6, 2026
**Status:** Learning Reference Guide
