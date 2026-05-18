<script>
  const contacts = [
    {
      label: 'GitHub',
      value: 'github.com/Macchi-Federico',
      href: 'https://github.com/Macchi-Federico',
      color: 'violet',
      icon: `<svg width="22" height="22" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.3 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61-.546-1.385-1.335-1.755-1.335-1.755-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 21.795 24 17.295 24 12c0-6.63-5.37-12-12-12z"/></svg>`,
    },
    // Aggiungi altri contatti qui (email, LinkedIn, ecc.)
    // {
    //   label: 'Email',
    //   value: 'tuaemail@example.com',
    //   href: 'mailto:tuaemail@example.com',
    //   color: 'orange',
    //   icon: `<svg ...>`,
    // },
  ];

  const info = [
    { key: '"nome"',     val: '"Federico Macchi"',     color: 'str' },
    { key: '"scuola"',   val: '"ITIS Edoardo Agnelli"', color: 'str' },
    { key: '"indirizzo"',val: '"Informatica e TLC"',    color: 'str' },
    { key: '"anno"',     val: '"5ª · 2025/26"',         color: 'str' },
  ];
</script>

<section id="contact">
  <div class="container">
    <p class="label">Contatti</p>
    <h2 class="heading">GitHub</h2>

    <div class="grid">
      <!-- left col -->
      <div class="left">
        <p class="intro">
          Qui il mio percorso scolastico e i miei progetti:
        </p>

        <div class="contact-list">
          {#each contacts as c}
            <a href={c.href} target="_blank" rel="noopener" class="clink clink-{c.color}">
              <span class="clink-icon">{@html c.icon}</span>
              <div class="clink-text">
                <span class="clink-label">{c.label}</span>
                <span class="clink-value">{c.value}</span>
              </div>
              <span class="clink-arrow">→</span>
            </a>
          {/each}
        </div>

        <div class="fun-fact">
          <span class="ff-icon">💡</span>
          <p>Questo portfolio è stato realizzato con <strong>SvelteKit</strong> — un framework che ho imparato durante il 5° anno.</p>
        </div>
      </div>

      <!-- right col: code card -->
      <div class="code-card">
        <div class="code-bar">
          <span class="dot r"></span>
          <span class="dot y"></span>
          <span class="dot g"></span>
          <span class="code-filename">fredericomacchi.json</span>
        </div>
        <div class="code-body">
          <pre><span class="p">{'{'}</span>
{#each info as row}
  <span class="line">  <span class="k">{row.key}</span><span class="p">: </span><span class="{row.color}">{row.val}</span><span class="p">,</span></span>
{/each}
<span class="p">{'}'}</span></pre>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  section {
    background: var(--bg-alt);
    border-top: 1px solid var(--border);
  }

  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 64px;
    align-items: start;
  }

  .intro {
    font-size: 1.05rem;
    color: var(--text-2);
    line-height: 1.8;
    margin-bottom: 32px;
  }

  .contact-list {
    display: flex;
    flex-direction: column;
    gap: 12px;
    margin-bottom: 32px;
  }

  .clink {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 18px 20px;
    border-radius: 16px;
    border: 1px solid var(--border);
    background: var(--bg-card);
    box-shadow: var(--shadow-sm);
    text-decoration: none;
    color: var(--text);
    transition: transform .18s, box-shadow .18s, border-color .18s;
  }

  .clink:hover {
    transform: translateX(5px);
    box-shadow: var(--shadow-md);
  }

  .clink-violet:hover { border-color: var(--violet); }
  .clink-orange:hover { border-color: var(--orange); }
  .clink-green:hover  { border-color: var(--green); }

  .clink-icon {
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 42px; height: 42px;
    border-radius: 12px;
  }

  .clink-violet .clink-icon { color: var(--violet); background: var(--violet-light); }
  .clink-orange .clink-icon { color: var(--orange); background: var(--orange-light); }
  .clink-green  .clink-icon { color: var(--green);  background: var(--green-light); }

  .clink-text {
    display: flex;
    flex-direction: column;
    gap: 2px;
    flex: 1;
  }

  .clink-label {
    font-family: var(--mono);
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    color: var(--text-3);
  }

  .clink-value {
    font-size: 0.9rem;
    font-weight: 500;
    color: var(--text);
  }

  .clink-arrow {
    color: var(--text-3);
    font-size: 1.1rem;
    transition: transform .18s, color .18s;
  }

  .clink:hover .clink-arrow { transform: translateX(3px); color: var(--text); }

  /* fun fact */
  .fun-fact {
    display: flex;
    gap: 14px;
    align-items: flex-start;
    padding: 18px 20px;
    background: var(--violet-light);
    border-radius: 14px;
    border: 1px solid #d5c8ff;
  }

  .ff-icon { font-size: 1.3rem; flex-shrink: 0; }

  .fun-fact p {
    font-size: 0.88rem;
    color: #4a3a9a;
    line-height: 1.6;
  }

  .fun-fact strong { color: var(--violet); }

  /* code card */
  .code-card {
    background: #1e1e2e;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: var(--shadow-lg);
  }

  .code-bar {
    display: flex;
    align-items: center;
    gap: 7px;
    padding: 14px 18px;
    background: #16162a;
    border-bottom: 1px solid #2e2e4a;
  }

  .dot {
    width: 11px; height: 11px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  .dot.r { background: #ff5f57; }
  .dot.y { background: #ffbd2e; }
  .dot.g { background: #28ca42; }

  .code-filename {
    margin-left: 8px;
    font-family: var(--mono);
    font-size: 0.74rem;
    color: #7777aa;
    letter-spacing: 0.04em;
  }

  .code-body {
    padding: 28px;
    overflow-x: auto;
  }

  pre {
    font-family: var(--mono);
    font-size: 0.88rem;
    line-height: 1.8;
    color: #cdd6f4;
    white-space: pre;
  }

  .line { display: block; }
  .p  { color: #7777aa; }
  .k  { color: #89b4fa; }
  .str{ color: #a6e3a1; }
  .num{ color: #fab387; }
  .arr{ color: #89dceb; }

  @media (max-width: 900px) {
    .grid { grid-template-columns: 1fr; gap: 40px; }
  }
</style>