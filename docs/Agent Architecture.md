# Agents, Tools, and Workflows

## agents/
- `flashcard-agent.ts`  
  Orchestrates flashcard generation, review sessions, and interacts with user state.
- `resource-agent.ts`  
  Discovers, validates, and ranks learning resources (web, books, PDFs).
- `study-plan-agent.ts`  
  Creates and adjusts study plans and learning stages based on user goals and progress.
- `analytics-agent.ts`  
  Processes session data (difficult cards, time spent) and computes learning-state updates.

---

## tools/
- `web-scraper-tool.ts`  
  Scrapes and extracts structured content from web resources given a topic.
- `search-tool.ts`  
  Wraps web/search APIs to find relevant links, papers, and references.
- `pdf-parser-tool.ts`  
  Parses PDFs, extracts text/structure, and returns sections for indexing.
- `ocr-tool.ts`  
  Extracts text from images or scanned documents for resource ingestion.
- `db-tool.ts`  
  Database access helper for storing resources, flashcards, sessions, and metrics.
- `metadata-extractor.ts`  
  Extracts titles, authors, dates, and citations from resources (optional).

---

## workflows/
- `resource-discovery-workflow.ts`  
  Given a topic/syllabus, finds resources, extracts metadata, and stores approved items.
- `study-plan-workflow.ts`  
  Builds a staged study plan from syllabus + user constraints (time, level, deadlines).
- `flashcard-generation-workflow.ts`  
  Generates flashcards from selected resources using templates and difficulty levels.
- `practice-session-workflow.ts`  
  Runs review sessions, records responses, timing, and card difficulty feedback.
- `adaptation-workflow.ts`  
  Consumes analytics to update user model and influence subsequent flashcard generation.
- `analytics-workflow.ts`  
  Aggregates session metrics, computes spaced-repetition schedules and progress reports.
