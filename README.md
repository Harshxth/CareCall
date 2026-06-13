# CareCall

> Agentic voice AI that calls discharged patients in their own language and walks them through recovery, built to cut avoidable readmissions.

[![Top 5 HackUSF 2026](https://img.shields.io/badge/Top%205-HackUSF%202026-FACC15)](#)
[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://python.org)
[![Google ADK](https://img.shields.io/badge/Google%20ADK-multi--agent-4285F4)](#)
[![Gemini](https://img.shields.io/badge/Gemini-reasoning-8E75B2)](#)
[![ElevenLabs](https://img.shields.io/badge/ElevenLabs-70%2B%20languages-111111)](#)

**Top 5 at HackUSF 2026.** Built in 24 hours with Alan Risal, Kevin Fernandez, and Sharan Santharam.

## The problem

1 in 5 patients are readmitted within 30 days. Often it is not a medical failure: they were discharged exhausted, handed a six-page document they could not fully process, and then left to manage recovery alone.

## What it does

CareCall calls patients the day after discharge, in their own language, and walks them through their recovery plan.

- A **9-step care-protocol state machine** guides each call through the recovery instructions.
- **Auto-escalation to nurses** the moment an urgent flag is raised.
- A **structured post-call report** is generated and emailed to the physician after every call.
- Voice in **70+ languages** via ElevenLabs.

## Architecture

A multi-agent system on **Google ADK + Gemini**. Gemini handles call summarization and highlight extraction, turning each conversation into a structured follow-up document for the doctor. **ElevenLabs** provides natural multilingual voice. A **HIPAA-compliant Supabase** backend stores encrypted PHI.

```
Discharge  ->  Voice call  ->  Comprehension check  ->  Triage / escalate  ->  Physician report
```

## Tech stack

| Layer | Tool |
| --- | --- |
| Agents | Google ADK |
| Reasoning | Gemini |
| Voice | ElevenLabs (multilingual, 70+ languages) |
| Backend | Supabase (HIPAA-compliant, encrypted PHI) |
| Frontend | React |

## My role

I built the multi-agent architecture: the Gemini-powered call summarization and highlight extraction that produces the structured physician report after each call, plus the ElevenLabs voice integration across 70+ languages.

## Credits

Team project built at HackUSF 2026 with Alan Risal, Kevin Fernandez, and Sharan Santharam. Originally authored as **DischargeGuard** by [@alanrisal](https://github.com/alanrisal); this repository is the same project.
