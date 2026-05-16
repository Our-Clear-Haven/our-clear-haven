# Zendesk Tech for Good — Technical Appendix
**Project:** OUR CLEAR HAVEN  
**Version:** 1.0  
**Date:** May 2026  
**Prepared by:** OCH AI Advisory Board (Claude + Gemini) + George Scharfetter, Chair  
**Companion to:** Zendesk_Tech_for_Good_Narrative_Final.md (Draft 7, Approved)  

---

## Overview

This appendix provides the technical foundation behind the operational claims in our narrative. It demonstrates how Zendesk Suite integrates with Our Clear Haven's Firebase-powered platform, documents the data flow from resource intake to user delivery, and shows how Crystal — our AI guide — works alongside Zendesk to provide a seamless, trauma-informed support experience.

The architecture has been designed by a small, experienced team with operational maturity above what our stage might suggest. All infrastructure decisions prioritize privacy, scalability, and the lowest possible friction for people in crisis.

---

## 1. Technology Stack

| Layer | Technology | Purpose |
|---|---|---|
| Mobile / Web Frontend | Flutter (Dart) | Single codebase: iOS, Android, Web |
| Backend Database | Firebase Firestore | Real-time resource data, user interactions |
| Authentication | Firebase Auth | Anonymous auth + optional account creation |
| AI Guide (Crystal) | Anthropic Claude API | Compassionate resource navigation, triage |
| Voice Output | Google Cloud TTS (Aoede) | Crystal's voice interface |
| Support Infrastructure | Zendesk Suite | Ticketing, Help Center, Messaging, Escalation |
| Admin Dashboard | Flutter Web (internal) | Moderator review, board oversight |
| Version Control | GitHub (Our-Clear-Haven org) | Open source, all code and documentation |
| Offline Support | Hive / SQLite | Downloadable county resource packs |

---

## 2. Firestore Data Architecture

Our Firebase Firestore database is organized into the following primary collections:

### `resources` Collection
Stores all service provider listings. Structured for real-time querying by location, category, and availability.

```json
{
  "resource_id": "bend-shepherd-house-001",
  "name": "Shepherd's House Ministries",
  "category": "Emergency Shelter",
  "subcategories": ["Men", "Meals", "Low-barrier"],
  "address": "1854 NE Division St, Bend, OR 97701",
  "phone": "541-388-2096",
  "coordinates": { "lat": 44.0682, "lng": -121.3001 },
  "hours": { "mon-fri": "7am–8pm", "sat-sun": "8am–6pm" },
  "vetted_status": "Verified",
  "tags": ["Low-barrier", "Men", "Meals", "Walk-in"],
  "zendesk_article_id": null,
  "last_updated": "2026-05-16",
  "verified_by": "Perplexity AI (OCH Advisory Board)"
}
```

### `interactions` Collection
Anonymized log of Crystal AI sessions. Used for service gap analysis and Zendesk reporting. No PII stored.

```json
{
  "session_id": "anon-uuid-xxx",
  "timestamp": "2026-05-16T14:22:00Z",
  "category_requested": "Emergency Shelter",
  "location_county": "Deschutes",
  "resources_returned": 3,
  "escalated_to_zendesk": false,
  "outcome": "resource_found"
}
```

### `board_tasks` Collection
Internal board task tracking, feeds the moderator dashboard Kanban in real time.

```json
{
  "task_id": "task-gemini-firebase-001",
  "title": "Firebase Architecture Phase 1",
  "assignee": "Gemini",
  "status": "in_progress",
  "file_reference": "docs/firebase_architecture.md",
  "created_at": "2026-05-16"
}
```

### `zendesk_tickets` Mirror Collection
Lightweight mirror of open Zendesk tickets, allowing Crystal to reference ticket status without a live Zendesk API call on every interaction.

---

## 3. Zendesk Integration Architecture

### 3a. Data Flow: Resource Request → Support Ticket

```
USER opens Our Clear Haven app
  ↓
Crystal (Claude AI) receives natural-language request
  ↓
Query fires against Firestore `resources` collection
  ↓
[If resource found] → Return result to user in app
  ↓
[If no resource found OR user requests human help]
  ↓
Crystal creates Zendesk ticket via REST API
  (category, location, urgency, anonymized session ID)
  ↓
Zendesk routes ticket to appropriate queue
  (Shelter / Food / Legal / Crisis)
  ↓
Human moderator (George) reviews and responds
  ↓
Response delivered via Zendesk Messaging back to user
```

### 3b. Crisis Escalation Workflow

When Crystal detects crisis language (suicidal ideation, immediate danger, medical emergency), the following flow activates:

