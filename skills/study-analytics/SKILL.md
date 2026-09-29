# Use when analyzing existing study-session logs. READ-ONLY. Never modify sessions.

## Purpose
- Analyze ONLY existing records from `study-session`
- DO NOT read/write to study-session, study-planner, or any other skill
- ONLY produce analysis output
- NEVER start, update, or end sessions
- NEVER create study plans or recommendations
- NEVER invent data

## Commands

### overview
Shows total: sessions, questions, total time planned vs real

### performance --subject < matière >
Shows performance metrics by subject

### trends --topic < tópico >
Shows evolution of accuracy by topic

### duration
Shows planned vs actual duration summary

### difficulties
Shows recurring difficulties (must appear in 2+ different sessions)

### summary
Full report on all available data

## Rules (Non-negotiable)

1. `0 sessions` → "no data available"
2. `1 session` → "data description only"
3. `2 sessions` → "descriptive comparison, no trend claimed"
4. `3+ sessions` → "can identify patterns, stating number of sessions"
5. NEVER claim "major difficulty" without comparable data
6. Difficulty: 1 session → registered; 2+ sessions → recurring
7. ALWAYS separate: [DADOS REGISTRADOS] | [ANÁLISE] | [SUGESTÕES]
8. NEVER confuse plannedDuration with actualDuration
9. NEVER invent performance thresholds, targets or criteria without explicit user input
10. Describe observed changes before interpreting them
11. No study plans, no Notion/Calendar modifications
12. NEVER transform analysis into planning - use study-planner for that

## Data Source
Read-only from existing `study-session` records. No local cache.