## Trigger

- The user asks for an automation result message or an interface prompt.

## Inputs

- The current message, sample result, screenshot, or explanation supplies the outcome.
- The interface location determines the format and any space limit.
- The meaning and source of each status establish what the message can claim.
- The expected client action identifies a supported next step.

## What happens

1. The plugin asks up to three short questions about missing information. It asks what happened and where the message appears when no details are supplied.
2. It waits for required answers and remembers them. If a status such as paid is undefined, it asks what the status proves before drafting that message.
3. It identifies the affected item and supported outcome. It distinguishes a saved item, a system status, and a confirmed real-world result.
4. It writes the requested message in plain English. It keeps internal identifiers and raw errors in builder or support details.
5. For a partial result or timeout, it states what succeeded and what remains unconfirmed. It does not recommend a retry that could repeat a completed action.
6. If a Zite builder prompt is requested, it separates visible copy from source conditions and values. It asks about an unknown mapping before implementation.
7. It returns the finished copy or prompt. If implementation was separately requested, it checks the mapping and rendered states and reports draft, preview, or published status.
8. It responds to a correction by revising the affected text using the latest established facts.

## Outputs

- Finished messages or a builder prompt in the current chat.
- An interface change only when separately requested and completed. The package includes writing rules without an account-specific logging workflow.