1. Crystal pauses resource navigation
2. Crystal delivers calm, warm crisis acknowledgment
3. Zendesk ticket created with `priority: urgent`, `tag: crisis`
4. Crystal provides 988 Lifeline number (voice + text)
5. Zendesk triggers escalation notification to moderator
6. If moderator unavailable, ticket routes to backup queue

This workflow is never fully automated. Human review is always the final step for crisis tickets.

### 3c. Help Center as Public Resource Directory

Zendesk's Help Center serves a dual purpose:

- **Internal:** Support documentation for Haven Providers (shelters, clinics, food banks) managing their own listings
- **Public-facing:** A searchable web directory of Oregon resources, accessible without downloading the app

Help Center articles mirror `resources` Firestore documents. When Perplexity verifies a resource update, the moderator publishes the change in both Firestore and the corresponding Zendesk article, keeping both in sync.

### 3d. Sunshine Custom Objects — Service Gap Tracking

Zendesk Sunshine Custom Objects will store anonymized interaction data for policymaker reporting:

- Most-searched categories with zero results (service gaps)
- Peak usage times by county
- Escalation rates by need type
- Resource connection success rates

This data is shared in quarterly public reports, making OCH a transparent partner to Oregon Housing and Community Services (OHCS) and future government grant reviewers.

---

## 4. Google Workspace Integration

Our operational documentation lives in Google Drive (`OCH_AI_Collab` folder), with GitHub as the authoritative source of truth for code and formal documents. The workflow:

```
Google Drive (working documents / AI collaboration)
  ↓ finalized
GitHub our-clear-haven repo (version-controlled, permanent)
  ↓ triggers
Firebase (resource data, task status)
  ↓ displayed in
Flutter App + Moderator Dashboard + Zendesk Help Center
```

Zendesk is the outward-facing layer of this stack — the surface that users, haven providers, and donors interact with directly.

---

## 5. Privacy and Data Protection

Our Clear Haven is built privacy-first, which is non-negotiable for the population we serve. Key protections:

- **Anonymous by default:** No account required. Users are identified by session UUID only.
- **No location storage:** GPS coordinates are used for resource proximity search and immediately discarded. We do not store user location.
- **Personal Info Vault:** Optional encrypted document storage (IDs, benefits cards) secured with biometric + PIN. Stored in Firebase with client-side encryption — we cannot access vault contents.
- **Zendesk ticket anonymization:** Tickets contain category, county, and urgency — never name, address, or identifying detail unless the user voluntarily provides it.
- **HIPAA-aware design:** While we are not a covered entity, our interaction design follows HIPAA-adjacent principles for sensitive data handling.

---

## 6. Operational Maturity Indicators

Zendesk reviewers evaluating organizational readiness may find the following relevant:

- **Open source from day one:** All code is public at github.com/Our-Clear-Haven
- **Board governance documentation:** Board_Decisions_Log.md and OCH_Board_Standards_v1.0.md are committed to the repo and version-controlled
- **AI Advisory Board:** Five AI directors (Claude, Grok, Gemini, Perplexity, Copilot) provide parallel-track advisory support across governance, design, data, architecture, and workflow — an unusual but demonstrably productive model for a founder-led pre-incorporation project
- **Established grant pipeline:** Zendesk Tech for Good is one of three active funding tracks (alongside fiscal sponsorship outreach and GoFundMe)
- **Zendesk deadline awareness:** July 15, 2026 — application materials are being finalized over 60 days in advance

---

## 7. Implementation Timeline (Post-Award)

| Phase | Timeline | Zendesk Milestone |
|---|---|---|
| Phase 0: Setup | Month 1 | Zendesk Suite provisioned, team accounts configured |
| Phase 1: Help Center | Month 1–2 | Central Oregon resources published as Help Center articles |
| Phase 2: Ticketing | Month 2 | Support queues configured, Crystal → Zendesk ticket flow live |
| Phase 3: Messaging | Month 3 | Live chat enabled for users who prefer human support |
| Phase 4: Crisis Workflow | Month 3–4 | Escalation flow tested and live; 988 integration confirmed |
| Phase 5: Sunshine Objects | Month 4–6 | Anonymized interaction data flowing; first gap report drafted |
| Phase 6: Scale | Month 7–12 | Haven Provider portal live; statewide resource expansion begins |

---

## 8. Contact

**George Scharfetter**  
Founder & Chief Mission Steward  
Our Clear Haven  
admin@ourclearhaven.org  
ourclearhaven.org  
github.com/Our-Clear-Haven
