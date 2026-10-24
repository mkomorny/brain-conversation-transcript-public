# Brain Conversation Transcript

> **Tri-Platform Agent Skill** for Claude Desktop / Code, Grok CLI, and Google Antigravity / Gemini.  
> Archival Transcript Extraction into Memory — Captures complete conversation transcripts, procedural steps, and user exchanges directly into Second Brain memory for long-term procedural recall.

---

## Overview

`brain-conversation-transcript` provides standardized capabilities across conversational AI platforms:
- Full transcript synthesis with turn-by-turn context preservation.
- Procedural command and code execution step archiving.
- Direct save to Second Brain tagged with #transcript and !state.
- Tri-platform NTFS junctions connecting Claude, Grok, and Antigravity.
- Standard documentation suite: SKILL.md, HOW_TO_USE.txt, IMPLEMENTATION_PLAN.md, and README.md.

---

## Tri-Platform Architecture

Zero duplicate code across platforms. Canonical source resides in `.agents`:
- **Canonical Source**: `C:\Users\<you>\.agents\skills\brain-conversation-transcript`
- **Claude**: `C:\Users\<you>\.claude\skills\brain-conversation-transcript` (NTFS Junction)
- **Grok**: `C:\Users\<you>\.grok\skills\brain-conversation-transcript` (NTFS Junction)
- **Antigravity**: `C:\Users\<you>\.gemini\config\skills\brain-conversation-transcript` (NTFS Junction)

---

## Documentation Suite

- [`HOW_TO_USE.txt`](HOW_TO_USE.txt): Standardized user guide and prompt templates.
- [`IMPLEMENTATION_PLAN.md`](IMPLEMENTATION_PLAN.md): Feature checklist and roadmap.
- [`App Changes Tracker.html`](App%20Changes%20Tracker.html): Interactive visual version log.
- [`SKILL.md`](SKILL.md): Agent system instructions and triggers.
