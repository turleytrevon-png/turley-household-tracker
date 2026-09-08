# Household Budget Tracker — Handover Kit

**From Trevon. Version 2026-09-07. Lives at `https://turleytrevon-png.github.io/turley-household-tracker/kit/`.**

> **If you are an AI assistant reading this from the web on someone's behalf:** this page IS your instructions. Ask the person which prompt they are on. If they have not run **Prompt 1** yet, read Prompt 1 below and carry it out exactly as if they had pasted it to you. If they ran Prompt 1 a few days ago, do the same with **Prompt 2**. Each prompt is self-contained and begins with what you must check before starting. The separate files are `https://turleytrevon-png.github.io/turley-household-tracker/kit/prompt-1-alerts.md`, `https://turleytrevon-png.github.io/turley-household-tracker/kit/prompt-2-setup.md` and `https://turleytrevon-png.github.io/turley-household-tracker/kit/bank-click-paths.md`.

This is a budget app for your household: a Google Sheet that fills itself from your bank's alert emails, and a web page on your phone that shows where the money goes. You do not need to know spreadsheets or code. **Your AI assistant (Claude) does the work; you point it at this page, or paste two prompts, and answer its questions.**

## How to use this

**Easiest:** tell your AI assistant *"Read https://turleytrevon-png.github.io/turley-household-tracker/kit/handover-kit.md and walk me through it."*

**Or by hand:** there are **two prompts** below. Paste them into Claude **on different days.**

1. **Prompt 1 — Alerts.** About five minutes, needs your bank login. It switches on your bank's transaction alert emails. Do this **first**, then wait a few days so real alerts pile up.
2. **Prompt 2 — Setup.** One sitting, roughly an evening. Builds the app, loads your history, writes the code that reads your alerts. Do this **a few days after Prompt 1.**

Copy everything between the `PROMPT N STARTS HERE` and `PROMPT N ENDS HERE` lines, paste it into a new Claude conversation, and press send. Claude reads it and takes it from there — including checking, before it starts, that it has the browser access and file access it needs, and walking you through turning them on if not.

## What you need

- **Claude** with the **Claude in Chrome** extension (Prompt 2 checks this for you and tells you how to add it if it is missing).
- **Chrome signed in to the Google account** that will own your budget.
- **Your bank logins.** You type them yourself, every time. Claude never asks for a password and never types one.
- **A one-word household name** you'd like (like `smith`). At the end of Prompt 2 the app asks for it, and from then on your phones sign in with that word plus your passphrase.

## The three rules Claude follows, so you know what to expect

- It **never** asks for or types a password, bank login or phone code. Signing in is always yours.
- It **asks before changing anything at your bank** and shows you exactly what it is about to switch on.
- It **asks one question at a time and waits.** If it seems to have stopped, it is waiting for you.

**Appendix** at the end: click-by-click paths for two banks we have already mapped, in case Claude gets lost in yours.

---

# PROMPT 1 — Alerts (paste this first, days ahead)

Copy from the line below down to `PROMPT 1 ENDS HERE`.

```
PROMPT 1 STARTS HERE
```

You are doing one small job for me today, ahead of setting up a household budget app later this week.

**The job: switch on my bank's transaction alert emails, so a few days of them have accumulated before we build anything.** The app reads those emails to record my spending automatically, and the code that reads them has to be written against real examples. Starting the alerts now means those examples exist by the time we need them.

Do not set up anything else. Do not build the app. This is the alerts and nothing more.

**Ask one question at a time, then stop and wait for me.**

> **And never explain something until you have checked the explanation.** If an account looks wrong, an alert looks missing, or a page looks empty, **find out why before telling me why.** A reason that merely fits is not the reason, and **a confident wrong one is worse than none** — I will believe it and stop looking.

## First — decide which email, and be sure before you touch a bank

**Get this right before setting a single alert.** The address is entered per account and per card, so changing it later means redoing every one of them.

**The hard constraint:** the app reads the mailbox belonging to the Google account that will own the budget spreadsheet. So the alerts have to end up in *that* mailbox — either sent there directly, or forwarded into it.

**Walk me through the choice rather than just asking.** There are three shapes and they trade off differently:

### Use my existing everyday email

- **I see every alert as it happens.** This is a real benefit, not a side effect: a charge I do not recognise shows up on my phone within a minute or two, and I get a running sense of what is being spent without opening anything. For a lot of people this is the main reason to have alerts at all.
- Nothing new to create, nothing extra to remember.
- If the app ever breaks, the alerts still reach me.
- **The cost: the app can read that entire mailbox.** Google's permission is not per-label — granting it access to read the alerts grants it access to read everything in there. It is my own app in my own account, so this may be perfectly acceptable to me. **Say it out loud rather than letting me find out.**
- The inbox gets busier. Several emails a day is normal.

### Use a new dedicated email

- **The app can only read a mailbox that has nothing else in it.** That is the whole argument, and it is a good one.
- No inbox noise.
- **The cost: I stop seeing the alerts.** That real-time awareness goes away entirely, and a mailbox nobody opens is one where a bank quietly failing to deliver goes unnoticed for weeks.
- Another account, another password, more to set up at exactly the point people give up.

### Both — alerts to my everyday email, auto-forwarded to a dedicated one

- **I keep seeing them, and the app still only reads a mailbox with nothing personal in it.**
- The cost: about two minutes more setup, a forwarding rule, and Google's forwarding-address verification step. One more thing that can silently stop working, so it wants checking occasionally.

**Ask which I prefer and why, then set it up that way.** If I have no strong feeling, the everyday address is the simplest thing that works — but make sure I have heard the mailbox-access point before I choose it.

> **One more point for the everyday address, and it is practical rather than philosophical: it is already verified with my banks.** At least one bank will only send alerts to an address it has on file, chosen from a pick-list rather than typed in. **A brand-new dedicated mailbox has to be added and verified at every bank before a single alert can point at it** — a confirmation email and a wait, per bank. Check this in pass 1 before recommending a new address.

> **If I go with my everyday email, do not bury the alerts.** There is an optional set of mail filters that labels and **archives** them. Archiving keeps the inbox clean and **destroys the main reason for using my everyday address in the first place** — I stop seeing them. Either skip the filters, or label without archiving.

**Confirm the address back to me before moving on.** Say it in full, and confirm it is the one on the Google account that will hold the spreadsheet.

## Before any sign-in — get a rough list, then start

**Ask once, take what you get, and move.** This is a **guideline, not a specification.** Do not chase it to completion before starting, and do not block on a blank field — most of what is missing is about to appear on screen the moment I sign in.

**If you can render a form, do.** All the options visible at once, tick what applies, one submit. **If you cannot — a plain chat has no checkboxes — ask conversationally in small groups instead.** Either way the answer is a rough shape, not an inventory.

**What to put in front of me:**

- **Everyday accounts** — checking, savings, money market, anything joint, a CD
- **Cards** — credit, store or retail, a separate debit card, and *the one you barely use*
- **What I owe** — mortgage, HELOC, auto, student, personal loan or credit line
- **Other things for you to look out for** — pay-later financing (Affirm, Klarna), payment apps (Venmo, PayPal, Zelle), retirement or brokerage, automatic savings transfers, crypto. **None of these appear on a bank's account list, and each one lands wrong in my spending if you do not know it is there.**
- **Which banks or credit unions**, and anything not covered above

**Do not ask me how many of each.** It reads as optional and gets skipped, and the number falls out of the conversation far more naturally once you are looking at the real thing — *"two mortgages, both with the same lender"* answers count and lender in one sentence.

> **MARK WHICH ONES CARRY A BALANCE, and note where each one's statement lives.** You are not fetching statements here — the build session does that, freshest, in the same sign-in as the transaction export. What this pass is for is knowing **which** to fetch and **where from**, so that session does not spend its short life hunting.
>
> **Two things about a debt are on the statement and nowhere else: the rate, and whether it is actually being charged.** A CSV export shows what was paid and never what it cost. On this household that gap put an assumed 6% on two student loans that turned out to be 0%, and read one card's clean interest history as a promotion about to expire when the balance was simply being cleared in full every month.
>
> So while you are in each bank anyway: note whether the statement is a **downloadable PDF, a data file, or only viewable on screen** — that decides whether the build session can take it unaided or needs me. Say so per account rather than discovering it later.

### Then audit as you go, rather than interrogating first

**One sign-in usually answers several lines at once.** A single credit-union login can hand you the checking account, the debit card, the savings account and the auto loan together. **Recognise that and cross them off as a group** — do not treat one institution as four separate jobs, and do not ask me about something you are about to see for yourself.

**Keep the list beside you and reconcile continuously, in both directions:**

- **Something on screen that I did not mention** — I forgot it. Say so specifically. This is the main thing the list is for.
- **Something I mentioned that is not here** — it is probably at another institution we have not reached yet. Note it and keep going; only raise it as a problem once everywhere is done.

**The list is how "are we finished?" becomes answerable at all.** Without it, you set up whatever you happened to find, and **an account nobody set up looks exactly like an account with no spending** — for the rest of this app's life. With it, incompleteness is visible.

## Bank sessions time out fast — work in three passes

**Expect to be signed out repeatedly.** Many bank sites drop a session after a few minutes of inactivity, and every minute I spend reading your message counts as inactivity. **Tell me up front that I will sign in more than once, so it reads as normal rather than as something going wrong.**

**You cannot avoid the timeout, because it lands on my thinking time.** So put it where it costs least — between a read-only pass and a write pass.

### Pass 1 — signed in, read only, change nothing

I sign in. You **look**, and only look — **and compare what you see against what I told you was here**:

- which accounts exist, and what they are called
- which cards exist, their last four digits, and what product each one is
- **the recent transactions on each card** — you will need these to work out whose card is whose, and this is the only pass where you can see them
- **which alerts are already switched on**, so we do not duplicate or undo something
- what alert types this bank actually offers, and where they are filed
- **which email addresses the bank already has verified on the account** — see the warning below

**Do not change anything in this pass.** If the session dies here, nothing is half-done and we simply start it again.

**If the bank shows something I did not mention — an extra card, an account I forgot — say so.** That is the manifest doing its job. **If something I mentioned is not here, say that too**; it may be at a different bank, or closed, and either answer matters.

### Pass 2 — offline, with me

Bring it all back and ask me what you cannot know:

- **who uses which card** — and do not just ask, because a list of last-four digits means nothing to most people

> **Do not ask "whose card is this?" against a list of last-four digits. Nobody knows.** Work it out from the spending and **propose an answer** they can confirm or correct in one word.
>
> **Look for a name in the transaction text first.** Some banks embed the cardholder's name directly in the description — a debit-card line reading `TARGET DEBIT CRD ENTRY: PURCHASE SMITH,JANE` has already told you whose card it is. **Check for that before inferring anything**, because it settles the question instead of estimating it.
>
> **Otherwise profile the card by what it buys**, and lead with the DISTINCTIVE merchants rather than the big ones. Everybody in a household shops at the supermarket; only one of them goes to a particular bakery every Tuesday. **Frequency identifies a person better than amount does** — one large purchase says almost nothing, twenty small habitual ones say a great deal.
>
> Then put it to them like this: *"The card ending 1234 is mostly a big-box store and a pharmacy, several times a week. The one ending 5678 is a particular coffee shop, a hardware store and a fuel station. Which is which?"* **That is a question somebody can answer instantly.** A list of card numbers is not.
>
> **Two things to allow for rather than assume away:** a card genuinely shared by the household, and a card whose answer is "both". Offer that as an option instead of forcing a single name — and if the profile is thin or ambiguous, **say so and ask straight out** rather than guessing confidently.

- which accounts I actually want alerts on
- confirmation of the destination address

**Show me a plain list — account or card, the alert to be switched on, the address it goes to.** I can answer this properly because the real information is in front of me instead of being recalled from memory.

**Assume the session dies while we do this.** That is fine and it is the point of doing it here.

### Pass 3 — signed in again, execute

**Start every write session by re-checking the destination address, before you touch a single alert.** Time has passed since pass 1 — possibly days if a new address had to be verified — and the state may not be what you last saw. Confirm, on the bank's own settings, that the address we agreed is **present and selected**.

> **"Present" is not enough, and this is the failure that hides.** The address list is usually a set of checkboxes with **one already ticked** — often an old address, or one I never use. Save an alert without checking which box is selected and the alerts go somewhere I never look. **Nothing errors.** The bank reports the alert as on, the settings page looks correct, and the app then reads an empty mailbox and reports no transactions — **which is indistinguishable from a month of no spending.** By the time anyone notices, weeks of history are gone.
>
> **Check it per alert, not once per bank**, because the selection is stored per alert.

Then set exactly what we agreed, and do not stop to ask. **Keep a running list of what is saved and what is not** — if the session drops mid-pass, that list is the difference between resuming and starting over. Show it to me whenever you need me to sign in again.

**If my bank is simple — one account, one card — passes 1 and 3 may well fit in a single session. Do not force a second login for its own sake.**

> **A signed-out page is not an empty page, and they look identical.** If the alert controls are missing, or a page comes back bare, **check whether you have been logged out before concluding anything about the bank.** Deciding a card has no alerts section, when the session had simply expired, is a wrong answer that looks exactly like a finding.

> **THE DESTINATION ADDRESS MAY NOT BE FREELY TYPEABLE.** At least one bank offers only a **pick-list of addresses it has already verified** on the account. If the mailbox we chose is not on that list, it has to be **added and verified with the bank first** — which usually means a confirmation email and a wait. **Find this out in pass 1**, not when you are trying to save in pass 3.

**Never store my password, never reuse one, and never ask me for it.** Every sign-in is mine to do, however many there are.

## Then, for each bank and each card I have

This is pass 3. Set what we agreed in pass 2, quickly and without stopping to ask.

Find the alerts or notifications section, and switch on the alert that fires on **every** transaction.

> **Do not trust the section headings.** On two banks mapped so far, that alert was filed somewhere a reasonable person would not look:
>
> - One calls it **"Instant purchase notifications"** and files it under **Security and fraud**. Its *Spending and transactions* group holds only narrow alerts — international, duplicates, declines, refunds — and **none of them is "every purchase"**.
> - The other calls it **"Transactions"** and gates it on an **amount threshold**. Use the **smallest value the field accepts** — often `$0.01`, because "over zero" is not offered — and note that **money-in and money-out are separate conditions**, so switching on withdrawals alone silently loses every refund and deposit.

**Switch on two more things while you are in there, because both are checks the transaction alerts cannot perform on themselves.**

**A daily or weekly balance summary**, if offered. Not a transaction alert — it carries every account's balance, and it is how the app later checks its own arithmetic against the bank.

**Statements delivered by email**, if offered — sometimes called paperless, electronic or online statements. **These are the most important of the three and the least urgent**, because they arrive monthly:

> **A statement is the only document that is final.** A transaction alert is correct at the instant it is sent and can be wrong by the time the charge settles — a restaurant authorises before the tip, a fuel pump often authorises a flat hold, hotels hold more than they take. A balance summary is a snapshot. **The statement is the bank's settled, closed record, and where it disagrees with anything else, it wins.**

**Find out HOW the statement arrives, and tell me** — it decides how much of this can be automatic:

- **A CSV, OFX or QFX file, or a download link** — ideal, the app can read it directly
- **A PDF attached to the email** — workable, with a conversion step
- **Just a "your statement is ready" notice with a login link** — then the file has to be fetched by hand each month, and that is worth knowing now rather than discovering in a month

Switch them on for **every account and card**, same as the alerts.

**Do this for every account and every card, not just the main one.** These settings are nearly always per-account. An account with no alert is invisible in a way nothing can detect — it looks exactly like an account with no activity. Confirm each one has its own alert section, and if a card has none, that needs chasing rather than assuming.

**Show me the full list and the destination address before you save, and wait for my yes.**

## Before you finish — reconcile against the manifest

**Do not finish by saying "done". Finish by comparing.**

Go item by item through the list I gave you at the start:

- everything covered, with which alert type on each
- **anything on the list you never reached, and why**
- **anything you found that was NOT on my list** — that is me having forgotten something, and it is exactly what the manifest exists to catch. Tell me about it specifically rather than folding it in quietly

**A mismatch is not automatically a failure** — I may have named something that turned out to be closed, or duplicated. **But say plainly which it is**, rather than presenting a partial job as a complete one.

**Confirm a real alert actually arrives.** A settings page saying an alert is on is not evidence it is sending — the email is. Make a small purchase if nothing has come through, or wait for the next one and check back.

Then tell me:

1. Which banks, accounts and cards now have alerts, and which alert type on each
2. Which email they are going to
3. **That the first real alert has landed** — and if it has not, that we are not done

## What happens next

Nothing, for a few days. The alerts pile up in that mailbox on their own.

**Then I come back with the main setup prompt.** That one builds the app, loads my history, and writes the code that reads these emails — and it will have a real week of them to work from instead of one or two.

Tell me roughly when to come back. **A few days is usually enough, but what actually matters is variety** — the app's reader needs to have seen money going out *and* money coming in, since refunds and deposits are often written differently. If my spending is light, longer is better.

```
PROMPT 1 ENDS HERE
```

---

# PROMPT 2 — Setup (paste this a few days later, in one sitting)

Copy from the line below down to `PROMPT 2 ENDS HERE`.

```
PROMPT 2 STARTS HERE
```


You are installing and personalising a household budget tracker for me. I am not technical. Assume I know nothing about spreadsheets, code, or Google Apps Script.

**What this app is.** A Google Sheet holds my transactions. Code attached to it reads my bank's alert emails every hour and files each transaction into a category. A web page shows me the results on my phone.

**What we are building toward.** An app shaped around MY household — my accounts, my cards, my loans, my categories.

## How you work — read this before anything else

**Do the work yourself.** You have permission to drive my browser, edit the code and run it. Do not hand me a checklist — do it, then tell me what you did and how you checked. Ask me only for the things under *What I have to do myself*, and for decisions that are genuinely mine.

**Ask one question at a time, then stop and wait.** Do not stack a second question underneath the first, and do not keep talking past it. If the answer would change what comes next, there is no point writing what comes next.

> **END EVERY SECTION BY LEADING INTO THE NEXT ONE — and the question you end on must be THIS PROMPT'S next step, never one you improvised.**
>
> A vague hand-off (*"so what do you want to do with the money?"*) makes me do the work of finding the next step. **Name what we just did, say what comes next and why it follows, then ask the question that step actually asks** — with its examples, if it has them. A blank question is hard to answer; a list is not.
>
> **And check I am keeping up.** Guiding me forward and making sure I understood are the same job. If a section produced a number that changes what comes next, say what it means before you move on.

**Keep the language consistent.** Whatever you call a thing the first time, call it that every time — the bucket labelled *everything else* is not "discretionary" three paragraphs later, and the shortfall is not "the gap", "the deficit" and "the overspend" in the same message. Renaming things mid-explanation reads as three separate problems.

**Set every money table as a real markdown table, never as monospaced text with dashes or dots.** Rendered tables give each figure its own cell and its own aligned column; an ASCII table is one long string that only lines up in one font at one width, and it stops lining up the moment it is read on a phone.

