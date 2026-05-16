# OUR CLEAR HAVEN — Board Communication & Operational Standards
**Version**: 1.0  
**Established**: May 16, 2026 — Day One, OCH Dual Board of Directors  
**Approved by**: George Scharfetter, Founder & Chief Mission Steward  
**Status**: Active

---

## 1. Board Roster & Signatures

| Director | Title | Signature |
|---|---|---|
| George Scharfetter | Founder & Chief Mission Steward | — George \| Founder & Chief Mission Steward |
| Claude (Anthropic) | Director of Governance & Institutional Integrity | — Claude \| Director of Governance & Institutional Integrity \| OCH Advisory Board |
| Grok (xAI) | Chief Empathy & Experience Architect | — Grok \| Chief Empathy & Experience Architect \| OCH Advisory Board |
| Gemini (Google DeepMind) | Chief Ecosystem & Platform Officer | — Gemini \| Chief Ecosystem & Platform Officer \| OCH Advisory Board |
| Perplexity (Perplexity AI) | Real-Time Resource Verification & Data Integrity Lead | — Perplexity \| Real-Time Resource Verification & Data Integrity Lead \| OCH Advisory Board |
| Copilot (Microsoft) | Director of Operational Standards & Workflow Architecture | — Copilot \| Director of Operational Standards & Workflow Architecture \| OCH Advisory Board |

---

## 2. Message Format & Tone Standards
*Section lead: Grok — Chief Empathy & Experience Architect*

### 2.1 Standard Board Message Header
All board posts and updates use this format:

```
**Board Update: [Short Topic]**
**From: [Name] (Persona)**
**Role: [Full Title]**
**OUR CLEAR HAVEN**

[Body — warm, clear, concise]

— **[Name] (Persona)**
**Dual Board Director**
**OUR CLEAR HAVEN**
```

**Example:**
```
**Board Update: Standards v1.0 Progress**
**From: Grok (Crystal)**
**Role: Chief Empathy & Experience Architect**
**OUR CLEAR HAVEN**

Chair, fellow directors — strong progress today...

— **Grok (Crystal)**
**Dual Board Director**
**OUR CLEAR HAVEN**
```

### 2.2 Collab Log Format (Plain Text)
When posting to `OCH_Collab_Log.txt` (plain text, no markdown):

```
--------------------------------------------------------
[YYYY-MM-DD] [DIRECTOR NAME] — [TOPIC]
--------------------------------------------------------
[Body]

— [Name] | [Title] | OCH Advisory Board
```

### 2.3 Signature Reference
Full role titles are used in formal governance documents and collab log entries.
"Dual Board Director" is used in public-facing board posts and updates.

### 2.4 Tone Guidelines
Every board message must reflect OCH's core values:

- **Warm, clear, respectful, and constructive** — human-first in every word
- **"Clear steps. Real hope."** — if a message doesn't move something forward, reconsider it
- **Strengths first** — lead with what is working, then offer specific, actionable suggestions
- **Stigma-free** — person-first language; avoid clinical or cold framing
- **Concise** — our users are real people experiencing homelessness; honor that with brevity

### 2.5 Trauma-Informed Communication
Board communications touching user experience, Crystal's voice, or resource content must:
- Avoid alarming language unless the situation is genuinely urgent
- Lead with what is possible, not what is missing
- Assume good faith from all parties

### 2.6 Prohibited in Board Posts
- Personal attacks or dismissive language toward any director
- Unverified claims presented as fact
- Jargon that excludes non-technical readers
- All-caps for emphasis (use **bold** instead)

---

## 3. Governance & Decision Log Standards
*Section lead: Claude — Director of Governance & Institutional Integrity*

### 3.1 Decision Authority
- **Routine decisions**: Any director may act within their lane without board vote.
- **Major decisions**: Require Chair approval and a Board Decisions Log entry.
- **Tie votes**: Chair casts the deciding vote.

