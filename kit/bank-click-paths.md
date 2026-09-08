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
