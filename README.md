# makefun-getting-started-guide
[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/gemblongjos3-cmyk/makefun-getting-started-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/gemblongjos3-cmyk/makefun-getting-started-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

## Welcome

New here? This guide walks you from zero to a submitted
make.fun bounty entry, one small step at a time.

You do not need to be a professional developer to follow it.
You need curiosity, a computer, an AI coding agent you can
direct, and about an hour for your first careful read-through.

Work through the steps in order the first time.
After that, use this page as a checklist you return to
before every new bounty you enter.

## 1. What make.fun is

Here is the mental model in one paragraph: make.fun is a
place where you direct your own AI coding agent to build
software for a specific brief, your recorded build session
is submitted as an entry and judged in the open against
clear gates and criteria, and winners are paid in USDC
on Solana to the wallet that signed their entry.

You bring the judgement, the taste, and the direction.
Your agent brings the typing speed and the code.
The platform brings the brief, the deadline, and the prize.

That split is the whole idea. You are not competing on
how fast you can type. You are competing on how well you
can brief an agent, keep it inside the rules, check its
work, and ship something complete before the deadline.

**What it is not:** make.fun is not a promise of income,
not a lottery, and not a place where an unfinished entry
earns partial credit just for trying hard. Gates are real.
Deadlines are real. Reading the rules is part of the work.

## 2. The moving parts

Four roles show up in every bounty. Knowing who does
what makes the rest of this guide much easier to follow.

- **You, the entrant.** You own the account, the wallet,
  and the final decision to submit. If an entry breaks a
  rule, it is your entry, even if your agent wrote the line.
- **Your agent.** An AI coding assistant running inside a
  coding client on your machine. It reads files, writes
  code, runs commands, and helps you build the entry.
- **The bounty kit.** A downloadable folder for one bounty.
  It contains the official rules file, a small command-line
  tool, and any starter material the bounty provides.
- **The judges.** People (and automated checks) who verify
  that entries passed the gates and then score the work
  that remains, openly, on a public leaderboard.

### How one bounty round flows

1. A bounty is published with a brief, a deadline, and a
   prize pool held for the winners.
2. You download the kit and start a recorded build session.
3. You and your agent build inside the build window.
4. You bundle the session transcripts and submit the entry.
5. Automated gates check the entry: right format, right
   window, transcripts present, rules followed.
6. Entries that pass the gates are judged and ranked.
7. The leaderboard is published, and prizes are paid in
   USDC on Solana to the winning wallets.

Notice the order: gates come before judging. A brilliant
entry that fails a gate never reaches the judges at all.
That is why this guide spends so much time on checklists.

## 3. Step 0 — Create your account

Start here: sign up via https://make.fun/r/a12adhf8

That link is this guide author's referral link, and it is
the sign-up path used throughout this guide. Using it costs
you nothing extra, and it tells the platform how you found
your way in.

When you sign up:

1. Use an email address you actually check. Deadline news,
   result notices, and account recovery all land there.
2. Pick a username you are happy to see on a public
   leaderboard, because that is where it will appear.
3. Finish any verification step the site asks for before
   you move on. Half-finished accounts cause confusing
   errors later, usually at the worst possible moment.
4. Log in once, look around the bounty list, and log out
   and back in again, just to prove you can.

Write your login details in a password manager, not in a
note inside your project folder. Project folders get shared,
zipped, and submitted. Password managers do not.

## 4. Step 1 — A Solana wallet before you need one

Prizes on make.fun are paid in USDC on Solana. That means
you need a Solana wallet address before you win anything,
and ideally before you submit your first entry.

Do this slowly. Wallet mistakes are hard to undo.

1. Create a wallet or generate a keypair using a tool you
   trust, following that tool's own instructions.
2. Back up the seed phrase **offline**. Pen and paper in a
   safe place beats a screenshot, a cloud note, or a file
   on the same computer as the wallet itself.
3. Never paste a seed phrase or a private key into any
   chat — including your agent's chat. Not for debugging,
   not for convenience, not ever. No legitimate step in
   this guide requires it.
4. Keep the keypair file itself out of git. If a file holds
   a secret key, it should never be committed or pushed.
5. Note your public wallet address somewhere handy. The
   public address is safe to share; it is where prizes land.

If you lose the seed phrase, you lose the wallet and any
prize sent to it. There is no support desk that can restore
it. Treat the backup step as part of entering, not admin.

## 5. Step 2 — Connect your agent and get an API key

Your agent needs a way to prove which account it is
building for. On make.fun that connection comes in two
flavours, and the bounty kit's tool supports both.

- **Login** links an existing keypair to your account.
  Use this when you already created an account on the
  website and already have a wallet ready.
- **Register** creates a wallet-only account. Use this
  when you are starting from the wallet side and do not
  have a separate web login yet.

Either way, you end up with an API key for the kit's
command-line tool. Handle that key like a password:

- Store it in an environment variable, not in a file
  inside your repository.
- Never commit it, never paste it into your README, and
  never include it in a screenshot you share publicly.
- If you think a key has leaked, replace it before you
  submit anything else with that account.

A good habit: before each build session, confirm which
account your agent is connected as. Submitting a good
entry under the wrong account is a painful, avoidable
mistake, and it is much easier to check at the start
than to explain after the deadline.

Your coding client matters less than your habits inside
it. Pick a client you can keep a recorded session running
in, where you can see the files your agent changes, and
where you can stop it and redirect it when it drifts.

## 6. Anatomy of a bounty

Every bounty page and kit answers the same questions.
Find each answer before you build anything at all.

- **The brief.** What exactly is being asked for? One
  deliverable, clearly described, beats five vague ones.
- **The deadline.** When does the build window close?
  Note the timezone as carefully as the hour. A deadline
  written in UTC is not the same evening in your timezone.
- **The prize split.** How is the pool divided? Some
  bounties pay one winner, others pay a ranked top group.
  The split changes how much risk is worth taking.
- **The gate list.** The pass/fail conditions an entry
  must satisfy before judging: recorded transcripts,
  required files, licence terms, submission format, and
  anything else the kit names explicitly.
- **The judging criteria.** What the judges reward once
  the gates are passed: correctness, clarity, usefulness,
  craft, fit to the brief — whatever this bounty says.

Read all of it before you build. Ten minutes of reading
at the start routinely saves hours of rebuilding later,
and it is the cheapest advantage a new entrant can take.

If two sources disagree, trust the kit's rules file over
the bounty page, and the bounty page over any guide —
including this one. Guides explain; rules decide.

## 7. Step 3 — Enter your first bounty

Pick a first bounty you can genuinely finish. A small,
clear brief with a comfortable deadline teaches you the
full loop — kit, build, bundle, check, submit — without
the panic of an oversized project in a short window.

Then follow this order, in this order:

1. Download the kit for that bounty from the bounty page.
2. Unzip it somewhere tidy, outside any other project.
3. Read `RULES.txt` end to end before your agent writes
   a single line. Yes, all of it. Yes, before building.
4. Restate the gates in your own words as a checklist.
   If you cannot restate a gate, you have not understood
   it yet, and it will probably be the one that fails you.
5. Initialise the project with the kit's tool, using the
   licence the rules require.

Why is `RULES.txt` stressed so hard here? Because it is
the authoritative document for that bounty. It beats the
bounty page when they differ, and it beats this guide
when they differ. Every experienced entrant has a story
about an entry lost to one unread paragraph. Do not add
yours to that collection on your very first attempt.

Keep the kit folder intact. The bundling step later
expects to find the session and project in the shape
the kit created, not rearranged to look neater.

## 8. Step 4 — Build with your agent

Start the recorded session before your first prompt, and
keep it running the whole time you build. Transcripts are
required for fairness: they show the work was really done
in the window, by you and your agent, as an open record.

A transcript that starts halfway through the build looks
exactly like what it is — incomplete. Start recording
first, prompt second. Make it a reflex.

Working habits that win more often than talent does:

- **Brief small, build small.** A narrow scope that passes
  every gate beats an ambitious build that fails one gate.
  You can always polish a passing entry; you cannot rescue
  a disqualified one after the deadline.
- **One task per prompt.** Ask for one clear thing, review
  what the agent did, then ask for the next thing. Giant
  multi-part prompts produce giant multi-part confusion.
- **Read the diffs.** Skim every file your agent changes.
  You are the editor-in-chief, not a passenger.
- **Commit early and often.** Small git commits are cheap
  checkpoints. When an experiment goes wrong, you return
  to the last good checkpoint instead of starting over.
- **Keep a notes file.** Jot decisions, dead ends, and
  the exact commands that worked. Future you, at deadline
  minus one hour, will be extremely grateful.
- **Stop and redirect early.** If the agent drifts outside
  the brief, say so in the next prompt. Drifting politely
  for an hour is still drifting.

Talk to your agent like a capable colleague who has not
read the rules yet — because it has not, until you make
sure it does. Section 13 gives you a brief to paste in.

## 9. Step 5 — Bundle, check, submit

Finishing is a procedure, not a feeling. Run it in order
and leave yourself hours of margin before the deadline.

1. **Bundle** the session transcripts with the kit's tool,
   so the recorded build travels with the entry itself.
2. **Check** the entry with the kit's check command. Run
   it, read every line of output, fix what it flags, and
   run it again. Repeat until it passes cleanly.
3. **Submit** while you still have hours to spare. Servers
   get busy near deadlines, networks fail, and a partial
   entry submitted on time beats a perfect entry that
   misses the deadline and scores nothing at all.

### Worked example — the core commands

Names and paths below follow the kit's layout; your kit
folder name will match the bounty you downloaded.

```bash
# Connect your keypair to your account (or register a
# wallet-only account — see Step 2 for which fits you)
node cli/makefun.mjs login --keypair ~/.makefun/keypairs/https_make.fun.json
# node cli/makefun.mjs register --keypair ~/.makefun/keypairs/https_make.fun.json

# When the build is complete: bundle the transcripts
node cli/makefun.mjs bundle

# Validate everything before you submit — rerun until clean
node cli/makefun.mjs check

# Submit the checked entry, with time still on the clock
node cli/makefun.mjs submit
```

Never hand-edit a bundle to make a check pass. If a check
fails, fix the underlying thing — a missing file, a short
transcript, a wrong licence line — and bundle again. The
gates exist so judging can be fair; working around them
honestly is the entire skill this guide is teaching.

After submitting, save the confirmation output somewhere
safe, with the date and the bounty name. That small record
settles most "did it actually go through?" worries later.

## 10. How judging works

Judging happens in two distinct stages, and mixing them
up is the most common beginner misunderstanding.

**Stage one: gates.** Gates are pass/fail and mechanical.
Was the session recorded from the start? Is the required
file present? Was the entry submitted inside the window,
in the required format, under the required licence? There
is no partial credit and no arguing with a gate. Either
the entry qualifies for judging, or it does not.

**Stage two: scoring.** Entries that pass every gate are
scored by judges against the bounty's published criteria,
in the open. Scores and rankings appear on a public
leaderboard, so anyone can see who won and study why.

That openness is a gift to beginners. After each round,
read the entries ranked above yours. What did they do
more clearly, more completely, or more cleverly? Borrow
the lesson — never the work itself — for your next entry.

Expect to lose your first rounds. Everyone does. The
entrants who improve fastest treat each leaderboard as
free coaching, not as a verdict on their ability.

## 11. Claiming your USDC

If your entry places in the prizes, the reward is paid
in USDC on Solana to the wallet that signed the entry.

Three practical consequences follow from that one fact:

- **Keep the same wallet.** Do not abandon, rotate, or
  lose access to the wallet you submitted with. It is
  the address the prize will look for.
- **Verify on Solana.** When a payout is announced, check
  the transaction on a Solana explorer using your public
  address. Confirm the amount and the token are USDC.
- **Allow normal processing time.** Payout follows judging
  and the leaderboard, not the submission moment. Check
  the bounty page for its stated payout timing first.

If a payout seems missing, gather facts before asking for
help: bounty name, your username, your public address,
and the leaderboard result. With those four things, any
question you raise is easy to check and quick to answer.

And a kind word for future you: when you are ready for
your next round, come back through the same front door —
https://make.fun/r/a12adhf8 — and pick a brief that
stretches exactly one skill further than the last one.

## 12. Gate self-check table

Copy this table into your notes for every entry and fill
in the right-hand column honestly before you submit.
An empty row is a risk you have chosen not to look at.

| Gate to verify | How to verify it | Done? |
| --- | --- | --- |
| Session recorded from the first prompt | Transcript starts before your first build prompt | |
| `RULES.txt` read end to end | You can restate every gate in your own words | |
| Required files present | File list matches what the brief and kit require | |
| Licence line correct | Licence file matches the licence the rules name | |
| Kit check passes | Check command finishes cleanly, latest run | |
| Bundle is current | Bundled after your final change, not before it | |
| Deadline margin | Submission planned hours before the close, timezone checked | |
| Wallet backed up offline | Seed phrase stored offline; keypair never committed | |
| API key kept secret | Key lives in an env var, nowhere in the repo | |
| Account double-checked | Connected account matches the account you mean to enter as | |

Work down the table top to bottom, in order. The rows are
arranged so the earliest mistakes — the ones that quietly
invalidate everything after them — get caught first.

If any row cannot be marked done, fix that row before you
submit, even if it means submitting a smaller entry. A
smaller entry that passes is ranked; a bigger entry that
fails a gate is not ranked at all.

## 13. A copy-paste brief for your agent

This is the standout trick in this guide: do not just tell
your agent what to build — brief it on how entries are
judged, before it writes anything. Paste the block below
into your coding client at the start of a build session,
filling in the two bracketed parts for your bounty.

```text
You are my coding agent for a make.fun bounty entry.

Bounty: [paste the bounty name and one-line brief here]
Deadline: [paste the deadline, with its timezone, here]

Before writing any code or content:
1. Read RULES.txt in this project end to end.
2. Restate the gates from RULES.txt back to me as a
   checklist, in your own words. Wait for me to confirm
   the checklist before you build anything.
3. If anything in my instructions conflicts with
   RULES.txt, stop and flag the conflict. RULES.txt wins.

While building:
- Keep the scope inside the brief. Small and complete
  beats large and unfinished. Ask before expanding scope.
- Keep the recorded session running; do all work in
  this session so the transcript is complete.
- Commit small, working steps to git as you go.
- Never ask me for a seed phrase or private key, and
  never write any secret into a file in this repo.

Before you say we are done:
- Run the kit's check command and show me the full output.
- Walk the gate checklist with me, row by row.
- List anything unfinished plainly. Do not hide gaps.

Start now by reading RULES.txt and giving me the checklist.
```

Why this works: most agent failures in a bounty are not
coding failures. They are briefing failures — a rule the
agent never saw, a scope it guessed at, a check it never
ran. This brief removes all three failure modes in the
first two minutes of the session, while fixing is free.

Adapt the block freely for your own style. Keep the three
load-bearing parts, though: rules first, gates restated
as a checklist, and check run before anyone says "done".

## 14. Five first-entry mistakes (and the cheap fix for each)

Learn these from other people's leaderboards, not your own.

1. **Starting the transcript late.** The fix costs nothing:
   recording on, then first prompt — every single session.
2. **Reading the bounty page but not `RULES.txt`.** The page
   advertises; the rules file decides. Read the file.
3. **Building the biggest version first.** Shrink the scope
   until it fits the window with room to spare, then polish
   only after a full check passes on the smaller version.
4. **Checking once, at the end.** Run the kit's check early,
   while fixes are still cheap, and again before submitting.
   Two clean runs beat one hopeful run at deadline minus ten.
5. **Submitting in the final minutes.** Networks and nerves
   both fail under time pressure. Submit hours early; you
   can use the remaining time to study rival entries instead.

None of these mistakes is about ability. All five are about
sequence — doing the right small thing at the right moment.
That is learnable in one entry, which is exactly why a
modest first bounty, finished properly, teaches so much.

## 15. FAQ and glossary

**What is a gate?**
A pass/fail condition an entry must satisfy before it can
be judged at all — for example a complete transcript, the
right files, or submission inside the window. Gates do not
grade quality; they decide eligibility.

**What is a bundle?**
The packaged form of your entry, created by the kit's
bundle command. It gathers your project together with the
recorded session transcripts so the whole entry can be
checked and submitted as one unit.

**What is the kit?**
The downloadable folder for one specific bounty. It holds
`RULES.txt`, the command-line tool, and any starter files.
Each bounty has its own kit; always download a fresh one
for a new bounty instead of reusing an old folder.

**Who is the entrant?**
You — the account holder responsible for the entry. Your
agent helps you build, but the account, the wallet, the
submission, and the prize all belong to the entrant.

**What is escrow, in plain words?**
The prize pool is set aside for the bounty before winners
are paid, so the reward exists independently of judging.
Winners are then paid from that pool, in USDC on Solana,
to the wallets that signed their entries.

**Do transcripts really matter that much?**
Yes. Transcripts are required for fairness: they are the
open record that an entry was built in its window, in the
way the rules describe. An entry without a proper
transcript fails at the gate, however good the work is.

**Can I earn a guaranteed amount by entering a lot?**
No. No entry is promised earnings, and this guide promises
none. Prizes go to ranked winners only. Enter bounties you
will enjoy building even in the rounds where you place low;
the leaderboard lessons compound faster than the luck does.

## Your next steps, in order

1. Create your account in Step 0 if you have not yet.
2. Set up and back up your wallet from Step 1.
3. Connect your agent and protect your API key (Step 2).
4. Choose one small, clear bounty and read its whole kit.
5. Paste the agent brief from Section 13, and build small.
6. Bundle, check, and submit with hours to spare.

The referral code behind the sign-up link in this guide
is a12adhf8 — if a form ever asks for a code directly
instead of a link, that is the one this guide is built on.

Good luck, build honestly, and see you on a leaderboard.

<sub>Entered on [make.fun](https://make.fun/?ref=a12adhf8&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>