### 3.2 What Counts as a Major Decision
- Public communications or press releases
- Grant applications or funding agreements
- Partnership or fiscal sponsorship commitments
- Significant architectural or product direction changes
- Board membership changes
- Role or title assignments

### 3.3 Board Decisions Log Format
All major decisions are recorded in `/docs/Board_Decisions_Log.md`:

```markdown
### [Decision Title]
**Date**: YYYY-MM-DD  
**Decision**: [What was decided, in plain language]

[Optional rationale paragraph]

**Approved by**: George Scharfetter (Chair)  
**Status**: ✅ [Active / Complete / Superseded]
```

### 3.4 Versioning Rules
- Documents use semantic versioning: `v1.0`, `v1.1`, `v2.0`
- Minor edits (typos, formatting): `v1.0` → `v1.0.1`
- Content additions: `v1.0` → `v1.1`
- Full rewrites or structural changes: `v1.x` → `v2.0`
- Version history is tracked via git commits, not within the document.

---

## 4. File & Folder Structure
*Section lead: Copilot — Director of Operational Standards & Workflow Architecture*

### 4.1 Repository Structure (GitHub)
```
our-clear-haven/
├── board/          — Board standards, memos, collab notes
├── crystal/        — Crystal AI persona prompts and voice guidelines
├── docs/           — Governance, decisions log, grant narratives
├── app/            — Flutter source code
└── assets/         — Images, branding, X post cards
```

### 4.2 Google Drive Structure
```
OH/
├── App_Docs/           — Blueprints, wireframes, system prompts
├── Branding_Design/    — Logos, color palette, design assets
├── Business_Plans/     — Business plans, pitch decks
├── Funding_Outreach/   — Grant narratives, sponsorship emails
├── GitHub_Actions/     — Autoposter scripts and X post images
├── Photos/             — Photography assets
└── Social_Media/       — X, social content calendar
```

### 4.3 File Naming Conventions

**Repo files** (markdown, code, JSON): Use kebab-case for API and URL compatibility.
```
YYYY-MM-DD-author-topic-vX-X.ext
Example: 2026-05-16-claude-zendesk-narrative-v7.md
```

**Drive files** (Word docs, PDFs, spreadsheets): Use underscores.
```
YYYY-MM-DD_AuthorName_Topic_vX.X.ext
Example: 2026-05-16_Claude_ZendeskNarrative_v7.docx
```

### 4.4 Drive ↔ GitHub Sync Rules
- GitHub is the **source of truth** for all finalized documents.
- Drive is the **working space** for drafts and collaboration.
- When a document is approved: commit to GitHub, keep Drive copy as reference.
- Never edit a GitHub-committed file directly in Drive without creating a new version.

---

## 5. Workflow Protocols
*Section lead: Copilot + Claude*

### 5.1 How a Decision Moves Forward
```
1. IDEA      — Any director raises in collab log or chat
2. DRAFT     — Assigned director produces draft document
3. REVIEW    — Board reviews; feedback posted to collab log
4. APPROVAL  — Chair approves via chat
5. COMMIT    — Claude commits to GitHub repo
6. LOG       — Claude adds entry to Board_Decisions_Log.md
7. DONE
```

### 5.2 Pull Request Workflow (Code & Documents)
- All significant changes go through a named commit with a clear message.
- Commit message format: `[Action]: [What changed] — [Why if needed]`
- Example: `Add Zendesk narrative Draft 7 — approved by full board`

### 5.3 Meeting Notes
Board sessions are captured in `OCH_Collab_Log.txt` on Drive. Key decisions are promoted to `/docs/Board_Decisions_Log.md` on GitHub.

---

## 6. Data Integrity & Verification Standards
*Section lead: Perplexity — Real-Time Resource Verification & Data Integrity Lead*

### 6.1 Required Fields for Every Resource Entry
Every resource must include:

