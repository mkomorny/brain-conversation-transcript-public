---
name: brain-conversation-transcript
description: >-
  Captures the conversation transcript, procedural steps, and user exchanges directly
  into a Second Brain memory. Analyzes the chat history, compiles a detailed transcript
  record with turn-by-turn context, and saves it immediately to Second Brain via remember.
---

# Brain Conversation Transcript (`/brain-conversation-transcript`)

Use this skill to archive the full procedural transcript and dialogue of the active conversation into your personal Second Brain knowledge base.

---

## When Invoked

Direct user invocation of this command carries explicit authorization. **Execute immediately** by analyzing the conversation transcript, calling the `second-brain` MCP `remember` tool, and reporting the confirmed memory ID and saved record.

---

## Execution Workflow

### Step 1: Read and Compile the Transcript
1. Scan the conversation transcript from the first user turn to the current state.
2. Structure the transcript record into clear sections:
   - **Session Overview**: Conversation ID, timestamp, and core user goals.
   - **Chronological Interaction Log**: Key prompts, agent actions taken, tools executed, and problems solved across each turn.
   - **Code & File Changes**: List of all files created, modified, or verified during the dialogue.
   - **Outcome / Final State**: The resolution reached at the end of the transcript.

### Step 2: Extract Tags and Volatility
- **Tags**: Include `#transcript`, `#conversation`, project name, tools used, and topic keywords.
- **Volatility**: Default to `!state` (or `!durable` if archiving a landmark session).
- **Source**: Set to `"antigravity"`, `"claude"`, or `"grok"` depending on the active platform.

### Step 3: Execute Save
Call `remember` on the `second-brain` MCP server immediately:
```json
{
  "content": "<structured conversation transcript record>",
  "tags": ["transcript", "conversation", ...],
  "volatility": "state",
  "source": "antigravity"
}
```

### Step 4: Confirm
Report back:
- 🆔 **Memory ID**
- 🏷️ **Tags & Volatility**
- 📄 **Transcript Summary & Confirmation**

---

## Syntax

```
/brain-conversation-transcript [optional focus or tag]
```

## Examples

```
/brain-conversation-transcript
/brain-conversation-transcript #live-actions
```
