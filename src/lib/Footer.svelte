<footer>
  <div class="container footer-inner">
    <div class="logo">
      <span class="logo-mark">FM</span>
      <span>Federico Macchi</span>
    </div>
    <p class="copy">
      © {new Date().getFullYear()} · Portfolio Esame di Maturità · ITIS Edoardo Agnelli
    </p>
  </div>
</footer>

<style>
  footer {
    border-top: 1px solid var(--border);
    padding: 28px 0;
    background: var(--bg-card);
  }

  .footer-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 12px;
  }

  .logo {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 0.88rem;
    font-weight: 600;
    color: var(--text);
  }

  .logo-mark {
    width: 28px; height: 28px;
    border-radius: 7px;
    background: var(--violet);
    color: #fff;
    font-family: var(--mono);
    font-size: 0.7rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }

  .copy {
    font-size: 0.78rem;
    color: var(--text-3);
    font-family: var(--mono);
    letter-spacing: 0.03em;
  }
</style>