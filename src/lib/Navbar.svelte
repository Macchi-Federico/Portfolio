<script>
  import { onMount } from 'svelte';

  let scrolled = $state(false);
  let menuOpen = $state(false);

  const links = [
    { label: 'Chi sono', href: '#about' },
    { label: '3° Anno',  href: '#year3' },
    { label: '4° Anno',  href: '#year4' },
    { label: '5° Anno',  href: '#year5' },
    { label: 'Contatti', href: '#contact' },
  ];

  onMount(() => {
    const onScroll = () => scrolled = window.scrollY > 40;
    window.addEventListener('scroll', onScroll);
    return () => window.removeEventListener('scroll', onScroll);
  });

  function close() { menuOpen = false; }
</script>

<header class:scrolled>
  <div class="container nav-inner">
    <a class="logo" href="#hero">
     
      <span class="logo-name">Federico Macchi</span>
    </a>

    <nav class:open={menuOpen}>
      {#each links as l}
        <a href={l.href} onclick={close}>{l.label}</a>
      {/each}
    </nav>

    <button class="burger" onclick={() => menuOpen = !menuOpen} aria-label="Menu">
      <span class:x={menuOpen}></span>
      <span class:x={menuOpen}></span>
      <span class:x={menuOpen}></span>
    </button>
  </div>
</header>

<style>
  header {
    position: fixed;
    inset: 0 0 auto;
    z-index: 200;
    padding: 18px 0;
    transition: background .25s, box-shadow .25s, padding .25s;
  }

  header.scrolled {
    background: rgba(250,250,248,.92);
    backdrop-filter: blur(20px);
    box-shadow: 0 1px 0 var(--border);
    padding: 12px 0;
  }

  .nav-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .logo {
    display: flex;
    align-items: center;
    gap: 10px;
    text-decoration: none;
  }

  .logo-mark {
    width: 34px;
    height: 34px;
    border-radius: 8px;
    background: var(--violet);
    color: #fff;
    font-family: var(--mono);
    font-size: 0.78rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    letter-spacing: 0;
    flex-shrink: 0;
  }

  .logo-name {
    font-size: 0.92rem;
    font-weight: 600;
    color: var(--text);
    letter-spacing: -0.01em;
  }

  nav {
    display: flex;
    gap: 2px;
    align-items: center;
  }

  nav a {
    padding: 6px 14px;
    font-size: 0.84rem;
    font-weight: 500;
    color: var(--text-2);
    border-radius: 8px;
    transition: background .15s, color .15s;
    letter-spacing: -0.01em;
  }

  nav a:hover {
    background: var(--surface);
    color: var(--text);
  }

  .burger {
    display: none;
    flex-direction: column;
    gap: 5px;
    background: none;
    border: none;
    cursor: pointer;
    padding: 6px;
  }

  .burger span {
    display: block;
    width: 22px;
    height: 2px;
    background: var(--text);
    border-radius: 2px;
    transition: all .25s;
    transform-origin: center;
  }

  .burger span.x:nth-child(1) { transform: translateY(7px) rotate(45deg); }
  .burger span.x:nth-child(2) { opacity: 0; }
  .burger span.x:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

  @media (max-width: 700px) {
    .burger { display: flex; }
    .logo-name { display: none; }

    nav {
      display: none;
      position: absolute;
      top: 100%;
      left: 0; right: 0;
      background: rgba(250,250,248,.98);
      border-top: 1px solid var(--border);
      flex-direction: column;
      align-items: stretch;
      padding: 8px 16px 16px;
      gap: 0;
    }

    nav.open { display: flex; }
    nav a { padding: 12px 8px; border-radius: 6px; }
  }
</style>