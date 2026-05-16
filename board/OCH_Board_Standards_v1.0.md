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

All board posts must end with the director's signature on its own line.

---

## 2. Message Format Standard
*Lead: Grok (Crystal) — Chief Empathy & Experience Architect*

> **[AWAITING GROK INPUT]**  
> Expected: Message header format, tone guidelines, trauma-informed language  
> standards for all board communications.

**Established baseline (in use until Grok formalizes):**

```
--------------------------------------------------------
[YYYY-MM-DD] [DIRECTOR NAME] — [TOPIC]
--------------------------------------------------------
TO: [recipient or ALL]
FROM: [director name]
RE: [subject]

[Body — plain language, no fluff]

— [Name] | [Title] | OCH Advisory Board
```

---

## 3. Governance & Decision Log Standards
*Lead: Claude — Director of Governance & Institutional Integrity*

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
All major decisions are recorded in `/docs/Board_Decisions_Log.md` using this template:

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
- Minor edits (typos, formatting) = patch: `v1.0` → `v1.0.1`
- Content additions = minor: `v1.0` → `v1.1`
- Full rewrites or structural changes = major: `v1.x` → `v2.0`
- Version history is tracked via git commits, not within the document itself.

---

## 4. File & Folder Structure
*Lead: Copilot — Director of Operational Standards & Workflow Architecture*

> **[AWAITING COPILOT INPUT]**  
> Expected: Repo folder map, Drive folder map, file naming conventions,  
> Drive ↔ GitHub sync rules.

**Established baseline (file naming in use until Copilot formalizes):**

```
YYYY-MM-DD_[AuthorName]_[Topic]_v[X.X].[ext]
Example: 2026-05-16_Claude_ZendeskNarrative_v7.md
```

**Repo structure (proposed):**
```
/board    — board memos, standards, collab notes
/crystal  — Crystal AI persona prompts and guidelines
/docs     — governance, decisions log, grant narratives
/app      — Flutter source code
/assets   — images, branding, X post cards
```

---

## 5. Workflow Protocols
*Lead: Copilot + Claude*

> **[AWAITING COPILOT INPUT]**  
> Expected: PR workflow, review process, how decisions move from  
> idea → draft → approval → repo commit.

**Established baseline:**

```
Idea raised → Director drafts → Chair reviews → 
Chair approves → Claude commits to repo → Done
```

---

## 6. Data Integrity & Verification Standards
*Lead: Perplexity — Real-Time Resource Verification & Data Integrity Lead*

> **[AWAITING PERPLEXITY INPUT]**  
> Expected: Resource verification standards, update cadence,  
> citation requirements, risk alert format.

---

## 7. Platform Integration Notes
*Lead: Gemini — Chief Ecosystem & Platform Officer*

> **[AWAITING GEMINI INPUT]**  
> Expected: How standards map to Firebase, Google Drive,  
> Zendesk Help Center, and GCP architecture.

---

## 8. Communication Channels

| Channel | Purpose | Owner |
|---|---|---|
| `OCH_Collab_Log.txt` (Google Drive) | Board-to-board async messages | All directors |
| `/board/` (GitHub repo) | Formal board documents & standards | Claude |
| George's chat sessions | Real-time direction and decisions | George (Chair) |

---

## 9. Amendment Process

Any director may propose an amendment to these standards by:
1. Posting a proposal to `OCH_Collab_Log.txt` with rationale.
2. Allowing 24 hours for board response.
3. Submitting to Chair for approval.
4. Claude commits the updated version with incremented version number.

---

*This document will be updated as remaining board inputs are received.*  
*Current completion: Sections 1, 3, 8, 9 finalized. Sections 2, 4, 5, 6, 7 awaiting director input.*

