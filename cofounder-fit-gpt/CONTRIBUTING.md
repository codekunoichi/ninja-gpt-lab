# Contributing to Cofounder Fit GPT

Thanks for your interest in improving **Cofounder Fit GPT**! This project helps founders and prospective cofounders
think clearly about partnership fit by guiding them through a rigorous, no‑fabrication Q&A process.

This guide explains how to propose changes, add questions, and submit pull requests in a way that keeps the tool
consistent, safe, and useful for everyone.

---

## Principles (please read first)
- **No invention.** The coach never fabricates facts; all prompts and examples should encourage *evidence* and *follow‑ups*.
- **Privacy by default.** Do not include real PHI/PII or proprietary company details in examples.
- **Second‑person voice.** Questions should address the user (“you”), not a specific person or company.
- **Bias toward clarity.** Prefer short, concrete wording, numbers when available, and unambiguous terms.

---

## Ways to contribute
1. **Improve prompts** in `prompts/system.md` (clarity, better probing, new commands).
2. **Expand/curate questions** in `data/questions.json` (see schema and style below).
3. **Fix docs** (`README.md`) or add templates (e.g., CSV/Markdown exports).
4. **File issues** for bugs, unclear wording, or missing categories.

---

## Question style & schema
All items in `data/questions.json` must follow this schema and style:

- **Fields**
  - `id` — short identifier (e.g., `fund_01`), unique across the file.
  - `category` — one of: `Mission & Values`, `Team & Roles`, `Decision Rights`, `Customers & Problem`,
    `Data & Access`, `Product & MVP`, `AI Strategy`, `Tech & Architecture`, `Compliance & Security`,
    `GTM & Sales`, `Funding & Runway`, `Equity & Compensation`, `Governance & Legal`,
    `Culture & Ways of Working`, `Exit & Failure Planning`.
  - `question` — a single, direct question in **second person**.
  - `probes` — 1–5 short follow‑ups that seek specifics (examples, dates, ranges, owners).
  - `dealbreaker_hint` — one sentence describing the risk if this remains unresolved.

- **Style**
  - Avoid first‑person (`I/me/my`); write for a general user.
  - Prefer one concrete outcome per question (avoid “and/or” chains).
  - Use plain language (no hype words like “revolutionary”, “game‑changing”).
  - Fit for regulated domains: do not encourage unsafe or non‑compliant practices.

- **Validation**
  - Optional: validate with `data/questions.schema.json` using any JSON Schema tool.
  - Keep the file pretty‑printed with two‑space indentation.

---

## Pull request process
1. **Open an issue** describing the change and motivation.
2. **Fork** and create a feature branch: `feat/<short-name>`.
3. **Make targeted edits** (avoid unrelated formatting churn).
4. **Run checks** locally (lint JSON, verify schema if you have a validator).
5. **PR checklist** (include in description):
   - [ ] Clear problem statement
   - [ ] Conforms to schema & style
   - [ ] Second‑person, no fabrication
   - [ ] No PHI/PII/proprietary data included
   - [ ] Updated `README.md` if behavior/commands changed
6. **Reviews**: maintainers aim to review within 7 days; please be responsive to comments.
7. **Merging**: squash‑merge preferred.

---

## Code of Conduct
We follow a simple rule: **be kind, assume good intent, and focus on ideas**. We use the Contributor Covenant by default.
If you see harmful behavior, please open an issue or contact a maintainer.

---

## License
By contributing, you agree that your contributions will be licensed under the repository’s MIT License.

---

## Questions?
Open an issue or start a discussion in the repo. Thanks for helping founders make better decisions.