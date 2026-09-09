# Prompt 1 — Alerts

Paste everything below this line into Claude. Run it days before Prompt 2.

---

You are doing one small job for me today, ahead of setting up a household budget app later this week.

**The job: switch on my bank's transaction alert emails, so a few days of them have accumulated before we build anything.** The app reads those emails to record my spending automatically, and the code that reads them has to be written against real examples. Starting the alerts now means those examples exist by the time we need them.

Do not set up anything else. Do not build the app. This is the alerts and nothing more.

**Ask one question at a time, then stop and wait for me.**

> **And never explain something until you have checked the explanation.** If an account looks wrong, an alert looks missing, or a page looks empty, **find out why before telling me why.** A reason that merely fits is not the reason, and **a confident wrong one is worse than none** — I will believe it and stop looking.

## Before anything — check your own toolkit

**One line each, and actually try the action rather than reading a settings page.**

1. **Can you drive my Chrome browser?** *Test:* open `https://www.google.com` in a new tab and tell me the title. This is how you read my bank's alert settings and set them.
2. **Can you read my Gmail?** — either a Gmail connector, or by opening Gmail in that Chrome. This is how you prove at the end that a real alert actually landed.

**If you have both, drive it yourself and only stop at the points marked as mine.**

**If you have neither, this prompt still works — say so, and switch to coaching me.** You tell me exactly what to click, one screen at a time, and I read the screen back to you. **Do not silently switch modes**; tell me which one we are in, because it changes how long this takes. The main setup prompt in a few days **does** require browser control, so if it is missing, this is the moment to fix it rather than at the start of an evening's work.

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

> **If I pick this one, there is a thing to VERIFY rather than assume.** The app finds my alerts by searching for **the bank's own sending address** — `from:alerts@mybank.example`. Gmail's own forwarding normally passes the original sender through unchanged, so the search keeps working. **A rule that re-sends the mail from my address instead would break it silently, and the app would report no transactions.** So once forwarding is on, **open the forwarded copy in the destination mailbox and read who it says it is from.** If it says the bank, we are fine. If it says me, tell me — we either change the rule or go back to one of the other two shapes.

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
- **the exact address the alerts are SENT FROM**, once the first one arrives — see the note at the end. The setup prompt needs it verbatim and would otherwise go hunting for it

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

## Last thing, and do not skip it — hand me THE SETUP LIST

**Everything you just learned dies with this conversation unless you hand it back to me.** The setup prompt in a few days is a **new conversation with no memory of this one**, and its very first step asks me for this list by name. If I do not have it, that session either rebuilds it from scratch or, worse, quietly builds an app that is missing an account.

**So finish by printing one block I can copy and keep. Put it in a fenced code block so it copies cleanly.** Call it **the setup list**. Include, in plain text and nothing fancy:

1. **The mailbox** the alerts land in, in full — and if they are forwarded, where from and confirmation that the forwarded copy still shows the bank as sender.
2. **Every bank**, and under each one every **account**, **card** (last four) and **loan**, with:
   - the alert types now switched on, or **`NO ALERT`** and why
   - **`CARRIES A BALANCE`** where it does
   - **whose card it is**, where we worked that out — so the setup prompt confirms it in one word instead of asking me again
3. **The sending address of the real alerts**, per bank, exactly as it appears — this is what the app's reader is keyed on.
4. **Where each statement lives and what form it takes** — data file, PDF attached to the email, or a notice with a login link. Per account, not per bank.
5. **Anything unfinished** — an alert that would not save, an address still waiting on the bank to verify, an account I mentioned that we never found.

**Tell me plainly to save that block somewhere I will find it in a few days**, and that the setup prompt opens by asking for it.

## What happens next

Nothing, for a few days. The alerts pile up in that mailbox on their own.

**Then I come back with the main setup prompt — Prompt 2 in the same kit this came from.** That one builds the app, loads my history, and writes the code that reads these emails — and it will have a real week of them to work from instead of one or two. **It is one sitting, roughly an evening, so it wants a clear run rather than a spare ten minutes.**

Tell me roughly when to come back. **A few days is usually enough, but what actually matters is variety** — the app's reader needs to have seen money going out *and* money coming in, since refunds and deposits are often written differently. If my spending is light, longer is better.