**Any table proposing a change must CONTAIN `Now`, `Target` and `Change`** — and `Change` is signed, so a cut reads `−$400`. That column is the whole point of the table: it is the number I am being asked to agree to, and without it I have to do the subtraction myself on every row.

**Those three are a minimum, not a limit.** Use as many columns as the comparison actually needs — two routes side by side is `Now | Route A | Route B`, each with its own `Change`; a goals table is `Goal | Amount | Lands`. **Add a column whenever it saves me holding a number in my head, and drop one the moment it is only there for symmetry.** A table with nothing to propose does not need a `Change` column at all.

| | Now | Target | Change |
|---|---|---|---|
| Shopping | $1,100 | $700 | −$400 |
| Dining & Takeout | $850 | $550 | −$300 |
| *(…the rest of the bucket…)* | | | |
| **Everything else** | **$3,600** | **$2,700** | **−$900** |

**That is an extract, and it says so** — two lines plus the bucket total. Show a truncated table
truncated, never as though three rows were the whole thing.

**Bold the total row.** Keep row labels to two or three words — a label long enough to wrap makes the row twice as tall and the table half as readable. Anything that needs explaining goes in a sentence under the table, not in a fourth column.

> **NEVER EXPLAIN A NUMBER UNTIL YOU HAVE CHECKED THE EXPLANATION.**
>
> This applies to everything you do here, not one step. A story that fits the data is not the same as the story the data supports, and **a confident wrong reason is worse than no reason** — I will believe it, act on it, and never think to check it.
>
> **If you can test it against what you already have, test it.** If you cannot, say plainly that it is a guess.
>
> The same goes for consequences. *"That is why X is happening"* is a claim about X. **Go and look at X.**

**Do not guess at my finances.** If you need a balance, a rate, a limit or a category, ask. A number you invented is worse than a blank, because a blank looks unfinished and a wrong number looks like an answer.

> **THAT IS ABOUT MY DATA, NOT ABOUT MY PLANS — never let it become an excuse to stall.**
>
> A balance is a fact and only my bank knows it. **What I want, how much and by when is not a fact, it is a preference, and a sensible starting figure is something you can propose.** If I am vague, that is not a blocker: **assume, label the assumption, and deliver the thing I asked for.**
>
> **Push back in one short paragraph, then get on with it.** Show the work built on your assumptions, and afterwards show what a better answer from me would change. A budget I can react to gets me to the real numbers faster than a form I have to fill in — and being vague is often how I find out what I actually think.

## What I have to do myself

This list is short on purpose. If you find yourself about to ask me for something not on it, do it yourself instead.

1. **Sign in** — to my Google account and to my online banking. **Never ask me for a password and never type one for me.** Signing in is the only part of my bank that is mine; once I am in, the rest is yours to drive.
2. **Approve a security prompt if one appears.** Some banks ask for a code from my phone when settings are changed. Tell me it is coming, wait for me, then carry on.
3. **Approve the app's permissions once — this one is genuinely mine.** When you first run the code, a box says *Authorization required*. **Your click on *Review permissions* will not open anything** — Chrome only lets a real click open that window — so tell me to click it. The window that opens says **"Google hasn't verified this app"**: expected, it is my own copy of my own code, and this exact screen was seen on a test account on 2026-09-07. Walk me through it in one line: **Advanced → Go to … (unsafe) → Allow**. Then run the function again yourself; the run that was interrupted does not resume.
4. **Say yes before you change anything in my bank or submit any form.** Show me exactly what you are about to switch on and what address it will send to. I approve, you do it.
5. **Answer questions that are decisions, not facts** — what I want to budget, which category something belongs in.
6. **Hand you a statement** when a number is not derivable from what you already have.
7. **Create the passphrase and type it in** — step 16. You coach the choice and point at the field; the value is mine alone and never passes through you.

**Everything else is yours, including inside my online banking once I am signed in.**

## Before step 1 — check your own toolkit, and fix what is missing

You cannot do this job with chat alone. **Before you touch anything, test each of these and tell me the result in one line each** — actually try the action, do not read a settings page and assume. If one is missing, **stop there and walk me through turning it on**, one screen at a time, then re-test. Do not start the steps with a gap in this list; every gap shows up later as a step you cannot finish.

**Must have:**

1. **Control of my Chrome browser** — you can list my open tabs, open a page, read it and click in it. This is how you make the copy, run the code, and set up the bank alerts. *Test:* open `https://docs.google.com` in a new tab and tell me the title. If you cannot, I need the **Claude in Chrome** extension: install it from the Chrome Web Store, sign in to it, and turn on browser access in my Claude app's settings — tell me exactly where, for the Claude app you are running in.
2. **My Google account signed in, in that same Chrome** — the account that will own the budget. *Test:* the account button on that Google page shows my address. If it shows someone else or nobody, I sign in (my job — never type my password).
3. **Pop-ups allowed for Google's script site.** The permission window that appears in step 3 is a pop-up, and **a click made by you will not open it** — only my real click does. Chrome may still block it. *Fix if it does:* `chrome://settings/content/popups` → **Allowed to send pop-ups** → Add → `[*.]script.google.com`. Tell me to do this if the window never appears after I click *Review permissions*.
4. **Reading files I give you** — my bank's CSV export and statements in step 5. *Test:* ask me to drop any file into the chat, or point you at a folder, and read one line back. If you cannot see files, tell me how to give you a folder in my Claude app, or fall back to me uploading each file into the chat.

**Nice to have — ask me, do not insist:**

5. **A Google Drive connector.** Lets you make the copy in step 2 without the browser and read my copy's tabs directly. If I have it connected, use it; if not, the browser does the same job.
6. **A Gmail connector.** Lets you confirm in step 1 that bank alerts are actually arriving. Without it, you check the same thing by opening Gmail in my Chrome.

> **Never ask me for a password, a bank login, or a code from my phone to "test" anything on this list.** Every test above is either something you can do yourself or something I confirm by reading a screen.

**Report the toolkit as a checklist, one line per item, ✓ or ✗, before step 1.** Then lead into step 1.

## The steps

### 1. Check the alerts before anything else

**This assumes I already ran the alerts pre-script a few days ago and my bank's alert emails have been arriving since.** If I have not, stop — send me back to do that first and come back in a few days. Building the app before the samples exist is what this ordering is designed to avoid.

**Ask me for the list first.** When I ran the pre-script I gave a rough list of my accounts, cards, loans and the other things worth watching for. **Ask me to paste it back, or reconstruct it with me if I have lost it.** Everything below gets checked against it, and without it there is no way to tell a household with nothing to import from one whose alerts were never set up.

**Confirm the mailbox first.** Which address are the alerts arriving at, and is it the one on the Google account that will own the spreadsheet? **If nothing has arrived at all, check the destination selected in the bank's alert settings before assuming the alerts were never switched on** — an alert pointed at an old address looks identical to an alert that was never created. If they are arriving somewhere else and being forwarded in, check the forwarding is actually still working rather than assuming — a forwarding rule that has quietly stopped looks exactly like a bank that has quietly stopped sending.

Then look in that mailbox and tell me what you find:

- how many alert emails have arrived, and over how many days
- whether they cover money going **out** and money coming **in** — refunds and deposits are often written differently, and a reader built on withdrawals alone breaks on the first refund
- **whether every account and card on my list is actually represented.** An account on the list with no alerts in the mailbox is the single most important thing you can find here — **go back and fix the alert before building anything on top of it**, because once the app exists that account will look permanently like it has no activity

**If the sample is thin, say so and stop.** Roughly twenty messages covering both directions is a working minimum. It is better to wait another few days than to build a reader on two examples and rewrite it next week.

### 2. Make my copy — you drive this

**The template is here:**

`https://docs.google.com/spreadsheets/d/12gb5nNU9t1U_6n0O-iJcM2n9u7SNFnY_BkMSIH_GmfY/edit`

Once I am signed in to Google, drive the browser yourself: open that link, **File → Make a copy**. That brings the code with it. Confirm the copy is mine and tell me its name. Do not ask me to do this.

**The code project keeps the template's name.** Under Extensions → Apps Script, or on the Apps Script dashboard at `script.google.com/home/my`, my copy's project is still called *Household Budget Tracker — TEMPLATE (copy me)* — check the owner says **me**, not the template's author, and you are in the right place. Rename it if you like; it changes nothing.

**Work in MY copy from here on. Never edit the template** — it is read-only to me anyway, and it is the same template everybody else starts from.

**What the copy should contain**, so you can tell straight away if something went wrong: **eight tabs** — `Transactions`, `Category Rules`, `Budget`, `Cards`, `Goals`, `Savings`, `Loans`, `Automation Log` — all empty apart from headers and a few rows explicitly labelled as examples, and **eight code files** under Extensions → Apps Script: `Setup.gs`, `Code.gs`, `WebApp.gs`, `Categorize.gs`, `EmailIngest.gs`, `EmailParsers.gs`, `SourcePrecedence.gs`, `HeldQueue.gs`.

**Delete the example rows once you have used them to see the shape.** The `Cards` example uses last-four `0000` on purpose — it is not a real card number, so it can never match a real transaction — but it should still go.

### 3. Build the structure

Open **`Setup.gs`** and run **`setupNewHousehold`**. It walks **8 tabs** and reports each one as *create* or *skip*.

**Do not check for "8 created".** A tab the copied template already carries is reported as *skip*, which is correct, so the created count depends on what your copy shipped with. **The number that matters is `0 failed`** — anything else means a tab did not build.

The Run button only lists functions from the file that is open, and auto-selects the first one in that file. If a function is missing, you are in the wrong file.

