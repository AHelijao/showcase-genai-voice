# GenAI Voice Assist — showcase

**Portfolio:** [ahelijao.github.io](https://ahelijao.github.io/) · Chapter III  
**Private source:** not linked

> Docs-only public view. No client names, no métier scripts, no account IDs / tfvars.

## Elevator

Evolve a **path-based (parcours) phone callbot** into a **GenAI conversation layer** on AWS — without throwing away the contact-center foundation.

## Need

| Pain | Response |
|------|----------|
| Rigid IVR / Lex journeys break on messy callers | Additive GenAI layer for freer dialogue |
| “Just call Bedrock from prod” is reckless | Separate **POC / AI module** from base Connect+Lex parcours |
| Ops needs repeatability | Terraform modules, env separation (dev/prod pattern) |

## Architecture (sanitized)

```text
Caller
  │
  ▼
Contact center (Amazon Connect)
  │
  ▼
NLU / bot (Lex) ── parcours intents (baseline)
  │
  │  optional code hook
  ▼
┌─────────────────────────────────────┐
│  AI callbot layer (additive)        │
│  · conversation memory (TTL)        │
│  · Lambda “brain”                   │
│  · managed GenAI invoke             │
└─────────────────────────────────────┘
```

**Design rule:** the GenAI module **adds** resources; it does not silently rewrite the baseline parcours stack. That keeps rollback and comparison honest.

## What this demonstrates

- Real cloud telephony + NLU + serverless GenAI composition
- IaC discipline for an AI feature, not a one-off console click
- Clear boundary between **journey bot** and **generative dialogue**

## Stack

`Amazon Connect` · `Lex` · `Lambda` · DynamoDB (short-lived memory) · `Bedrock` (or equivalent managed LLM path) · `Terraform` modules

## Explicitly not in this repo

Domain prompts, client vocabulary, production tfvars, IAM account specifics, Lambda source.


## Full source (private)

Access required. The implementation lives in a **private** repository:

- [genai-voice-assist](https://github.com/AHelijao/genai-voice-assist)

Without collaborator access, GitHub will show **404**. To request access: email [helijao.andriamandranto@gmail.com](mailto:helijao.andriamandranto@gmail.com), message on [LinkedIn](https://linkedin.com/in/helijaoa), or open an issue on **this** showcase repo — I’ll grant access case by case.

---

← back to [portfolio](https://ahelijao.github.io/) · Helijao Andriamandranto
