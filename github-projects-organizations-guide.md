# GitHub Projects & Organizations: Team Management Guide

## Overview

GitHub Projects and Organizations are tools for managing collaborative work at scale. Organizations provide team structure, access control, and shared settings. GitHub Projects (formerly called Projects) offers task management, kanban boards, and automation for tracking work. Together, they enable teams to organize repositories, manage workflows, and collaborate efficiently.

### Why It Matters
- **Team structure** - Organize developers and responsibilities
- **Access control** - Manage permissions and security
- **Task management** - Track issues, PRs, and progress
- **Workflow automation** - Automate repetitive tasks
- **Visibility** - See what the team is working on
- **Accountability** - Track who's doing what
- **Planning** - Organize sprints and milestones
- **Scaling** - Manage multiple projects and teams

### Main Use Cases
- Creating teams and managing access
- Organizing multiple repositories
- Planning sprints and releases
- Tracking issues and PRs
- Automating workflow processes
- Setting organization policies
- Managing billing and licenses
- Collaborating across teams

---

## 1. Core Concepts & Fundamentals

### Organizations vs Personal Accounts

```mermaid
graph TB
    A["GITHUB STRUCTURE"]
    
    A --> B["Personal Account"]
    B --> B1["Individual developer<br/>Public/private repos<br/>Full control<br/>Personal projects"]
    
    A --> C["Organization"]
    C --> C1["Team/company account<br/>Shared repositories<br/>Team management<br/>Access control<br/>Shared settings"]
    
    A --> D["Organization Benefits"]
    D --> D1["Multiple repos<br/>Team roles<br/>Permissions control<br/>Audit logs<br/>Billing management"]
    
    style A fill:#fff9c4,color:#f57f17
    style B fill:#e3f2fd,color:#0d47a1
    style C fill:#e3f2fd,color:#0d47a1
    style D fill:#e8f5e9,color:#1b5e20
```

### GitHub Organizations Hierarchy

```mermaid
graph TB
    A["🏢 ORGANIZATION"]
    
    A --> B["Teams"]
    B --> B1["Developers team<br/>Frontend team<br/>Backend team<br/>DevOps team"]
    
    A --> C["Members"]
    C --> C1["Owner: Full control<br/>Maintainer: Manage repos<br/>Member: Developer<br/>Guest: Limited access"]
    
    A --> D["Repositories"]
    D --> D1["Shared code<br/>Public visibility<br/>Private visibility<br/>Internal only"]
    
    A --> E["Settings"]
    E --> E1["Permissions<br/>Policies<br/>Billing<br/>Security"]
    
    A --> F["Projects & Milestones"]
    F --> F1["Track work<br/>Plan sprints<br/>Manage releases<br/>View progress"]
    
    style A fill:#fff9c4,color:#f57f17
    style B fill:#e3f2fd,color:#0d47a1
    style C fill:#e3f2fd,color:#0d47a1
    style D fill:#e3f2fd,color:#0d47a1
    style E fill:#e3f2fd,color:#0d47a1
    style F fill:#e3f2fd,color:#0d47a1
```

### GitHub Projects Overview

```mermaid
graph TB
    A["📊 GITHUB PROJECTS"]
    
    A --> B["Task Management"]
    B --> B1["Track issues<br/>Track PRs<br/>Track custom items<br/>Assign ownership"]
    
    A --> C["Views"]
    C --> C1["Table view<br/>Board view<br/>Roadmap view<br/>Custom fields"]
    
    A --> D["Automation"]
    D --> D1["Auto-add issues<br/>Move on status<br/>Archive completed<br/>Workflow triggers"]
    
    A --> E["Collaboration"]
    E --> E1["Share project<br/>Different access levels<br/>Team visibility<br/>Public/private"]
    
    A --> F["Integration"]
    F --> F1["Links to issues<br/>Links to PRs<br/>Updates from code<br/>Real-time sync"]
    
    style A fill:#e3f2fd,color:#0d47a1
    style B fill:#bbdefb,color:#0d47a1
    style C fill:#bbdefb,color:#0d47a1
    style D fill:#bbdefb,color:#0d47a1
    style E fill:#bbdefb,color:#0d47a1
    style F fill:#bbdefb,color:#0d47a1
```

---

## 2. Creating & Managing Organizations

### Creating an Organization

