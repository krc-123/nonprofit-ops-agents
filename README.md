# Nonprofit ops agents

Runbooks for the scheduled AI agents that run the back office of a national nonprofit I lead as Executive Director. Each one is a prompt that fires on a schedule in a fresh session with no memory, reads its state from a spreadsheet or a project document, does a bounded piece of work, writes its state back, and reports in a few lines. Between them they replaced roughly a staff-day a week of prospect research, outreach drafting, grant tracking, and KPI collection for an organization with eight staff.

These are generalized versions. The originals name people, files, funders, and figures; this copy names roles and placeholders. The structure, the rules, and the hard-won constraints are unchanged.

| Agent | Cadence | What it does |
|---|---|---|
| `agents/weekly-contracts-and-grants-scan.md` | Weekly | Finds new, real, open contracts and grants the organization could pursue, re-checks deadlines on existing rows, and rotates the pipeline sheet |
| `agents/foundation-prospect-validation.md` | Nightly | Works through a vendor's ranked list of foundation prospects, 20 a night, and establishes eligibility, procedure, deadline, and a real contact from each funder's own site |
| `agents/daily-grant-todo.md` | Daily | Reads the grant tracker and tells the ED which one grant to finish today, plus two or three quick wins and a 30-day deadline watch |
| `agents/daily-partner-outreach-drafts.md` | Daily | Writes 30 personalized partner emails as drafts, never sends, after deduplicating against everything already in Sent |
| `agents/daily-partner-prospecting.md` | Daily | Finds 30 to 50 verified organizations to partner with, on a rotating weekday theme so each day explores new territory |
| `agents/conference-outreach.md` | Daily | Grows a prospect list of large conferences for an earned-revenue service and drafts outreach only where a real contact was verified |
| `agents/college-program-scouting.md` | Nightly | Builds a master list of college programs state by state, 20 a night, with verified contacts from official sites |
| `agents/weekly-kpi-pull.md` | Weekly | Fills the revenue and partnership rows of the KPI sheet from the payment processor and the mailbox, with the cell-by-cell rules learned from getting it wrong |
| `agents/daily-rfp-scan.md` | Daily | Scans procurement sources for RFPs a small advisory firm could bid on and keeps a pipeline document current |

## The rules every agent follows

**Drafts, never sends.** Any agent that writes to a person creates a draft in the mailbox and stops. A human reads and sends every one. This is the rule that makes the rest acceptable.

**Never fabricate.** No invented deadlines, contacts, email addresses, amounts, or organizations. If a fact could not be confirmed on the source's own site, the cell says "unconfirmed, verify" and the agent moves on. An email address that was not seen on an official page is not an email address.

**Deduplicate against reality, not against memory.** Before drafting to anyone, search Sent for the address and the domain. Before adding a prospect, read the master list. Before re-reporting an opportunity, read the pipeline. The agent has no memory between runs, so the state lives in the files, and the files are the truth.

**Accuracy over volume.** Thirty verified rows beat fifty with guesses. Zero new rows is an acceptable result and is reported as one.

**Work around the tools' limits, in writing.** The spreadsheet connector could not edit an existing sheet, so the agents rotate the master: build a new one with every old row plus the new ones, read it back and check the row count, and only then archive the old file. A failed check leaves the old master alone and reports. The weekly KPI runbook records the keystroke rules that stopped values landing in the wrong column.

**Report short, in the ED's voice.** Each run ends with a message that can be read over coffee: what is new, what is due, what changed, what went wrong.

**Distinguish confirmed from inferred.** Every finding is labelled one or the other.

## Running them

Each file is a complete prompt. Paste it into whichever scheduled-agent system you use, replace the bracketed placeholders, point it at your own sheet or document, and give it the connectors it names (a mailbox, a drive, a web search, a shell). Start each one in a dry-run mode that writes to a draft file rather than the master until you trust it.

## License

CC BY 4.0.
