---
theme: default
title: A better discussion process for PEPs
info: A five-minute introduction to a proposal for improving PEP discussions.
colorSchema: light
aspectRatio: 16/9
canvasWidth: 1100
duration: 5min
timer: countdown
fonts:
  sans: Arial
  provider: none
drawings:
  enabled: false
defaults:
  layout: default
  transition: fade
---

# PEP Discussion Process Discussion

<p class="lead">Modernize the PEP discussion process in<br/> just 5 "easy" steps!</p>

<div class="cover-art" aria-hidden="true">
<svg class="cycle-arrows" viewBox="-65 -65 390 390" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="discuss-arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="5" markerHeight="5" orient="auto-start-reverse"><path d="M 0 0 L 10 5 L 0 10 z" fill="#3776ab" /></marker>
<marker id="refine-arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="5" markerHeight="5" orient="auto-start-reverse"><path d="M 0 0 L 10 5 L 0 10 z" fill="#e2ad13" /></marker>
</defs>
<path d="M 216 59 C 260 70 278 115 242 149" fill="none" stroke="#3776ab" stroke-width="5" stroke-linecap="round" marker-end="url(#discuss-arrow)" />
<path d="M 36 166 C -65 166 -65 59 -7 59" fill="none" stroke="#e2ad13" stroke-width="5" stroke-linecap="round" marker-end="url(#refine-arrow)" />
</svg>
<span class="blue-block">discuss</span><span class="yellow-block">refine</span>
</div>

<div class="bottom-note">Emma Smith - 2026-10-21</div>

<!--
10 seconds · cumulative 0:10

The discussion and refinement of a PEP should form a productive cycle. These three experiences show how discussion can become the hardest part of being an author.
-->

---

# Status quo

<blockquote class="responsibility-quote">The PEP author is responsible for building consensus within the community and documenting dissenting opinions.</blockquote>

<div class="quote-citation">—  <a href="https://peps.python.org/pep-0001/#what-is-a-pep">PEP 1 · What is a PEP?</a></div>

<!--
20 seconds · cumulative 0:30

PEP 1 puts the responsibility directly on the author: building consensus within the community and documenting dissenting opinions. That is a substantial job alongside designing the proposal. What support does an author need to do it well?
-->

---
class: discussion-burden
---

# This is hard to manage alone.

<div class="burden-grid">
<div class="card"><h3>Difficult to scale feedback</h3><p>Python is more popular than ever. That means more participants in discussions and longer threads</p></div>
<div class="card"><h3>Contentious discussions</h3><p>Breaking an impasse can look like shutting down discussion or ignoring feedback.</p></div>
<div class="card"><h3>Long threads filter voices</h3><p>People are put off by overly long discussions. Creates a natural filter for strong (i.e. negative) opinions</p></div>
</div>

<!--
45 seconds · cumulative 1:15

Python's larger community brings more participants and longer discussions; relying on one author to absorb and manage all that feedback does not scale. Carter Baxter's essay describes a similar problem in organizational leadership. I am applying that framing here, not treating it as data about PEP threads. Consensus is not always reachable, and breaking an impasse can look like shutting people down. Off-topic discussion also needs shared moderation. Finally, long threads discourage participation and can favor those with strong views. My concern is that negative views become overrepresented, as in the PyBay account; that is a concern to investigate, not an established correlation.
-->

---

# 1. Disallow questioning authors’ motivations in discussions

<div class="grid-two compact motive-columns mt-18">
<div><h3>Why?</h3><p>Questioning motives in a PEP thread is not productive and is demotivating.</p></div>
<div><h3>Where should earnest concerns go?</h3><p>Bring them directly to the <strong>Steering Council / PEP-Delegate</strong>, or the <strong>Code of Conduct Working Group</strong>, as appropriate.</p></div>
</div>

<!--
35 seconds · cumulative 1:50

The first proposed change is to disallow questioning authors' motivations, or the motivations behind PEP decisions, in PEP discussion threads. The rationale is that this is not what those threads are for: they should improve the proposal and inform its review. Participants can challenge the rationale, evidence, and trade-offs. If someone has earnest concerns about motives, bring them directly to the Steering Council or PEP-Delegate, or to the Code of Conduct Working Group for conduct concerns. Authors should not have to adjudicate those concerns in their own proposal thread.
-->

---

# 2. Introduce a PEP Guide.

<p class="subtitle">A partner to the authors in managing a productive conversation.</p>