```mermaid
graph TB
    A["🏢 CREATE ORGANIZATION"]
    
    A --> B["Step 1: Go to Settings"]
    B --> B1["GitHub → Settings<br/>Organizations section<br/>New organization button"]
    
    A --> C["Step 2: Choose Plan"]
    C --> C1["Free: Unlimited public<br/>Pro: Advanced features<br/>Enterprise: Full control<br/>Pricing based on seats"]
    
    A --> D["Step 3: Basic Info"]
    D --> D1["Organization name<br/>Billing email<br/>Contact email<br/>Description"]
    
    A --> E["Step 4: Invite Members"]
    E --> E1["Email addresses<br/>GitHub usernames<br/>Set role (owner/member)<br/>Send invitations"]
    
    A --> F["Step 5: Repository Setup"]
    F --> F1["Create org repos<br/>Transfer existing<br/>Set permissions<br/>Configure teams"]
    
    A --> G["Ready to Use"]
    G --> G1["Team collaboration<br/>Shared repositories<br/>Project management<br/>Access control"]
    
    A --> B --> C --> D --> E --> F --> G
    
    style A fill:#fff9c4,color:#f57f17
    style B fill:#e3f2fd,color:#0d47a1
    style C fill:#e3f2fd,color:#0d47a1
    style D fill:#e3f2fd,color:#0d47a1
    style E fill:#e3f2fd,color:#0d47a1
    style F fill:#e3f2fd,color:#0d47a1
    style G fill:#e8f5e9,color:#1b5e20
```

### Organization Settings Overview

```
Organization Settings:

┌─ General ─────────────────────────────────────┐
│ Organization name                             │
│ Organization type (company, open source, etc) │
│ Description & website                         │
│ Profile picture                               │
│ Public/private visibility                     │
└───────────────────────────────────────────────┘

┌─ Members ─────────────────────────────────────┐
│ Add members                                   │
│ Manage roles (owner, member)                  │
│ Two-factor authentication required            │
│ Export members list                           │
└───────────────────────────────────────────────┘

┌─ Teams ───────────────────────────────────────┐
│ Create teams                                  │
│ Assign members to teams                       │
│ Set team permissions                          │
│ Manage team visibility                        │
└───────────────────────────────────────────────┘

┌─ Repository ──────────────────────────────────┐
│ Add repositories                              │
│ Transfer repositories                         │
│ Default permissions                           │
│ Force fork deletion                           │
└───────────────────────────────────────────────┘

┌─ Billing ─────────────────────────────────────┐
│ Manage payment method                         │
│ View invoices                                 │
│ Manage licenses                               │
│ Billing contacts                              │
└───────────────────────────────────────────────┘

┌─ Security ────────────────────────────────────┐
│ Two-factor authentication required            │
│ SAML single sign-on                           │
│ IP whitelist                                  │
│ Audit log                                     │
└───────────────────────────────────────────────┘
```

---

## 3. Teams & Permissions

### Team Structure

```mermaid
graph TB
    A["👥 ORGANIZATION TEAMS"]
    
    A --> B["Team Types"]
    B --> B1["Feature teams<br/>Frontend/Backend<br/>Platform teams<br/>Cross-functional"]
    
    A --> C["Team Roles"]
    C --> C1["Team maintainer<br/>Can manage members<br/>Create sub-teams<br/>Assign permissions"]
    
    A --> D["Team Permissions"]
    D --> D1["Pull/read only<br/>Push/write<br/>Admin/manage<br/>Per repository"]
    
    A --> E["Membership"]
    E --> E1["Public members<br/>Can see publicly<br/>Private members<br/>Secret membership"]
    
    A --> F["Nesting"]
    F --> F1["Parent teams<br/>Child teams<br/>Inherit permissions<br/>Organizational sync"]
    
    style A fill:#e3f2fd,color:#0d47a1
    style B fill:#bbdefb,color:#0d47a1
    style C fill:#bbdefb,color:#0d47a1
    style D fill:#bbdefb,color:#0d47a1
    style E fill:#bbdefb,color:#0d47a1
    style F fill:#bbdefb,color:#0d47a1
```

### Role-Based Access Control

```mermaid
graph TB
    A["🔐 ROLES & PERMISSIONS"]
    
    A --> B["Owner"]
    B --> B1["Full organization access<br/>Manage members<br/>Manage teams<br/>Manage repositories<br/>Manage billing<br/>Delete organization"]
    
    A --> C["Maintainer"]
    C --> C1["Manage repositories<br/>Manage team members<br/>Cannot change org settings<br/>Cannot delete org"]
    
    A --> D["Member"]
    D --> D1["Access assigned repos<br/>Create public repos<br/>Cannot access org settings<br/>Limited visibility"]
    
    A --> E["Guest"]
    E --> E1["Limited access<br/>Cannot see all repos<br/>Read-only on assigned<br/>Temporary access"]
    
    style A fill:#fff9c4,color:#f57f17
    style B fill:#ffccbc,color:#d84315
    style C fill:#fff3e0,color:#e65100
    style D fill:#e3f2fd,color:#0d47a1
    style E fill:#f3e5f5,color:#4a148c
```