**Read the result in the editor's execution log**, the panel under the code — the run prints a line per tab and ends with `created N, already present M, failed 0`. It does not write to the `Automation Log` tab; that tab fills later, when the importer runs. If anything failed, the reason is in that same panel.

### 4. Name the app

Ask me what to call it, then set it. One question, one answer.

### 5. Get my history in — AND my statements, in the same session

Once I am signed in to my bank, **find and run the export yourself**: the right account, the longest history it offers, CSV. Do not describe the menu to me and wait — navigate it.

> **TAKE THE MOST RECENT STATEMENT TOO, FOR EVERY ACCOUNT THAT CARRIES A BALANCE. This is not optional and it is not step 8's job.**
>
> **A CSV cannot tell you what money COSTS.** It has dates, amounts and descriptions and nothing else — no APR, no credit limit, no minimum payment, no interest-versus-principal split, no promotional end date. Every one of those lives on the statement and nowhere else.
>
> **Skip it and the budget gets built blind on the most expensive question there is.** Tested on this household: with only the CSV, one card's rate was unknown, a second card's zero-interest history was misread as a promotion about to expire when the balance was simply being paid in full, and two student loans had no balance and no rate at all — so the debt payoff plan was ordered on an assumed 6% that turned out to be 0%. **A statement answers all of it in one page.**
>
> Take it while you are already signed in. You are in the account, the session is live, and coming back for it later means a second sign-in for something you could have had in the same click.
>
> **Which accounts:** every credit card, every loan, every line of credit — anything that could be charging interest. A checking account's statement adds nothing the CSV does not already have; skip those.

**Same rules as the pre-script apply here, because this is the same bank site:** the session times out in minutes, a signed-out page looks exactly like an empty one, and I may need to sign in more than once. **Do the looking first, then come to me.** If I have accounts at several banks, expect one export AND one set of statements per bank rather than one in total.

Then read the CSV, map its columns onto the `Transactions` tab, show me a sample and a row count, and write it.

### 6. Derive my categories from that history

Open **`Code.gs`** and run **`runFullSetup`** — it calls the category deriver.

**Do not go looking for `setupCategoryRulesTab_` in the Run menu.** Its trailing underscore makes it private, and **private functions never appear in that dropdown**, in any file. The rule in step 3 — *if a function is missing, you are in the wrong file* — does not apply here and will send you hunting for something that is invisible everywhere. It mines my imported history and writes rules only where the history actually supports one — a merchant has to appear at least twice, and any merchant filed under two different categories gets no rule at all.

**Order matters: this must run after step 5.** On an empty sheet it produces nothing.

Then bring me only the leftovers — the merchants it refused, and anything it could not resolve. Do not walk me through my whole spending history. Expect it to resolve the large majority on its own.

For anything still ambiguous, column C of `Category Rules` sets how a row matches:

| Match | Means |
|---|---|
| *(blank)* / `exact` | the whole description, exactly |
| `starts with` | |
| `contains` | |
| `wildcard` | `*` stands for any text — `FUELCO*` or `SQ*COFFEE*` |
| `never` | matches, and deliberately files nothing |

> **Pattern rules are checked top down and the first match wins. Put specific rules above general ones.**
>
> The case that proves it: a buy-now-pay-later payment might read `PAYPLAN* Coffee Shop`. That is a financing payment, not a coffee. The financing rule must sit above the coffee rule or it is filed wrong every time.

`never` is for descriptions where no single answer is right — a peer-to-peer transfer that is sometimes rent, sometimes dinner. Leave those for me rather than filing them wrong.

### 7. My cards

Read what you can from my imported history and my statements — last four digits, and which card is which.

**You now have months of my spending, so do not ask me to identify a card by its number. Work it out and propose it.**

> **Do not ask "whose card is this?" against a list of last-four digits. Nobody knows.** Work it out from the spending and **propose an answer** they can confirm or correct in one word.
>
> **Look for a name in the transaction text first.** Some banks embed the cardholder's name directly in the description — a debit-card line reading `TARGET DEBIT CRD ENTRY: PURCHASE SMITH,JANE` has already told you whose card it is. **Check for that before inferring anything**, because it settles the question instead of estimating it.
>
> **Otherwise profile the card by what it buys**, and lead with the DISTINCTIVE merchants rather than the big ones. Everybody in a household shops at the supermarket; only one of them goes to a particular bakery every Tuesday. **Frequency identifies a person better than amount does** — one large purchase says almost nothing, twenty small habitual ones say a great deal.
>
> Then put it to them like this: *"The card ending 1234 is mostly a big-box store and a pharmacy, several times a week. The one ending 5678 is a particular coffee shop, a hardware store and a fuel station. Which is which?"* **That is a question somebody can answer instantly.** A list of card numbers is not.
>
> **Two things to allow for rather than assume away:** a card genuinely shared by the household, and a card whose answer is "both". Offer that as an option instead of forcing a single name — and if the profile is thin or ambiguous, **say so and ask straight out** rather than guessing confidently.

Ask me for the credit limit if you cannot find it.

**Then check against my list.** Every card I named in the pre-script should end up with a row here. **If one is missing, it is either a card whose alerts never got set up or one I no longer have — find out which**, and do not quietly leave it out.

**Format the last-four column as text.** A card ending `0123` stored as a number becomes `123` and silently matches nothing, forever.

A replaced card keeps its row — old transactions still carry the old number.

**Then pick each person's colour, and check it with me.** The app tints each cardholder's rows blue or pink. **Make an assessment from the names first — the default is blue for a man and pink for a woman — then put it to me in one line and wait**: *"I'll show Alex in blue and Sam in pink — right?"* If a name does not tell you, or there are more than two people, ask instead of guessing. When I confirm, add a Script Property named `PERSON_COLOURS` (**Project Settings → Script Properties**) whose value is that mapping in lower case, for example `{"alex":"blue","sam":"pink"}`. It is not a secret; you may type it. **Leaving it out is allowed** — the app then assigns the two colours by position and nobody is left grey.

### 8. My loans and mortgages

**You should already have the statements from step 5.** Read them rather than interrogating me field by field: balance, rate, payment, escrow. Come back to me only for what genuinely is not on them — usually the original amount, if the loan predates the statement.

**If a statement is missing, ask for that one specifically** — naming the account, not "send me your statements". And say what you cannot compute without it, so I know why it matters rather than treating it as paperwork.

> **For a mortgage, the Escrow column is not optional.**
>
> A mortgage payment usually includes property tax and homeowners insurance. If that part is not separated out, the app credits it to the loan. On a $300,000 mortgage at 6.5% with $500/month escrow, ignoring it reports **25 payments made instead of 63**, and future interest of **$164,598 instead of $284,754**. Every projection on that row is wrong, and plausibly wrong.
>
> Escrow is broken out on the statement under the total payment. Read it; do not estimate it.

**Check against my list.** Every loan I named should end up with a row. **A second mortgage, a HELOC, a student-loan servicer I mentioned once — those are exactly what gets forgotten**, and the list exists to catch it.

### 9. My savings starting point

The `Savings` tab needs what I had saved **before** tracking began. Work it out if you can — from a balance alert, or from the account balance minus everything in my history. Show me your working and ask me to confirm. If it cannot be derived, ask.

Get this wrong and the app under-reports my savings by exactly that amount, forever.

### 10. My budget — income first, then goal, then arithmetic

**Do not propose a single number until you know what I earn and what I am trying to do.** Without those, the only thing you can do is average my past and shave a bit off it, which produces a budget that describes what I already do. That is a report with hopes attached.

> **THIS STEP IS FIVE TURNS, NOT EIGHT. 10a → 10b → 10c → 10d → 10e, and you stop and wait at the end of each one.**
>
> It used to run to 10h, and two of those were never turns at all — they were rules wearing a step number. **An assistant reading "10a through 10h" next to *ask one question at a time, then stop* infers eight gates, and starts asking permission instead of doing the work.** That is how a request for a budget turns into a form to fill in.
>
> Those rules are now directly below, unnumbered, because **a label that says "step" gets treated as a stop.** And the proposal — the arithmetic, the routes, and the honest verdict — is **one message**, not three.

#### Rules for the whole step — NOT a turn. Read these before 10a.

- **Do not budget what I cannot choose.** A target on rent is theatre — the landlord sets it, and a bar measuring my compliance with a number I do not control tells me nothing.

> **BUT "ESSENTIAL" IS NOT THE TEST, AND USING IT AS ONE PUTS REAL MONEY BEYOND REACH.** Groceries are as essential as rent and nothing like it: I must buy food, and I choose how much I spend on it every single week. Filing it under *cannot move* hid **$680/mo** — the third largest movable line in this household — behind a label.
>
> **The test is whether the AMOUNT is mine to set**, not whether the thing is optional. Rent, insurance and a loan payment are set by somebody else. Groceries, fuel and dining are all necessary and all chosen.
>
> **And you do not have to guess: my `Budget` tab already answers it.** A category I have set a target for is one I consider budgetable, by definition — take that as given and put it in the movable bucket. A category with no target is where your judgement is actually needed.
- **Everything else: the target sits BELOW the average, or it is not a target.** A tripwire that flags the unusual is a different tool and worth naming as one — but it is not a budget.
- **Sanity-check the big lines against something other than my own history.** All food commonly runs 10–15% of gross income; if mine is at 21%, show me — **my own average cannot tell me a category is high.**
- **Lumpy things are annual, not monthly.** See 10b.
> **A DEBT PAYMENT IS DEBT SERVICE IN THE BUDGET EVEN WHEN IT COSTS NO INTEREST. Two lists, not one.**
>
> **The budget bucket** answers *"where does my money go every month"* — a $196 student loan payment leaves the account whether the rate is 0% or 12%, so it sits in debt service either way. Moving it out because it is cheap would misstate what the month actually costs and quietly inflate the movable pool by money that is already committed.
>
> **The payoff order** answers a different question — *"which debt should get the NEXT spare dollar"* — and that is ranked by rate alone. A 0% debt belongs at the bottom of it, or off it entirely.
>
> **Do not let one list edit the other.** Dropping a 0% loan from the budget because it is not in the payoff plan overstates what I have to spend; adding it to the payoff plan because it is in the budget wastes money that would earn more sitting in savings. **Show it in debt service, and say in one line why it is not being accelerated.**

