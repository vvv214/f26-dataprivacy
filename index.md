---
title: Data Privacy
description: An advanced undergraduate course on privacy attacks, differential privacy, and privacy-enhancing technologies.
---

<div class="course-home">
  <nav class="course-nav" aria-label="Course navigation">
    <a class="course-brand" href="{{ '/' | relative_url }}">Data Privacy</a>
    <div class="course-nav-links">
      <a href="#schedule">Schedule</a>
      <a href="{{ '/lab.html' | relative_url }}">Labs</a>
      <a href="{{ '/project.html' | relative_url }}">Project</a>
      <a href="{{ '/policy.html' | relative_url }}">Policy</a>
      <a href="{{ '/resources.html' | relative_url }}">Resources</a>
    </div>
  </nav>

  <header class="course-hero">
    <p class="hero-kicker">University of Virginia / Fall 2026</p>
    <h1>Data Privacy</h1>
    <p class="hero-lede">
      Learn to find privacy failures, reason about meaningful guarantees, and build systems that hold up under scrutiny.
    </p>
    <div class="hero-actions">
      <a class="primary-action" href="#schedule">View the schedule</a>
      <a class="secondary-action" href="{{ '/project.html' | relative_url }}">Explore the final project &rarr;</a>
    </div>
  </header>

  <section class="course-facts" aria-label="Course at a glance">
    <div>
      <span>Level</span>
      <strong>Advanced undergraduate</strong>
    </div>
    <div>
      <span>Meetings</span>
      <strong>Tuesday + Thursday</strong>
    </div>
    <div>
      <span>Practice</span>
      <strong>Four labs</strong>
    </div>
    <div>
      <span>Capstone</span>
      <strong>Scoped final project</strong>
    </div>
  </section>

  <section class="home-section course-story" aria-labelledby="story-title">
    <div class="section-heading">
      <p class="section-kicker">The course arc</p>
      <h2 id="story-title">From attack to assurance.</h2>
      <p>We begin with failures students can observe directly, then develop the tools needed to evaluate and reduce privacy risk.</p>
    </div>
    <div class="lens-grid">
      <article>
        <span class="lens-index">01</span>
        <h3>Find the leak</h3>
        <p>Extraction, memorization, membership inference, linkage, singling-out, and reconstruction.</p>
      </article>
      <article>
        <span class="lens-index">02</span>
        <h3>Measure the risk</h3>
        <p>Attack evaluation, adjacency, sensitivity, privacy mechanisms, composition, and accounting.</p>
      </article>
      <article>
        <span class="lens-index">03</span>
        <h3>Build the defense</h3>
        <p>Private learning, MPC, homomorphic encryption, trusted execution, and network privacy.</p>
      </article>
    </div>
  </section>

  <section class="home-section course-structure" aria-labelledby="structure-title">
    <div class="section-heading compact">
      <p class="section-kicker">How it works</p>
      <h2 id="structure-title">Technical depth, with room to practice.</h2>
    </div>
    <div class="structure-grid">
      <div class="structure-copy">
        <p>
          This course is built for students who want to make technically defensible privacy decisions, not just recognize vocabulary. Lectures connect mechanisms to real failure modes; labs turn those ideas into experiments; the final project asks you to explain and defend a focused result.
        </p>
        <p>
          You should be comfortable with Python, basic probability, and modifying short pieces of code. Prior privacy research, LLM training, and advanced cryptography are not required.
        </p>
      </div>
      <dl class="course-details">
        <div>
          <dt>Instructor</dt>
          <dd><a href="https://tianhao.wang">Tianhao Wang</a></dd>
        </div>
        <div>
          <dt>Format</dt>
          <dd>In-person lectures, labs, quizzes, reading warm-ups, and a project</dd>
        </div>
        <div>
          <dt>Background</dt>
          <dd>Python programming and basic probability</dd>
        </div>
        <div>
          <dt>Logistics</dt>
          <dd>Room, time, TA, and Canvas details will be posted before classes begin</dd>
        </div>
      </dl>
    </div>
  </section>

  <section class="home-section grading-section" aria-labelledby="grading-title">
    <div class="section-heading compact">
      <p class="section-kicker">Assessment</p>
      <h2 id="grading-title">Grading at a glance.</h2>
    </div>
    <div class="grading-grid" aria-label="Grading weights">
      <a href="{{ '/lab.html' | relative_url }}"><strong>35%</strong><span>Labs</span></a>
      <a href="{{ '/project.html' | relative_url }}"><strong>30%</strong><span>Project</span></a>
      <div><strong>20%</strong><span>Quizzes</span></div>
      <div><strong>10%</strong><span>Participation</span></div>
      <div><strong>5%</strong><span>Reading</span></div>
    </div>
    <p class="section-footnote">
      Project milestones include a topic check-in, proposal, poster/demo, and final report. See the <a href="{{ '/project-present.html' | relative_url }}">milestone guide</a>, <a href="{{ '/project-rubric.html' | relative_url }}">rubric</a>, and <a href="{{ '/policy.html' | relative_url }}">course policies</a>.
    </p>
  </section>

  <section id="schedule" class="home-section schedule-section" aria-labelledby="schedule-title">
    <div class="schedule-intro">
      <div class="section-heading compact">
        <p class="section-kicker">Fall 2026</p>
        <h2 id="schedule-title">Schedule</h2>
      </div>
      <p>One week per row. Topics and due dates may shift as the semester develops.</p>
    </div>

    {% include_relative schedule.md %}
  </section>

  <section class="resource-band" aria-labelledby="resource-title">
    <div>
      <p class="section-kicker">Go further</p>
      <h2 id="resource-title">Privacy courses and books worth keeping nearby.</h2>
    </div>
    <a class="secondary-action" href="{{ '/resources.html' | relative_url }}">Browse resources &rarr;</a>
  </section>

  <footer class="course-footer">
    <span>Data Privacy / UVA / Fall 2026</span>
    <a href="https://tianhao.wang">Tianhao Wang</a>
  </footer>
</div>