### Repository Permissions per Team

```
┌─ Repository Access Levels ──────────────────┐
│                                             │
│ Pull (Read):                                │
│  - View & clone                             │
│  - Open issues/discussions                  │
│  - No push access                           │
│                                             │
│ Push (Write):                               │
│  - Pull + push branches                     │
│  - Review/merge PRs                         │
│  - Create releases                          │
│  - Cannot delete repo                       │
│                                             │
│ Admin:                                      │
│  - Full repo control                        │
│  - Change settings                          │
│  - Manage collaborators                     │
│  - Delete repo                              │
│  - Manage protection rules                  │
│                                             │
│ Triage:                                     │
│  - Manage issues/PRs                        │
│  - Cannot push                              │
│  - Close/reopen issues                      │
│  - Assign labels                            │
│                                             │
│ Maintain:                                   │
│  - Manage without delete                    │
│  - Manage PRs/issues                        │
│  - Manage wiki/pages                        │
│  - Cannot delete repo                       │
│                                             │
└─────────────────────────────────────────────┘
```

---

## 4. GitHub Projects - New Version

### Creating a Project

```mermaid
graph TB
    A["📊 CREATE PROJECT"]
    
    A --> B["Step 1: Navigate"]
    B --> B1["Repository Projects tab<br/>Or Organization Projects<br/>New project button"]
    
    A --> C["Step 2: Template"]
    C --> C1["Table<br/>Board (Kanban)<br/>Roadmap<br/>Blank custom"]
    
    A --> D["Step 3: Configure"]
    D --> D1["Project name<br/>Description<br/>Visibility (public/private)<br/>Fields & columns"]
    
    A --> E["Step 4: Add Items"]
    E --> E1["Add existing issues<br/>Add existing PRs<br/>Create new items<br/>Bulk import"]
    
    A --> F["Step 5: Organize"]
    F --> F1["Set status<br/>Assign owners<br/>Add labels<br/>Set priority"]
    
    A --> G["Ready to Track"]
    G --> G1["Monitor progress<br/>Update status<br/>Collaborate<br/>View reports"]
    
    A --> B --> C --> D --> E --> F --> G
    
    style A fill:#fff9c4,color:#f57f17
    style B fill:#e3f2fd,color:#0d47a1
    style C fill:#e3f2fd,color:#0d47a1
    style D fill:#e3f2fd,color:#0d47a1
    style E fill:#e3f2fd,color:#0d47a1
    style F fill:#e3f2fd,color:#0d47a1
    style G fill:#e8f5e9,color:#1b5e20
```

### Project Views

```mermaid
graph TB
    A["👁️ PROJECT VIEWS"]
    
    A --> B["Table View"]
    B --> B1["Spreadsheet style<br/>All items in rows<br/>Custom columns<br/>Filter & sort<br/>Best for: Data overview"]
    
    A --> C["Board View"]
    C --> C1["Kanban board<br/>Columns = status<br/>Drag between columns<br/>Card details<br/>Best for: Workflow"]
    
    A --> D["Roadmap View"]
    D --> D1["Timeline display<br/>Dates on axis<br/>Project duration<br/>Dependency view<br/>Best for: Planning"]
    
    A --> E["Custom Views"]
    E --> E1["Save filters<br/>Saved searches<br/>Team-specific views<br/>Multiple perspectives"]
    
    style A fill:#e3f2fd,color:#0d47a1
    style B fill:#bbdefb,color:#0d47a1
    style C fill:#bbdefb,color:#0d47a1
    style D fill:#bbdefb,color:#0d47a1
    style E fill:#bbdefb,color:#0d47a1
```

### Project Automation

```yaml
# GitHub Projects can automate:

When issue is opened:
  → Automatically add to project
  → Set status to "Todo"
  → Add "triage" label

When PR is ready for review:
  → Move to "In Review" column
  → Assign to reviewer
  → Add "needs-review" label

When PR is merged:
  → Move to "Done" column
  → Archive item
  → Notify team

When issue is closed:
  → Remove from project
  → Archive card
  → Update milestone progress

When status changes:
  → Update PR status
  → Change labels
  → Notify assignee
  → Update linked items
```

---

## 5. Organization Workflows & Best Practices

### Team Workflow Setup

