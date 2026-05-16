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
