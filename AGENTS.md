# Working on assam-exam-pyq

Previous-year question bank for Assam recruitment exams. Part of AxomRank: see README.md for the overview and roadmap.

## Layout

- `exams/<EXAM>/<YEAR>/data/<paper>.json`: canonical records
- `questions.csv`: generated unified export (do not hand-edit)
- `scripts/labels/`: topic labels per question number. `scripts/taxonomy.json`: allowed subject/topic pairs
- `scripts/solutions/`: worked answers with reasoning. `scripts/question_corrections.json`: OCR repairs

## Commands

- `python scripts/taxonomy.py && python scripts/taxonomy.py --check`
- `python -m unittest discover -s scripts -p 'test_*.py'`

## Rules

- Never present a worked solution as an official key. Keep `answer_source` accurate
- Keep original PDFs and images byte-for-byte
- Record every editorial change in `scripts/editorial_revisions.json`, with the original wording
- Historical current-affairs questions are answered as at the exam date
- Commit as the `axomrank` account, in small reviewable commits.
