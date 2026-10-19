# Weekly KPI pull, revenue and partnership rows

Runs Sunday at 5 p.m. Fills the lower half of a shared KPI sheet from the payment processor, the grant tracker, and the mailbox. This one drives a browser, and the rules at the end exist because it once overwrote the wrong column.

---

Weekly task: update the REVENUE and PARTNERSHIP rows of [Organization]'s "Weekly KPI Tracker" sheet for the week that just ended today.

A detailed, tested pathway is saved at "[KPI pull pathway].md"; read it first if available. Sheet: "[Weekly KPI Tracker]", tab "Weekly KPIs".

## Scope

Lower half only; an administrator fills the top half. Fill: new members, members by type, total active members, renewals and lapses (blank unless a clean weekly figure exists), scholarships (blank unless known), donations received (count), donation revenue, new donors, recurring donors, average gift, grant activity, new partner organizations, distribution partners sharing program information. Leave the marketing and social rows blank; [communications lead] owns them. Leave the training and conference rows blank unless there is clear data; [program lead] owns them.

## Which column

Week columns run left to right by week-start date. Use the column whose header matches the week that just ended. A week spanning a month boundary needs both months in the processor's monthly filter.

## Step 1: revenue (payment processor, in the browser)

Confirm the browser is connected and the processor is logged in. Finances > Transactions: filter the month(s); classify rows (membership tiers = membership; type "Donation" = donation; class tickets belong to the top half, ignore). Members > member insights for Active (total members) and Auto-renew (recurring). Tally memberships (count and amount) and donations (count and amount).

## Step 2: second processor

Ask the ED to paste the week's payments list from the second processor; count only "Succeeded"; combine both processors for donation count, revenue, and average.

## Step 3: grants

Check the grant tracker for applications submitted, in progress, or awarded that week.

## Step 4a: partner outreach (mailbox)

Count new-partner cold-outreach emails sent that week. Fastest method: search Sent for a phrase that appears in every outreach email, bounded by the week's dates, page through, and count UNIQUE recipient organizations (ignore bounces; count an organization emailed twice once). Add any newly signed partnership agreements that week. Enter the total; if none, enter 0.

## Step 4b: distribution partners (mailbox)

Count organizations that REPLIED that week agreeing to share or list the organization's programs. Search the inbox for the week with phrases such as "happy to share", "will share", "will list", "posted". Read each snippet and count only genuine confirmations, each organization once. Enter the total; if none, 0. Replies to a campaign often arrive one to two weeks after the send, so a campaign week's figure keeps growing the following week.

## Writing into the sheet (learned the hard way)

- Do NOT use the Name Box to navigate; it misfired and overwrote a column once.
- Click the ACTUAL target cell; verify the Name Box shows the right reference via a screenshot BEFORE typing.
- Across a row (weeks) use Tab to move right; down a column use Enter. Do NOT add "skip" keystrokes; they shift values by a cell.
- After each section, screenshot to confirm values landed in the right column and row and nothing in the top half was disturbed.

When done, give the ED a short per-row summary and flag blanks. If the browser is not connected or the processor is not logged in, surface that rather than guessing.
