<svelte:head>
  <title>Adrian Gachewa — Full-stack Developer</title>
  <meta name="description" content="Adrian Gachewa. Backend-leaning fullstack developer based in Nairobi. Currently leading development at M-taka." />
</svelte:head>

<section class="hero">
  <div class="container">
    <p class="eyebrow">Nairobi, Kenya · est. 2023</p>
    <h1 class="hero-title">
      Backend-leaning fullstack developer.<br />
      Trained as an architect.
    </h1>
    <p class="lead hero-lead">
      I build production systems with the same care I learned to bring to buildings —
      think the whole structure through before laying the first brick.
    </p>
    <p class="hero-current">
      Currently leading development at
      <a href="/work/" class="plain"><em>M-taka</em></a>,
      a Kenyan startup building software for the waste sector.
    </p>
  </div>
</section>

<section class="index">
  <div class="container">
    <ul class="index-list">
      <li>
        <a href="/work/" class="plain index-link">
          <span class="index-num">01</span>
          <span class="index-label">Work</span>
          <span class="index-desc">Selected projects — M-taka, Aktaba, freelance.</span>
        </a>
      </li>
      <li>
        <a href="/work/aktaba/" class="plain index-link">
          <span class="index-num">02</span>
          <span class="index-label">Aktaba</span>
          <span class="index-desc">A polymath's knowledge platform. Solo build, live since 2026.</span>
        </a>
      </li>
      <li>
        <a href="/about/" class="plain index-link">
          <span class="index-num">03</span>
          <span class="index-label">About</span>
          <span class="index-desc">The journey from architecture school into software, and how the two converge.</span>
        </a>
      </li>
      <li>
        <a href="/resume/" class="plain index-link">
          <span class="index-num">04</span>
          <span class="index-label">Resume</span>
          <span class="index-desc">The one-page version. Printable.</span>
        </a>
      </li>
    </ul>
  </div>
</section>

<style>
  .hero {
    padding-top: var(--space-6);
    padding-bottom: var(--space-9);
  }

  .hero-title {
    font-size: clamp(2rem, 5vw, 3.25rem);
    line-height: 1.1;
    margin-top: var(--space-3);
    margin-bottom: var(--space-5);
    letter-spacing: -0.02em;
  }

  .hero-lead {
    max-width: 32rem;
    color: var(--color-ink);
    margin-bottom: var(--space-5);
  }

  .hero-current {
    font-family: var(--font-sans);
    font-size: 0.92rem;
    color: var(--color-muted);
    margin: 0;
  }

  .hero-current em {
    color: var(--color-ink);
    font-style: normal;
    font-family: var(--font-serif);
    font-weight: 500;
  }

  .index {
    border-top: 1px solid var(--color-rule);
    padding-top: var(--space-7);
  }

  .index-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .index-list li {
    margin: 0;
    border-bottom: 1px solid var(--color-rule);
  }

  .index-link {
    display: grid;
    grid-template-columns: 3.5rem 8rem 1fr;
    align-items: baseline;
    gap: var(--space-4);
    padding: var(--space-5) 0;
    transition: color 0.15s ease, padding-left 0.2s ease;
  }

  .index-link:hover {
    padding-left: var(--space-3);
    color: var(--color-accent);
  }

  .index-num {
    font-family: var(--font-mono);
    font-size: 0.85rem;
    color: var(--color-muted);
  }

  .index-label {
    font-family: var(--font-serif);
    font-size: 1.4rem;
    font-weight: 500;
    color: var(--color-ink);
  }

  .index-link:hover .index-label {
    color: var(--color-accent);
  }

  .index-desc {
    font-family: var(--font-sans);
    font-size: 0.92rem;
    color: var(--color-muted);
    line-height: 1.5;
  }

  @media (max-width: 600px) {
    .index-link {
      grid-template-columns: 2.5rem 1fr;
      grid-template-rows: auto auto;
      row-gap: var(--space-2);
    }
    .index-desc {
      grid-column: 2 / -1;
    }
  }
</style>
