<svelte:head>
  <title>About — Adrian Gachewa</title>
  <meta name="description" content="From architecture school to software. On design-first thinking, sharpening the axe, and the place of human judgment in an AI world." />
</svelte:head>

<article class="prose">
  <div class="container">
    <p class="eyebrow">About</p>
    <h1>How I got here, and how I work.</h1>

    <p class="lead">
      I didn't take the straight path into software. I was supposed to. I went to architecture
      school instead. Looking back, I'm not sure the detour cost me anything — and I'm increasingly
      sure it gave me the shape of mind I use to do this work.
    </p>

    <h2>The detour</h2>
    <p>
      The pull toward tech started in high school. I knew, the way you know a few things in life
      without having to think about them, that this was the field where I could give form to ideas
      and refine them until they sailed — and that the refining is what I most wanted to do. Tech
      was an open arena. Your skill was the ticket. That felt like paradise.
    </p>
    <p>
      I ended up in architecture school by way of family pressure. I was grumpy for a year, then
      decided to be where I was. Architecture turned out to be its own form of giving-form-to-ideas,
      and I found I loved a lot of it. But I never let go of the pull toward software.
    </p>
    <p>
      Somewhere in second year we did a programming unit in C++. I felt like a fish returned to
      water. Long after the unit ended I kept going, working through Stroustrup's
      <em>Programming: Principles and Practice</em> on my own — back when the closest thing to an
      AI tutor was the Amazon review section telling you that, yes, this chapter is genuinely harder
      than the rest of the book, keep going. One quote stuck from that period and has stayed with me
      since: <em>when the terrain disagrees with the map, trust the terrain.</em>
    </p>
    <p>
      After graduating in 2023, I made the switch. Bootcamp, then a stretch of self-directed study
      — full textbooks on networking, on algorithms, on databases, with one on operating systems
      still pending. Then freelance, then leading development at M-taka.
    </p>

    <h2>How I work</h2>
    <p>
      My approach is short to describe and long to apply:
      <strong>meticulous planning, rigorous preparation, precise execution.</strong> Closer to
      "slow is the fastest way to get there" than to "move fast and break things." Given eight
      hours to cut a tree, I'd spend five sharpening the axe.
    </p>
    <p>
      In practice, this means the bulk of my effort goes into the phase before the keyboard. The
      database design. The trade-off analysis. The boundary decisions. The naming. The
      architecture-shaped questions that, if you answer them well, make the code almost write
      itself; and if you answer them badly, make every later week of coding harder than it needed
      to be.
    </p>
    <p>
      This is masterplanning carried over from architecture, where you don't start with where the
      bricks go — you start with how people move through the place, what light it needs, what
      weather it has to survive. In software the equivalents are: who the users actually are, what
      the data will outlast, where the system will break under load. Same instinct, different
      substrate.
    </p>
    <p>
      There's a real risk this approach turns into paralysis. In architecture school it sometimes
      did — I once read most of a permaculture book between receiving a community housing brief
      and starting the project, which was wonderful for the masterplan and ruinous for the deadline.
      In software it's behaved better. The constraints are tighter, the rewards of careful design
      are larger, and most projects don't reward extra weeks of preparation past a point.
    </p>

    <h2>The why before the how</h2>
    <p>
      <em>Software Architecture: The Hard Parts</em> states this as the second law of software
      architecture: <em>the why is more important than the how.</em> An engineer doesn't just need
      to know how to implement; they need to understand why one implementation has better
      trade-offs than another. This sounds obvious. In practice it's the thing most often
      skipped — under deadline pressure, under framework hype, under the desire to start typing.
    </p>
    <p>
      A consequence: there's no universal answer to most engineering questions. Every project has
      its context — the delivery timeline, the users, the team size, the criticality, the
      maintenance horizon, the failure modes you can tolerate. An engineer who understands this
      doesn't reach for microservices the moment a project looks large, doesn't reach for graph
      databases the moment they hear "relationships," doesn't reach for the framework that won
      Hacker News last month. They reach for what fits.
    </p>
    <p>
      Another consequence I keep close, also from <em>The Hard Parts</em>:
      <em>data outlasts systems.</em> The systems we build today will be torn out and rewritten;
      the data inside them will survive multiple rewrites and still be the asset the business cares
      about. So I pay disproportionate attention to data modeling. It's the part most likely to
      still matter in five years.
    </p>

    <h2>The AI question</h2>
    <p>
      It would be strange to write about how I work in 2026 without addressing this. AI can write
      code now. AI can design now. AI can prompt other AIs. Is the role of the software developer
      being hollowed out from the inside?
    </p>
    <p>
      My honest answer is: it depends, in interesting ways, on what you mean by "software
      developer." If the work is producing implementations of well-specified problems in
      well-trodden domains, the AI is excellent and getting better, and that work is changing
      character fast. If the work is the design that comes <em>before</em> the implementation —
      knowing what to build, knowing what to leave out, knowing which trade-offs the model can't
      see — then human judgment is where the value concentrates. I lean into the second.
    </p>
    <p>
      In practice this looks like writing prompts that carry a lot of weight. On one M-taka
      project that required significant architectural thinking, the project brief I built for
      the AI agent came to about 3,000 words. That sounds extreme. It was. But it captured the
      database design, the deployment topology, the extensibility surfaces, the failure cases I
      could anticipate, and a dozen smaller decisions I'd already made. The agent did the mundane
      coding well because I'd done the un-mundane work first.
    </p>
    <p>
      I also debate with agents. Not out of contrarianism — out of pattern recognition for the
      kinds of mistakes a model trained on average code makes. The number of times I've pressed
      on a recommendation and watched it revise itself toward something more reasonable is
      significant. I'm not always right, but I'm right often enough to keep doing it.
    </p>
    <p>
      The danger I try not to fall into is the inverse: trusting the model on questions only I have
      the context to answer. That failure mode is everywhere right now. People with the prompting
      skill of an expert and the judgment of a novice ship things that look right and fail in
      ways they didn't think to check. Human-in-the-loop only works if the human in the loop is
      actually thinking.
    </p>

    <h2>What I'm doing now</h2>
    <p>
      I lead backend development at <a href="/work/">M-taka</a>. I maintain
      <a href="/work/aktaba/">Aktaba</a>, the personal knowledge platform I built and use daily.
      I read more than is probably wise — software architecture, design, networking, occasionally
      a book on something completely unrelated because the cross-pollination is where the good
      ideas come from. I'm always interested in talking to people who think carefully about systems.
    </p>

    <hr />

    <p class="footer-note">
      <a href="mailto:gachewaadrian@gmail.com">gachewaadrian@gmail.com</a>
      <span class="sep">·</span>
      <a href="https://github.com/GachewaRa" target="_blank" rel="noopener">github.com/GachewaRa</a>
      <span class="sep">·</span>
      <a href="/resume/">Resume</a>
    </p>
  </div>
</article>

<style>
  .prose h2 {
    margin-top: var(--space-8);
  }

  .footer-note {
    font-family: var(--font-sans);
    font-size: 0.9rem;
    color: var(--color-muted);
  }

  .footer-note .sep {
    margin: 0 var(--space-3);
  }
</style>
