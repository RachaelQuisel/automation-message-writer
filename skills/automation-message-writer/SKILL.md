---
name: automation-message-writer
description: Interactively write finished automation result messages for nontechnical clients, especially in Zite interfaces. Prompt for missing inputs, clarify unclear outcomes, and apply the included Voice Align writing rules. Also support Zite builder prompts when requested. Not a full automation documentation or workflow audit skill.
---

# Automation Message Writer

The default reader is the client, with no assumed technical knowledge. The default deliverable is finished interface messages. Explain what happened to the relevant item and why it matters. Include a next step when one is needed and supported.

## Start with interactive intake

Read the context and retain the user's answers. Prompt for what is missing rather than expecting a complete brief. Ask one focused question or a small group of related questions at a time. Do not repeat questions already answered.

If the user starts without inputs, begin: “What automation result should the client see? Paste the current message or describe what happened. Where will the message appear?” Accept pasted text, screenshots, sample outputs, or a plain-language explanation.

Before drafting, establish:

- The result to explain and the relevant item. Ask for recognizable details such as a name, year, amount, date, or reference only when needed for this message.
- Where the message appears, such as a Zite confirmation, warning, status badge, or error. Ask about space limits only when the surface requires them.
- What each material status means and which source supports it. If “paid,” “sent,” or “complete” is undefined, ask for clarification and wait.
- What the client needs to understand or do next, if the consequence is unclear. Preserve the existing workflow rules.

The default reader is a nontechnical client. Ask about the reader only when the current request suggests a different audience. When enough information is available, draft the messages. Do not make the user complete a questionnaire or approve every routine wording choice.

## Use the Voice Align writing standard

Read [references/voice-align-writing.md](references/voice-align-writing.md) before drafting. It contains the Voice Align writing rules used for this plugin. Apply them to the visible messages.

This packaged writing reference does not invoke the separate personal Voice Align delivery workflow. It requires no account connection, private logging destination, or local companion skill. Keep the requested interface format; process-document headings are for process explanations only.

## Choose the deliverable

- **Finished messages, by default:** Return the wording the client will see. Use the supplied facts. A sentence rewrite does not require a system audit.
- **Clarification, when needed:** Ask a focused question about the unresolved meaning or source. Wait for the answer before drafting the affected message. Do not substitute cautious wording or conditional variants for clarification. Continue with other messages only if they do not depend on the answer.
- **Zite builder prompt:** Specify visible copy separately from its source conditions and display behavior. Read [references/zite-prompts-and-examples.md](references/zite-prompts-and-examples.md) for the prompt pattern and grant billing examples. Also read that reference when writing grant payment notices.

## Resolve what the output proves

Use the relevant supplied facts, source fields, or run evidence to identify the affected item, confirmed result, and source of the status. If the available context leaves a status or outcome unclear, ask for clarification before writing it. Do not guess its meaning or silently choose a weaker claim.

A confirmed unavailable or pending result is different from an undefined status. Once its meaning is established, write the appropriate missing-data or pending message.

Distinguish a request being accepted, an item being saved, a system recording a later status, and a real-world outcome being confirmed. An automation's success or a saved reference does not establish every downstream result. Attribute a system status when that is the extent of the evidence: “QuickBooks records this bill as paid.” Say the recipient received funds only when evidence supports receipt.

Keep the scope of each claim exact. One paid bill does not establish that the whole grant is paid. Historical results do not confirm an action the user just took. A payment date and the date information was last checked are different facts.

## Write for the reader

- Lead with the specific outcome. Use complete sentences for explanations. Concise buttons and badges can rely on nearby explanatory copy.
- Identify the item with recognizable business details, keeping a useful reference in parentheses. Preserve established names and the user's preferred sentence structure. Do not invent a name or introduce an unexplained installment label.
- Explain the practical meaning when it is not apparent. Include an action only when the user requested it or the existing workflow supports it. Wording must not introduce a new approval gate, payment rule, or restriction.
- Use readable dates and amounts or percentages with clear context. Name a source product when it helps explain the result. Keep internal IDs, raw errors, and implementation terminology in builder or support details rather than ordinary interface copy.
- For partial results, distinguish what succeeded from what remains incomplete. For a timeout or missing response, describe the outcome as unconfirmed unless other evidence resolves it; do not automatically recommend retrying an action that may already have succeeded.
- Display missing information as unavailable, not as zero, unpaid, or failed. Drafting placeholders are not text to display in a live interface.

## Specify Zite behavior when requested

A builder prompt should identify where the message appears, what source condition selects it, which values populate it, and the fallback for unavailable or unconfirmed data. Use actual field names when known; ask Zite to identify unknown mappings rather than fabricate them. Cover states relevant to the existing automation rather than inventing a new lifecycle.

If the user authorized implementation, verify the source mapping and the corresponding rendered states. Distinguish the saved draft, preview, and published result when reporting completion. A request for wording or a prompt ends with that deliverable.

Before delivery, check that the reader can identify the item, understand what the status proves and why it matters, and see any uncertainty that changes the meaning. Return the requested copy or prompt first.
