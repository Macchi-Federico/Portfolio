<script>
  import Navbar from '$lib/Navbar.svelte';
  import Footer from '$lib/Footer.svelte';

  let { children } = $props();
</script>

<Navbar />
{@render children()}
<Footer />

<style>
  :global(*) { margin: 0; padding: 0; box-sizing: border-box; }

  :global(:root) {
    /* Palette chiara */
    --bg:          #fafaf8;
    --bg-alt:      #f3f2ee;
    --bg-card:     #ffffff;
    --surface:     #efefeb;

    /* Accenti vivaci */
    --violet:      #6c47ff;
    --violet-light:#ede8ff;
    --orange:      #ff6b35;
    --orange-light:#fff0ea;
    --green:       #22c27a;
    --green-light: #e4faf0;
    --blue:        #1d9bf0;
    --blue-light:  #e8f5fe;

    /* Testo */
    --text:        #1a1a1a;
    --text-2:      #555551;
    --text-3:      #9a9990;

    /* Bordi */
    --border:      #e2e0d8;
    --border-2:    #cdcbc2;

    /* Font */
    --font:        'DM Sans', 'Segoe UI', sans-serif;
    --mono:        'DM Mono', 'Fira Code', monospace;

    /* Shadows */
    --shadow-sm:   0 1px 4px rgba(0,0,0,.06), 0 2px 12px rgba(0,0,0,.04);
    --shadow-md:   0 4px 24px rgba(0,0,0,.09), 0 1px 4px rgba(0,0,0,.05);
    --shadow-lg:   0 12px 48px rgba(0,0,0,.12);
  }

  :global(html) { scroll-behavior: smooth; }

  :global(body) {
    background: var(--bg);
    color: var(--text);
    font-family: var(--font);
    line-height: 1.65;
    overflow-x: hidden;
  }

  :global(a) { color: var(--violet); text-decoration: none; }

  :global(section) { padding: 96px 0; }

  :global(.container) {
    max-width: 1120px;
    margin: 0 auto;
    padding: 0 28px;
  }

  :global(.label) {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-family: var(--mono);
    font-size: 0.72rem;
    font-weight: 500;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--text-3);
    margin-bottom: 10px;
  }

  :global(.label::before) {
    content: '';
    display: block;
    width: 16px;
    height: 2px;
    background: var(--violet);
    border-radius: 1px;
  }

  :global(.heading) {
    font-size: clamp(1.9rem, 4vw, 2.8rem);
    font-weight: 700;
    line-height: 1.15;
    letter-spacing: -0.03em;
    color: var(--text);
    margin-bottom: 48px;
  }

  :global(.chip) {
    display: inline-block;
    padding: 3px 11px;
    border-radius: 99px;
    font-family: var(--mono);
    font-size: 0.71rem;
    font-weight: 500;
    letter-spacing: 0.04em;
    background: var(--surface);
    color: var(--text-2);
    border: 1px solid var(--border);
  }

  :global(.chip.violet) { background: var(--violet-light); color: var(--violet); border-color: transparent; }
  :global(.chip.orange) { background: var(--orange-light); color: var(--orange); border-color: transparent; }
  :global(.chip.green)  { background: var(--green-light);  color: var(--green);  border-color: transparent; }
  :global(.chip.blue)   { background: var(--blue-light);   color: var(--blue);   border-color: transparent; }
</style>