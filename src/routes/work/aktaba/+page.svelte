<svelte:head>
  <title>Aktaba — Case study — Adrian Gachewa</title>
  <meta name="description" content="Aktaba: a polymath's knowledge platform. Solo build, FastAPI + SvelteKit + Postgres + Neo4j." />
</svelte:head>

<article class="prose">
  <div class="container">
    <p class="eyebrow">Case study · Solo build</p>
    <h1>Aktaba</h1>
    <p class="lead">
      A polymath's notebook. Highlights become notes; notes carry tags across domains; tags pull
      into study areas you can share; ideas get reasoned through on canvases inside matters.
    </p>

    <dl class="facts">
      <div>
        <dt>Live at</dt>
        <dd><a href="https://aktaba.com" target="_blank" rel="noopener">aktaba.com</a></dd>
      </div>
      <div>
        <dt>Stack</dt>
        <dd>FastAPI · SvelteKit · Postgres · Neo4j · S3</dd>
      </div>
      <div>
        <dt>Built</dt>
        <dd>May 2025 — Jan 2026 (≈ 8 months, solo)</dd>
      </div>
      <div>
        <dt>Status</dt>
        <dd>In production · users across multiple countries</dd>
      </div>
    </dl>

    <h2>Why it exists</h2>
    <p>
      I read a lot. Not just to consume — to <em>compose</em>. A passage from a permaculture book
      reshapes how I think about software architecture; a chapter on database normalization changes
      how I see urban planning. The problem with reading like this is that ideas accumulate faster
      than any single domain can hold them, and the most valuable connections are usually the ones
      that cross between domains.
    </p>
    <p>
      Existing tools handle parts of this. Some store highlights well; others tag well; others
      visualize well. None I could find handled the full cycle the way I needed: ingest a highlight,
      decompose it into discrete notes, tag each note across multiple domains, attach notes to
      projects I'm working on, and surface the cross-domain connections when I'm thinking about a
      problem. So I built it.
    </p>

    <h2>The shape of the system</h2>
    <p>
      Aktaba is intentionally small in surface area but rich underneath. At the bottom are
      highlights — passages pulled from books — and notes, which you carve out of highlights
      or write directly. Notes get tags. From there, things compose: matters bring notes onto
      a canvas where you reason through a question by linking them together. Study areas pull
      notes in by tag for focused learning. Threads sequence notes into walkable narratives.
      Projects hold work in progress; documents hold source material.
    </p>
    <p>
      The interesting design work sits in how these compose, and in the architecture that makes
      the relationships queryable at speed.
    </p>

    <h3>Polyglot persistence</h3>
    <p>
      Two databases, doing different jobs:
    </p>
    <ul>
      <li>
        <strong>Postgres</strong> holds the canonical records — users, notes, highlights, tags,
        documents, projects, study areas. Relational queries, full-text search, transactional
        writes. Standard fare done carefully.
      </li>
      <li>
        <strong>Neo4j</strong> holds the link graph that lives inside matters. When you're
        working on a canvas, every link you draw between two notes carries a direction
        (uni- or bidirectional), a strength on a 1-to-5 scale, a type
        (<code>relates_to</code>, <code>supports</code>, <code>contradicts</code>, and so on),
        and optionally a comment. Trying to model that cleanly in SQL — joins, recursive CTEs,
        ad-hoc weight columns, type tables — was a war I'd lose every time I added a feature.
      </li>
    </ul>
    <p>
      The two stores stay consistent through write-time fan-out: writes go to Postgres first,
      then any matter-graph edges project into Neo4j. Reads use whichever store fits the
      query shape.
    </p>

    <h3>Study areas</h3>
    <p>
      A study area is a workspace for learning a specific subject. You attach a set of tags —
      say <code>AI</code> and <code>big-data</code> for studying machine intelligence — and
      Aktaba pulls in every note carrying those tags, alongside the documents, highlights,
      projects, matters, and threads you've placed inside. You read through, mark the irrelevant
      ones out, take the rest into matters where you reason through specific questions
      (<em>Can thinking be formalized?</em> — that kind of thing), and keep a learning journal
      alongside as you go.
    </p>
    <p>
      The point is twofold. First, a study area becomes a real artifact of having studied
      something. You can share one — with or without an expiry — and someone can see what you've
      been working through. It's a portfolio of mind, not of code. Second, it makes Aktaba a
      working environment for learning, not just a storage system for what you've already
      learned.
    </p>

    <h3>Deployment</h3>
    <p>
      Deployed globally with regular backups and streaming replication for durability. Typical page
      latency is about 600ms from East Africa; the dashboard, which aggregates across the graph,
      sits around 1.3s — acceptable given how much it does, but on the list of things to keep
      improving.
    </p>

    <h2>What I learned building it</h2>
    <p>
      A few things stand out, looking back at eight months of solo work.
    </p>
    <p>
      <strong>One:</strong> the graph database earned its place, but it earned it the hard way.
      Early on I tried to push the matter-link graph into Postgres with recursive CTEs and a
      few side tables for edge types and weights. It worked for a while. But once I started
      designing the canvas interactions that would surface weighted, typed paths between notes,
      the SQL got unreadable and the planner started doing things I couldn't predict. Switching
      to Neo4j for the link layer was a structural decision, not a performance one — though the
      performance followed.
    </p>
    <p>
      <strong>Two:</strong> shipping solo forces ruthless prioritization in a way working in a team
      doesn't. There were dozens of features I wanted on day one. Most of them I deliberately
      didn't build. The ones I did build, I built so they actually held up.
    </p>
    <p>
      <strong>Three:</strong> sometimes AI needs creative input from you, not just better prompts.
      The threads feature — notes arranged in a snake layout that moves left-to-right then folds
      back, or top-to-bottom then folds back up — broke every time card sizes changed. Multiple
      prompt attempts with the agent didn't resolve it. The fix had to come from rethinking the
      problem: compute each note's logical position in the sequence first, then place each one by
      fitting to the grid based on its actual size, and only after that render the links between
      them. The agent could implement the solution; it couldn't find it.
    </p>
    <p>
      <strong>Four:</strong> API response sizing is a UX-meets-resources judgment, not a rule.
      Bundle too much into one response and you waste bandwidth and the user's memory loading
      data they won't use. Hit the network for every small interaction and you stress both the
      connection and the user's perception of speed. The networking textbook I worked through
      made the principle explicit — don't use the network unnecessarily — but the practice is
      finding where <em>unnecessary</em> lives on each surface.
    </p>
    <p>
      <strong>Five:</strong> UI for tools you live inside is different from UI for tools you
      visit. After using Aktaba daily for a few months, I switched the palette from one with a
      subtle blue tint to one that's almost entirely neutral gray. The blue was fine in five-minute
      sessions and slightly tiring after two hours. The neutral gray disappears, which is what a
      tool should do.
    </p>
    <p>
      <strong>Six:</strong> the product is itself a reading instrument now. I use Aktaba almost
      daily — 2,500+ notes, 120 tags, 50 projects, 90+ highlights, 20 documents, 3 matters,
      1 study area. Every time I find a connection I wouldn't have surfaced any other way, the
      eight months feel well-spent.
    </p>

    <h2>What's next</h2>
    <p>
      Marketing has been minimal so far — a single listing on AlternativeTo.net brought the first
      international users. The platform is open to growth but I'm building deliberately, taking
      user feedback before pushing distribution. Features on the roadmap include richer document
      handling, sharper canvas interactions, and better surfacing of cross-domain connections.
    </p>

    <hr />

    <p class="footer-note">
      <a href="https://aktaba.com" target="_blank" rel="noopener">aktaba.com →</a>
      <span class="sep">·</span>
      <a href="/work/">All work</a>
    </p>
  </div>
</article>

<style>
  .prose h2 {
    margin-top: var(--space-8);
  }

  .facts {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: var(--space-4);
    margin: var(--space-6) 0 var(--space-7);
    padding: var(--space-5);
    background: var(--color-bg-subtle);
    border-radius: 4px;
  }

  .facts > div {
    display: flex;
    flex-direction: column;
    gap: var(--space-1);
  }

  .facts dt {
    font-family: var(--font-sans);
    font-size: 0.75rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--color-muted);
  }

  .facts dd {
    margin: 0;
    font-size: 0.95rem;
    color: var(--color-ink);
  }

  .footer-note {
    font-family: var(--font-sans);
    font-size: 0.9rem;
    color: var(--color-muted);
  }

  .footer-note .sep {
    margin: 0 var(--space-3);
  }

  @media (max-width: 600px) {
    .facts {
      grid-template-columns: 1fr;
    }
  }
</style>