```mermaid
graph TB
    A["⚙️ ORGANIZATION WORKFLOW"]
    
    A --> B["1. Team Structure"]
    B --> B1["Define teams<br/>Frontend, backend, devops<br/>Clear ownership<br/>Cross-team leads"]
    
    A --> C["2. Repository Permissions"]
    C --> C1["Team → Repo mapping<br/>Default access levels<br/>Code review policy<br/>Branch protection"]
    
    A --> D["3. Project Boards"]
    D --> D1["Create sprint board<br/>Weekly planning<br/>Daily standup<br/>Sprint review"]
    
    A --> E["4. Communication"]
    E --> E1["Team discussions<br/>Issue labels<br/>PR templates<br/>Code of conduct"]
    
    A --> F["5. Documentation"]
    F --> F1["Org README<br/>Team wikis<br/>Getting started<br/>Development guide"]
    
    A --> G["6. Automation"]
    G --> G1["Auto-assign PR reviewers<br/>Auto-add to project<br/>Auto-update labels<br/>Auto-enforce policies"]
    
    style A fill:#fff9c4,color:#f57f17
    style B fill:#e3f2fd,color:#0d47a1
    style C fill:#e3f2fd,color:#0d47a1
    style D fill:#e3f2fd,color:#0d47a1
    style E fill:#e3f2fd,color:#0d47a1
    style F fill:#e3f2fd,color:#0d47a1
    style G fill:#f3e5f5,color:#4a148c
```

### Best Practices for Organizations

```mermaid
graph TB
    A["🏆 BEST PRACTICES"]
    
    A --> B["1️⃣ Clear Ownership"]
    B --> B1["Each repo has owner<br/>Each team has lead<br/>Clear responsibility<br/>Escalation path"]
    
    A --> C["2️⃣ Permissions Model"]
    C --> C1["Least privilege<br/>Default: read only<br/>Grant as needed<br/>Regular audits"]
    
    A --> D["3️⃣ Branch Protection"]
    D --> D1["Main branch protected<br/>Require PR reviews<br/>Pass status checks<br/>Dismiss stale"]
    
    A --> E["4️⃣ Code Review Process"]
    E --> E1["Clear standards<br/>Assigned reviewers<br/>Feedback culture<br/>Learning opportunity"]
    
    A --> F["5️⃣ Documentation"]
    F --> F1["CONTRIBUTING.md<br/>Runbooks<br/>Architecture docs<br/>Easy onboarding"]
    
    A --> G["6️⃣ Team Communication"]
    G --> G1["Regular syncs<br/>Async updates<br/>Clear priorities<br/>Celebrate wins"]
    
    A --> H["7️⃣ Audit & Security"]
    H --> H1["Review audit logs<br/>Monitor access<br/>Remove inactive<br/>Update permissions"]
    
    style A fill:#fff9c4,color:#f57f17
    style B fill:#e3f2fd,color:#0d47a1
    style C fill:#e3f2fd,color:#0d47a1
    style D fill:#e3f2fd,color:#0d47a1
    style E fill:#e3f2fd,color:#0d47a1
    style F fill:#e3f2fd,color:#0d47a1
    style G fill:#e3f2fd,color:#0d47a1
    style H fill:#ffebee,color:#b71c1c
```

---

## 6. Quick Cheatsheet

### Organization Setup Checklist

```mermaid
graph TB
    A["✅ ORG SETUP CHECKLIST"]
    
    A --> B["Foundation"]
    B --> B1["☑ Create organization<br/>☑ Add logo/description<br/>☑ Set billing contact<br/>☑ Configure plan"]
    
    A --> C["Teams"]
    C --> C1["☑ Create teams<br/>☑ Add team members<br/>☑ Set team permissions<br/>☑ Designate leads"]
    
    A --> D["Repositories"]
    D --> D1["☑ Create/transfer repos<br/>☑ Set default permissions<br/>☑ Add CONTRIBUTING.md<br/>☑ Configure branches"]
    
    A --> E["Security"]
    E --> E1["☑ Enable 2FA<br/>☑ Review audit log<br/>☑ Set IP whitelist<br/>☑ Configure SAML"]
    
    A --> F["Projects"]
    F --> F1["☑ Create project board<br/>☑ Add initial items<br/>☑ Configure automation<br/>☑ Share with team"]
    
    A --> G["Policies"]
    G --> G1["☑ Code of conduct<br/>☑ Security policy<br/>☑ Review policy<br/>☑ Release process"]
    
    style A fill:#fff9c4,color:#f57f17
    style B fill:#fff3e0,color:#e65100
    style C fill:#e3f2fd,color:#0d47a1
    style D fill:#e3f2fd,color:#0d47a1
    style E fill:#ffebee,color:#b71c1c
    style F fill:#e8f5e9,color:#1b5e20
    style G fill:#f3e5f5,color:#4a148c
```

