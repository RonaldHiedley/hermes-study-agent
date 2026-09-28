# Use when starting, logging, or ending study sessions. Tracks temporal and performance metadata.

## Flow

### start-session
Input: `Subject, Topic, Planned Duration, Objective`
Captures automatically: startTime, date, subject, topic, plannedDuration, objective
Initializes: questions_attempted=0, correct=0, accuracy=0%, difficulties=[], observations=[]
Returns: session_id
Example: `Study: matemática, função composta, 45 min, entender domínio`
**Important:** `log-progress` only updates partial data. Use `end-session` when done to calculate actual duration and percentage.

### log-progress
Input format: `<n> questões +<acertos> <dificuldade> "<observação>"`
Updates existing session
Example: `5 questões +3 domínio "tive que refazer 3"`
**Only call log-progress when you have actual progress to add.** Accumulates questions_attempted, correct, difficulties, observations

### end-session
Captures: endTime (automatic), actualDuration (calculated or user-provided), accuracy (calculated)
Finalizes and saves session to persistent storage
**Rule:** If you explicitly state how long you studied, that value becomes actualDuration. Otherwise, actualDuration is calculated from start/end timestamps.

## Data Schema
```yaml
sessionId: uuid
startTime: ISO-timestamp
endTime: ISO-timestamp
date: YYYY-MM-DD
subject: string
topic: string
plannedDuration: ISO-duration (from start-session input)
actualDuration: ISO-duration (calculated from timestamps OR explicitly stated)
objective: string
questionsAttempted: integer
correct: integer
accuracy: percentage (or "unknown" if no attempts)
difficulties: array[string]
observations: array[string]
```

## Duration Rules
- plannedDuration comes from the initial "X minutos" in start-session
- actualDuration is calculated from start/end timestamps unless user explicitly states time studied
- NEVER replace plannedDuration with actualDuration
- No invented duration values

## Notes
- No automated reminders (use cron separately)
- No external integrations (Notion/Calendar/Anki)
- No auto-registration without explicit confirmation
- Prompt for missing data only when operationally necessary