# GenAI Voice Assist — showcase

**Portfolio:** [ahelijao.github.io](https://ahelijao.github.io/) · Chapter III

> Sanitized public view. No client names, no domain scripts, no production configs.

## What it is

An evolution of a **path-based / scripted phone callbot** toward a **GenAI conversation layer** on AWS: more natural understanding, less rigid branching, still grounded in contact-center + NLU + serverless infrastructure.

## Problem

Journey bots scale poorly when callers don’t follow the happy path. Adding a model is not enough — you need staging, IaC, and clear boundaries between dialogue intelligence and backend systems.

## What this shows

- Callbot architecture shift: fixed parcours → GenAI-assisted dialogue
- Cloud building blocks: contact center, NLU, Lambda, managed GenAI
- Multi-environment delivery with Terraform

## Stack

`Amazon Connect` · `Lex` · `Lambda` · `Bedrock` · `Terraform` · (supporting AWS data stores as needed)

## What’s intentionally omitted

Business flows, prompts tied to a specific métier, tfvars, account IDs, and any production secrets.

## Status

Architecture showcase. Implementation details on request / under NDA.

---

*Helijao Andriamandranto — software & cybersecurity*