### GitHub Projects Features

| Feature | Description | Use Case |
|---------|-------------|----------|
| **Table View** | Spreadsheet-like organization | See all items at once |
| **Board View** | Kanban columns | Workflow visualization |
| **Roadmap View** | Timeline with dates | Release planning |
| **Custom Fields** | Add metadata | Priority, effort, owner |
| **Automation** | Auto-update status | Reduce manual work |
| **Filtering** | Search & filter | Find relevant items |
| **Sorting** | Organize items | By priority, date, etc |
| **Templates** | Save field configs | Consistency |

### Common Commands

```bash
# Via GitHub CLI (gh)

# Create organization (must be owner)
gh org create

# List org members
gh org members list

# Invite member
gh org invite-member USERNAME

# Create team
gh team create TEAM_NAME

# Add to team
gh team add-member TEAM_NAME USERNAME

# List projects
gh project list

# Create project
gh project create --title "Project Name"
```

---

## 7. Real-World Scenarios

### Scenario 1: Setting Up Organization for Growing Team

**Situation:** Company growing from 5 to 20 developers, need structure

**Before:** Chaos
- All repos in personal accounts
- No clear permissions
- Everyone can access everything
- No tracking of work
- Merge conflicts and confusion

**After:** Well-organized
```
MyCompany Organization
├── Backend Team
│   ├── api repo (pull/push)
│   ├── database repo (push)
│   └── services repo (push)
├── Frontend Team
│   ├── web repo (push)
│   ├── mobile repo (push)
│   └── shared-ui repo (pull)
├── DevOps Team
│   ├── infrastructure repo (admin)
│   ├── deployment repo (push)
│   └── monitoring repo (push)
└── Projects
    ├── Q1 Roadmap
    ├── Sprint Board
    └── Hiring Dashboard
```

**Implementation Steps:**
1. Create organization
2. Create teams (Backend, Frontend, DevOps)
3. Transfer/create repositories
4. Set team permissions per repo
5. Create project board for sprint
6. Add branch protection to main
7. Setup automated code review
8. Configure audit logging

**Result:** 
- Clear ownership
- Managed permissions
- Work tracking
- Team coordination

---

### Scenario 2: Managing Sprint with Projects

**Situation:** Sprint planning and tracking

```
Project Board: Sprint 2026-01-Q1

Views:
├── Board (Kanban)
│   ├── Backlog (15 items)
│   ├── Ready (5 items)
│   ├── In Progress (8 items)
│   ├── In Review (3 items)
│   └── Done (12 items)
│
├── Roadmap
│   ├── Q1 Milestones
│   ├── Feature timeline
│   └── Release schedule
│
└── Table (Full view)
    ├── All items
    ├── Assigned to: John, Jane, etc
    ├── Priority: Critical, High, Medium
    └── Status: All above

Automation:
- New issue added → Auto-add to project
- Mark "Ready" → Notify team
- Assign PR → Move to "In Review"
- Merge PR → Move to "Done" & archive
- Comment "won't fix" → Move to "Declined"
```

**Daily Standup:**
- Use project board as reference
- What's in progress?
- What's blocked?
- What's ready next?

---

### Scenario 3: Code Review Policy with Teams

**Situation:** Enforce code quality across organization

```
Policy:
1. All PRs require review
2. Two from specific teams
3. Backend PRs: 2 backend team members
4. Frontend PRs: 2 frontend team members
5. Cross-team: 1 from each

Implementation:
├── Branch Protection Rule
│   ├── Require pull request reviews: 2
│   ├── Require status checks: tests pass
│   ├── Require branches up to date
│   └── Dismiss stale reviews
│
├── Code Owners File
│   ├── /backend/* → @company/backend
│   ├── /frontend/* → @company/frontend
│   ├── /infra/* → @company/devops
│   └── *.json → @company/backend
│
└── CONTRIBUTING.md
    ├── Review expectations
    ├── Code standards
    ├── Testing requirements
    └── Release process
```

**Result:** 
- Consistent quality
- Knowledge sharing
- Team awareness
- Fewer bugs

---

## 8. Best Practices & Anti-Patterns

### GitHub Organizations Best Practices

