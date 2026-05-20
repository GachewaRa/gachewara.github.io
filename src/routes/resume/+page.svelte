<svelte:head>
  <title>Resume — Adrian Gachewa</title>
  <meta name="description" content="Resume — Adrian Gachewa, full-stack developer." />
</svelte:head>

<article class="resume">
  <div class="container-wide resume-toolbar no-print">
    <p class="meta">Print this page (Cmd/Ctrl + P) to save as PDF.</p>
    <button type="button" onclick={() => window.print()} class="print-btn">Print / Save PDF</button>
  </div>

  <div class="container-wide resume-sheet">
    <header class="resume-header">
      <div class="resume-name-block">
        <h1>Adrian Gachewa</h1>
        <p class="resume-title">Full-stack Developer · Backend-leaning</p>
      </div>
      <div class="resume-contact">
        <p>Nairobi, Kenya</p>
        <p><a href="mailto:gachewaadrian@gmail.com">gachewaadrian@gmail.com</a></p>
        <p>+254 717 990 230</p>
        <p>
          <a href="https://github.com/GachewaRa" target="_blank" rel="noopener">github.com/GachewaRa</a>
        </p>
        <p>
          <a href="https://gachewara.github.io">gachewara.github.io</a>
        </p>
      </div>
    </header>

    <p class="summary">
      Backend-leaning fullstack developer with 3 years building production systems.
      Architecture-school background informs how I approach system design. Currently leading
      development at M-taka, a Kenyan startup building software for the waste sector.
    </p>

    <section class="resume-section">
      <h2>Experience</h2>

      <div class="role">
        <div class="role-head">
          <h3>Lead Developer — M-taka</h3>
          <span class="role-dates">Jul 2025 – Present</span>
        </div>
        <p class="role-context">
          <em>Early-stage Kenyan startup. Software for the waste-management sector.</em>
        </p>
        <ul>
          <li>
            Led the architectural redesign and 3-month rebuild of the company's core platform
            after identifying that the original design wouldn't scale with the diversity of
            customer needs. Made the call to rebuild rather than patch, owned the architecture
            end to end, and shipped without service interruption.
          </li>
          <li>
            Drove a substantial performance gain on the data-heaviest parts of the system —
            slowest views moved from <strong>minutes to sub-second</strong>; standard views from
            seconds to a few hundred milliseconds. Combined query optimization with a
            right-sized deployment topology for current scale.
          </li>
          <li>
            Designed the platform's configurability model so most new customer needs resolve
            through configuration rather than code changes.
          </li>
          <li>
            Shipped offline-first functionality across the user-facing application, with a sync
            model that minimizes conflicts across user-scoped operations.
          </li>
          <li>
            Owned the data migration between legacy and successor systems across incompatible
            schemas.
          </li>
          <li>
            Coordinated a team of two (frontend dev + fullstack dev) through the rebuild while
            leading from the backend.
          </li>
        </ul>
      </div>

      <div class="role">
        <div class="role-head">
          <h3>Freelance Full-stack Developer</h3>
          <span class="role-dates">2023 – 2025</span>
        </div>
        <ul>
          <li>
            <strong>Edmond Serenity</strong> —
            <a href="https://edmondserenity.com" target="_blank" rel="noopener">edmondserenity.com</a>.
            Resident management system for a US nursing home: patient records, medication
            schedules, daily care logs. Co-built with one collaborator. Live since Oct 2025.
          </li>
          <li>
            <strong>Murunga Mangich Advocates</strong> —
            <a href="https://murungamangichadvs.co.ke" target="_blank" rel="noopener">murungamangichadvs.co.ke</a>.
            Document management system for a Kenyan law firm. Built solo. Live since Feb 2026.
          </li>
          <li>
            Earlier work (2023–2024): bots, internal tools, business sites for Kenyan SMBs.
            Cut my teeth on relational database design building a learning-management system from
            scratch with a peer.
          </li>
        </ul>
      </div>
    </section>

    <section class="resume-section">
      <h2>Selected Project</h2>
      <div class="role">
        <div class="role-head">
          <h3>Aktaba — Personal knowledge-management platform</h3>
          <span class="role-dates">
            <a href="https://aktaba.com" target="_blank" rel="noopener">aktaba.com</a>
          </span>
        </div>
        <p class="role-context">
          <em>Solo build · Live since early 2026 · 8 months idea to launch</em>
        </p>
        <p>
          A polymath's notebook: ingest highlights from books, slice them into notes, tag them
          across domains, attach them to projects, work with them on an infinite canvas. Designed
          and built end-to-end.
        </p>
        <ul>
          <li>
            <strong>Stack:</strong> FastAPI · SvelteKit · Postgres · Neo4j · S3. Postgres for
            records, Neo4j for cross-domain relationships between notes, tags, and projects.
          </li>
          <li>
            Globally deployed with regular backups and streaming replication. ~600ms typical page
            latency from East Africa.
          </li>
          <li>
            In active daily personal use: 2,500+ notes across 120 tags, 50 projects, 90+ highlights,
            20 documents, 3 matters, 1 study area. Users in multiple countries via an
            AlternativeTo.net listing.
          </li>
        </ul>
      </div>
    </section>

    <section class="resume-section stack-section">
      <h2>Stack</h2>
      <dl class="stack-list">
        <div>
          <dt>Backend</dt>
          <dd>Python (FastAPI, Django) · REST · async patterns · query optimization</dd>
        </div>
        <div>
          <dt>Data</dt>
          <dd>Postgres · Neo4j · Redis · relational + graph modeling · migrations</dd>
        </div>
        <div>
          <dt>Frontend</dt>
          <dd>TypeScript · SvelteKit · React · PWA / offline-first</dd>
        </div>
        <div>
          <dt>Infra</dt>
          <dd>AWS · S3 · Docker · CI/CD · Linux</dd>
        </div>
        <div>
          <dt>Strengths</dt>
          <dd>
            system design · database modeling · architecture trade-off reasoning ·
            technical writing · AI-assisted development workflows
          </dd>
        </div>
      </dl>
    </section>

    <section class="resume-section">
      <h2>Education</h2>
      <div class="role">
        <div class="role-head">
          <h3>Bachelor of Architectural Studies</h3>
          <span class="role-dates">Technical University of Kenya · 2023</span>
        </div>
        <p>
          Masterplanning, structural reasoning, and design under constraint — the disciplines
          I now apply to software.
        </p>
        <p class="role-context">
          <em>Self-directed:</em> worked through standard texts on networking, algorithms,
          databases, and <em>Software Architecture: The Hard Parts</em>. Bootcamp 2023.
        </p>
      </div>
    </section>

    <section class="resume-section languages">
      <h2>Languages</h2>
      <p>English · Kiswahili</p>
    </section>

    <p class="refs"><em>References available on request.</em></p>
  </div>
