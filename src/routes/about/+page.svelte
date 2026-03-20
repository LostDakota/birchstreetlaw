<!--
  about/+page.svelte — Attorney Bios
-->
<script>
  import BirchDivider from '$lib/BirchDivider.svelte';
</script>

<svelte:head>
  <title>About Our Attorneys — Birch Street Law PLLC</title>
  <meta name="description" content="Meet the attorneys of Birch Street Law PLLC: David P. Sisk (Managing Attorney) and Rebekah Zinn (Retired Superior Court Commissioner and Mediator)." />
</svelte:head>

<!-- Page Hero -->
<div class="page-hero">
  <div class="container">
    <h1>Our Attorneys</h1>
    <p>Experienced, caring advocates who understand what's at stake.</p>
  </div>
</div>

<!-- David Sisk -->
<section class="section">
  <div class="container">
    <div class="bio-layout">
      <div class="bio-avatar">
        <div class="bio-initial" aria-hidden="true">DS</div>
      </div>
      <div class="bio-content">
        <p class="bio-title">Managing Attorney</p>
        <h2>David P. Sisk</h2>
        <p class="bio-focus">
          Probate &bull; Guardianship &bull; Real Estate &bull; Estate Planning &bull; TEDRA Litigation
        </p>

        <p>
          Attorney David P. Sisk brings a diverse background to his practice, which concentrates on 
          probate, guardianship, real estate, estate planning, and probate litigation, including TEDRA. 
          David previously practiced as a general litigation attorney and decided to narrow his focus 
          to areas he is passionate about — helping elderly and vulnerable individuals, as well as 
          families who need assistance navigating challenging life and end-of-life events.
        </p>
        <p>
          David also enjoys assisting homeowners with issues involving easements, boundary line disputes, 
          and real estate transactions.
        </p>
        <p>
          David understands how upsetting the loss or incapacity of a loved one can be. He knows he 
          cannot spare clients the grief that comes with loss, but he hopes to put their minds at ease 
          regarding legal questions so families can focus on their own needs. Having seen the impact of 
          poorly-crafted wills and trusts, David also offers estate planning services designed to 
          minimize the risk of future disputes.
        </p>
        <p>
          For contested matters, it is essential to have an attorney who is familiar with the law and 
          comfortable in the courtroom. David's philosophy in litigation is to apply a collaborative 
          and holistic approach — looking at the big picture and working with other parties to resolve 
          issues rather than incurring emotional and financial costs in prolonged litigation.
        </p>
        <p>
          David is originally from Ohio, where he spent over ten years working in state and local 
          government, including three years in the state legislature. He spent two years living and 
          working in South Korea as an English teacher, where he eventually met his wife Sooyoung. 
          David is a graduate of Youngstown State University (B.A., pre-law and writing) and 
          Rutgers School of Law – Newark, where he was Chair of the Rutgers Moot Court Board and 
          a finalist in multiple moot court competitions.
        </p>
        <p>
          When not practicing law, David spends time gardening and restoring old homes with Sooyoung. 
          He also loves hiking and camping on the Olympic Peninsula, and kayaking on the Hood Canal.
        </p>
        <a href="tel:13603587445" class="btn btn-primary mt-3">(360) 358-7445</a>
      </div>
    </div>
  </div>
</section>

<BirchDivider />

<!-- Rebekah Zinn -->
<section class="section section--alt">
  <div class="container">
    <div class="bio-layout">
      <div class="bio-avatar">
        <div class="bio-initial bio-initial--green" aria-hidden="true">RZ</div>
      </div>
      <div class="bio-content">
        <p class="bio-title">Mediator &amp; Of Counsel</p>
        <h2>Rebekah Zinn</h2>
        <p class="bio-focus">
          Mediation &bull; Dispute Resolution &bull; Family Law &bull; Probate &bull; Civil Litigation
        </p>

        <p>
          Rebekah Zinn is a retired Washington State Superior Court Commissioner with 18 years of 
          experience in trial and appellate courts. Her deep expertise spans multiple areas of law, 
          and she brings a practical, grounded understanding of what is truly at stake when a 
          judicial officer decides a case.
        </p>
        <p>
          As a mediator, Ms. Zinn's role is to be neutral — to help parties reach their own 
          agreements. She facilitates civil, fair conversations where all voices can be heard in 
          a safe environment. She will share her experience and understanding only when the parties 
          request it, and solely as background information to help reach resolutions — not as 
          legal advice intended to sway any decision.
        </p>
        <p>
          Ms. Zinn believes mediation can be transformative. By resolving disputes outside of court, 
          parties often achieve outcomes that are more creative, more lasting, and less costly — 
          financially and emotionally — than going to trial.
        </p>
        <p>
          Ms. Zinn highly encourages parties who have attorneys to bring them to mediation and 
          to listen carefully to their lawyers' counsel throughout the process.
        </p>
        <a href="/mediation" class="btn btn-primary mt-3">Learn About Mediation</a>
      </div>
    </div>
  </div>
</section>

<style>
  .bio-layout {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 2.5rem;
    align-items: start;
  }

  @media (max-width: 640px) {
    .bio-layout {
      grid-template-columns: 1fr;
    }
  }

  .bio-avatar {
    padding-top: 0.5rem;
  }

  .bio-initial {
    width: 88px;
    height: 88px;
    border-radius: 50%;
    background-color: var(--green-deep);
    color: var(--white);
    font-family: var(--font-serif);
    font-size: 1.6rem;
    font-weight: 600;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    letter-spacing: 0.05em;
  }

  .bio-initial--green {
    background-color: var(--green-mid);
  }

  .bio-title {
    font-size: 0.8rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--green-mid);
    margin-bottom: 0.25rem;
  }

  .bio-focus {
    font-size: 0.875rem;
    color: var(--gray-warm);
    margin-bottom: 1.5rem;
    font-style: italic;
  }

  .bio-content h2 {
    margin-bottom: 0.25rem;
  }
</style>
