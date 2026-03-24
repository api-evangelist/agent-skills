# The Agent Skills Spec Has a Governance Problem

**Author:** Dachary Carey
**Date:** 2026-03-20
**Source:** LinkedIn

---

The Agent Skills spec has a governance problem.

Agent Skills claims to be "a simple, open format for giving agents new capabilities." 20+ platforms have adopted it. But Anthropic, the spec's creator, still controls the repo unilaterally, and that's starting to cause real interoperability problems.

In the last month alone:

- A directory structure change landed as a "visual cleanup" with "no semantic changes," then required a follow-up PR to clarify the language it supposedly didn't change
- The allowed-tools field uses Claude Code-specific tool names (Read, Write, Bash) in a supposedly platform-neutral spec
- A complete rewrite of the implementation guide shipped with no changelog or version bump

The spec has no version number. No changelog. No review process for breaking changes. No governance beyond two Anthropic-affiliated maintainers. Community issues proposing basic governance (versioning, changelogs, labels on spec-altering PRs) get converted to discussions that don't get actioned.

This matters if you publish or consume Agent Skills. A skill that works on Claude Code may silently fail on Cursor, Copilot, or Roo Code, and you won't know why because there's no way to tell which version of the spec anyone is building against.

If you work at a company that publishes Agent Skills and has a partnership with Anthropic, this is where you can help. Raise this with your partner team. GitHub issues from individual contributors are easy to dismiss. Enterprise partners raising governance concerns in business reviews are not. The technical fixes are straightforward (version the spec, publish changelogs, give stakeholders a voice). What's missing is the incentive for Anthropic to act.

The spec is at a crossroads. It can become a real open standard with proper governance, or it can keep quietly drifting toward a Claude Code implementation guide with an "open" label. Which way it goes depends on whether the companies building on it speak up.