</article>

<style>
  .resume-toolbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: var(--space-2) var(--space-5);
    margin-bottom: var(--space-5);
    background: var(--color-bg-subtle);
    border-radius: 4px;
  }

  .resume-toolbar .meta {
    margin: 0;
  }

  .print-btn {
    font-family: var(--font-sans);
    font-size: 0.85rem;
    padding: 0.5rem 1rem;
    background: var(--color-ink);
    color: var(--color-bg);
    border: none;
    border-radius: 3px;
    cursor: pointer;
    transition: background 0.15s ease;
  }

  .print-btn:hover {
    background: var(--color-accent);
  }

  .resume-sheet {
    background: var(--color-bg);
  }

  .resume-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: var(--space-5);
    padding-bottom: var(--space-5);
    border-bottom: 1px solid var(--color-rule);
    margin-bottom: var(--space-5);
  }

  .resume-name-block h1 {
    margin-bottom: var(--space-2);
    font-size: 2rem;
  }

  .resume-title {
    font-family: var(--font-sans);
    font-size: 0.95rem;
    color: var(--color-muted);
    margin: 0;
    letter-spacing: 0.01em;
  }

  .resume-contact {
    text-align: right;
    font-family: var(--font-sans);
    font-size: 0.82rem;
  }

  .resume-contact p {
    margin: 0;
    line-height: 1.55;
    color: var(--color-ink-soft);
  }

  .summary {
    font-size: 1rem;
    color: var(--color-ink);
    margin-bottom: var(--space-6);
    max-width: 42rem;
  }

  .resume-section {
    margin-top: var(--space-6);
  }

  .resume-section h2 {
    font-family: var(--font-sans);
    font-size: 0.78rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    color: var(--color-muted);
    margin: 0 0 var(--space-4) 0;
    padding-bottom: var(--space-2);
    border-bottom: 1px solid var(--color-rule);
  }

  .role {
    margin-bottom: var(--space-5);
  }

  .role-head {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: var(--space-3);
    margin-bottom: var(--space-2);
    flex-wrap: wrap;
  }

  .role-head h3 {
    font-size: 1.1rem;
    margin: 0;
    font-weight: 600;
  }

  .role-dates {
    font-family: var(--font-sans);
    font-size: 0.82rem;
    color: var(--color-muted);
  }

  .role-context {
    color: var(--color-muted);
    font-size: 0.92rem;
    margin-bottom: var(--space-2);
  }

  .role ul {
    padding-left: 1.1rem;
  }

  .role li {
    margin-bottom: var(--space-2);
    font-size: 0.95rem;
    color: var(--color-ink-soft);
    line-height: 1.55;
  }

  .stack-list {
    display: grid;
    grid-template-columns: 7rem 1fr;
    row-gap: var(--space-2);
    column-gap: var(--space-4);
    margin: 0;
  }

  .stack-list > div {
    display: contents;
  }

  .stack-list dt {
    font-family: var(--font-sans);
    font-size: 0.82rem;
    color: var(--color-muted);
    font-weight: 500;
  }

  .stack-list dd {
    margin: 0;
    font-size: 0.92rem;
    color: var(--color-ink);
  }

  .languages p {
    margin: 0;
    font-size: 0.95rem;
  }

  .refs {
    margin-top: var(--space-6);
    color: var(--color-muted);
    font-size: 0.88rem;
    text-align: center;
  }

  @media (max-width: 600px) {
    .resume-header {
      flex-direction: column;
    }
    .resume-contact {
      text-align: left;
    }
    .stack-list {
      grid-template-columns: 1fr;
      gap: var(--space-1);
    }
    .stack-list dt {
      margin-top: var(--space-2);
    }
  }

  @media print {
    :global(:root) {
      --color-bg: white;
      --color-bg-subtle: #f5f5f5;
      --color-ink: black;
      --color-ink-soft: #222;
      --color-muted: #555;
      --color-rule: #ccc;
      --color-accent: black;
      --color-accent-soft: #555;
    }
    :global(body) {
      background: white;
      color: black;
      font-size: 10pt;
      line-height: 1.4;
    }
    :global(.site-header),
    :global(.site-footer),
    .no-print {
      display: none !important;
    }
    :global(main) {
      padding: 0 !important;
    }
    .resume-sheet {
      max-width: 100%;
      padding: 0;
    }
    .resume-name-block h1 {
      font-size: 18pt;
    }
    .resume-section h2 {
      font-size: 9pt;
      letter-spacing: 0.12em;
    }
    .role-head h3 {
      font-size: 11pt;
    }
    .role li,
    .summary,
    .stack-list dd {
      font-size: 10pt;
    }
    .role,
    .resume-section {
      page-break-inside: avoid;
    }
    a {
      color: black;
      text-decoration: none;
    }
  }
</style>
