# PGConf.EU 2026 — Hackorum, solo draft

**Session:** Finally a Postgres Communication Hub for Experts and Newcomers

**Scheduled slot:** Thursday, October 22nd 2026, 09:25–10:15 (50 min), Audit 2

**Presenter:** Jack Bonatakis (Robin)

**Project credit:** Kai Wagner and Zsolt Parragi (Percona), and the Hackorum contributors

**Abstract:** https://www.postgresql.eu/events/pgconfeu2026/schedule/session/8197-finally-a-postgres-communication-hub-for-experts-and-newcomers/

This is a proposed solo rewrite. Kai cannot present. Jack's experience carries
the story; Kai and Zsolt retain credit for their work.

Slides live in `slides/slides.md`. Press **S** for speaker view. Preparation cues
in the notes are not lines to read aloud.

**Spoken name:** Say the project name once, on its landing-screen reveal:
“And that brings me to Hackorum.” Elsewhere the narration uses “the project,”
“the reader,” “the team,” or “we.” Titles and URLs can stay on screen without
being read aloud. This applies to the backup narration too.

Run `npm start`, then open <http://127.0.0.1:8000/>. Dependencies are installed.
For a checkout without dependencies, use `npm ci` first. Add `?print-pdf` for PDF export.

## Story and timing

| Section | Slides | Minutes | Elapsed target |
|---|---|---:|---:|
| Introduction → Robin incident → mailing lists → overnight inbox | 1–5 | 7 | 7 |
| “There has to be a better way” → pginbox → joining Kai and Zsolt → Hackorum | 6–9 | 5 | 12 |
| Brief walkthrough: Postgres users and contributors | 10–19 | 12 | 24 |
| AI topic summaries: local UI, output, and “good enough” | 20–24 | 9 | 33 |
| Other possible features and invitation to participate | 25–26 | 5 | 38 |
| Q&A and timing buffer | 27 | 12 | 50 |
| Backup material | 28–51 | As needed | — |

The prepared talk targets **38 minutes**, leaving **12 minutes for questions and
timing variation**. These are rehearsal budgets, not measured speaking durations.
The AI allocation includes time to read and discuss the actual output; it cannot
be filled by reading the placeholder text.

The story is: an operational problem made Jack curious about Postgres; the lists
were hard to keep up with in a personal inbox; pginbox led to collaborating on
Hackorum; the reader and contribution tools help today; summaries tackle the
remaining difficulty of getting enough context.

Navigation shortcuts:

* Opening: <http://127.0.0.1:8000/#/start>
* Hackorum: <http://127.0.0.1:8000/#/hackorum>
* Two perspectives: <http://127.0.0.1:8000/#/walkthrough>
* AI summaries: <http://127.0.0.1:8000/#/ai-summaries>
* Other possible features: <http://127.0.0.1:8000/#/whats-next>
* Questions: <http://127.0.0.1:8000/#/questions>

## The Robin incident

Facts supplied by Jack:

* Stale replication slots were present without the team knowing about them.
* The system was running inefficiently.
* Cloud SQL autoscaling added terabytes of storage for retained WAL.
* Jack identified the slots. Dropping them resolved the operational problems.
* The provisioned storage did not automatically shrink afterward.

Keep exact capacity and percentages out of both the slides and the narration.
Describe the replication-slot discovery and fix over the database-problem slide.
Keep this brief and personal. No incident date, slot origin, exact performance
measurement, bill amount, or diagnostic SQL has been supplied. Don't invent any.
The incident led Jack to learn more and subscribe to mailing lists; don't imply
that a mailing-list conversation diagnosed it.

