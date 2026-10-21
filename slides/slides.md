<style>
.highlight-box {
  border: 2px solid #653df4;
  background: rgba(101, 61, 244, 0.10);
  padding: 18px;
  border-radius: 10px;
  margin-top: 14px;
}

.warning-box {
  border: 2px solid #ff4444;
  background: rgba(255, 68, 68, 0.15);
  padding: 18px;
  border-radius: 10px;
  margin-top: 14px;
}

.title-slide h2 {
  max-width: none;
  line-height: 1.1;
}

.speakers {
  color: #653df4;
  font-weight: 700;
  font-size: 1.05em;
  margin-top: 1.5em;
}

.speakers .org {
  color: #8a8a95;
  font-weight: 400;
  font-size: 0.78em;
}

.venue {
  font-size: 0.66em;
  color: #6b6b75;
  margin-top: 0.3em;
}

/* keep headings clear of the QR code in the top-right corner */
.reveal h1,
.reveal h2,
.reveal h3 {
  max-width: 1450px;
  margin-left: auto;
  margin-right: auto;
}

.cols {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 50px;
}

.cols ul {
  text-align: left;
}

.reveal .team-intro {
  color: #000;
  font-weight: 400;
}

.participation-spectrum {
  width: 90%;
  margin: 0 auto;
  padding: 60px 0;
}

.spectrum-labels {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  gap: 80px;
}

.reveal .spectrum-labels h3 {
  margin: 0;
  font-size: 1.3em;
  text-align: left;
}

.reveal .spectrum-labels h3:last-child {
  text-align: right;
}