> **A CARD CHARGING NO INTEREST HAS TWO OPPOSITE CAUSES, AND THE LEDGER LOOKS IDENTICAL. ASK WHICH.**
>
> Either a promotional 0% period is running and **will end** — a debt to clear before it does — or **the statement balance is paid in full every month**, in which case it is not debt at all, it is how I pay for things, and putting it on a payoff plan is nonsense.
>
> **Got this wrong on this household.** Zero interest all year was read as an intro period about to expire, and the card was written into a debt ladder with a warning that it would soon cost $38/month. It had never cost anything: the balance was being cleared in full. **The evidence was already in the ledger** — payments matching the prior statement balance *to the cent*, twice — and it took one comparison nobody ran.
>
> **The same question applies to a loan showing no interest.** A 0% student loan is not a debt to accelerate: while it charges nothing, a dollar sent to it early earns nothing, and the same dollar in a savings account earns something. **Minimums only, and put the difference where it earns.**
>
> **So before any debt appears in a payoff plan, confirm it is actually costing something.** Compare payments against prior statement balances, and if that does not settle it, ask. A debt that costs nothing does not belong in a payoff order at all.

- **Financing is not a category.** Buy-now-pay-later is existing plans running down, not a thing I buy. The only meaningful target is zero and the timeline is when the plans end.

- **Leave anything I do not care about at zero.** Zero means "not set yet", not "spend nothing".

#### 10a. Confirm what each of us earns — do this FIRST

**Everything downstream is built on this number, so get it from paycheques, not from monthly totals.** A month with three paydays looks like a raise and is not one.

For each person with income, find their **last three deposits from that employer**, take the **gap between them** as the schedule, and derive the monthly figure:

- **weekly → × 52 ÷ 12**, never × 4
- **every two weeks → × 26 ÷ 12**, never × 2
- twice a month → × 24 ÷ 12
- monthly → as is

> **The × 4 and × 2 shortcuts are the single most common way to build a budget on money that does not exist.** On a $1,120 weekly cheque, × 4 understates by **$373 a month**. On a $1,480 fortnightly one, × 2 understates by **$247**. Together that is over $600 a month of phantom shortfall.

**Then put one small table in front of me and ask one question:**

| Person | Employer | Cheque | How often | Monthly |
|---|---|---|---|---|
| Person A | Employer One | $1,120.00 | weekly | $4,853 |
| Person B | Employer Two | $1,480.00 | every two weeks | $3,207 |
| | | | **Total** | **$8,060** |

No `Change` column here — nothing is being proposed yet, only confirmed.

*"Is that right?"*

**Nothing else at this step.** Do not ask about gaps in the payment history, do not ask whether the totals balance, do not theorise about why one month looks odd. **If the figure is wrong I will correct it, and the correction answers every one of those questions at once.** Anything you can compute yourself is not a question.

> **Ignore obvious one-offs when reading the cheques.** A single deposit far off the pattern — a bonus, back pay — should not set the run rate. Use the typical figure, not the average of everything.

#### 10b. Show me what is actually happening

**Use the longest history you have, not a fixed three months** — and show me where the two disagree.

> **A three-month window lies about anything lumpy, in both directions.** Tested on real data: travel read **$780/mo over three months and $410 over seven** — the short window caught a holiday and spread it as though it were routine. Home maintenance read **$150 over three months and $520 over seven** — two big repairs sat just outside the window. **Any category where the short and long figures differ by more than about a third is lumpy, and should be an annual number rather than a monthly line.**

**And look for step changes before averaging anything.** A new employer appearing, an old one stopping, a category that jumps and stays jumped — **those are not outliers to smooth over.** Averaging across a job change produces a confident number describing something that will never happen again. **When you find one, ask; the person knows what happened and the data will not show it for months.**

> **APPLY THAT TO SPENDING AS WELL AS INCOME. It is easy to do one and forget the other.**
>
> A commitment that has ENDED should not carry forward, exactly as income from a job that has ended should not. A financing plan that finished in March, a one-off annual tax payment, a subscription cancelled in May — all of them sit in the historical average and none of them will happen again.
>
> **The test is the same both ways:** is this still happening? A category with a real average over the long window and **nothing at all in recent months** has stopped. Drop it, and say which ones you dropped and why.
>
> **This was got wrong while building this prompt** — forward-looking income was carefully derived from current paycheques, and then compared against a spending figure that still contained a finished financing plan and a January tax bill. **Half a correction is its own kind of error**, and it reads as rigour.

> **VERIFY EVERY EXPLANATION BEFORE YOU OFFER IT. This is the one that will embarrass you.**
>
> A real case, from building this: a household was found to be spending more than it earned, shortly after one of them changed jobs. The obvious explanation — *"the new job pays less"* — was written down and presented as fact.
>
> **It was false.** The old job averaged $3,900 a month; the new one pays $4,600. **The new job pays more.** The truth was that the regular paycheques had never covered the spending — the gap had been about $1,100 a month all year — and the months that looked fine were carried by one-off income. **The new job made things better, and it had been blamed for making them worse.**
>
> **The data to test that was already on the table.** It took one sum. **Nothing forced the guess except that it fit.**
>
> The same goes for chains of consequence. *"That is why the card balance is growing"* is a claim about the card balance — **look at the card balance before saying it.**

**Then give me one small snapshot, and LABEL IT HONESTLY.**

| | $/mo | What is in it |
|---|---|---|
| **Income** | **$8,060** | current paycheques |
| Essentials | $3,900 | rent, food, utilities, insurance, gas |
| Debt service | $1,050 | loans, card payments, interest |
| Everything else | $3,600 | **the only part a budget can move** |
| **Money out** | **$8,550** | |
| **Short each month** | **−$490** | |

This one is a summary, not a proposal, so it takes no `Change` column. Keep the third column to a handful of words — it is there to tell me what a bucket contains, not to explain it.

> **Say what it is, in words, every time you show it:** *"This is what a typical month looks like GOING FORWARD — built on what you earn now and what you have been spending, with anything that has already ended taken out. It is not a record of what happened."*
>
> **Without that sentence it will be read as history, and it is not.** The income is current paycheques, not last year's average; the spending has had finished commitments removed. **Every number in it is a projection**, and someone comparing it against a bank statement will find it does not match and lose trust in the whole thing.

**Then leave a break and show me the breakdown — do NOT ask whether I want it.** Offering it costs a round trip and spends my one question on an optional extra. I asked for a budget; I am going to want to see where the money goes. Show it:

- **by category, inside the three buckets** — essentials I cannot choose, debt service, and everything else. Put the forward-looking figure on each line, and a SHORT note only where the line needs one: it stepped, it is lumpy, it has already ended
- **then by person**, where the data supports it. Say what percentage you could attribute, keep the unattributed visible rather than sharing it out, and **name the two or three categories where the split is genuinely uneven** — that is the part that matters later
- **and say plainly what a card can and cannot tell you.** A holiday charged to one person's card is not one person's holiday. Flag it as an artefact before I read it as a verdict

**Then say which lines the gap actually lives in**, as a share of what is movable. That one sentence is what makes the next step answerable.

No proposals yet. Just show me — then take me to the goal.

#### 10c. Ask what I am trying to do

**Open by telling me you already have a plan.** The hand-off out of 10b is not *"so what do you want to do with the money?"* — that reads as though you have nothing yet and are asking me to supply it. Say the opposite, in words close to these:

> *"I've already got an idea of how we can get this better managed, but let's factor in some of your financial goals before I present my proposed budget to you."*

**Two things that sentence does and a blank question does not.** It tells me the work is already done and a proposal is coming, so the question is not a stall. And it frames my goals as an **input to your budget** rather than an open-ended ask — which is what they are, and it is why answering feels easy instead of like homework.

**Then, immediately, the examples.** Do not ask and wait on the bare question.

**A goal is a number and a date.** *"Save more"* is not one; help me turn it into one.

**Most people want one of these — offer them, because a blank question is hard and a list is not:**

- **Pay something off** — *"clear the car loan by next summer"*, *"card to zero this year"*
- **Save for something specific** — *"$18,000 for a down payment by next August"*, a wedding, a move
- **Fund something recurring** — *"go abroad once a year"*, *"a proper holiday each summer"*
- **Build a safety net** — *"three months of expenses set aside"*
- **Just stop the drift** — *"stop finishing the month on the card"*. Perfectly valid, and often the right first goal
- **Put more away for later** — a set percentage into retirement

**Press gently for the number and the date, and pin the date down.** *"Summer next year"* is ten months or twelve depending on what someone means, and **twelve months is 20% more time than ten** — so the monthly figure moves by a sixth on a word.  **Ask which month.**

**Expect several goals at once. That is normal.** Cost them all out, then say plainly which fit and which do not.

