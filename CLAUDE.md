@AGENTS.md

# Voice Journal AI App — System Context

## Product Overview

We are building a Voice-First Mental Clarity Journal application.

Users record 1–2 minutes of daily voice reflections.
The system converts speech into structured emotional insights, behavioral patterns, and weekly mental clarity reports.

This is NOT:
- a chatbot
- a therapy product
- a meditation app
- a generic journaling app

This IS:
- structured voice journaling
- emotional pattern recognition system
- insight-driven reflection tool

---

## Product Principles

All decisions must follow these principles:

### 1. Simplicity first
- one primary action per screen
- minimal cognitive load
- no clutter

### 2. Production-grade UX
- must feel like Apple Health / Day One / Calm
- no “AI prototype” aesthetics
- no chat UI patterns

### 3. Structured intelligence
- unstructured voice → structured insights
- avoid free-form AI output
- consistent JSON-based AI outputs

### 4. Non-therapeutic tone
- no medical advice
- no therapy language
- focus on reflection and clarity

---

## Core User Flow

1. User records voice (1–2 minutes)
2. Audio is uploaded and processed asynchronously
3. Speech-to-text conversion
4. AI extracts:
   - emotional state
   - triggers
   - behavioral patterns
   - short summary
   - 1 micro-action suggestion
5. User receives structured insight card
6. Data is stored for long-term pattern analysis

---

## Core Features (MVP)

### Voice Journal
- press-and-hold or tap-to-record
- auto-stop optional
- no typing anywhere in core flow

### Insight Generation
AI must always return structured output:
- emotional state
- summary
- triggers
- pattern detection (if available)
- micro-action

### History Timeline
- list or calendar view
- play voice recordings
- view AI insights per entry

### Weekly Report
- emotional trends
- recurring triggers
- comparison vs previous week
- simple insights (not analytics-heavy)

### Notifications
- daily reminder
- gentle tone
- no AI-sounding messages

---

## Data Model Principles

Store:
- audio files (object storage)
- transcripts
- AI insights
- emotional states
- weekly summaries
- derived patterns

All time-series data must be optimized for trend analysis.

---

## AI System Rules

### Pipeline
Audio → STT → Transcript → NLP → Structured Insight → Memory Update

### Output Format (strict)
AI responses must always be structured JSON.

### Constraints:
- no long responses
- no conversational tone
- no therapy language
- no hallucinated psychological diagnosis

---

## UX Rules

### Navigation
- bottom tabs or minimal navigation
- max 4–5 screens

### Core Screens
- Home (record)
- Processing state
- Insight result
- History
- Weekly report
- Settings

### UI Style
- neutral, calm, minimal
- no neon / futuristic UI
- no chat bubbles
- no “AI assistant avatar”

---

## Backend Architecture Guidelines

Preferred:
- FastAPI (Python) for AI + audio pipeline

Must include:
- async job queue for processing voice entries
- object storage for audio (S3-compatible)
- structured database (PostgreSQL recommended)

---

## System Constraints

- latency of insight generation can be async (not real-time required)
- reliability > complexity
- clarity of insights > AI sophistication
- retention comes from pattern insights, not AI conversation

---

## Differentiation Logic

This product is NOT:
- journaling app (because it extracts structured patterns)
- voice recorder (because it generates emotional intelligence)
- AI chatbot (because there is no conversation loop)

Users return because:
- they see emotional patterns over time
- they get clarity about their mental state
- they understand triggers in their life

---

## Engineering Priorities

1. reliable voice capture
2. stable async processing pipeline
3. consistent AI outputs
4. fast insight delivery UX
5. clean data model for long-term trends

---

## Output Expectations for Claude

When asked to design or extend the system, Claude should produce:

- concrete architecture
- real production decisions
- UI that matches modern consumer apps
- no vague startup ideas