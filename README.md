# Mehreen Munir

**AI workflow engineering** — retrieval, grounded drafts, human review, audit trails.

I build systems that answer from a known source, show the evidence, and stop for a person when the answer is not safe to send. Independent. Python. This profile is the portfolio; there is no separate website yet.

## What I actually ship

| Piece | What you get |
| --- | --- |
| Retrieval + grounded draft | The answer cites a source ID / file. Unsupported questions abstain. |
| Mandatory human review | Approve, reject, or request changes before any outbound action. |
| Audit trail | A durable log of classification, retrieval, draft, and review decisions. |
| Honest scope | README states what is implemented vs intentionally out of scope. |

I do not claim production RAG, LLM inference, or client data I cannot show. The public repos below are what runs today.

## Proof (runnable)

**[customer-support-automation-human-review](https://github.com/clossal/customer-support-automation-human-review)** — the current reference implementation.

`sample ticket → deterministic classification → FAQ retrieval → source-grounded draft → human review → SQLite audit trail`

Local Python + SQLite. No paid APIs, no customer data, no email send. FAQ retrieval is source-grounded; the app does **not** call an LLM. That is deliberate: the workflow (retrieve, ground, review, log) is the same shape I use for RAG/AI automation.

```bash
git clone https://github.com/clossal/customer-support-automation-human-review.git
cd customer-support-automation-human-review
python3 app.py
# http://127.0.0.1:8010/  then  /seed  for the sample queue
```

**Also runnable**

- [solana-ml-dashboard](https://github.com/clossal/solana-ml-dashboard) — Streamlit app: synthetic Solana-style data, features, model, backtest.
- [Telegram-Strategy-Simulator](https://github.com/clossal/Telegram-Strategy-Simulator) — Streamlit strategy simulator with a Telegram-style dashboard.

**In progress (not pin-ready)**

- [reddit-gtm-research](https://github.com/clossal/reddit-gtm-research) — prototype notes for a Reddit GTM research agent (LangGraph / ChromaDB planned). Not a finished system.

Older repos (`time-series-projects`, `Deep-Learning`) are archives. Client data stays private.

## How to hire

- **Email:** [mehreen.munir@protonmail.com](mailto:mehreen.munir@protonmail.com)
- **Offer:** review-first AI workflows for support, FAQ, and internal document Q&A.
- **Next public work:** documented RAG repos (ingest → retrieve → evaluate), pinned here when they run.

If you found this from a proposal: the support-workflow repo is the demo. Read its README for exact scope before we talk about a production RAG stack.
