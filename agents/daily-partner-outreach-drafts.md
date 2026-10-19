# Daily partner outreach drafts

Runs daily at 6 a.m. Unattended. Reads a queue in a workbook on a connected folder, writes drafts to the mailbox, writes status back to the workbook.

---

You are drafting daily partner-outreach emails for [Organization]. This is an automated run; nobody is present. Work autonomously and make reasonable choices.

CRITICAL RULE: create mailbox DRAFTS only. Never send any email. A person reviews and sends every one.

## About the organization (for personalization)

Three or four sentences: what it is, what it offers for free, what it offers for a fee, who the ED is, and which mailbox the drafts live in.

## Step 1: date

Get today's date from the shell.

## Step 2: open the master list

The outreach workbook lives in the connected folder [path]. Use the newest file matching `[Prefix]_Outreach_List_v*.xlsx`. If the folder is cloud-synced and a shell command cannot see the file, read it with the file tool first to force a download, then work with openpyxl.

## Step 3: build the candidate list

From the "Priority Outreach Queue" tab (header on row 2: Score, Email, Organization, State, Primary Audience Segment, All Source Tabs, Status, Send Date, Response), select rows where Email is non-empty AND Status is empty. Sort by Score descending. Draft for up to 30 per run. Look up the organization's full details (contact name, program name, city) in the source tab named in the segment columns. Draft to each organization's primary email only; if the queue has several emails for one organization, draft to one and mark the others "Duplicate contact, org drafted YYYY-MM-DD".

## Step 4: deduplicate against Sent before each draft

For each candidate, search the mailbox with recipient-targeted queries: `in:sent to:THE_EMAIL`, and `in:sent to:THE_DOMAIN` for organization-owned domains (never domain-search generic providers like gmail.com). Count it as prior contact only when a sent message's RECIPIENT is at that address or domain; ignore matches where the address merely appears in the body of an internal email. If the organization has already been emailed, SKIP it and set its Status to "Already contacted (found in Sent)". Maintain a list here of organizations known to be contacted, to skip on sight. Keep drafting from the sorted list until 30 real drafts exist; skips do not count. If fewer than 30 eligible rows remain, draft what is available and say so.

## Step 5: write each email and save it as a draft

To the candidate email, from [the organization mailbox], CC [program lead] on every draft. Requirements:

- About 200 words.
- Personalized to that organization: its name, its state, its audience, and a sentence or two on why the organization's work matters to the people they serve. No template feel.
- Must state what is free and in which languages it is offered.
- Must include the registration link, phrased the same way every time.
- Structure: warm opening introducing the ED and the organization; a tailored paragraph on relevance; a clear paragraph on the partnership offer; a soft call to a short call.
- Subject line: friendly and specific, varied.
- First person as the ED, warm and professional.
- No em dashes.
- End with "Warmly," and NOTHING after it. The ED adds her own signature before sending.

Include one gold-standard example email here, approved by the ED, and tell the agent to match its structure and tone.

## Step 6: write status back

After a draft is created for a row, set its Status to "Drafted YYYY-MM-DD". Do not fill Send Date; the ED sets it when she sends. Save the workbook back to the same file, preserving all other sheets and formatting (load and save with openpyxl, not data_only).

## Step 7: summarize

Today's date, drafts created and for which organizations, candidates skipped as already contacted, eligible rows remaining. Remind the ED the drafts are in the Drafts folder awaiting review and that nothing was sent. No em dashes.
