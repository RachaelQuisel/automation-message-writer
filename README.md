# Automation Message Writer

I built this plugin to help automation builders write messages their clients can understand. It asks up to three short questions about missing details. It waits for required answers and remembers them. It clarifies ambiguous statuses before returning finished interface copy. It includes the Voice Align writing standard.

## Install

In Claude Code, add this repository as a marketplace and install the plugin by name:

```text
claude plugin marketplace add RachaelQuisel/automation-message-writer
claude plugin install automation-message-writer@automation-message-writer
```

The marketplace catalog is `.claude-plugin/marketplace.json`. It lists this repository root as the plugin source, next to `.claude-plugin/plugin.json`.

## Start

In Codex, invoke `$automation-message-writer` after adding the plugin or skill. In Claude Code, invoke `/automation-message-writer:automation-message-writer` after loading the plugin.

You can start with: “Help me write the message for this automation.” The assistant will ask what happened and where the message appears. You can supply a current message, a sample result, a screenshot, or a plain-language explanation.

If a status such as “paid” is unclear, the assistant asks for its meaning before drafting. It remembers answers already supplied. The default reader is a client with no technical knowledge.

## Package contents

- The interactive Automation Message Writer skill.
- The Voice Align writing reference.
- Fictional Zite examples and an optional builder prompt.
- A 1024 × 1024 transparent PNG icon.
- Separate Codex and Claude plugin manifests.

This package writes copy from information you provide. It includes no service connection or account-specific logging workflow. Publishing or changing a live interface is a separate request.

## Local validation

The package includes both plugin manifest layouts. Manifest validation confirms structure; it does not establish installation in either app. The ZIP contains the plugin folder as its top-level directory.

Read [how it works](Automation-Message-Writer-HowItWorks-2026-10-03.md) for the questions, steps, and results.

## License

MIT. See [LICENSE](LICENSE).
