<!--
<script>
  const skills = [
    { name: 'C',              color: 'violet' },
    { name: 'Python',         color: 'blue'   },
    { name: 'HTML & CSS',     color: 'orange' },
    { name: 'JavaScript',     color: 'orange' },
    { name: 'SQL',            color: 'green'  },
    { name: 'Java',           color: 'blue'   },
    { name: 'Linux',          color: 'violet' },
    { name: 'Reti & Sistemi', color: 'green'  },
    { name: 'Arduino',        color: 'green'  },
    { name: 'Git',            color: 'orange' },
    { name: 'SvelteKit',      color: 'violet' },
    { name: 'Django',         color: 'green'  },
  ];
</script>

<section id="about">
  <div class="container">
    <p class="label">Chi sono</p>
    <h2 class="heading">About me</h2>

    <div class="grid">
      
      <div class="text-col">
        <p>
          Sono <strong>Federico Macchi</strong>, studente dell'Istituto Internazionale
          Edoardo Agnelli di Torino, indirizzo <strong>Informatica e Telecomunicazioni</strong>.
          Ho sempre avuto una grande passione per la tecnologia e il mondo digitale,
          che mi ha spinto a scegliere questo percorso.
        </p>
        <p>
          In questi cinque anni ho acquisito competenze che spaziano dalla
          programmazione ai sistemi operativi, dalle reti alle basi di dati.
          Ogni anno ha rappresentato un tassello fondamentale del mio percorso formativo.
        </p>
        <p>
          Nel tempo libero mi piace sperimentare con progetti personali,
          sport e attività formative.
        </p>

        <div class="skills-block">
          <p class="skills-title">Competenze acquisite</p>
          <div class="chips">
            {#each skills as s}
              <span class="chip {s.color}">{s.name}</span>
            {/each}
          </div>
        </div>
      </div>

     
      <div class="info-col">
        <div class="info-card">
          <div class="info-card-header">
            <div class="avatar">FM</div>
            <div>
              <p class="info-name">Federico Macchi</p>
              <p class="info-role">Studente ITIS · 5ª classe</p>
            </div>
          </div>

          <div class="info-rows">
            <div class="row">
              <span class="row-icon">🏫</span>
              <div>
                <p class="row-label">Scuola</p>
                <p class="row-val">Istituto Internazionale Edoardo Agnelli</p>
              </div>
            </div>
            <div class="row">
              <span class="row-icon">💻</span>
              <div>
                <p class="row-label">Indirizzo</p>
                <p class="row-val">Informatica e TLC</p>
              </div>
            </div>
            <div class="row">
              <span class="row-icon">📅</span>
              <div>
                <p class="row-label">Anno scolastico</p>
                <p class="row-val">5ª classe · 2025/26</p>
              </div>
            </div>
            <div class="row">
              <span class="row-icon">📍</span>
              <div>
                <p class="row-label">Città</p>
                <p class="row-val">Torino</p>
              </div>
            </div>
            <div class="row">
              <span class="row-icon">⏱️</span>
              <div>
                <p class="row-label">PCTO</p>
                <p class="row-val">200 ore completate</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  section {
    background: var(--bg-alt);
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
  }

  .grid {
    display: grid;
    grid-template-columns: 1fr 360px;
    gap: 64px;
    align-items: start;
  }

  .text-col {
    display: flex;
    flex-direction: column;
    gap: 18px;
  }

  .text-col p {
    font-size: 1.05rem;
    color: var(--text-2);
    line-height: 1.8;
  }

  .text-col strong {
    color: var(--text);
    font-weight: 600;
  }

  .skills-block {
    margin-top: 12px;
    padding: 24px;
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 16px;
    box-shadow: var(--shadow-sm);
  }

  .skills-title {
    font-family: var(--mono);
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--text-3);
    margin-bottom: 14px;
  }

  .chips {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  /* info card */
  .info-card {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: var(--shadow-md);
  }

  .info-card-header {
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 24px 24px 20px;
    background: linear-gradient(135deg, var(--violet-light) 0%, var(--orange-light) 100%);
    border-bottom: 1px solid var(--border);
  }

  .avatar {
    width: 52px; height: 52px;
    border-radius: 14px;
    background: var(--violet);
    color: #fff;
    font-family: var(--mono);
    font-size: 1rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    box-shadow: 0 4px 12px rgba(108,71,255,.3);
  }

  .info-name {
    font-size: 1rem;
    font-weight: 700;
    color: var(--text);
    letter-spacing: -0.02em;
  }

  .info-role {
    font-family: var(--mono);
    font-size: 0.72rem;
    color: var(--text-3);
    margin-top: 2px;
    letter-spacing: 0.04em;
  }

  .info-rows {
    padding: 8px 0;
  }

  .row {
    display: flex;
    align-items: flex-start;
    gap: 14px;
    padding: 14px 24px;
    border-bottom: 1px solid var(--border);
    transition: background .15s;
  }

  .row:last-child { border-bottom: none; }
  .row:hover { background: var(--surface); }

  .row-icon { font-size: 1.1rem; flex-shrink: 0; margin-top: 1px; }

  .row-label {
    font-family: var(--mono);
    font-size: 0.7rem;
    color: var(--text-3);
    letter-spacing: 0.07em;
    text-transform: uppercase;
    margin-bottom: 2px;
  }

  .row-val {
    font-size: 0.88rem;
    color: var(--text);
    font-weight: 500;
  }

  @media (max-width: 900px) {
    .grid { grid-template-columns: 1fr; gap: 40px; }
  }
</style>
-->