```mermaid
graph TB
    A["🏆 ORGANIZATION BEST PRACTICES"]
    
    A --> B["1️⃣ Repository Naming"]
    B --> B1["Descriptive names<br/>Consistent prefix<br/>Lowercase with hyphens<br/>Clear purpose"]
    
    A --> C["2️⃣ Team Naming"]
    C --> C1["Team name = responsibility<br/>@company/backend<br/>@company/frontend<br/>Clear hierarchy"]
    
    A --> D["3️⃣ Permission Tiers"]
    D --> D1["Principle of least privilege<br/>Default: no access<br/>Grant as needed<br/>Regular review"]
    
    A --> E["4️⃣ Branch Protection"]
    E --> E1["Protect main branch<br/>Require reviews<br/>Require status checks<br/>Up-to-date requirement"]
    
    A --> F["5️⃣ Code Owners"]
    F --> F1["Define in CODEOWNERS<br/>Auto-request review<br/>Clear accountability<br/>Knowledge distribution"]
    
    A --> G["6️⃣ Documentation"]
    G --> G1["Org README<br/>Team wikis<br/>Getting started guide<br/>Contributing guidelines"]
    
    A --> H["7️⃣ Audit Trail"]
    H --> H1["Regular log review<br/>Monitor access changes<br/>Track permissions<br/>Compliance"]
    
    style A fill:#fff9c4,color:#f57f17
    style B fill:#e3f2fd,color:#0d47a1
    style C fill:#e3f2fd,color:#0d47a1
    style D fill:#e3f2fd,color:#0d47a1
    style E fill:#e3f2fd,color:#0d47a1
    style F fill:#e3f2fd,color:#0d47a1
    style G fill:#e3f2fd,color:#0d47a1
    style H fill:#ffebee,color:#b71c1c
```

### Anti-Patterns to Avoid

```mermaid
graph TB
    A["❌ ANTI-PATTERNS"]
    
    A --> B["Everyone = Admin"]
    B --> B1["Dangerous<br/>Accidental deletions<br/>Lack of control<br/>Security risk"]
    
    A --> C["No Documentation"]
    C --> C1["New members lost<br/>Inconsistent setup<br/>Repeated mistakes<br/>Slow onboarding"]
    
    A --> D["No Code Review"]
    D --> D1["Quality suffers<br/>Bugs increase<br/>Knowledge silos<br/>Learning blocked"]
    
    A --> E["Unprotected Main"]
    E --> E1["Anyone can push<br/>Breaks easily<br/>No history safety<br/>Deploys fail"]
    
    A --> F["Ignored Audit Logs"]
    F --> F1["No visibility<br/>Security blind spot<br/>Compliance issues<br/>Breach undetected"]
    
    A --> G["No Automation"]
    G --> G1["Manual busywork<br/>Inconsistent process<br/>Human error<br/>Slow workflow"]
    
    A --> H["Too Many Repos"]
    H --> H1["Confusing<br/>Duplicated code<br/>Maintenance burden<br/>Hard to find things"]
    
    style A fill:#ffebee,color:#b71c1c
    style B fill:#ffccbc,color:#d84315
    style C fill:#ffccbc,color:#d84315
    style D fill:#ffccbc,color:#d84315
    style E fill:#ffccbc,color:#d84315
    style F fill:#ffccbc,color:#d84315
    style G fill:#ffccbc,color:#d84315
    style H fill:#ffccbc,color:#d84315
```

---

## 9. Summary & Key Takeaways

### What You Should Know

✅ **Organizations structure teams** - Manage multiple repos and members  
✅ **Role-based access** - Owner, maintainer, member, guest roles  
✅ **Teams group developers** - By function or feature  
✅ **Projects track work** - Issues, PRs, custom items  
✅ **Projects have views** - Table, board, roadmap  
✅ **Automation reduces manual work** - Auto-add, auto-status, auto-archive  
✅ **Branch protection enforces quality** - Reviews, checks, up-to-date  
✅ **Audit logs provide visibility** - Security, compliance, accountability  

### Quick Comparison: Personal vs Organization

| Feature | Personal | Organization |
|---------|----------|--------------|
| **Repositories** | Single owner | Shared |
| **Team management** | N/A | Full featured |
| **Access control** | Simple | Role-based |
| **Projects** | Basic | Advanced |
| **Audit log** | Limited | Detailed |
| **Billing** | Per user | Per org |
| **SAML/SSO** | No | Yes |
| **For teams** | ❌ Not ideal | ✅ Perfect |

---

## 10. Interview & Exam Prep

### Common Interview Questions

**Q1: What's the difference between a personal account and an organization?**
> Personal accounts are for individuals, organizations are for teams/companies. Organizations allow multiple repositories, team management, role-based access control, shared settings, audit logging, and centralized billing. Organizations are essential for team collaboration.

