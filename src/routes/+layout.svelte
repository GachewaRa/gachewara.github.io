<script lang="ts">
  import '../app.css';
  import { page } from '$app/stores';

  let { children } = $props();

  const nav = [
    { href: '/', label: 'Index' },
    { href: '/work/', label: 'Work' },
    { href: '/about/', label: 'About' },
    { href: '/resume/', label: 'Resume' }
  ];

  function isActive(href: string, current: string): boolean {
    if (href === '/') return current === '/';
    return current.startsWith(href);
  }
</script>

<div class="shell">
  <header class="site-header">
    <div class="container-wide header-inner">
      <a href="/" class="brand plain" aria-label="Adrian Gachewa — Home">
        <span class="brand-name">Adrian Gachewa</span>
        <span class="brand-role">Full-stack developer</span>
      </a>
      <nav aria-label="Primary">
        <ul>
          {#each nav as item}
            <li>
              <a
                href={item.href}
                class="nav-link plain"
                class:active={isActive(item.href, $page.url.pathname)}
              >
                {item.label}
              </a>
            </li>
          {/each}
        </ul>
      </nav>
    </div>
  </header>

  <main>
    {@render children?.()}
  </main>

  <footer class="site-footer">
    <div class="container-wide footer-inner">
      <div class="footer-col">
        <span class="meta">Adrian Gachewa · Nairobi, Kenya</span>
      </div>
      <div class="footer-col footer-links">
        <a href="mailto:gachewaadrian@gmail.com">Email</a>
        <a href="https://github.com/GachewaRa" target="_blank" rel="noopener">GitHub</a>
        <a href="/resume/">Resume</a>
      </div>
    </div>
  </footer>
</div>

<style>
  .shell {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }

  main {
    flex: 1;
    padding-top: var(--space-7);
    padding-bottom: var(--space-9);
  }

  .site-header {
    border-bottom: 1px solid var(--color-rule);
    background: var(--color-bg);
  }

  .header-inner {
    display: flex;
    align-items: baseline;
    justify-content: space-between;
    padding-top: var(--space-5);
    padding-bottom: var(--space-5);
    gap: var(--space-5);
  }

  .brand {
    display: flex;
    flex-direction: column;
    line-height: 1.1;
  }

  .brand-name {
    font-family: var(--font-serif);
    font-size: 1.1rem;
    font-weight: 500;
    color: var(--color-ink);
  }

  .brand-role {
    font-family: var(--font-sans);
    font-size: 0.78rem;
    color: var(--color-muted);
    margin-top: 2px;
    letter-spacing: 0.01em;
  }

  nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    gap: var(--space-5);
  }

  nav li {
    margin: 0;
  }

  .nav-link {
    font-family: var(--font-sans);
    font-size: 0.88rem;
    color: var(--color-muted);
    letter-spacing: 0.01em;
    padding: 2px 0;
    border-bottom: 1px solid transparent;
  }

  .nav-link:hover {
    color: var(--color-ink);
  }

  .nav-link.active {
    color: var(--color-ink);
    border-bottom-color: var(--color-accent);
  }

  .site-footer {
    border-top: 1px solid var(--color-rule);
    padding-top: var(--space-5);
    padding-bottom: var(--space-6);
    background: var(--color-bg);
  }

  .footer-inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: var(--space-4);
    flex-wrap: wrap;
  }

  .footer-links {
    display: flex;
    gap: var(--space-5);
    font-family: var(--font-sans);
    font-size: 0.85rem;
  }

  @media (max-width: 600px) {
    .header-inner {
      flex-direction: column;
      align-items: flex-start;
      gap: var(--space-3);
    }
    nav ul {
      gap: var(--space-4);
    }
    .footer-inner {
      flex-direction: column;
      align-items: flex-start;
    }
  }
</style>
