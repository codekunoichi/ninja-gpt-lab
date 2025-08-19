# Cofounder Fit GPT

A custom GPT that helps founders (and future cofounders) think clearly, answer rigorously, and
track decisions across the tough questions that make or break a founding team.

**Design principles**
- No invention. The model never fabricates; it asks follow‑ups and marks Unknowns.
- One question at a time, with a live scoreboard.
- Socratic probing to elicit specifics, tradeoffs, and evidence.
- Exportable artifacts: Answer Sheet, Red‑Flags Ledger, Deal/No‑Deal Scorecard, Email outlines.

## Quick Start

1. **Clone this repo**  
   ```bash
   git clone https://github.com/<you>/cofounder-fit-gpt.git
   cd cofounder-fit-gpt
   ```

2. **Create your Custom GPT** (ChatGPT > Explore > Create a GPT)  
   - **Name:** Cofounder Fit Coach  
   - **Instructions:** paste `prompts/system.md`  
   - **Knowledge:** upload `data/questions.json` and (optionally) your own PDFs/notes.  
   - **Capabilities:** turn ON web browsing only if you want link lookups; otherwise OFF.  
   - **Privacy:** disable training on your data.

3. **Use it**  
   - Say: *“/start Funding & Runway”* or *“/start Decision Rights”*.  
   - The coach will ask, reflect, probe, draft, and track status.  
   - At any time: `/scoreboard`, `/export answers`, `/export redflags`, `/export scorecard`.

4. **Capture outputs**  
   - Paste `/export answers` into `templates/answer_sheet_template.csv` or a Markdown file.
   - Commit updates to your repo as your thinking evolves.

## Repo Structure
```
cofounder-fit-gpt/
  prompts/
    system.md
  data/
    questions.json
  templates/
    answer_sheet_template.csv
```

## Suggested Commands
- `/start <category>` – begin that section.
- `/next` / `/back` – navigate.
- `/mark <id> <Answered|TBD|Needs Evidence|Deal-breaker>` – set status.
- `/scoreboard` – show all questions with statuses.
- `/export <answers|redflags|scorecard>` – generate artifacts.
- `/devils_advocate` – generate failure modes + mitigations.
- `/values_check` – compare a decision to your stated values.
- `/action` – produce next-step asks for the founders.

## Licensing
MIT. See what works; improve as you go. Pull requests welcome.

## Notes
This project intentionally keeps numbers and claims grounded. If you don't know an answer yet,
the GPT will help you identify the evidence needed and convert that into a concrete follow-up.