**Q2: Explain the role hierarchy in GitHub organizations.**
> Owner has full control over organization settings, members, and billing. Maintainers can manage repositories and team members but not org settings. Members have basic access to assigned repositories. Guests have limited temporary access. Permission flows hierarchically.

**Q3: How would you structure teams for a company with frontend, backend, and DevOps groups?**
> Create three teams: @company/frontend, @company/backend, @company/devops. Assign members to appropriate teams. Grant each team permissions on their relevant repositories (frontend team has push on web repo, pull on API repo, etc). This provides clear ownership and least-privilege access.

**Q4: What are GitHub Projects and what problems do they solve?**
> GitHub Projects are task management boards that track issues, PRs, and custom items. They solve the problem of scattered work—everything's in one place. Kanban boards visualize workflow, automation reduces manual updates, and integration with issues/PRs keeps data in sync.

**Q5: Explain different project views and when to use each.**
> Table view is best for overview of all items (spreadsheet-like). Board view (Kanban) is best for workflow visualization with columns as statuses. Roadmap view is best for planning with timeline visibility. Use table for data review, board for daily work, roadmap for releases.

**Q6: What's the purpose of branch protection rules?**
> Branch protection enforces quality by requiring pull request reviews before merge, ensuring status checks pass, requiring branches are up-to-date with main, and allowing dismissal of stale reviews. Prevents accidental pushes, enforces review, catches bugs early.

**Q7: How would you implement an audit trail in your organization?**
> Enable and regularly review the organization audit log (Settings → Audit Log). Monitor member additions/removals, permission changes, repository transfers, team changes. Keep records for compliance. Set up alerts for sensitive actions. Create audit reports.

**Q8: What's the principle of least privilege and how to apply it?**
> Give each member the minimum permissions they need. Default: no access. Grant read on public repos, write on assigned repos, admin only if needed. Review quarterly. Removes risk of accidental damage. Separates concerns. Follows security best practices.

### Practice Scenarios

**Scenario A:** Your organization is 50 people, chaos in access control. How would you restructure?
- Audit current permissions and document
- Create team structure (by function)
- Move members to teams
- Assign team permissions per repo
- Set branch protection rules
- Enable audit logging
- Document in CONTRIBUTING.md
- Monthly permission reviews

**Scenario B:** You need to enforce code review before merging. How?
- Repository → Settings → Branches
- Add branch protection rule for main
- Require pull request reviews: 2
- Add CODEOWNERS file
- Auto-request appropriate reviewers
- Require status checks pass
- Require up-to-date before merge
- Train team on process

**Scenario C:** Team of 10 developers, need to track sprint work. How?
- Create GitHub Project
- Add issues/PRs to project
- Create views: Board (workflow), Roadmap (timeline)
- Assign items to team members
- Set automation: issue → "Todo", PR → "In Review", merge → "Done"
- Daily standup using board view
- Sprint review using table view
- Measure velocity from closed items

---

## 11. Troubleshooting Common Issues

### Issue: Permission Denied for Team Member

**Problem:** Team member can't access a repository

**Solutions:**

```bash
1. Verify Team Membership
   Organization → Teams
   Check member in correct team
   Add if missing

2. Check Team Permissions
   Team Settings → Repository Access
   Ensure team has access to repo
   Check access level (pull/push/admin)

3. Check Personal Access
   Repository → Collaborators
   Not overridden individually
   Team permission should apply

4. Check Outside Collaborators
   Might have limited access
   Change to full member

5. Verify GitHub Account
   Correct GitHub username?
   Capitalization matters
   Check for typos

6. Review Audit Log
   Settings → Audit Log
   See if access was revoked
   Check recent changes

# Example: Add team to repository
Organization → Teams → [Team Name]
Repositories tab → Add Repository
Select repository, choose access level
```

### Issue: Can't Create Project or Access It

**Problem:** Project creation fails or can't see project

**Solutions:**

```bash
1. Check Permissions
   Must be org member (at least)
   Owner access for org projects
   May vary for repo projects

2. Verify Project Visibility
   Private projects: only members
   Public projects: visible to all
   Check settings for correct visibility

3. Confirm Organization Plan
   Projects available on most plans
   Check organization billing
   May need upgrade for advanced features

4. Check Project Access Settings
   Project → Access
   Ensure user has access
   May need to invite specifically

5. Browser Cache
   Clear cache and refresh
   Try incognito window
   Try different browser

6. Try Different Org
   Can create in organization?
   Can create in repository?
   Permissions might differ

# If still failing:
Check GitHub Status: https://www.githubstatus.com
Contact GitHub Support
```