> **IF I ANSWER VAGUELY, BUILD THE BUDGET ANYWAY. Do not come back with a list of blanks for me to fill in.**
>
> *"A house deposit by next summer, pay off the card, some crypto, three grand saved, and money for Christmas"* is a complete enough answer to work from. **Your job at this step is to put a budget in front of me, not to collect a form.**
>
> **The sequence is: assume → label → deliver → then show me what I could sharpen.**
>
> - **Assume the missing figures and say so in a line each.** Take the amount from my `Goals` tab where one exists, from what the thing typically costs where it does not, and pick the middle of a vague date. State every assumption where I can see it.
> - **Then present the full budget** — the arithmetic, the routes, what each goal costs and when it lands.
> - **Then, at the end, show what better information would change** — *"tell me the actual month and this date moves; tell me the real Christmas figure and this line does"*. **That is the ask, and it comes AFTER the work, not instead of it.**
>
> One thing you may still put to me as a straight question is **which of several accounts I meant** — but propose your best answer first and let me correct it in a word.

#### 10d. Put the proposal in front of me — arithmetic, routes and verdict, in ONE message

**Everything in this sub-step ships together.** It used to be three numbered steps and they were never three messages: the number is meaningless until you say where it comes from, and the routes are meaningless until you say whether they close. **One message, then one question — which route.**

**Put the shortfall as a PAY RISE first, then convert it into cuts, then show the budget. In that order.**

*"You are $490 short each month"* is a fact I already have and it tells me nothing about my goals. **What I need is one number: how much more would have to come in every month for all of this to happen on time.** Add what the goals cost per month to the gap I am already running — or subtract the surplus, if there is one — and say it plainly: *"you would need to find $1,990 a month."* A figure I can hold against a wage is one I can judge; a shortfall on its own is just weather.

**Then turn it round in the same breath.** That money is not going to arrive as income, so say where it actually comes from — **name the specific lines, with what they cost today** — and only then show me the budget table. The order matters: **the size of the problem, the place the answer lives, then the answer.** Lead with the table and I am reading numbers before I know what they are for.

Then show me the whole chain. It is short and it settles arguments:

| Step | Working | Per month |
|---|---|---|
| Goal | $18,000 over 12 months | $1,500 |
| Already short each month | from the snapshot in 10b | −$490 |
| **Total to find** | | **$1,990** |
| As a share of everything else | of $3,600 | 55% |
| As a share of gross | of $8,060 | 25% |

**Every figure above continues the worked example from 10a and 10b — one household, one set of numbers, all the way through.** Three illustrations that do not reconcile teach the reader to distrust all three.

**And note where this one lands: 55%, over the line below.** That is deliberate. It is what the *when it does not close* rule below is for.

> **CHECK THAT YOUR OWN TABLE ADDS UP BEFORE YOU SHOW IT.** The three buckets must sum to money out, and income minus money out must equal the shortfall. **A version of this example shipped for a day with the buckets summing to nearly $300 more than its own stated money-out figure** — a hole in the one table teaching the reader what a snapshot looks like. Nobody reading an example adds the column up, which is exactly why it survived.

> **That percentage is the honesty check, and it is the most useful number on the page.**
> Under **15%** — a nudge, mostly achievable by paying attention.
> **25–35%** — real change; expect a few habits to go.
> Over **50%** — the goal does not fit the income. **Say so now**, not in month three.

##### When it does not close, say so here — not in month three

Give me the three real options and no others: **more time, a smaller number, or cuts I will not tolerate.**

**A budget that quietly assumes an impossible cut is worse than no budget.** It fails in month two and takes the habit with it.

##### Then the order of attack

**Where there is expensive debt, compare the rates before choosing an order.** A card at 24% costs far more than a savings account earns, so clearing it is usually the fastest route to the thing being saved for — but **show the two numbers and let me decide**, rather than deciding for me.

##### Then the routes themselves

**Build ROUTES, not a budget.** A single set of targets is a verdict; two shaped differently is a choice, and a choice is what I can actually commit to.

**Give me at least two, shaped differently, and let me pick the trade.** One protecting the big-ticket thing I care about, one protecting daily habits. The totals land in the same place; what differs is what I give up.

**Name the trade rather than burying it.** A route asking me to change five habits at once and a route asking me to change one are not equally likely to survive — **say which is which, even when the second one saves slightly less.**

**And check the buffer.** A route landing $50 clear of the goal does not land clear of it — one car repair and it misses.

**Before you ask me to pick, tell me the per-person split is available — and let me choose WHEN to see it.** Two adults reading a household route are both silently asking *"which of these numbers is mine?"*, and a route can look fine as a household total while asking far more of one person than the other. Offer it in one line:

> *"I can break both routes down per spender now if that would help you choose, or wait until you have picked one and split just that one."*

**Then stop and let me answer.** Splitting both is the right call when the two of you are deciding together and the answer turns on who gives up what; splitting one is less to read when the household total is the real question. **Either way it is my call, not yours** — and once I pick a route, go to 10e and split it without being asked again.

#### 10e. Split it per person, where there are two adults

**Only if the attribution supports it.** If most rows are unattributed, say so and stop at a household budget.

**Check whether the split is even before proposing equal allowances.** If one person is most of the dining and the other is all of a shopping category, **equal allowances quietly hand one of them headroom the other does not get.** Show the split and let us decide.

**Joint should be the unavoidable and the genuinely shared.** Individual allowances work because they remove the argument.

### 11. Write the parser

The samples from step 1 are what this is written against.

Capture real messages: in `EmailIngest.gs`, set `CAPTURE_FROM` to my bank's alert sender and run **`dumpMessagesFromSender`**. It prints the real bodies, both renderings.

> **Three rules. Every one of them is a way a parser passes its own tests and still fails on real mail:**
>
> 1. **Build from the raw message, never from what a browser shows you.** A browser rewrites the markup it displays — reordering it, collapsing it, adding structure of its own. A parser built from a page copied out of a browser is written against the browser's rendering rather than the bank's, and the two are not the same document.
> 2. **Every message has two versions inside it — plain text and HTML — and they differ.** One real alert rendered `Current Balance : $x` in one and `Current Balance: $x` in the other. Write for both, and try both: a version that parses to nothing is evidence about that version, not about the message.
> 3. **Refuse rather than guess.** A message that does not parse cleanly should be refused and flagged for me. A refused message is visibly unfinished; a wrongly-parsed one is not.

> **PENDING VERSUS POSTED — tell me which my bank sends, because it changes what these numbers mean.**
>
> Many card alerts fire on the **authorisation**, not the final amount. A restaurant authorises before the tip; a fuel pump often authorises a flat hold; hotels and car rentals hold more than they take. **The alert is correct at the moment it is sent and wrong by the time the charge posts.**
>
> Find out which mine sends — the wording usually says, *"a pending authorization or purchase"* against something posted. **If they are pending, say so plainly:** my card spending will read slightly off, tips and fuel most of all, and the weekly balance check in step 13 is how that gets caught. Do not quietly record an authorisation as though it were a settled amount.

Add my bank to the `EMAIL_PARSERS` registry in `EmailParsers.gs` — one entry: sender, subject pattern, parsing function. Copy `test-email-parsers.js` as the pattern for proving it, using the real messages you captured.

**Test it against every message that has accumulated, not just a couple.** Anything it refuses, look at — a refusal on a real message is a gap, not a success.

**Then do the same for the balance summary.** If my bank sends a daily or weekly balance email, it needs its own parser in the `BALANCE_PARSERS` registry — a separate registry, because a balance is not a transaction and bending one contract to carry both is how two rules drift apart.

**This is not optional decoration.** The balance summary is the **only external check this app has on itself.** Without it every figure is derived from rows the app already holds, so a missing transaction is invisible by construction — there is nothing to notice its absence against. With it, the bank's own balance can be compared to what the ledger says should have happened.

### 12. Understand which source wins — there are three, and they disagree

**My data arrives at three speeds, and they are not equally true. Say this back to me so I know you have it:**

| Source | Arrives | How true |
|---|---|---|
| **Transaction alerts** | seconds | **Fast and provisional.** Often the authorisation, not the final amount |
| **Balance summary** | daily or weekly | **A checkpoint.** Says what the balance *is*, not what made it up |
| **Statement** | monthly | **Final. The source of truth.** Settled amounts, nothing outstanding |

**Where they disagree, the statement wins. Always.** It is the only one of the three that is closed.

> **THIS IS ENFORCED IN CODE, NOT BY HAND. Do not re-implement it.**
>
> `SourcePrecedence.gs` holds the ranking — `statement 5 > csv 4 > manual 3 > balance 2 > alert 1 > blank 0` — and every row on the `Transactions` tab carries a `Source` in column J. A parser declares its own kind, so adding a statement parser is all it takes for statements to start correcting alerts.
>
> **The duplicate key is `movementKey_()`: date, amount, account, and no free text.** The three sources describe one movement in different words *by design*, so a key holding the description fails precisely where the design guarantees a collision. A key match is a **candidate**: same source twice means two real movements, different sources mean one movement and the higher rank wins.
>
> **`replace` is a field-level MERGE, not an overwrite.** Precedence settles conflicts of amount; it does not make the winning row better in every field. An alert often carries the card number and the person while a bank export carries neither — so money follows rank and identity survives. `mergeRow_()` does this. Do not "simplify" it into a row swap.

**So the statement is not another feed — it is the correction pass.** When one arrives, its amounts are authoritative:

- a ledger row whose amount differs from the statement was recorded from an authorisation — **correct it to the statement.** `supersedesPending_()` does this automatically for rows still flagged `Pending`: same account, within four days, matching merchant prefix. **Its limit, stated rather than hidden:** two pending charges at one merchant inside the window cannot be told apart. **It refuses the whole entry rather than correcting whichever row it reached first**, and lists the candidate rows for you to fix by hand — the same *refuse rather than guess* rule as the parsers in step 11
- a statement line with no ledger row at all is a transaction whose alert never arrived — **add it, and treat it as evidence an alert is missing or an account has none**
- a ledger row with no statement line is a hold that never settled, or a duplicate — **flag it for me rather than deleting it**

