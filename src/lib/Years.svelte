<script>
  import { base } from "$app/paths";

  const year3 = {
    label: '3° Anno',
    period: '2023 / 2024',
    projects: [
      {
        title: 'Calcolatore Codice Fiscale',
        desc: 'Partendo dalle informazioni personali (nome, cognome, data e luogo di nascita, sesso) il programma calcola automaticamente il codice fiscale secondo le regole ufficiali.',
        tags: ['C'],
        href: 'https://github.com/Macchi-Federico/Codice-Fiscale',
        file: `${base}/presentazioni/FedericoMacchi _Codice-Fiscale.pptx`,
      },
      {
        title: 'La Mattanza',
        desc: 'ELABORATO A PARTIRE DA "LA MATTANZA".',
        tags: ['Italiano'],
        file: `${base}/presentazioni/LA_MATTANZA.pdf`,
      },
      {
        title: 'La Zoomafia',
        desc: 'ELABORATO A PARTIRE DA "LA MATTANZA".',
        tags: ['Italiano'],
        file: `${base}/presentazioni/ZOOMAFIA.pdf`,
      },
    ],
  };

  const year4 = {
    label: '4° Anno',
    period: '2024 / 2025',
    subjects: ['Informatica', 'Sistemi & Reti', 'TPSIT'],
    projects: [
      {
        title: 'Quiz Patente',
        desc: "Web app per prepararsi all'esame teorico della patente. L'utente risponde a domande a scelta multipla con feedback immediato e punteggio finale.",
        tags: ['Python', 'Tkinter'],
        href: 'https://github.com/Macchi-Federico/Quiz_Patente',
      },
    ],
  };

  const year5 = {
    label: '5° Anno',
    period: '2025 / 2026',
    subjects: ['Informatica', 'Sistemi & Reti', 'TPSIT', 'Gestione Progetto'],
    projects: [
      {
        title: 'App 1522',
        desc: "Applicazione web per la gestione delle richieste di supporto al numero antiviolenza 1522. Sviluppata con Django, include autenticazione, form di contatto e pannello admin.",
        tags: ['Python', 'Django', 'HTML/CSS'],
        href: 'https://github.com/Macchi-Federico/1522',
      },
      {
        title: 'Prigione Domestica',
        desc: "Presentazione per educazione civica sul tema della prigionia domestica e della libertà. Analisi del fenomeno con riflessioni personali.",
        tags: ['Italiano'],
        file: `${base}/presentazioni/La-Prigione-Domestica-Dati-Psicologia-e-Diritto.pdf`,
      },
      {
        title: 'How to Use the Internet Safely',
        desc: "An analysis of the main risks of the web and best practices for a conscious and safe use of the internet.",
        tags: ['Inglese'],
      },
      {
        title: 'Incontro con Roberto Saviano',
        desc: "Dialogo con lo scrittore a partire dal suo libro",
        tags: ['Italiano'],
      },
      {
        title: 'Artificial Intelligence',
        desc: "Advantages and Disadvantages of AI",
        tags: ['Inglese'],
      },
      {
        title: 'Primo Levi e la "zona grigia"',
        desc: "Riflessione sulla prigionia nei campi di concentramento attraverso la testimonianza di Levi e il concetto di vergogna del sopravvissuto",
        tags: ['Italiano'],
      },
      {
        title: 'Aktion T4 e Lebensborn',
        desc: "Approfondimento su due programmi del regime nazista: l'eliminazione sistematica delle persone con disabilità e il progetto di selezione eugenetica promosso dalle SS.",
        tags: ['Italiano'],
      },
      {
        title: 'La Costituzione italiana',
        desc: "Studio degli articoli 1-12, fondamento dei diritti e dei doveri che regolano la convivenza civile nella Repubblica italiana.",
        tags: ['Italiano'],
      },
      {
        title: "Il '68",
        desc: "Analisi del movimento studentesco e sociale del 1968, tra proteste, ideali e trasformazioni culturali durature.",
        tags: ['Italiano'],
      },
      {
        title: 'Water and Soil Pollution',
        desc: "An examination of the causes and consequences of environmental pollution, alongside the key measures and policies for its prevention and mitigation.",
        tags: ['Inglese'],
      },
      {
        title: 'Social and Ethical Problems of the Internet',
        desc: "A reflection on the social and ethical challenges posed by the internet, including privacy, misinformation, digital inequality and online behaviour.",
        tags: ['Inglese'],
      },
    ],
  };