### Issue: Audit Log Shows Unexpected Changes

**Problem:** Permissions or settings changed without authorization

**Solutions:**

```bash
1. Review Recent Audit Log
   Settings → Audit Log
   Filter by action type
   Sort by most recent
   Check for unauthorized changes

2. Identify User
   Who made the change?
   Were they authorized?
   Check their access level

3. Verify Intent
   Was it accidental?
   Was it authorized but not communicated?
   Talk to the person

4. Secure Account
   If unauthorized: change passwords
   Enable 2FA if not enabled
   Review connected applications
   Remove suspicious access

5. Implement Controls
   Restrict to minimum members
   Owner approval for changes
   Only specific people can...
   Require 2FA for admins

6. Document Policy
   Create access change policy
   Approval process
   Notification requirements
   Audit frequency

# Export audit log for investigation
Settings → Audit Log
Export as CSV
Review offline
Keep for records
```

### Issue: Team Members Can't See Each Other

**Problem:** Team members aren't aware of each other

**Solutions:**

```bash
1. Check Team Privacy
   Team → Settings → Privacy
   Private: members only see listed
   Public: members visible to all
   Change to match need

2. Set Member Visibility
   Each member's profile
   Can be public or private
   Controls what others see

3. Use Discussion
   Team → Discussions
   Create team space
   Share updates
   Improve visibility

4. Team Mention
   @team-name in issues/PRs
   Notifies all members
   Visible participation

5. Update Team Page
   Organization → Teams → [Team]
   Add description
   List members
   Show what team does

6. Team Sync Meeting
   Regular team calls
   Build relationships
   Align on priorities
```

---

## 12. Visual Summary

### Organization Setup Flow

```mermaid
graph TB
    A["Create Organization"]
    
    B["Setup Teams"]
    B --> B1["Frontend<br/>Backend<br/>DevOps<br/>etc"]
    
    C["Configure Repositories"]
    C --> C1["Create/transfer<br/>Set permissions<br/>Add teams"]
    
    D["Set Branch Protection"]
    D --> D1["Require reviews<br/>Require checks<br/>Up-to-date<br/>Status checks"]
    
    E["Create Project Board"]
    E --> E1["Define views<br/>Setup automation<br/>Add items"]
    
    F["Document & Train"]
    F --> F1["CONTRIBUTING.md<br/>CODEOWNERS<br/>Team wiki<br/>Runbooks"]
    
    G["Secure & Monitor"]
    G --> G1["Audit log review<br/>2FA required<br/>Regular audits<br/>Compliance"]
    
    H["Team Collaboration Ready"]
    H --> H1["Clear structure<br/>Managed access<br/>Work tracked<br/>Quality enforced"]
    
    A --> B --> C --> D --> E --> F --> G --> H
    
    style A fill:#fff3e0,color:#e65100
    style B fill:#e3f2fd,color:#0d47a1
    style C fill:#e3f2fd,color:#0d47a1
    style D fill:#fff9c4,color:#f57f17
    style E fill:#e8f5e9,color:#1b5e20
    style F fill:#f3e5f5,color:#4a148c
    style G fill:#ffebee,color:#b71c1c
    style H fill:#c8e6c9,color:#1b5e20
```

---

## 13. Organizations Checklist & Planning

### Pre-Launch Checklist

```yaml
Organization Planning:

□ Structure
  □ Team names and responsibilities
  □ Repository organization
  □ Code ownership model
  □ Permission tiers

□ Members
  □ List of initial members
  □ Team assignments
  □ Role assignments
  □ Contact information

□ Repositories
  □ Existing repos to transfer
  □ New repos to create
  □ Default branch name
  □ Naming convention

□ Policies
  □ Code review process
  □ Commit message format
  □ Branch naming convention
  □ Release process

□ Security
  □ 2FA requirement
  □ Branch protection rules
  □ CODEOWNERS file
  □ Security policy

□ Documentation
  □ README for organization
  □ CONTRIBUTING guidelines
  □ Code of conduct
  □ Development setup guide

□ Automation
  □ GitHub Actions workflows
  □ Automatic reviewers
  □ Status check requirements
  □ Project automation

□ Communication
  □ Team channels
  □ Regular syncs
  □ Notifications setup
  □ Escalation path

□ Monitoring
  □ Audit log review process
  □ Permission audits schedule
  □ Performance metrics
  □ Issue tracking
```

---

**Last Updated:** January 7, 2026  
**Difficulty Level:** Intermediate to Advanced  
**Prerequisites:** GitHub account, team collaboration experience, repository knowledge
