# Claude Code Configuration for BEBA-ROS

This directory defines Claude Code roles and slash-command templates for the BEBA Monography repository.

## Structure

```text
.claude/
  agents/       role definitions
  commands/     reusable task prompts
```

## Principle

Claude Code works on repository objects, not vague chat tasks.

Preferred object types:

- Concept
- Claim
- Evidence Map
- Theory Integration Unit
- Ontology Candidate
- Chapter Draft
- Paper Draft
- Figure
- ADR

## Rule

Do not automatically modify canonical ontology or ConstructLedger unless explicitly instructed. Create candidates first.
