<!--
  mediation/+page.svelte
  Content sourced from https://birchstreetlaw.com/mediation/
-->
<script>
  import BirchDivider from '$lib/BirchDivider.svelte';

  /** FAQ accordion state — tracks which item is open */
  let openIndex = $state(null);

  function toggle(i) {
    openIndex = openIndex === i ? null : i;
  }

  const faqs = [
    {
      q: 'What is Mediation?',
      a: `Mediation is a way for two or more people who have a conflict to reach a resolution outside of court. Mediation is impartial, confidential, and voluntary. The mediator's role is to facilitate a civil, fair conversation in which both people can be heard in a safe environment with the goal of reaching agreements. Those agreements can become a court order or a contract that is legally binding, or it can be an informal agreement that the parties promise to follow through on.

Mediation can be done with everyone in the same room, talking direct to one another with the mediator facilitating that conversation. Mediation can also be done with the parties in different rooms, with the mediator moving between those rooms and sharing information only with the party's permission. Often, mediation is a blend of those two styles.`
    },
    {
      q: 'Does the Mediator Decide My Case?',
      a: `No, the mediator's role is to be neutral and to help the parties reach their own agreements. Ms. Zinn has extensive experience in the neutral role that mediation requires. She is a retired Washington State Superior Court Commissioner who has 18 years of experience in trial and appeals courts, expertise in multiple areas of law, and a practical understanding of what is at stake to have a judicial officer decide your case or to go to trial.

She will only share her experience and understanding when the parties want that information. Further, that information is not legal advice or meant to sway the parties' decisions, but it can be used as background information to help reach resolutions. The parties can have their own lawyers present and, if they do, Ms. Zinn highly encourages the parties to listen to their lawyer's advice.`
    },
    {
      q: 'Is My Case Ready for Mediation?',
      a: `Mediation is a voluntary process. Parties must be willing and able to negotiate in good faith to resolve their case. In order to mediate, all of the people who are needed to make a decision in the case must be present. Parties can mediate with or without a lawyer.

Some cases may not be right for mediation, including cases in which there is a pending guardian ad litem (GAL) report, CPS is actively involved, or there is an active domestic violence protection order for the parties. The Court might require you to go to mediation whether you feel ready or not. If you do not feel ready to mediate but it is court-ordered, Ms. Zinn will guide you through how to fulfill your court obligation.`
    },
    {
      q: 'What Are the Fees?',
      a: `Rebekah Zinn's hourly rate is $345.00 per hour. For mediations, Ms. Zinn charges a four-hour minimum that may be non-refundable. The four-hour minimum begins with an hour for preparing to mediate the case. Ms. Zinn charges a reduced rate of $165.00 for attorney travel time.

The parties usually split the fee evenly. Unless there is a court order or agreement to pay in a different way, each party is responsible for their portion of the fee. Ms. Zinn requires prepayment of a deposit for a four-hour minimum of time, which is $1,380.00 in total or $690.00 each for two parties who are splitting the fee evenly. This is only a deposit towards work that is actually performed. Additional time will be billed to the parties and is expected to be promptly paid.`
    },
    {
      q: 'How Is Mediation Scheduled?',
      a: `Mediations are generally scheduled for an entire day, up to eight hours (9–5 p.m.) unless it is agreed by all parties and the mediator to extend the session beyond 5 p.m. or to a second mediation session when needed.

The parties and their lawyers must be prepared to attend the mediation all day and agree to not double-book themselves that day. Rest breaks will be provided as needed.

Ms. Zinn wants mediation to work for everyone, so please let her or her staff know if any accommodations are needed or desired.`
    },
    {
      q: 'How Should I Prepare?',
      a: `Ms. Zinn encourages the parties to prepare a Mediation Statement, which is a statement of the issues for mediation, what you are seeking to accomplish, and why you believe the facts and law support your position. This Mediation Statement may be up to 10 pages, double-spaced. Additionally, the parties can attach additional evidence and key portions of the court record to the Mediation Statement.

Ms. Zinn will not research the case file, facts, or law and will limit preparation to the materials that the parties presented. She will limit preparation to one hour total without the express agreement of both parties. Mediation Statements are due to the Mediator and the other party three business days before the Mediation.

The parties will be encouraged to have separate, brief telephone conferences with Ms. Zinn before the mediation. This will help Ms. Zinn understand how best to achieve settlement in the case.

For those attending mediation in-person, bringing a lunch and snacks is highly recommended. Bring items that will help you be comfortable throughout the day. Having a laptop or notebook can also be useful. Attorneys are encouraged to be prepared to write a settlement agreement during the mediation and potentially have it signed that day.`
    },
    {
      q: 'Where Is Mediation Held?',
      a: `Mediation can be in-person at Birch Street Law in Shelton, Washington, or another location convenient to the parties and agreed ahead of time. Zoom mediation is available as well.`
    },
  ];
</script>

<svelte:head>
  <title>Mediation Services — Birch Street Law PLLC</title>
  <meta name="description" content="Rebekah Zinn offers professional mediation services in Washington State. Resolve disputes outside of court — confidential, impartial, and effective." />
</svelte:head>

<!-- Page Hero -->
<div class="page-hero">
  <div class="container">
    <h1>Mediation Services</h1>
    <p>Resolve disputes outside of court — with a neutral, experienced mediator on your side.</p>
  </div>
</div>