<div class="roles">
<div class="role"><span class="index">FOCUS</span><h3>Keep discussion on-topic</h3><p>Re-direct off-topic comments to new threads. Handle comments on already-decided points.</p></div>
<div class="role"><span class="index">UNBLOCK</span><h3>Recognize an impasse</h3><p>Advise when to consult the Steering Council, poll the thread, or reject an idea.</p></div>
<div class="role"><span class="index">ESCALATE</span><h3>Advise on active/contentious threads</h3><p>Suggest when to involve DPO moderators to lock or slow-mode threads.</p></div>
</div>

<div class="source">Inspired by the Rust project’s project proposal champion role.</div>

<!--
35 seconds · cumulative 2:25

Second, introduce a PEP guide, inspired by the Rust project's proposal guide role. They work with authors on productive discussion, help turn comments into useful feedback, and advise when to consult the Steering Council at an impasse or request moderator intervention. Document practical tools too, including asking moderators to consider slow mode. Guide selection and support still need design; the role does not carry acceptance authority.
-->

---

# 3. Encourage shorter threads

<p class="subtitle">Whenever the author(s) reach a decision on a discussion topic:</p>

<div class="flow mt-18">
<div><span>1</span><h3>Lock</h3><p>The current<br>discussion thread</p></div>
<b aria-hidden="true">→</b>
<div><span>2</span><h3>Update</h3><p>A new PR to<br>python/peps</p></div>
<b aria-hidden="true">→</b>
<div><span>3</span><h3>Restart</h3><p>Begin the next<br>discussion round.</p></div>
</div>

<!--
45 seconds · cumulative 3:10

Third, encourage shorter threads by making an author's decision on a discussion topic the trigger for a fresh round. Lock the current thread, open a new python/peps PR, and start the next thread using the changelog and summary format on the next slide. This proposal defines when to move on; the next defines what context to carry forward. Choosing an alternative should produce a recorded rationale and a fresh starting point. An author's design decision is distinct from formal acceptance. Who performs the lock and how the handoff works still need to be settled.
-->

---

# 4. PEP Changelogs and thread summaries

<div class="record-grid">
<div class="record-main"><div class="tag">In the PEP · Existing practice</div><h3>Update the PEP text</h3><br><h3>Update rejected ideas</h3><br><div class="changelog-proposal"><div class="tag">Proposal</div><h3>Keep a required changelog</h3><p>Explain what changed and why.</p></div></div>
<div class="record-side"><div class="tag">In every new discussion thread</div><h3>Link the PR.</h3><h3>Copy the changelog.</h3><h3>Summarize the previous discussion.</h3><p>Decisions made, rejected ideas, and topics still open.</p></div>
</div>

<div class="source">h/t to Barry Warsaw for PEP changelogs</div>

<!--
45 seconds · cumulative 3:55

Fourth, require a PEP changelog, as suggested by Barry Warsaw, and make each new discussion thread start with a summary. Updating the PEP text and recording rejected ideas are existing practices. The proposed addition is to require a changelog explaining what changed and why. Every new thread should link the PR, copy the changelog, and summarize previous discussion: decisions made, ideas rejected, and questions still open. This gives readers the context to contribute without reconstructing earlier threads. Whether to exempt purely editorial updates remains an open detail.
-->

---

# 5. Introduce a final comment period.

<div class="fcp"><span>Discuss & revise</span><b>→</b><span class="highlight">Final comment period</span><b>→</b><span>Formal decision</span></div>

<div class="grid-two compact">
<div><h3>Goal</h3><p>Ensure people know when a PEP is going to be submitted for decision so they don't feel left out.</p></div>
<div><h3>Open Questions</h3><p>Who starts it, how long it lasts, and when new feedback reopens discussion (maybe when the author or SC/delegate think it should?).</p></div>
</div>

<div class="source">Inspiration: <a href="https://rust-lang.github.io/rfcs/introduction.html#what-the-process-is">The Rust RFC Book · Final comment period</a></div>

<!--
35 seconds · cumulative 4:30

Finally, introduce a final comment period inspired by Rust: a clearly announced opportunity for feedback before formal resolution. PEP 810 shows why: reviewers may be waiting for a quieter moment while authors believe discussion has converged. Make that review window explicit. We still need to decide who starts it, its duration, and what new evidence sends a PEP back to revision. Expiry would not automatically accept the PEP; the relevant decision authority still decides.
-->