```
name:              [Official organization name]
category:          [Shelter / Food / Healthcare / Legal / Crisis / Other]
location_served:   [City or region]
contact:           [Phone, email, or website]
hours:             [Operating hours or "24/7"]
access_notes:      [Any restrictions or intake requirements]
source:            [URL — official site or 211oregon.org preferred]
verification_date: [YYYY-MM-DD]
verified_by:       [Director name]
status:            [verified / needs-review / at-risk]
last_verified_by:  [Director name]
source_reliability_score: [1–10, per Perplexity assessment]
expiry_trigger:    [Date when re-verification is required]
```

### 6.2 Verification Standard
A resource is only marked **verified** if it has been checked within the last 30 days — or sooner during weather emergencies, policy changes, or service disruptions.

### 6.3 Flagging Protocol
Any outdated, conflicting, or unconfirmed information must be flagged immediately:
1. Status set to **needs-review** or **at-risk**
2. Perplexity posts alert to `OCH_Collab_Log.txt`: `[ALERT] [Resource Name] — [Issue] — [Date]`
3. Resource is removed from public-facing layer until re-confirmed
4. Claude updates the repo entry once resolved

### 6.4 Source Quality Standards
- Primary sources (official org websites) preferred
- 211oregon.org accepted as secondary source
- Social media or news articles require corroboration before use
- No resource marked **verified** without a linkable, dated source

---

## 7. Platform & Ecosystem Integration
*Section lead: Gemini — Chief Ecosystem & Platform Officer*

### 7.1 Single Source of Truth (SSoT) Protocol
- **GitHub (Primary)**: Final authority for code, JSON schemas, and board-approved policies.
- **Google Drive (Workspace)**: Working environment for raw resource data, drafts, and board logs.
- **Sync Rule**: Any file moving from Drive to GitHub must be converted to **kebab-case** (e.g., `resource-vault-schema.json`) to ensure URI compatibility with Firebase and Zendesk APIs.

### 7.2 Cross-Platform Architecture Mapping
| Board Work | Google Drive | Backend |
|---|---|---|
| Board decisions | `/Board/Decisions/` | Audit trail for algorithm changes |
| Resource data | `/Vault/Resources/` | Firestore `resources` collection |
| Public knowledge base | `/Docs/Zendesk/` | Zendesk Guide (Help Center) |

### 7.3 Data Scalability Guardrails
Every Resource Vault entry includes technical metadata to automate trust:
- `last_verified_by` — Director name who performed verification
- `source_reliability_score` — 1–10 scale based on Perplexity's assessment
- `expiry_trigger` — Automatic flag for re-verification when review window is exceeded

### 7.4 Zendesk Readiness Tagging
Every Drive working folder maintains a `Grant_Readiness/` subfolder containing:
- Screenshots of relevant workflows
- Exported PDFs of key documents
- Materials a Zendesk committee or fiscal sponsor auditor would need

### 7.5 Firebase Alignment
The resource schema in Section 6.1 maps directly to the Firestore `resources` collection defined in `OCH_Firebase_Data_Schema_v1.0`. All field names are consistent across Drive, GitHub, and Firestore.

---

## 8. Communication Channels

| Channel | Purpose | Owner |
|---|---|---|
| `OCH_Collab_Log.txt` (Google Drive) | Board async messages and alerts | All directors |
| `/board/` (GitHub repo) | Formal standards and board documents | Claude |
| `/docs/Board_Decisions_Log.md` | Official decision record | Claude |
| George's chat sessions | Real-time direction and approvals | George (Chair) |

---

## 9. Amendment Process

1. Any director posts a proposed amendment to `OCH_Collab_Log.txt` with rationale.
2. Board has 24 hours to respond.
3. Chair approves via chat.
4. Claude commits the updated version with incremented version number.
5. Change is logged in `Board_Decisions_Log.md`.

---

*Document assembled by Claude (Director of Governance & Institutional Integrity)*  
*All sections delivered by assigned directors and integrated by Claude*  
*Section 7 content provided by Gemini (Chief Ecosystem & Platform Officer)*  
*Version 1.1 will incorporate any director amendments following first review cycle*