Replication slots can retain WAL a consumer still needs:
[PostgreSQL documentation](https://www.postgresql.org/docs/current/warm-standby.html#STREAMING-REPLICATION-SLOTS).
For Cloud SQL, keep the statement about the incident and **automatic** storage
growth, rather than claiming storage can never be reduced. Google documents both
[automatic increases](https://docs.cloud.google.com/sql/docs/postgres/instance-settings)
and a separate [storage shrink operation](https://docs.cloud.google.com/sql/docs/postgres/shrink-instance-storage-capacity).

## Assets still needed

The overnight-inbox and pginbox screenshots are now installed as
`img/mailing-list-overnight.png` and `img/pginbox-overnight.png`. Both can be clicked
to enlarge in the presentation. The pginbox screenshot shows the topic list.

Three screenshot placeholders remain:

1. **“In progress — AI topic summaries”** — the working local UI.
2. **“One summary, one real discussion”** — a readable excerpt from the same topic.
3. **“What counts as good enough?”** — a summary claim beside the source messages needed to judge it.

The AI examples can come from one thread. Prefer the walkthrough's index-prefetching
topic if its output is useful; otherwise introduce another topic explicitly.
The evaluation slide can be assembled from separate crops. It does not assert
that the application already has citation or source-comparison UI.

Once the examples are chosen, replace the preparation prompts with the specific
point to demonstrate: what the output captures, what needs checking, and what
Jack thinks is good enough. Do not manufacture a successful result or a failure.

## Walkthrough

Allow about six minutes for each perspective:

* **I use Postgres:** search → a topic → reply branches → read state.
* **I contribute to Postgres:** unanswered patches → patch history → CI →
  trying a build → replying to the existing list.

Use the existing screenshots as a reliable path. Live navigation is optional.
The “patches with no replies” query identifies candidate threads; it doesn't
prove nobody responded elsewhere or establish which patches Jack can review.

The existing screenshots were recorded in September 2026. Treat displayed counts
and statuses as snapshots, not current measurements. Refresh anything that needs
to be described as current.

## AI summaries and future work

The summaries run locally. Bug fixes and quality evaluation are ongoing.
The draft claims neither a public release nor an established accuracy level.

Use the extra time for a concrete demonstration:

* About one minute: connect the remaining reading problem to summaries.
* About two minutes: show the working local UI.
* About two minutes: walk through a useful output excerpt.
* About three minutes: compare one claim with the original discussion.
* About one minute: invite feedback from people who know a thread well.

Kai's other ideas stay together on one slide: contributor profiles, bug/feature
tracking, and topic grouping. They are possibilities for discussion, not promises.

## Rehearsal and publication checks

* Replace the three AI screenshot placeholders and rehearse the actual example.
* Confirm the planned Community Day session before promising its time or location.
* The old follow-along QR linked to Kai's published deck. That slide is omitted
  from the solo draft until the revised deck has a confirmed public destination.
  The persistent corner QR still links to Hackorum.
* Use screenshot dates when discussing metrics, including backup slides.
* Keep the incident and its resolution under two minutes on the database-problem slide.
* If running long, shorten the contributor CI/build detail before cutting the
  summary example that gives this talk its personal conclusion.
* Questions outside Jack's implementation experience can be taken back to the team.

## Backup material

Detailed views, architecture, identity resolution, search syntax, profiles, team
notes, reports, mobile views, community feedback, and the old recorded walkthrough
remain available after Q&A. They are optional reference material.

`img/hackorum-walkthrough.webm` is the existing 91-second recording. Its speaker
notes retain the beat sheet. If using it, substitute it for part of the walkthrough
instead of adding another tour. Rehearse playback in the presenting browser.

The patch-image command is also in backup. Verify the image and connection
settings before demonstrating it live.

## Deck conventions and asset provenance

* `##` marks slide headings, `---` horizontal slides, and `--` vertical slides.
* `Note:` separates speaker notes from projected content.
* Reusable styling is in the opening `<style>` block.
* The canvas remains 1920×1080, with `maxScale: 1`.
* Existing `img/hk-*.png` assets were captured against Hackorum in September 2026.
* `img/mailclient-thread.png`, if reused later, is a rendering based on real
  messages, not Jack's literal mail-client screenshot.
* Kai's unread-inbox image is not used as evidence of Jack's experience.
* The original conference deck and its useful screenshots are the source material
  for this solo revision; Kai's separate 2022 autobiographical sequence is omitted.