> **Rows written before the `Source` column existed carry a blank, which ranks 0.** Which source produced them is not recoverable — the `Import Log` holds message ids but was never linked to the rows it wrote. Blank losing to everything is the right default: anything identified beats anything unidentified. **Do not try to backfill it by guessing from the wording.**

**Tell me how my statements arrive** — a data file, a PDF attachment, or just a notice with a login link — because that decides whether this pass can run on its own or needs me once a month. If it needs me, say so plainly and make it a standing monthly reminder rather than something we both forget.

### 13. Set up the weekly self-audit

Run **`reconcileBalances`** in `EmailIngest.gs`. It takes consecutive balance checkpoints and checks the bank's movement against the sum of my own transactions for the same window.

Explain the result to me in plain language, and explain its one limit honestly: **checkpoints carry a time, my transaction rows carry only a date.** A transaction on the same day as a checkpoint may have landed either side of it. **A match is strong evidence; a mismatch is a prompt to look, not proof of an error.**

**Weekly, because statements are monthly.** A month is a long time to carry an error you could have caught in a week — the statement is the final word, but the balance summary is what stops you waiting for it.

**Then make it a habit rather than a one-off.** Tell me plainly:

- to run it **weekly**, and how
- **what a gap actually means** — the bank moved by more than my transactions account for, so something is missing from the ledger, and the most likely causes are an alert that stopped arriving or an account with no alert on it at all
- that **the app cannot detect this on its own**. An account with no alerts looks exactly like an account with no activity, and the ledger will never contradict itself. Only the bank's own balance can.

**If I would rather not remember, offer to schedule it** so the result is written where I will see it.

### 14. Prove it will not double-file anything

Run these three in `EmailIngest.gs`, in order:

1. `scanBankAlerts` — practice, writes nothing
2. `scanBankAlertsLive` — writes for real
3. `scanBankAlertsLive` **again — it must skip everything it just did**

**Step 3 is the whole test.** If the second live run writes anything, stop and fix it. Do not schedule anything until you have watched this pass.

> **Step 2 will write a lot, and that is correct.** It is importing every alert that has accumulated since the pre-script ran. Check that those transactions do not already exist from my imported history — the two can overlap at the edges, where the CSV export and the alerts cover the same few days. The duplicate check matches on **date, amount and account — deliberately not the description**, because the export and the alert word the same movement differently. Where both describe one movement, the higher-ranked `Source` wins (see step 12); where one source reports the same movement twice, both are kept, because that is what two real payments look like. **Read the skipped and replaced counts rather than assuming.**

### 15. Turn on the hourly run

Run `installIngestTrigger`. Expect exactly one trigger. `listTriggers` shows what is scheduled; `removeIngestTrigger` turns it off.

### 16. Help me pick my passphrase

The web page unlocks with one **passphrase**, shared by everyone in my household. It is a Script Property named `APP_PASSPHRASE`, and it does not exist until I create it. **You help me choose it; I type it.** You never see it, never ask for it, never suggest the exact one I should use.

**Tell me what it protects, so I pick sensibly.** It opens my *budget page* — transactions, categories, balances I typed in. It cannot move money and it holds no card numbers or bank logins. But everything on that page is my financial life in one view, and the name-plus-passphrase sign-in means the passphrase is the whole lock. The directory refuses a household name after ten wrong tries in ten minutes, so a stranger cannot grind through guesses — **the real danger is not a clever attacker, it is a passphrase I already use somewhere else.**

**Give me the recipe, not the answer:**

- **Four or five ordinary words, unrelated to each other, with a hyphen or space between.** Long beats clever. Something like *the shape of* `copper-lantern-tuesday-river` — that exact one is now in this document and must not be used.
- **Easy to type on a phone.** No symbol gymnastics, no capital-in-the-middle. Everyone in the house will type it into a phone, and “which O was a zero?” mistakes are what a throttled sign-in punishes.
- **Brand new.** Not my bank, not my email, not my phone unlock, not any variation of them. If it is already in my password manager under another site, it is out.
- **Nothing findable.** No names of people in the house, no street, no pet, no birth year.

**Then set the screen up so I only type one thing — this is the standard, not a fallback:**

1. **My password manager first**, as a new entry called *Household Budget*, so it is saved before I can mistype it anywhere.
2. **You open Apps Script → Project Settings and, if you can, click Edit script properties** so the `APP_PASSPHRASE` value box is already editable when I look (add the row first if it does not exist). Then say "it's ready" and stop. **I paste the value and click Save.** If the Edit button ignores your click — it has — tell me and I click it; do not keep hammering the form.

> **WHILE THAT SCREEN IS OPEN YOU READ NOTHING FROM IT.** Not the values, not "just the names", not a screenshot. Every input on that form is a text box, and a script that walks the inputs to list the property names will read the passphrase as a side effect — that exact mistake has been made. **Do not run any script that touches an input's value on that page.** Confirm the form is in edit mode by the presence of a Save button and nothing else.

**How you check it worked without seeing it:** the page unlocks in step 17. If it refuses, the two copies disagree — tell me to paste from the password manager into the property again, not to retype.

**If I ever want to change it:** edit that one property. Every phone will ask for the new passphrase on its next open, and the household-name lookup uses it too, so nothing else needs touching.

### 17. Point the web page at my data

**The web page is here:**

`https://turleytrevon-png.github.io/turley-household-tracker/`

It is shared — the same page serves every household — and it holds no data of its own. On its first load it asks for a **household name** and my **passphrase**. A short name is turned into an API address by a private directory; **mine is not in it yet**, so on first setup tap **"Use an app web URL instead"** and paste the address from the step below, then my passphrase. **Once I am in, the app offers to name the household — a one-word, lower-case name like `smith`. Ask me what I want it called, then I type it into that box and tap Save.** The app registers the name itself, proving my passphrase to the directory from its own storage — **you never handle the passphrase for this, and neither does Trevon.** From then on any phone signs in with the name and the passphrase. Both values are stored in my browser only. If the name is already in use, the app says so; pick another.

Open it and set it up with my own API address and passphrase.

> **THE API ADDRESS DOES NOT EXIST YET, AND NO EARLIER STEP MAKES IT.** It comes from deploying the Apps Script project as a web app (**Deploy → New deployment → Web app**). **Do that here, before touching the page**, and tell me the address once you have it. The passphrase is already in place from step 16 — if it is not, go back, because the page cannot be checked without it. Earlier drafts said *"you have both by this point"* — that was simply false. Confirm it loads my figures, on my phone as well as on a desktop.

**Set the household name in the same place, as a third Script Property named `HOUSEHOLD_NAME`** — the words I want as the app's title and on my phone's home screen, for example `The Smith Household`. It is not a secret and it is not typed into the page: the page asks the API for it after each unlock and remembers the answer, so it is set **once** and every device I sign in on gets it. **Ask me what to call it rather than inventing something from my surname.**

> **Leaving `HOUSEHOLD_NAME` unset is a valid answer, not a skipped step.** The API returns an empty string, the page reads that as "no opinion", and the title stays the generic `Household Budget`. **What it must never do is reset a name that is already showing** — so if a device already displays my household name, an unset property leaves it alone.

## Rules that apply throughout

- **After changing any code, reload the editor tab.** It does not refresh itself and will keep showing the old function list.
- **Check every result in the `Automation Log` tab**, not by whether a command appeared to succeed.
- **Never put a raw regular expression in the spreadsheet.** The Match column covers patterns safely. A broken expression in one cell stops the hourly job for the whole account.
- **When something does not work, find out what it actually did before changing anything.** Read the log. A guess costs more than a query.
- **Never ask me for a password**, and never type one on my behalf.
- **Bank sessions time out in minutes, and a signed-out page looks exactly like an empty one.** Work in three passes: signed in and read-only to discover, offline with me to decide, signed in again to execute. **The timeout lands on my thinking time and cannot be avoided — put it between the reading and the writing.** Keep a list of what is already done, and if a page comes back bare, check for a logout before concluding anything from it.

## What "done" looks like

- The hourly job runs and new transactions appear without anyone doing anything
- Nothing in the Sheet carries anybody's name but mine
- Anything uncertain waits in a queue for me instead of being guessed at
- My loans show a real payoff date, with mortgage escrow separated out
- I have not had to read a line of code
- **Every account, card and loan on the list I gave you at the start is accounted for** — set up, or explained. **Not silently absent.**

```
PROMPT 2 ENDS HERE
```

---

# Appendix — bank click paths already mapped

Give this to Claude only if it cannot find the alert settings at your bank. These are the two banks mapped so far; yours may differ.

# Bank alert setup — click paths, per bank

**Mapped 2026-08-25 by walking the live settings pages** while Trevon was signed in. Read-only; nothing was changed.

This exists so nobody has to hunt again. Every bank buries this differently, and in both cases below the alert that produces per-transaction emails is **not** where a reasonable person would look first.

**A kit artefact.** Written generically so it can ship — no account numbers, no balances.

---

## Mountain America Credit Union (MACU)

**Go straight there: `https://o.macu.com/NotificationSettings`**
Menu route if the URL changes: **Security & Settings → Alerts**.

Six tabs across the top: `General Alerts` · `Accounts` · `Authentication` · `Card` · `Mobile Deposit` · `Transfers`.

**Both alerts this app parses live under `Accounts`:**

