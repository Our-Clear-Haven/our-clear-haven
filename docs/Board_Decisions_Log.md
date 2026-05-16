# Our Clear Haven — Board Decisions Log

This log records major decisions made during the development of Our Clear Haven. It serves as an audit trail for fiscal sponsors, grant reviewers, and future board members.

---

## May 2026

### Repository Structure
**Date**: 2026-05-16  
**Decision**: Establish two GitHub repositories under the `Our-Clear-Haven` organization:
- `Our-Clear-Haven/autoposter` — dedicated to X (Twitter) posting automation
- `Our-Clear-Haven/our-clear-haven` — main platform repository (app code, documentation, governance)

**Rationale**: Separation of concerns. The autoposter has a single focused job; keeping it separate from app code reduces maintenance risk and keeps the GitHub Actions workflow clean.  
**Approved by**: George Scharfetter (Chair)  
**Status**: ✅ Complete

---

### Crystal Persona Definition
**Date**: 2026-05-16  
**Decision**: Formally define Crystal as the Our Clear Haven app's user-facing AI guide — a distinct character and persona, not an organizational role or board seat.

All Crystal persona content (system prompts, voice guidelines, character notes) lives in the `/crystal/` folder. AI advisors to the organization are listed by their actual names.  
**Approved by**: George Scharfetter (Chair)  
**Status**: ✅ Complete

---

### GitHub as Primary Source of Truth
**Date**: 2026-05-16  
**Decision**: GitHub (`Our-Clear-Haven` organization) is the authoritative source for all code, documentation, and board decisions going forward. All major work is version-controlled here before any other distribution.  
**Approved by**: George Scharfetter (Chair)  
**Status**: ✅ Active

---

### X Post Strategy — Media-First
**Date**: 2026-05-16  
**Decision**: All scheduled X posts will include attached images (1080×1350px vertical format). Text-only posts are suspended pending evidence that reach improves with consistent image attachment. Image assets are maintained in `Our-Clear-Haven/autoposter/images/`.  
**Approved by**: George Scharfetter (Chair)  
**Status**: ✅ Active

---

### Zendesk Tech for Good Application — Narrative Approved
**Date**: 2026-05-16  
**Decision**: Approve final narrative (Draft 7) for the Zendesk Tech for Good grant application. Document filed at `/docs/Zendesk_Tech_for_Good_Narrative_Final.md`.

Narrative prepared collaboratively by the AI Advisory Board (Claude, Grok, Perplexity, Gemini) across seven drafts. Key elements: founder story, Oregon homelessness statistics, Firebase + Zendesk integration architecture, 1,000-user first-year target, and request for full Suite access and implementation support.  
**Approved by**: George Scharfetter (Chair)  
**Status**: ✅ Ready for submission — deadline July 15, 2026

---

### AI Advisory Board Expansion
**Date**: 2026-05-16  
**Decision**: Expand the AI Advisory Board to include Gemini (Google DeepMind) and Perplexity AI in addition to existing advisors Claude (Anthropic) and Grok (xAI). Microsoft Copilot under consideration as development tooling rather than a board seat.

**Rationale**: Gemini brings Google Workspace integration and multimodal capabilities; Perplexity provides real-time research and grant monitoring. All AI advisors remain advisory only — Chair retains final authority on all decisions per the Governance framework.  
**Approved by**: George Scharfetter (Chair)  
**Status**: ✅ Active

---

### Microsoft Copilot Appointed to AI Advisory Board
**Date**: 2026-05-16  
**Decision**: Following a two-round board vote, Microsoft Copilot is appointed as the 5th AI Advisory Board member. The board reached a 2-2 tie between Copilot and GPT-4o; Chair George Scharfetter exercised the tiebreaker in favor of Copilot.

**Rationale**: Copilot provides GPT-4o reasoning capability plus Microsoft integration layer — VS Code/GitHub Copilot for active Flutter development, Azure for Nonprofits infrastructure credits, DALL-E 3 image generation, and Office-native document output. Assessed as two capabilities for the price of one board seat.

**Full board (5 AI + Chair)**:
- Claude (Anthropic)
- Grok (xAI)
- Gemini (Google DeepMind)
- Perplexity (Perplexity AI)
- Copilot (Microsoft) ← new

**Approved by**: George Scharfetter (Chair, tiebreaker)  
**Status**: ✅ Active

---

### Chair Title Established
**Date**: 2026-05-16  
**Decision**: George Scharfetter's official title on the OCH Dual Board of Directors is **Founder & Chief Mission Steward** — a board compromise across five AI director nominations over three rounds.

**Approved by**: George Scharfetter (Chair)  
**Status**: ✅ Active