.spectrum-line {
  position: relative;
  height: 8px;
  margin: 45px 15px 55px;
  border-radius: 4px;
  background: linear-gradient(90deg, #c4b5fd, #653df4);
}

.spectrum-line::before,
.spectrum-line::after {
  content: "";
  position: absolute;
  top: 50%;
  width: 26px;
  height: 26px;
  border-radius: 50%;
  transform: translateY(-50%);
}

.spectrum-line::before {
  left: -13px;
  background: #c4b5fd;
}

.spectrum-line::after {
  right: -13px;
  background: #653df4;
}

.spectrum-details {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 100px;
}

.reveal .spectrum-details ul {
  display: block;
  margin: 0;
  padding-left: 1.1em;
  font-size: 0.82em;
  text-align: left;
}

.spectrum-details ul:last-child {
  justify-self: end;
}

.spectrum-details li + li {
  margin-top: 0.4em;
}

.reveal .slides section.walkthrough-feature {
  box-sizing: border-box;
  height: 1080px;
  padding-top: 110px;
}

.feature-spectrum {
  position: absolute;
  top: 20px;
  left: 20px;
  width: 300px;
  font-size: 24px;
  line-height: 1.2;
  color: #51466f;
}

.feature-spectrum-labels {
  display: flex;
  justify-content: space-between;
}

.feature-spectrum-track {
  position: relative;
  height: 5px;
  margin: 16px 8px 0;
  border-radius: 3px;
  background: linear-gradient(90deg, #c4b5fd, #653df4);
}

.feature-spectrum-track::after {
  content: "";
  position: absolute;
  left: var(--spectrum-position);
  top: 50%;
  width: 16px;
  height: 16px;
  border: 3px solid #fff;
  border-radius: 50%;
  background: #653df4;
  box-shadow: 0 0 0 2px #653df4;
  transform: translate(-50%, -50%);
}

.team-portraits {
  display: flex;
  justify-content: center;
  gap: 100px;
  margin-top: 35px;
}

.team-portraits figure {
  margin: 0;
  text-align: center;
}

.reveal .team-portraits img {
  display: block;
  width: 250px;
  height: 250px;
  margin: 0 auto 15px;
  object-fit: cover;
  border: none;
  border-radius: 50%;
  box-shadow: 0 5px 18px rgba(0, 0, 0, 0.12);
}

.team-portraits figcaption {
  font-size: 0.7em;
}

.image-with-notes {
  display: grid;
  grid-template-columns: minmax(0, 3fr) minmax(0, 2fr);
  align-items: center;
  gap: 60px;
}

.reveal .image-with-notes > img {
  display: block;
  width: auto;
  height: auto;
  max-width: 100%;
  max-height: 620px;
  justify-self: center;
  object-fit: contain;
  margin: 0;
  background: none;
  border: none;
  box-shadow: none;
}

.reveal .image-with-notes > ul {
  display: block;
  margin: 0 0 0 1em;
  text-align: left;
}

.image-with-notes li + li {
  margin-top: 0.5em;
}

.reveal img.screenshot-shadow {
  border-radius: 8px;
  box-shadow: 0 8px 28px rgba(0, 0, 0, 0.16);
}

.reveal img.feedback-qr {
  width: 555px;
  height: 555px;
  padding: 60px;
  background: #fff;
  border: none;
  box-shadow: none;
  image-rendering: pixelated;
}

.questions-layout {
  display: grid;
  grid-template-columns: minmax(0, 1fr) 740px;
  align-items: center;
  gap: 60px;
}

.reveal .questions-feedback {
  margin: 0;
  padding-left: 40px;
  border-left: 2px solid #d4d4d8;
}

.reveal .questions-feedback .feedback-qr {
  display: block;
  margin: 0 auto;
}

.questions-feedback figcaption {
  font-size: 0.7em;
  line-height: 1.5;
}

.reveal-viewport.feedback-only,
.reveal-viewport.hide-corner-qr {
  background-image: none;
}

.reveal img.summary-screenshot {
  display: block;
  width: auto;
  height: auto;
  max-width: 100%;
  max-height: 580px;
  margin: 30px auto;
  border: none;
}

.reveal img.summary-excerpt {
  width: 100%;
}

.reveal img.summary-full {
  max-height: 700px;
}

.summary-example > * {
  flex: 1;
  min-width: 0;
}

.summary-example ul {
  font-size: 0.9em;
}

.table {
  font-size: 0.7em;
}

.table table {
  width: 94%;
  margin: 0 auto;
  table-layout: fixed;
}

.table th,
.table td {
  padding: 10px 12px;
  vertical-align: top;
  word-break: break-word;
}

.incident-stats {
  display: flex;
  justify-content: center;
  gap: 130px;
  margin: 55px 0;
}
.incident-stats > div {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.incident-stats strong {
  color: #653df4;
  font-size: 2.8em;
}
.incident-stats span {
  font-size: 0.7em;
}
</style>

<!-- .slide: id="start" class="title-slide" -->

## Finally a Postgres<br>Communication Hub

### for Experts and Newcomers

<p class="speakers">Jack Bonatakis<br><span class="org">Robin</span></p>
<p class="venue">PGConf.EU 2026 · Valencia · October 22nd · Audit 2</p>

Note:

* **Opening and Robin story: seven minutes through “The next morning”.** Good morning. I'm Jack.
* This is already a pretty long title. So I might as well make it longer.
* **Advance to the subtitle, then pause.**
---

<!-- .slide: id="subtitle" class="title-slide" -->

## Or, So you wanna be a Postgres Hacker?

Note:

* **About 30 seconds, within the opening allocation.** Let the subtitle land before continuing.
* Kai was originally going to present this with me, but unfortunately he couldn't make it. So the perspective of the talk has shifted a bit.
* I'm coming at this as someone who uses Postgres, got curious about how it's built, and wanted to find a way into those conversations.
* That's the story I'll tell today: how I got here, what made it hard to follow along, and what we're building to make it easier.
---

## I'm Jack

* **Principal Engineer at Robin**
* A Postgres user who got curious about how Postgres gets *built*

Note:

* I came to this as someone using Postgres to build a product. I wanted to understand more about what was happening underneath it.
* I'm still learning my way around the development community. That's the perspective I'm bringing today.
* Who here uses Postgres in their day job? And who follows its development on the mailing lists? Pause for the hands; don't assume what the room will do.
* First, the problem at Robin that sent me looking.
---

## It started with a database problem

* Terabytes of added storage, all WAL
* The system was running inefficiently
* Storage kept growing
* We hadn't yet found what was holding it there

Note:

* Our system at Robin was running very inefficiently, and Cloud SQL kept automatically adding storage.
* We had added terabytes of storage for retained WAL: PostgreSQL's write-ahead log.
* At that point we didn't know about the replication slots that turned out to be behind it.
* **Delivery:** Keep the incident and its resolution to about two minutes on this slide. Leave exact capacity and percentages out of the presentation.
* Replication slots keep track of data a consumer may still need. They can cause PostgreSQL to retain WAL while waiting for that consumer.
* I eventually found stale slots we hadn't known about. Dropping those slots resolved the problems we were seeing.
* The storage aftermath remained. Cloud SQL had automatically grown the disk, and resolving the WAL retention didn't automatically reduce that provisioned capacity.
* This is the account of our incident, not a recommendation to drop arbitrary slots. I don't need to take the audience through SQL commands here.
* The investigation got me curious about how Postgres works and how it gets developed.
* **Technical reference:** [PostgreSQL replication slots and WAL retention](https://www.postgresql.org/docs/current/warm-standby.html#STREAMING-REPLICATION-SLOTS).
* **Wording reference:** [Cloud SQL automatic storage increases](https://docs.cloud.google.com/sql/docs/postgres/instance-settings). Keep the claim about automatic shrinking and our incident: Google also documents a separate [storage shrink operation](https://docs.cloud.google.com/sql/docs/postgres/shrink-instance-storage-capacity).
---

## That curiosity led to the mailing lists

* I wanted to understand more about Postgres
* That led me to the conversations where development happens
* So I subscribed to a few mailing lists

<p style="margin-top:45px;"><em>It seemed like a reasonable next step…</em></p>

Note:

* Following that investigation, I wanted to understand more about the database we depended on and the people developing it.
* That led me to the Postgres mailing lists. I subscribed because I wanted to learn from those conversations.
* I wasn't planning to build a mailing-list reader. I was trying to follow along.
* **Keep the chronology honest:** Don't claim the lists diagnosed the Robin incident or that I posted a patch or question there; those aren't part of this story.
---

## The next morning

<div class="image-with-notes">

<img class="screenshot-shadow" src="img/mailing-list-overnight.png" alt="Jack's inbox showing technical Postgres mailing-list emails received overnight" data-preview-image>

* **50+ deeply technical emails** waiting in my inbox
* Try to understand them one by one, while more arrive
* Or ignore them, and lose the reason I subscribed

</div>

Note:

* This is the experience that made the problem concrete for me: waking up to fifty-plus deeply technical emails.
* Each one might be interesting, but understanding it can require reading the previous messages, looking up the proposal, and figuring out what the disagreement is about.
* Meanwhile, new emails keep arriving. I can spend my available time reading them one by one, or ignore them and fall further behind.
* I wanted to follow Postgres development, but I didn't want every conversation to become another item to process in my inbox.
* **Screenshot:** My actual overnight inbox. Point to the arrival times and the technical subjects to make the volume concrete.
---

## There has to be a better way

* Keep the mailing-list traffic **out of my inbox**
* Open a conversation when I have time to follow it
* Make the flow of messages easier to navigate

Note:

* **Joining forces: five minutes through meeting Kai and Zsolt.**
* I wanted a dedicated place for this reading. Somewhere I could go when I had the time and attention, without the messages piling up alongside my work email.
* The conversations themselves were valuable. I wanted an easier way to follow them.
* My response was to build a tool for it.
---

## pginbox

<div class="cols">

<img src="img/pginbox-overnight.png" class="screenshot-shadow" alt="pginbox listing overnight Postgres discussions with mailing lists, activity times and message counts" data-preview-image style="height:700px; width:auto; flex-shrink:0; background:none; border:none;">

* A dedicated reader for the Postgres mailing lists
* The conversations I wanted to follow, outside my personal inbox

</div>

Note:

* This was pginbox. It was my attempt to make that experience work for me.
* **With the screenshot (~90 seconds):** Point to the conversation list, activity times and message counts. The same subjects from the inbox are here, grouped as discussions. Explain how I would choose a topic to read, rather than processing every incoming message in my inbox.
* Stick to what the screenshot actually shows. The point is the reading experience and why I built it, not a full tour of a second product.
* While I was doing this, other people were working on the same problem.
---

## Then I connected with Kai and Zsolt

* <span class="team-intro"><strong>Kai Wagner</strong> and <strong>Zsolt Parragi</strong> were building <strong>Hackorum</strong></span>
* We compared what we'd built and where we wanted to go
* Same problem, same community
* We decided to **sunset pginbox and build Hackorum together**

<div class="team-portraits">
  <figure>
    <img src="img/kai-wagner.jpg" alt="Kai Wagner">
    <figcaption>Kai Wagner</figcaption>
  </figure>
  <figure>
    <img src="img/zsolt-parragi.png" alt="Zsolt Parragi">
    <figcaption>Zsolt Parragi</figcaption>
  </figure>
</div>

Note:

* I hadn't known they were already working on the same problem. Kai, Zsolt and I got on a call and compared the projects.
* We were trying to help the same people follow the same conversations. It made sense to put our effort into one project.
* We decided to sunset pginbox, and I joined their team.
* Credit to Kai and Zsolt for the work that was already there, especially Zsolt for building the reader. I'm presenting work from the team today; the summaries later in the talk are the part I'm currently building.
* **Reference, not spoken:** [The projects join forces](https://percona.community/blog/2026/05/13/two-projects-one-mission-hackorum-and-pginbox-join-forces/).
* **Photo sources, not spoken:** Public GitHub profile photos for [Kai](https://github.com/ImTheKai) and [Zsolt](https://github.com/dutow).
---

<!-- .slide: id="walkthrough" -->

<div class="participation-spectrum" role="group" aria-label="A spectrum from using Postgres to contributing to Postgres">
  <div class="spectrum-labels">
    <h3>I use Postgres</h3>
    <h3>I contribute to Postgres</h3>
  </div>
  <div class="spectrum-line" aria-hidden="true"></div>
  <div class="spectrum-details">
    <ul>
      <li>Find a relevant discussion</li>
      <li>Understand its context</li>
      <li>Keep up without filling my inbox</li>
    </ul>
    <ul>
      <li>Find work that needs attention</li>
      <li>Follow patches and test results</li>
      <li>Try a change and join the discussion</li>
    </ul>
  </div>
</div>

Note:

* **Walkthrough: twelve minutes across this section; about six per perspective.**
* Think of this as a spectrum. You can move along it, and you can be both a user and a contributor. Someone using Postgres may have exactly the test case or operational experience a contributor needs.
* First I'll look at it as a user trying to understand a conversation. Then I'll follow the tools that help someone contribute.
* Use the existing screenshots as the reliable walkthrough. A live view is optional; don't spend the whole slot touring menus.
---

<!-- .slide: id="hackorum" -->

## Hackorum

<img class="screenshot-shadow" src="img/hk-landing.png" data-preview-image style="height:690px; width:auto; background:none; border:none;">

[hackorum.dev](https://hackorum.dev)

Note:

* **Delivery cue: the project name is spoken only here. The title and URL remain on screen.**
* And that brings me to Hackorum.
* It's a conversation-oriented interface to the Postgres mailing lists.
* The mailing-list discussions are still the underlying conversations. The reader gives you a place to browse and follow them.
* Point to the list of topics. Each row is a conversation, with information about its activity and state.
* Let's start with finding a discussion as a Postgres user.
---

<!-- .slide: class="walkthrough-feature" -->

<div class="feature-spectrum" style="--spectrum-position:15%;" role="img" aria-label="User to hacker spectrum: closer to the user end">
  <div class="feature-spectrum-labels" aria-hidden="true"><span>User</span><span>Hacker</span></div>
  <div class="feature-spectrum-track" aria-hidden="true"></div>
</div>

## Find a conversation worth following

<div class="image-with-notes">

<img class="screenshot-shadow" src="img/hk-search.png" data-preview-image>

* Search for a subject, person, or patch
* Narrow the results and save a useful search

</div>

Note:

* **User path, step 1:** Start with something you care about. It might be a feature you depend on or a change you want to understand.
* This screenshot shows the search interface. Point out the filters and a result; explain how they help narrow the reading.
* The advanced query syntax is in backup if somebody wants the details. The goal in this walkthrough is to find a relevant conversation.
* Open the index-prefetching example next. It's an existing example in this deck, not the thread that diagnosed the Robin incident.
---

<!-- .slide: class="walkthrough-feature" -->

<div class="feature-spectrum" style="--spectrum-position:25%;" role="img" aria-label="User to hacker spectrum: closer to the user end">
  <div class="feature-spectrum-labels" aria-hidden="true"><span>User</span><span>Hacker</span></div>
  <div class="feature-spectrum-track" aria-hidden="true"></div>
</div>

## Read it as a conversation

<img class="screenshot-shadow" src="img/hk-thread.png" data-preview-image style="height:700px; width:auto; background:none; border:none;">

Note:

* **User path, step 2:** Here is a topic. The discussion and its related information are together on one page.
* Start with the title and the messages. This is the actual conversation people had on the mailing list.
* The screenshot is of index prefetching, a long-running discussion. I don't need to be an expert on that patch to see the reading problem: there's a lot of history here.
* The sidebar also contains patch and review information. I'll return to that from the contributor perspective.
---

<!-- .slide: class="walkthrough-feature" -->

<div class="feature-spectrum" style="--spectrum-position:35%;" role="img" aria-label="User to hacker spectrum: between the user end and the middle">
  <div class="feature-spectrum-labels" aria-hidden="true"><span>User</span><span>Hacker</span></div>
  <div class="feature-spectrum-track" aria-hidden="true"></div>
</div>

## Follow the branches of the discussion

<div class="cols">

<img class="screenshot-shadow" src="img/hk-thread-outline.png" data-preview-image style="height:600px; width:auto; flex-shrink:0; background:none; border:none;">

* Colour-coded reply branches, reconstructed from `In-Reply-To`
* *"#5...#20 to Tomas Vondra (#1)"* - a sub-debate you can read or skip as a unit
* Collapse what you don't care about, jump straight to any message

</div>

Note:

* **User path, step 3:** Long discussions split. An objection can produce its own branch while other parts of the conversation continue.
* The outline reconstructs those reply relationships. Point to one branch and show where its messages sit.
* This gives me a way to focus my reading and return to the main conversation, rather than treating every message as an unrelated email.
* It still takes reading to understand the argument. Remember that distinction; it is what the summary work later in the talk addresses.
---

<!-- .slide: class="walkthrough-feature" -->

<div class="feature-spectrum" style="--spectrum-position:35%;" role="img" aria-label="User to hacker spectrum: between the user end and the middle">
  <div class="feature-spectrum-labels" aria-hidden="true"><span>User</span><span>Hacker</span></div>
  <div class="feature-spectrum-track" aria-hidden="true"></div>
</div>

## Come back when you have time

* **Per-message** read tracking - not per-thread
* Come back in three weeks, pick up at exactly the right message
* "Jump to unread" &middot; "Mark all read" &middot; "Collapse all"
* **Ignore a thread** so it stops shouting at you

Note:

* **User path, step 4:** Being able to leave is part of a useful reading experience.
* Per-message read state means I can come back to where I stopped in a long thread. I can jump to unread messages or ignore a topic I no longer want to follow.
* That gets back to why I built pginbox: I want to choose when to read these discussions, without a queue growing in my personal inbox.
* Now change perspectives. Suppose I've found something I can help with.
---

<!-- .slide: class="walkthrough-feature" -->

<div class="feature-spectrum" style="--spectrum-position:60%;" role="img" aria-label="User to hacker spectrum: just toward the hacker end of the middle">
  <div class="feature-spectrum-labels" aria-hidden="true"><span>User</span><span>Hacker</span></div>
  <div class="feature-spectrum-track" aria-hidden="true"></div>
</div>

## Find a place to contribute

```text
has:patch messages:1 first_after:6m
```

<div class="image-with-notes">

<img class="screenshot-shadow" src="img/hk-newcomer.png" data-preview-image>

* Patch threads with no replies: a concrete place to look

</div>

Note:

* **Contributor path, step 1:** This query looks for a patch, one message, and a thread started within the last six months.
* One message means no reply in that thread. It gives me a specific set of conversations to look at rather than an undifferentiated inbox.
* It doesn't tell me whether I have the expertise to review each patch, or whether discussion happened somewhere else. I still need to read and judge where I can help.
* The screenshot is a captured example. Don't quote its counts as current measurements.
---

<!-- .slide: class="walkthrough-feature" -->

<div class="feature-spectrum" style="--spectrum-position:75%;" role="img" aria-label="User to hacker spectrum: closer to the hacker end">
  <div class="feature-spectrum-labels" aria-hidden="true"><span>User</span><span>Hacker</span></div>
  <div class="feature-spectrum-track" aria-hidden="true"></div>
</div>

## Follow the patch as it changes

<div class="cols">

<img class="screenshot-shadow" src="img/hk-patchsets.png" data-preview-image style="height:600px; width:auto; background:none; border:none;">

* **Daily** sync with **commitfest.postgresql.org**, status inline
* Commitfest tags, reviewer and committer attribution
* Every **patchset version** in the thread, with diffstat and one-click download

</div>

Note:

* **Contributor path, step 2:** Once I pick a topic, I want to know which version of the patch I'm looking at and what is happening with review.
* Show the patchset versions and the commitfest information together. A long conversation can contain several attempts at a solution.
* Being able to see that history helps me avoid testing an old version by mistake.
* This brings the relevant context together before I start working on the change.
---

<!-- .slide: class="walkthrough-feature" -->

<div class="feature-spectrum" style="--spectrum-position:80%;" role="img" aria-label="User to hacker spectrum: closer to the hacker end">
  <div class="feature-spectrum-labels" aria-hidden="true"><span>User</span><span>Hacker</span></div>
  <div class="feature-spectrum-track" aria-hidden="true"></div>
</div>

## Check the build and test results

<img class="screenshot-shadow" src="img/hk-ci-dashboard.png" data-preview-image style="height:700px; width:auto; background:none; border:none;">

Note:

* **Contributor path, step 3:** The project also has patch CI. The dashboard shows build and test states.
* Point to a status and explain what it tells a reader to investigate: application problems, a required rebase, or failing tests.
* This is the project's own CI, marked beta in the existing deck. It has a different scope from the commitfest tooling; it doesn't remove the need for review.
* The screenshot is an earlier snapshot. Avoid presenting its run counts as live activity.
* The useful next step is getting from a conversation to something you can actually try.
---

<!-- .slide: class="walkthrough-feature" -->

<div class="feature-spectrum" style="--spectrum-position:85%;" role="img" aria-label="User to hacker spectrum: closer to the hacker end">
  <div class="feature-spectrum-labels" aria-hidden="true"><span>User</span><span>Hacker</span></div>
  <div class="feature-spectrum-track" aria-hidden="true"></div>
</div>

## Try somebody's patch

<div class="image-with-notes">

<img class="screenshot-shadow" src="img/hackorum-build.png" alt="Hackorum patch CI panel with Docker and Git commands for trying a patch build" data-preview-image>

* A patch build you can run
* Bring observations back to the same discussion

</div>

Note:

* **Contributor path, step 4:** The CI panel includes a command for running a Postgres image built from the patch.
* Point to it in the screenshot. This can help someone try a change without first putting together the whole build themselves.
* A Postgres user may have a workload or reproduction that is useful here, even if they're not ready to review the code.
* A command example is in backup. Only demonstrate it live if I've checked the image and prepared the environment before the talk.
---

<!-- .slide: class="walkthrough-feature" -->

<div class="feature-spectrum" style="--spectrum-position:90%;" role="img" aria-label="User to hacker spectrum: closer to the hacker end">
  <div class="feature-spectrum-labels" aria-hidden="true"><span>User</span><span>Hacker</span></div>
  <div class="feature-spectrum-track" aria-hidden="true"></div>
</div>

## Reply to the list, from Hackorum

<img class="screenshot-shadow" src="img/hk-composer.png" data-preview-image style="height:700px; width:auto; background:none; border:none;">

Note:

* **Contributor path, step 5:** I can write a reply from the interface and send it to the mailing list.
* Point to the composer. Your reply joins the existing mailing-list conversation.
* The goal is a path from finding a topic, through understanding and trying it, to giving useful feedback.
* Those are the two perspectives: keeping up as a user, and moving the work forward as a contributor. Often they're the same person.
---

<!-- .slide: id="ai-summaries" -->

## I can navigate it. Can I catch up?

> “500 messages. What happened, what was decided, what is still open?”

* An outline shows **where the conversation branches**
* Read state shows **where I left off**
* I still need **enough context to join in**

Note:

* **AI summaries: nine minutes, including showing and discussing a real example.**
* This is where the reading problem comes back. The interface makes the conversation easier to navigate, but I can still arrive at a topic with hundreds of messages and no idea what happened.
* The outline gives me structure. It doesn't by itself explain the proposal, the objections, or what is unresolved.
* That's the part I'm working on now: automatic AI topic summaries.
* This is the transition from existing features to work running in my local environment.
---

## In progress: AI topic summaries

<p class="venue">Running locally · Bug fixes and quality evaluation in progress</p>

<p style="font-size:0.7em;"><strong>Topic:</strong> <a href="https://hackorum.dev/topics/52309" target="_blank" rel="noopener noreferrer">Introduce XID age based replication slot invalidation</a></p>

<img class="screenshot-shadow summary-screenshot summary-full" src="img/hackorum-summary.png" alt="AI topic summary of a discussion about invalidating stale replication slots, with message references" data-preview-image>

Note:

* **About two minutes:** This works locally today. I'm working through bugs and trying to decide where the line of “good enough” is.
* This example summarizes a discussion about invalidating stale replication slots based on transaction-ID age. Introduce it as a different thread from the earlier walkthrough.
* Explain what the topic is about, then show where the summary lives and what a reader sees.
* Pick one useful piece of context in the actual output. Explain what it helps you understand or which part of the conversation it helps you read next.
* Don't imply the feature is deployed, or promise behaviour that isn't present in the local build.
---

## One summary, one real discussion

<img class="screenshot-shadow summary-screenshot summary-excerpt" src="img/overview.png" alt="Summary overview describing the replication-slot invalidation proposal and its revisions, with references to original messages" data-preview-image>

Note:

* **About two minutes:** Stay with the same thread. Show a short excerpt at a size the room can read.
* Give enough background to interpret it. Then walk through what this particular output gets across: the proposal, a disagreement, or something still unresolved.
* Explain the next reading step it suggests. This is the practical value: helping me choose where to spend my attention.
* Point out the overview and its message references. Explain which original message you would read next to check or explore the proposal.
---

## Did we get it right?

<img class="screenshot-shadow summary-screenshot summary-excerpt" src="img/concern.png" alt="Summary excerpt describing a concern about choosing an XID-based cutoff, with references to messages 19 and 20" data-preview-image>

* Does it preserve **disagreement and uncertainty**?
* Does it distinguish a **proposal from a decision**?
* Can a reader **check it against the discussion**?

> What would you need to trust it to get you oriented?
<!-- .element: class="highlight-box" -->

Note:

* **About three minutes, including a pause for the audience to read the example.**
* A summary can sound convincing and still leave someone with the wrong understanding. A suggestion can turn into an apparent decision; one person's objection can sound like a community consensus.
* The excerpt describes a concern about choosing an XID-based cutoff and cites messages 19 and 20. Use those source messages when evaluating whether it represents the discussion fairly; the excerpt alone doesn't establish accuracy.
* Work through one concrete judgment: what is captured accurately, what is missing, and what I would want to change. A nuanced example is enough; don't manufacture a failure.
* These questions are my evaluation criteria, not claims that every generated summary already meets them.
* Clearly identifying generated content and letting people verify it against the discussion matter to the reading experience.
---

## Help me judge it against a thread you know

* What important context did it miss?
* Did it represent the participants fairly?
* Would it help someone new enter the conversation?

> Bring a thread you know well. Let's compare.

Note:

* **About one minute:** The best feedback here comes from somebody who understands the original discussion.
* I'm interested in whether it helps a new reader get oriented while preserving the details that matter to participants.
* If you have a thread in mind, come find me after the talk. We can compare the output with your understanding of it.
* That's the feature I'm actively working on. There are also broader ideas the team wants community input on.
---

<!-- .slide: id="whats-next" -->

## Other directions we want to explore

* **Contributor profiles:** connect community contribution data
* **Bug and feature tracking:** follow state across a discussion
* **Topic grouping:** connect related threads over time

> Who maintains the information, and how should the community shape it?

Note:

* **Other directions and invitation: five minutes across this slide and the next.**
* These are the other ideas Kai had in the original talk. They remain possibilities for discussion, not a release commitment.
* Contributor profiles: how can the data we already collect support the community's work on recognising contributions?
* Bug and feature tracking: a thread can contain a report, discussion and a fix. Making its state useful raises questions about who maintains it.
* Topic grouping: a larger project can span several threads with different titles over years. Connecting them could help people understand the whole effort.
* Give each idea a short example, then focus on the shared question: how do we make this useful without creating another queue of maintenance work for the same busy contributors?
---

<!-- .slide: data-state="hide-corner-qr" data-background-color="#ffffff" -->

## Follow a conversation. Tell us what gets in the way.

* **Use it:** [hackorum.dev](https://hackorum.dev)
* **Code and issues:** [github.com/hackorum-dev/hackorum](https://github.com/hackorum-dev/hackorum)
* **AI summaries:** bring a thread you know well
* **Community Day:** continue the discussion on Friday

<img src="img/hackorum-qrcode.png" data-preview-image style="height:260px; width:auto; background:none; border:none; box-shadow:none;">

Note:

* My route here started with stale replication slots at Robin. Understanding our database got me interested in the conversations behind it.
* pginbox was my first attempt to make those conversations easier to follow. Now I'm working with the team on that same problem.
* Try following a topic you care about. Tell us where the interface helps and where you still get stuck.
* If you contribute to Postgres, I'd especially like to know whether these tools help people arrive with better context.
* The existing plan includes a discussion about the project at Community Day on Friday. Confirm the session details before presenting; don't invent a time or room.
* Thank you. I'm happy to take questions.
---

<!-- .slide: id="questions" data-state="feedback-only" data-background-color="#ffffff" -->

## Questions?

<div class="questions-layout">

<div>

### Jack Bonatakis

[hackorum.dev](https://hackorum.dev)

[github.com/hackorum-dev/hackorum](https://github.com/hackorum-dev/hackorum)

<p style="font-size:0.7em; line-height:1.5; margin-top:40px;">Thanks to <strong>Kai</strong> for inviting me to join this talk, <strong>Zsolt</strong> for all his great work on Hackorum, and the whole <strong>Percona team</strong> for their support.</p>

</div>

<figure class="questions-feedback">
  <img src="img/talk-feedback-qr.png" class="feedback-qr" alt="QR code for feedback on this talk">
  <figcaption><strong>How was the talk?</strong><br>Scan to leave feedback.</figcaption>
</figure>

</div>

Note:

* **Twelve minutes reserved for Q&A and timing buffer.** The prepared sections target thirty-eight minutes.
* Answer from my own experience. For implementation details outside my work, say what I know and take the remaining question back to the team.
* Invite the audience to scan the QR code and leave feedback while taking questions.
* The backup slides have deeper product views and the recorded walkthrough. They are optional, not another section to present.
---

<div id="backup-slides"></div>

# Backup slides :-)

Note:

* Everything past here is for a question that deserves a picture.
---

## Backup: the topic index, in detail

<img class="screenshot-shadow" src="img/hk-landing.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* The icons under each title, left to right: notes on this topic with a count, commitfest entry, attachment, patch submission, CI state, unread count.
* The coloured bar down the left of each row is your personal read state. New, partially read, fully read.
--

## Backup: a thread, in detail

<img class="screenshot-shadow" src="img/hk-thread-big.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Index prefetching, five hundred and four messages.
* Note the commits panel in the left rail. This thread has already produced several commits on master and on REL_19_STABLE, each one shown with its branch badges.
--

## Backup: per-topic CI history

<img class="screenshot-shadow" src="img/hk-ci-topic.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Per patchset: the base commit we picked, when it was applied, when it was last rebased, where it was pushed, and every CI run against it.
* A line like "v23, superseded, stale ten months, pg 19" tells you at a glance that an old version was tested against a Postgres generation that no longer matters.
--

## Backup: CI is an infrastructure problem

Building **every patch on the list** is not a feature, it's a fleet.

* Rebase every patchset every time master moves
* Per-major-version build images ("eras")
* An orchestrator deciding what is worth building next
* 11,397 runs in 7 days &middot; 84.4% success &middot; median build 2m50s

Note:

* Just running CI on the patches sounds like a weekend project. It is not.
* The hard part is not building a patch. The hard part is deciding, continuously, which of six thousand patchsets are worth a runner right now, because master moves and every patchset silently rots.
* Credit Zsolt for this work. Detailed scheduling and infrastructure questions may need a follow-up with him.
--

## Backup: CI statistics

<img class="screenshot-shadow" src="img/hk-ci-stats.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Success rate, median build and test time, queue wait, infrastructure errors.
* The corpus tab does something slightly mad. It lays today's patchsets out over PostgreSQL's history to ask how far behind the average patch actually is.
--

## Backup: teams

<img class="screenshot-shadow" src="img/hk-teams-settings.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Create a team, invite members, set it private, public or open, and share saved searches across the team.
--

## Backup: a team profile

<img class="screenshot-shadow" src="img/hk-team.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* A team gets an aggregate profile. Combined messages, patches, commit credits by role, and the patch threads that landed rate.
* The figures belong to the captured team profile. Treat them as a historical snapshot; they do not by themselves establish why rates differ.
--

## Backup: notifications

<img class="screenshot-shadow" src="img/hk-activities.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Activity feed for mentions, for replies on threads you participate in, and for team events.
--

## Backup: drafts and sent mail

<img class="screenshot-shadow" src="img/hk-drafts.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Every outgoing message has a state. Draft, sending, pending, sent, failed.
* Pending means the mail was accepted but the list has not echoed it back yet. We do not claim success until we have seen the message arrive on the list like everybody else's.
* Drafts stuck in sending for more than ten minutes get reset automatically.
--

## Backup: the help pages

<img class="screenshot-shadow" src="img/hk-help.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Search syntax and account linking.
* The search guide is worth reading even if you never use the reader. It is a decent taxonomy of the questions you might want to ask a mailing list.
---

## Backup: under the hood

```
+----------------------------------------------+
|  Rails 8 - Ruby 3.4 - Hotwire/Turbo - Slim   |
|  Propshaft - ImportMap - Stimulus            |
+----------------------------------------------+
|  PostgreSQL 18  (primary + side DBs)         |
|  Solid Queue  -  Solid Cache  -  Solid Cable |
+----------------------------------------------+
|  IMAP / own mailserver -> EmailIngestor -> PG|
|  Commitfest poller -> PG                     |
|  git history importer -> PG                  |
|  Patch CI orchestrator -> GitHub Actions     |
+----------------------------------------------+
|  Docker Compose - Caddy - PgHero             |
+----------------------------------------------+
```

**No Redis. No Elasticsearch. No Sidekiq. It's Postgres all the way down.**

Note:

* This is the architecture documented in the original deck. Rails supplies the application framework, with Postgres-backed services.
* Full-text search is Postgres. The job queue is Postgres. The cache is Postgres.
* We run our own mail server for list ingestion rather than depending on an IMAP label in a Gmail account, which was exactly as fragile as it sounds.
---

## Backup: identity resolution

```ruby
# kai@example.com  +
# kai.wagner@percona.com  +--> Person #42 (Kai Wagner) - tier: contributor
# kaiwo@github.com  +

# PersonIdPropagationJob: runs when an alias -> person mapping changes
class PersonIdPropagationJob < ApplicationJob
  def perform(person_id, old_person_id)
    ActiveRecord::Base.transaction do
      Message.where(sender_person_id: old_person_id)
             .update_all(sender_person_id: person_id)
      TopicParticipant.where(person_id: old_person_id)
                      .update_all(person_id: person_id)
      Person.find(old_person_id).destroy if old_person_id
    end
  end
end
```

* One person, many aliases - merged atomically in a background job
* Feeds tiers, search filters, stats and commit credits
* Admins can preview a merge before committing to it

Note:

* A preview lets an administrator inspect the proposed identity merge before committing it.
---

## Backup: why not just a forum?

<div class="table">

| | Mailing list | Forum (Discourse) | Hackorum |
|---|---|---|---|
| Source of truth | Email | The forum DB | **Email** |
| If the UI disappears | Email remains | Depends on archive / backups | **Mailing-list archive remains** |
| Offline / your client | yes | no | **yes (still email)** |
| Threading UI | no | yes | yes |
| Search | weak | yes | yes |
| Vendor neutral | yes | depends | yes |

</div>

Note:

* The row that matters is the second one.
* A forum stores its conversations in its own database, so preservation depends on how that service and its backups are operated.
* If this interface goes away tomorrow, the mailing-list archive remains, and everybody's mail client keeps working exactly as it did.
* That asymmetry is the entire design.
---

## Backup: Advanced search

<img class="screenshot-shadow" src="img/hk-search.png" data-preview-image style="height:600px; width:auto; background:none; border:none;">

```
from:andres[messages:>=10] has:patch
```

Note:

* The dependent-condition example distinguishes messages from one person from the total messages in the topic.
* Use this if someone asks about search syntax, rather than during the short walkthrough.
---

## Backup: Commits and discussions

<img class="screenshot-shadow" src="img/hk-person-commits.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Show how commit information connects back to the discussion and to contributor credit.
* The screenshot is a historical example, not a current count.
---

## Backup: Contributor profiles

<img class="screenshot-shadow" src="img/hk-person.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Show the profile and multiple aliases. The figures are from the captured example.
* Avoid inferring contribution quality from a single metric.
---

## Backup: Team notes

<img class="screenshot-shadow" src="img/hk-note.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* Show the note attached to the topic and the mention/tag workflow.
* This is a place to discuss how colleagues can keep context together.
---

## Backup: Community reports

<img class="screenshot-shadow" src="img/hk-report-weekly.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* The reports summarise activity such as messages, topics and participants.
* Use the period shown on the screenshot when discussing its figures.
---

## Backup: Community statistics

<img class="screenshot-shadow" src="img/hk-stats.png" data-preview-image style="height:800px; width:auto; background:none; border:none;">

Note:

* These views let people explore activity across the archive.
* The chart alone does not establish why participation changes.
---

## Backup: Mobile and dark mode

<img class="screenshot-shadow" src="img/hk-mobile.png" data-preview-image style="height:400px; width:auto; background:none; border:none;">
<img class="screenshot-shadow" src="img/hk-landing-dark.png" data-preview-image style="height:400px; width:auto; background:none; border:none;">

Note:

* The interface includes mobile and dark-mode views. Show these if someone asks about reading on a phone.
---

## Backup: Recorded walkthrough

<video data-autoplay muted playsinline controls
       src="img/hackorum-walkthrough.webm"
       style="height:790px; width:auto; background:none; border:none; box-shadow:none;"></video>

<p class="venue"><a href="#/backup-slides">Backup slides</a> &middot; <a href="https://hackorum.dev">hackorum.dev</a></p>

Note:

* Optional replacement for part of the screenshot walkthrough if useful; do not add another full tour to the scheduled talk.
* 0:00 Every thread on six mailing lists, as a conversation. The icons are state. Patch, CI, notes, unread.
* 0:12 A saved search. Every one of these has a patch and nobody has answered. Anyone can use it.
* 0:24 One thread. Index prefetching. Five hundred and four messages over three years.
* 0:36 The thread outline. That structure was in the mail headers all along. Nobody was showing it to you.
* 0:48 CI on every patch, and that docker line gives you a running Postgres built from this patch.
* 0:56 Search is a real query language. Andres, ten or more messages of his own, in threads with a patch.
* 1:04 Shared notes on a thread, with at-mentions and hash-tags your team can search.
* 1:12 And you can answer the list from here. Your address, correct headers, real mail.
* 1:20 Thousands of patch builds a day.
* 1:28 You can try it at the address on screen.
---

## Backup: Community feedback

<img class="screenshot-shadow" src="img/quote-david-steele.png" data-preview-image style="width:1150px; height:auto; background:none; border:none;">

<img class="screenshot-shadow" src="img/hackorum-discord.png" data-preview-image style="width:1150px; height:auto; background:none; border:none;">

<img class="screenshot-shadow" src="img/hackorum-usefulness.png" data-preview-image style="width:1700px; height:auto; background:none; border:none;">

*&mdash; Andrey Borodin, on `pgsql-hackers`*

Note:

* These are the attributed community comments preserved from the original deck. Give the audience time to read them.

---

## Backup: run a patch image

```bash
docker run --rm -p 5432:5432 ghcr.io/hackorum-dev/postgres-patch:t47973
psql -h localhost -U postgres
```

<img class="screenshot-shadow" src="img/hk-ci-banner.png" data-preview-image style="height:480px; width:auto; background:none; border:none;">

Note:

* Example command preserved from the original deck for topic 47973. Check the current image and connection settings before a live demonstration.
* This is optional reference material, not an instruction for the audience to execute during the prepared talk.