</script>
<!-- ============ 3° Anno ============ -->
<section id="year3" class="year-section year-violet">
  <div class="container">
    <div class="year-eyebrow">
      <span class="year-bubble violet">3°</span>
      <div>
        
        <p class="year-period">2023 / 2024</p>
      </div>
    </div>

    <h2 class="heading year-heading">{year3.label} <span class="accent-violet"></span></h2>
    <p class="year-desc">{year3.description}</p>

    <div class="subjects-row">
      {#each year3.subjects as s}
        <span class="chip violet">{s}</span>
      {/each}
    </div>

    <div class="projects-grid">
      {#each year3.projects as p}
        <div class="pcard pcard-violet">
          <div class="pcard-inner">
            <div class="pcard-header">
              <h3>{p.title}</h3>
              {#if p.href}
                <a href={p.href} target="_blank" rel="noopener" class="gh-link violet" title="Vedi su GitHub">
                  <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.3 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61-.546-1.385-1.335-1.755-1.335-1.755-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 21.795 24 17.295 24 12c0-6.63-5.37-12-12-12z"/></svg>
                </a>
              {/if}
            </div>
            <p class="pcard-desc">{p.desc}</p>
            <div class="pcard-tags">
              {#each p.tags as t}
                <span class="chip violet">{t}</span>
              {/each}
            </div>
            <div class="pcard-actions">
              {#if p.href}
                <a href={p.href} target="_blank" rel="noopener" class="pcard-cta violet">
                  Vedi progetto <span>→</span>
                </a>
              {/if}
              {#if p.file}
                <a href={p.file} download class="pcard-dl">
                  <svg width="14" height="14" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v2a2 2 0 002 2h12a2 2 0 002-2v-2M7 10l5 5 5-5M12 15V3"/>
                  </svg>
                  Scarica presentazione
                </a>
              {/if}
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- ============ 4° Anno ============ -->
<section id="year4" class="year-section year-orange">
  <div class="container">
    <div class="year-eyebrow">
      <span class="year-bubble orange">4°</span>
      <div>
      
        <p class="year-period">2024 / 2025</p>
      </div>
    </div>

    <h2 class="heading year-heading">{year4.label} <span class="accent-orange"></span></h2>
    <p class="year-desc">{year4.description}</p>

    <div class="subjects-row">
      {#each year4.subjects as s}
        <span class="chip orange">{s}</span>
      {/each}
    </div>

    <div class="projects-grid">
      {#each year4.projects as p}
        <div class="pcard pcard-orange">
          <div class="pcard-inner">
            <div class="pcard-header">
              <h3>{p.title}</h3>
              {#if p.href}
                <a href={p.href} target="_blank" rel="noopener" class="gh-link orange" title="Vedi su GitHub">
                  <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.3 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61-.546-1.385-1.335-1.755-1.335-1.755-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 21.795 24 17.295 24 12c0-6.63-5.37-12-12-12z"/></svg>
                </a>
              {/if}
            </div>
            <p class="pcard-desc">{p.desc}</p>
            <div class="pcard-tags">
              {#each p.tags as t}
                <span class="chip orange">{t}</span>
              {/each}
            </div>
            <div class="pcard-actions">
              {#if p.href}
                <a href={p.href} target="_blank" rel="noopener" class="pcard-cta orange">
                  Vedi progetto <span>→</span>
                </a>
              {/if}
              {#if p.file}
                <a href={p.file} download class="pcard-dl">
                  <svg width="14" height="14" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v2a2 2 0 002 2h12a2 2 0 002-2v-2M7 10l5 5 5-5M12 15V3"/>
                  </svg>
                  Scarica presentazione
                </a>
              {/if}
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- ============ 5° Anno ============ -->
<section id="year5" class="year-section year-green">
  <div class="container">
    <div class="year-eyebrow">
      <span class="year-bubble green">5°</span>
      <div>
        
        <p class="year-period">2025 / 2026</p>
      </div>
    </div>

    <h2 class="heading year-heading">{year5.label} <span class="accent-green"></span></h2>
    <p class="year-desc">{year5.description}</p>

    <div class="subjects-row">
      {#each year5.subjects as s}
        <span class="chip green">{s}</span>
      {/each}
    </div>

    <div class="projects-grid">
      {#each year5.projects as p}
        <div class="pcard pcard-green">
          <div class="pcard-inner">
            <div class="pcard-header">
              <h3>{p.title}</h3>
              {#if p.href}
                <a href={p.href} target="_blank" rel="noopener" class="gh-link green" title="Vedi su GitHub">
                  <svg width="18" height="18" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.3 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61-.546-1.385-1.335-1.755-1.335-1.755-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 21.795 24 17.295 24 12c0-6.63-5.37-12-12-12z"/></svg>
                </a>
              {/if}
            </div>
            <p class="pcard-desc">{p.desc}</p>
            <div class="pcard-tags">
              {#each p.tags as t}
                <span class="chip green">{t}</span>
              {/each}
            </div>
            <div class="pcard-actions">
              {#if p.href}
                <a href={p.href} target="_blank" rel="noopener" class="pcard-cta green">
                  Vedi progetto <span>→</span>
                </a>
              {/if}
              {#if p.file}
                <a href={p.file} download class="pcard-dl">
                  <svg width="14" height="14" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M4 16v2a2 2 0 002 2h12a2 2 0 002-2v-2M7 10l5 5 5-5M12 15V3"/>
                  </svg>
                  Scarica presentazione
                </a>
              {/if}
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .year-section {
    border-top: 1px solid var(--border);
    position: relative;
  }

  .year-violet { background: #fdfcff; }
  .year-orange { background: #fffcfa; }
  .year-green  { background: #fafffe; }

  .year-violet::before,
  .year-orange::before,
  .year-green::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 4px;
    border-radius: 0 4px 4px 0;
  }
  .year-violet::before { background: var(--violet); }
  .year-orange::before { background: var(--orange); }
  .year-green::before  { background: var(--green); }

  .year-eyebrow {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 28px;
  }

  .year-bubble {
    width: 64px; height: 64px;
    border-radius: 18px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.6rem;
    font-weight: 900;
    letter-spacing: -0.05em;
    flex-shrink: 0;
    line-height: 1;
  }

  .year-bubble.violet { background: var(--violet-light); color: var(--violet); }
  .year-bubble.orange { background: var(--orange-light); color: var(--orange); }
  .year-bubble.green  { background: var(--green-light);  color: var(--green); }

  .year-period {
    font-family: var(--mono);
    font-size: 0.82rem;
    color: var(--text-3);
    letter-spacing: 0.06em;
    margin-top: 2px;
  }

  .year-heading { margin-bottom: 16px; }

  .accent-violet { color: var(--violet); }
  .accent-orange { color: var(--orange); }
  .accent-green  { color: var(--green); }

  .year-desc {
    font-size: 1.05rem;
    color: var(--text-2);
    line-height: 1.8;
    max-width: 680px;
    margin-bottom: 28px;
  }

  .subjects-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 40px;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
  }

  .pcard {
    border-radius: 20px;
    border: 1px solid var(--border);
    background: var(--bg-card);
    box-shadow: var(--shadow-sm);
    transition: transform .2s, box-shadow .2s;
    overflow: hidden;
  }

  .pcard:hover {
    transform: translateY(-5px);
    box-shadow: var(--shadow-lg);
  }

  .pcard-violet { border-top: 3px solid var(--violet); }
  .pcard-orange { border-top: 3px solid var(--orange); }
  .pcard-green  { border-top: 3px solid var(--green); }

  .pcard-inner {
    padding: 24px;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }

  .pcard-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 12px;
  }

  .pcard-header h3 {
    font-size: 1.05rem;
    font-weight: 700;
    color: var(--text);
    letter-spacing: -0.02em;
    line-height: 1.3;
  }

  .gh-link {
    flex-shrink: 0;
    padding: 6px;
    border-radius: 8px;
    transition: background .15s, color .15s;
    display: flex;
  }

  .gh-link.violet { color: var(--violet); }
  .gh-link.orange { color: var(--orange); }
  .gh-link.green  { color: var(--green); }
  .gh-link:hover  { background: var(--surface); }

  .pcard-desc {
    font-size: 0.88rem;
    color: var(--text-2);
    line-height: 1.65;
    flex: 1;
  }

  .pcard-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  /* ---- bottoni azioni ---- */
  .pcard-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    align-items: center;
  }

  .pcard-cta {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-size: 0.83rem;
    font-weight: 600;
    border-radius: 8px;
    padding: 8px 14px;
    transition: filter .15s;
  }

  .pcard-cta span { transition: transform .15s; }
  .pcard-cta:hover span { transform: translateX(3px); }

  .pcard-cta.violet { color: var(--violet); background: var(--violet-light); }
  .pcard-cta.orange { color: var(--orange); background: var(--orange-light); }
  .pcard-cta.green  { color: var(--green);  background: var(--green-light); }
  .pcard-cta:hover  { filter: brightness(.95); }

  /* bottone download — stile neutro grigio */
  .pcard-dl {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    font-size: 0.83rem;
    font-weight: 600;
    border-radius: 8px;
    padding: 8px 14px;
    color: var(--text-2);
    background: var(--surface);
    border: 1px solid var(--border);
    transition: background .15s, color .15s, border-color .15s;
  }

  .pcard-dl:hover {
    background: var(--border);
    color: var(--text);
    border-color: var(--border-2);
  }

  @media (max-width: 640px) {
    .projects-grid { grid-template-columns: 1fr; }
  }
</style>