<!-- Intro -->
<section class="section">
  <div class="container">
    <div class="mediation-intro">
      <div>
        <h2>Why Consider Mediation?</h2>
        <p>
          Going to court is expensive, slow, and uncertain. Mediation offers a confidential, 
          voluntary process where the parties — not a judge — determine the outcome. It's often 
          faster, less costly, and produces more creative and durable resolutions than litigation.
        </p>
        <p>
          Rebekah Zinn brings 18 years of experience as a Washington State Superior Court 
          Commissioner to every mediation. She understands the law, the courts, and — most 
          importantly — what it takes to help people find common ground.
        </p>
        <a href="/contact" class="btn btn-primary mt-3">Schedule Mediation</a>
      </div>
      <div class="mediation-highlights">
        {#each [
          { label: 'Confidential', desc: 'What happens in mediation stays in mediation.' },
          { label: 'Neutral', desc: 'Ms. Zinn has no stake in the outcome — only in your success.' },
          { label: 'Voluntary', desc: 'Agreements are reached by the parties themselves.' },
          { label: 'Efficient', desc: 'Resolve in one day what could take months in court.' },
        ] as h}
          <div class="highlight-item">
            <div>
              <strong>{h.label}</strong>
              <p>{h.desc}</p>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>

<BirchDivider />

<!-- FAQ Accordion -->
<section class="section section--alt">
  <div class="container">
    <div class="text-center mb-4">
      <h2>Frequently Asked Questions</h2>
      <p class="text-muted">Everything you need to know about the mediation process.</p>
    </div>

    <div class="faq-list">
      {#each faqs as faq, i}
        <div class="faq-item">
          <button
            class="faq-question"
            onclick={() => toggle(i)}
            aria-expanded={openIndex === i}
          >
            <span>{faq.q}</span>
            <svg class="faq-icon" style="transform: {openIndex === i ? 'rotate(45deg)' : 'rotate(0)'}" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" aria-hidden="true">
              <line x1="12" y1="5" x2="12" y2="19"/>
              <line x1="5" y1="12" x2="19" y2="12"/>
            </svg>
          </button>
          {#if openIndex === i}
            <div class="faq-answer">
              {#each faq.a.trim().split('\n\n') as para}
                <p>{para}</p>
              {/each}
            </div>
          {/if}
        </div>
      {/each}
    </div>
  </div>
</section>

<!-- CTA -->
<section class="section section--dark">
  <div class="container text-center">
    <h2>Ready to Mediate?</h2>
    <p class="cta-sub">
      Contact Birch Street Law to discuss whether mediation is right for your situation, 
      or to schedule a session with Rebekah Zinn.
    </p>
    <div class="cta-actions mt-4">
      <a href="tel:13603587445" class="btn btn-gold">(360) 358-7445</a>
      <a href="/contact" class="btn btn-outline-cream">Contact Us</a>
    </div>
  </div>
</section>

<style>
  /* Intro grid */
  .mediation-intro {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
    align-items: start;
  }

  @media (max-width: 768px) {
    .mediation-intro {
      grid-template-columns: 1fr;
    }
  }

  .mediation-highlights {
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
  }

  .highlight-item {
    padding: 1rem 1.25rem;
    background: var(--white);
    border-radius: var(--radius);
    box-shadow: var(--shadow-sm);
    border-left: 4px solid var(--gold);
  }

  .highlight-item strong {
    display: block;
    font-family: var(--font-serif);
    color: var(--navy);
    font-size: 1rem;
    font-weight: 600;
    margin-bottom: 0.15rem;
  }

  .highlight-item p {
    font-size: 0.875rem;
    color: var(--gray-warm);
    margin: 0;
  }

  /* FAQ */
  .faq-list {
    max-width: 820px;
    margin-inline: auto;
  }

  .faq-item {
    border-bottom: 1px solid var(--cream);
    padding-block: 1.5rem;
  }

  .faq-item:first-child {
    border-top: 1px solid var(--cream);
  }

  .faq-question {
    font-family: var(--font-serif);
    font-size: 1.1rem;
    color: var(--navy);
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 1rem;
    user-select: none;
    background: none;
    border: none;
    width: 100%;
    text-align: left;
    padding: 0;
  }

  .faq-icon {
    flex-shrink: 0;
    width: 22px;
    height: 22px;
    color: var(--gold);
    transition: transform 0.2s ease;
  }

  .faq-answer {
    margin-top: 1rem;
    max-width: 72ch;
  }

  .faq-answer p {
    color: var(--gray-dark);
    font-size: 0.95rem;
    line-height: 1.8;
  }

  /* CTA section */
  .cta-sub {
    color: var(--gold-light);
    max-width: 520px;
    margin-inline: auto;
    margin-top: 0.75rem;
  }

  .cta-actions {
    display: flex;
    gap: 1rem;
    justify-content: center;
    flex-wrap: wrap;
  }

  .btn-gold {
    display: inline-block;
    padding: 0.75rem 1.75rem;
    border-radius: var(--radius);
    font-family: var(--font-sans);
    font-size: 0.9rem;
    font-weight: 600;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    cursor: pointer;
    transition: all var(--transition);
    text-decoration: none !important;
    background-color: var(--gold);
    color: var(--navy);
    border: 2px solid var(--gold);
  }

  .btn-gold:hover {
    background-color: var(--gold-light);
    border-color: var(--gold-light);
    color: var(--navy);
  }

  .btn-outline-cream {
    display: inline-block;
    padding: 0.75rem 1.75rem;
    border-radius: var(--radius);
    font-family: var(--font-sans);
    font-size: 0.9rem;
    font-weight: 500;
    letter-spacing: 0.04em;
    text-transform: uppercase;
    cursor: pointer;
    transition: all var(--transition);
    text-decoration: none !important;
    background-color: transparent;
    color: var(--cream);
    border: 2px solid rgba(245,240,232,0.5);
  }

  .btn-outline-cream:hover {
    background-color: rgba(245,240,232,0.12);
    border-color: var(--cream);
    color: var(--cream);
  }
</style>
