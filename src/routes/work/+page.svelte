<svelte:head>
  <title>Work — Adrian Gachewa</title>
  <meta name="description" content="Selected projects by Adrian Gachewa — M-taka ERP, Aktaba, and freelance work." />
</svelte:head>

<article class="page">
  <div class="container">
    <p class="eyebrow">Work</p>
    <h1>Selected projects</h1>
    <p class="lead">
      A mix of employed work, a personal product, and freelance builds. Most live in production; one shaped how I think about relational databases.
    </p>
  </div>

  <div class="container-wide">
    <section class="project">
      <div class="project-meta">
        <span class="mono">2025 — Present</span>
        <span class="meta">M-taka · Lead Developer</span>
      </div>
      <div class="project-body">
        <h2>Core platform rebuild</h2>
        <p class="project-summary">
          Led the architectural redesign and 3-month rebuild of M-taka's core operational platform.
          After identifying that the original design wouldn't scale with the diversity of customer
          needs, made the call to rebuild rather than patch, owned the architecture end to end, and
          shipped the new system without service interruption.
        </p>
        <ul class="project-points">
          <li>
            <strong>Flexible by design.</strong> Designed the platform's configurability model so
            most new customer needs resolve through configuration rather than code changes.
          </li>
          <li>
            <strong>Performance.</strong> Took the data-heaviest parts of the system from minutes
            to sub-second on the slowest views, and from seconds to a few hundred milliseconds on
            standard ones.
          </li>
          <li>
            <strong>Offline-first.</strong> Shipped offline functionality across the user-facing
            application, with a sync model that minimizes conflicts.
          </li>
          <li>
            <strong>Migration.</strong> Owned the data migration between legacy and successor
            systems across incompatible schemas.
          </li>
        </ul>
        <p class="stack mono">
          Django · Postgres · SvelteKit · Redis · Docker
        </p>
      </div>
    </section>

    <section class="project">
      <div class="project-meta">
        <span class="mono">2025 — Present</span>
        <span class="meta">Solo · Live at aktaba.com</span>
      </div>
      <div class="project-body">
        <h2>Aktaba</h2>
        <p class="project-summary">
          A personal knowledge-management platform for working across domains. Ingest highlights from
          books, slice them into notes, tag them, attach them to projects, and work with them on an
          infinite canvas. Designed and built end-to-end over 8 months.
        </p>
        <p>
          <a href="/work/aktaba/">Read the case study →</a>
        </p>
        <p class="stack mono">
          FastAPI · SvelteKit · Postgres · Neo4j · S3
        </p>
      </div>
    </section>

    <section class="project">
      <div class="project-meta">
        <span class="mono">2025</span>
        <span class="meta">Freelance · United States</span>
      </div>
      <div class="project-body">
        <h2>Edmond Serenity</h2>
        <p class="project-summary">
          Resident management system for a US nursing home: patient records, medication schedules,
          and daily care logs. Co-built with one collaborator. Live since October 2025.
        </p>
        <p>
          <a href="https://edmondserenity.com" target="_blank" rel="noopener">edmondserenity.com →</a>
        </p>
      </div>
    </section>

    <section class="project">
      <div class="project-meta">
        <span class="mono">2026</span>
        <span class="meta">Freelance · Kenya</span>
      </div>
      <div class="project-body">
        <h2>Murunga Mangich Advocates</h2>
        <p class="project-summary">
          Document management system for a Kenyan law firm — file storage, search, and matter
          organization. Built solo. Live since February 2026.
        </p>
        <p>
          <a href="https://murungamangichadvs.co.ke" target="_blank" rel="noopener">murungamangichadvs.co.ke →</a>
        </p>
      </div>
    </section>

    <section class="project earlier">
      <div class="project-meta">
        <span class="mono">2023 — 2025</span>
        <span class="meta">Freelance · Various</span>
      </div>
      <div class="project-body">
        <h2>Earlier work</h2>
        <p class="project-summary">
          Bots, internal tools, and business sites for Kenyan SMBs. Cut my teeth on relational
          database design building a learning-management system from scratch with a peer —
          tables drawn on the back of old architecture sheets, foreign keys argued over for hours.
          It didn't ship, but the schema thinking it forced has shaped every system I've built since.
        </p>
      </div>
    </section>
  </div>
</article>

<style>
  .page > .container {
    margin-bottom: var(--space-7);
  }

  .project {
    display: grid;
    grid-template-columns: 12rem 1fr;
    gap: var(--space-6);
    padding: var(--space-6) 0;
    border-top: 1px solid var(--color-rule);
  }

  .project:last-child {
    border-bottom: 1px solid var(--color-rule);
  }

  .project-meta {
    display: flex;
    flex-direction: column;
    gap: var(--space-1);
    padding-top: var(--space-2);
  }

  .project-meta .meta {
    color: var(--color-muted);
  }

  .project-meta .mono {
    color: var(--color-ink);
    font-size: 0.82rem;
  }

  .project-body h2 {
    margin-top: 0;
    margin-bottom: var(--space-3);
    font-size: 1.6rem;
  }

  .project-summary {
    color: var(--color-ink);
    margin-bottom: var(--space-4);
  }

  .project-points {
    margin-top: var(--space-3);
    margin-bottom: var(--space-4);
  }

  .project-points li {
    margin-bottom: var(--space-3);
  }

  .stack {
    color: var(--color-muted);
    font-size: 0.8rem;
    margin-top: var(--space-4);
    margin-bottom: 0;
  }

  @media (max-width: 720px) {
    .project {
      grid-template-columns: 1fr;
      gap: var(--space-3);
    }
    .project-meta {
      flex-direction: row;
      gap: var(--space-4);
      padding-top: 0;
    }
  }
</style>