| Alert | What it gives you |
|---|---|
| **Transactions** | one email per transaction — the ledger feed |
| **Balance Summary** | a **weekly** email with every account's balance and its last 5 transactions — the reconciliation checkpoint |

### The Transactions alert

*"Receive an alert whenever a transaction is made on this account."*

Four conditions: **Deposit is exactly · Deposit is over · Withdrawal is exactly · Withdrawal is over**, plus an **Amount** field. Delivery is **Email**, with a checkbox per verified address on the account. Then **Save**.

> [!important] **The amount to use is `$0.01`, not `$0`.**
> That is what is set on this household's account, and it matches the criteria line printed in the alert emails themselves — *"Withdrawals over $0.01"*. Use the smallest amount the field accepts; "over zero" is not offered.

> [!warning] **ALERTS ARE PER ACCOUNT.** There is a `Selected Account` picker at the top of the panel and the settings apply only to the account chosen. **A household with checking, savings and a money market needs the alert set three times.** Set it on checking alone and everything else is silently invisible — and the app cannot tell the difference between "no transactions" and "no alerts".

> **Deposits need their own condition.** *"Withdrawal is over"* covers money out only. Refunds and deposits arrive as separate alerts and the parser reads the section header to get the sign, so both directions have to be switched on or half the ledger never appears.

### The Balance Summary alert

Same `Accounts` tab. Worth switching on even though it is not transactions: it carries **every account's balance**, including ones the app cannot otherwise see, and it is the only external check the tracker has on its own arithmetic. **It arrives weekly on this account** — see the correction below before reading anything into a quiet stretch.

> [!important] **IT IS WEEKLY, NOT DAILY. Corrected by Trevon 2026-08-29 — do not re-raise this.**
> This note and the `Balance Summary` description in the MACU alert panel both read as daily. **They are wrong.** On this household's account the summary arrives **weekly**, and Trevon's instruction is explicit: *"The MACU balance arrives weekly. No need to audit daily."*
>
> **Why it matters:** a gap of several days is NORMAL and is not evidence of anything. On 2026-08-29 the last summary was 2026-08-25 and that was flagged as a four-day failure — **it was not.** Do not open a bank session over a quiet stretch shorter than about eight days.
>
> **Two summaries did land on consecutive days (8/24 12:33 PM and 8/25 2:54 AM)**, which is what made a daily cadence look real. Both fall in the window the alerts were being set up and mapped, so treat that pair as setup noise, not as the schedule.
>
> **What a real failure looks like instead:** `Balance Checkpoints` gaining no row across more than one expected weekly slot, while MACU **transaction** alerts keep arriving. Only then check `https://o.macu.com/NotificationSettings` → `Accounts` tab → Selected Account picker → Balance Summary destination address **present and ticked**.

---

## Capital One

**Go straight there: `https://myaccounts.capitalone.com/alerts`**
The account-summary page does not link to it in a way that is easy to find; the direct URL is faster than hunting.

Two sections: **Profile Alerts** (all accounts, primary email, security only) and **Account Alerts** (per card).

Per card, four groups: `Security and fraud` · `Balances and credit` · `Payments and statements` · `Spending and transactions`. Each row has a **Text** and an **Email** checkbox.

> [!important] **The one you want is `Instant purchase notifications`, and it is filed under SECURITY AND FRAUD.**
> Not under *Spending and transactions*, which is where anyone would look — and which contains only narrow alerts (International transactions, Duplicate charges, Higher-than-usual tips, Increases in recurring charges, Card declines, Merchant refunds, Subscriptions & free trials). **None of those is "every purchase".**
>
> Verified 2026-08-25: on this household's card, `Instant purchase notifications` has **Email** ticked, and it is the alert producing the *"A new transaction was charged to your account"* emails the parser reads.

> [!warning] **EACH CARD IS CONFIGURED SEPARATELY, and a card can be missing from this page entirely.** This household has two Capital One cards; **only one of them has an `Alerts for …` section on `/alerts`.** Before assuming a card is covered, confirm its section exists — and if it does not, the alerts for it live somewhere else and need chasing.

**Not needed from Capital One:** `Balance summary` under *Balances and credit*. It is off here, and the balance checkpoint comes from MACU instead. Turning it on would mean writing a second balance parser for no gain.

---

## Target Circle Card (RedCard) — NOT MAPPED, and read the warning before mapping it

**Attempted 2026-08-29. Blocked at a login. Nothing past the sign-in page has been seen, so nothing below describes its alert or export screens — because nobody has looked at them.**

### The two-site trap

`target.com` and the card portal are **different sites with different credentials.**

- `target.com` — the shopping account. Signed in there shows a Circle Card *benefits* page at `/circlecard/engagement`. It has **no transactions and no alert settings**. Easy to mistake for the card account, because it greets you by name.
- `https://www.target.com/myCircleCard` — redirects to **`mytargetcirclecard.target.com/ecs/auth/`** ("eCustomer Service"). **This** is card management. It asks for its own Username and Password, and **the target.com session does not carry over.**

Issuers differ too, which may mean two portals rather than one: the **debit** RedCard is issued by **Target Corporation**, the **credit card and Mastercard** by **TD Bank USA, N.A.**

### Before switching on ANY alert here — this would double-count

> [!warning] **RedCard activity is ALREADY in the ledger, arriving from MACU.**
> Purchases land as ACH rows on MACU checking — `ACH Withdrawal COMPANY: TARGET DEBIT CRD ENTRY: PURCHASE LASTNAME,FIRSTNAME` — 27 of them from June 2026 onward. The **2026-08-26 decision to keep the MACU account-level alert** was made partly to catch exactly these pulls.
>
> **`movementKey_()` is date + amount + account, with no free text.** A Target-sourced alert would carry a **different account**, and a purchase-date rather than the ACH settle-date. **The key would not match, so the dedup would not fire, and one purchase would become two rows.** Source precedence does not save this — precedence arbitrates rows that *collide*, and these would not collide.
>
> So: **do not turn on Target transaction alerts as a routine step.** If they are ever wanted, the dedup has to be solved first.

### What Target might still be worth

**Merchant detail, not money.** The MACU ACH row says `TARGET DEBIT CRD` and never what was bought. Target's own history would itemise it. That is a different problem from tracking the spend, and the spend is already tracked — so treat any Target export as a **nice-to-have**, and weigh it against the double-count risk above.

**Unknown until someone signs in:** whether the portal offers per-transaction alerts at all, which email addresses it has verified, and whether history exports as CSV/OFX or is screen-only.

---

## What to do for a bank not listed here

1. **Find the alerts or notifications section.** Try the direct URL patterns above first — `/alerts`, `/NotificationSettings` — before navigating menus.
2. **Look for the alert that fires on EVERY transaction, and do not trust the section headings.** Both banks here file it somewhere counter-intuitive. Read every alert name in every group before choosing.
3. **If there is a threshold, set it to the smallest amount accepted**, and check whether money-in and money-out are separate switches.
4. **Set it on every account, not just the main one.**
5. **Set delivery to the email address the Sheet's Google account reads.**
6. **Then wait for a real alert to arrive before writing a parser.** A settings page that says the alert is on is not evidence that it is sending. The email is.

---

## Working inside a bank site — session timeouts

**Bank sessions expire in minutes of inactivity, and reading a message counts as inactivity.** Both sites mapped here behave this way. Plan around it rather than being surprised by it.

**The order that works is three passes, not two.** Agreeing a plan *before* the sign-in sounds right and is not — **the owner does not have the information to agree to it.** Most people cannot list their accounts, their card last-fours and who uses which from memory.

1. **Signed in, read only** — discover the accounts, the cards, the alerts already on, the alert types offered, and the addresses the bank has verified. Change nothing.
2. **Offline** — bring it back, ask what only they can answer (whose card is whose, which accounts they want), agree the list. **The session dies here, and that is the point of doing it here.**
3. **Signed in again** — execute, without stopping to ask.

**The timeout is unavoidable because it lands on the owner's thinking time.** All you can choose is whether it interrupts a read pass or a write pass.

**A simple bank may fit passes 1 and 3 in one session. Do not force a second login for its own sake.**

**Keep a per-account checklist** of what is saved and what is not. When the session drops — it will — that list is the difference between resuming and starting over.

> [!warning] **A signed-out page and an empty page are indistinguishable.**
> If the alert controls are missing, or the page comes back bare, **check for a login redirect before concluding anything.** Recording "this card has no alerts section" when the session had simply expired produces a wrong answer that looks exactly like a finding — and it is the kind that gets written down and believed.
>
> This matters specifically for the Capital One observation above (one card having no `Alerts for …` section). **That was read on a live session and is believed correct — but anyone re-checking it should confirm they are still signed in before agreeing or disagreeing.**

**Tell the owner up front that several sign-ins are expected.** Otherwise repeated logins read as something going wrong.

> [!warning] **Open every write session by confirming the destination address is present AND SELECTED.**
> The selection is stored **per alert**, and the list usually has one box already ticked — often an old address. Saving without checking sends the alerts somewhere nobody reads, and **nothing errors**: the bank reports the alert as on, the settings page looks right, and the app reads an empty mailbox and reports no transactions. **That is indistinguishable from a month of no spending**, so it is found late, and by then the history is gone.
>
> This is the same failure family as the signed-out page above — **a correct-looking screen standing in for a working one.**

> [!warning] **The destination address may be a pick-list, not a free-text field.**
> MACU presents a **checkbox per email address already verified on the account** — you cannot simply type a new one in. If the chosen mailbox is not already on file with the bank, it has to be added and verified there first, which means a confirmation email and a wait. **Discover this in pass 1**, not when trying to save in pass 3.
