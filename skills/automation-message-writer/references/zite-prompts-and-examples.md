# Zite message examples and optional builder prompt

These examples use fictional values. Replace them with supplied facts. Brackets are drafting placeholders, not literal interface text.

## Clarify before drafting

If the user supplies an undefined status, ask: “What does ‘paid’ mean here? Does QuickBooks record the bill as paid, or is receipt by the recipient confirmed?” Wait for the answer before writing the payment message.

If no inputs are supplied, ask: “What automation result should the client see? Paste its current message or describe what happened. Where will the message appear?”

## Grant bill examples

Use the known year, grant number, and payment percentage to identify the bill. Put a useful bill reference in parentheses. A display label does not rename the accounting record.

If QuickBooks status is the established meaning:

> This grant was already billed. QuickBooks records the 2027–2028 Grant #2041 bill for 50% of the award (bill 700123) as paid on March 12, 2028.

If only bill creation is confirmed:

> The 2027–2028 Grant #2041 bill for 50% of the award (bill 700123) was created in QuickBooks.

If receipt by the recipient is confirmed:

> [Recipient] received [amount] for [grant or payment] on [payment date] (bill [reference]).

## Confirmed incomplete results

If bill creation succeeded and saving its reference failed:

> The bill was created in QuickBooks. Its reference could not be saved here.

If the result of a timed-out request is confirmed to be unresolved:

> We haven’t confirmed whether the bill was created in QuickBooks.

If payment information could not be loaded:

> Payment details are unavailable right now.

Missing payment details do not establish that the bill is unpaid. Do not automatically recommend retrying an action that may already have succeeded.

## Builder prompt, only when requested

> Update the [location] message for [action or item].
>
> **Visible copy:** “[finished sentence].”
>
> **Display condition and values:** Show it when [verified source condition]. Populate [visible values] from [known source fields]. The status means [supported outcome].
>
> **Fallback:** When [known missing or unconfirmed condition], show “[accurate fallback].” Keep historical results separate from confirmation of the action just taken.
>
> Preserve existing workflow rules. Verify the rendered states against the source data. Report whether the result is a draft, preview, or published change.

Ask about unknown mappings before implementing them. The default deliverable remains finished messages.
