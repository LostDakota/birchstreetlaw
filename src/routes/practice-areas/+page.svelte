<!--
  practice-areas/+page.svelte — Full Practice Areas page
-->
<script>
  import BirchDivider from '$lib/BirchDivider.svelte';

  const areas = [
    {
      id: 'probate',
      title: 'Probate',
      icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>`,
      summary: 'Administering a deceased person\'s estate through Washington\'s probate process.',
      body: `When a loved one passes, their estate often needs to go through probate — the legal process by which a court supervises the distribution of assets, payment of debts, and transfer of property. Probate can be straightforward or complex depending on the nature of the estate.

Birch Street Law assists personal representatives (executors) and heirs with:
- Opening and closing probate estates
- Identifying and inventorying assets
- Notifying creditors and resolving claims
- Distributing assets to beneficiaries
- Small estate affidavits and non-probate transfers
- Intestate succession (estates without a will)

We guide our clients through every step, from filing the petition to final distribution, with clear communication throughout.`
    },
    {
      id: 'guardianship',
      title: 'Guardianship',
      icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>`,
      summary: 'Legal protection for minors and incapacitated adults who cannot care for themselves.',
      body: `Guardianship proceedings establish a court-supervised relationship in which a responsible adult (the guardian) is authorized to make decisions for a person who cannot make decisions for themselves — whether due to age, disability, or incapacity.

Birch Street Law handles:
- Guardianship petitions for minors
- Guardianship and conservatorship for incapacitated adults
- Limited guardianships tailored to the individual's actual needs
- Emergency guardianship proceedings
- Annual reporting and court compliance
- Contested guardianship matters

David Sisk is passionate about protecting vulnerable individuals and ensuring that guardianship orders reflect the least-restrictive approach needed to keep a person safe.`
    },
    {
      id: 'tedra',
      title: 'Trust & Estate Disputes (TEDRA)',
      icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg>`,
      summary: 'Litigation and dispute resolution for trust and estate conflicts under Washington\'s TEDRA.',
      body: `Washington's Trust and Estate Dispute Resolution Act (TEDRA) provides a framework for resolving disputes involving trusts, wills, powers of attorney, and estates — both through litigation and non-judicial settlement agreements.

Birch Street Law represents clients in TEDRA matters including:
- Will contests (undue influence, lack of capacity, fraud)
- Trustee removal and surcharge actions
- Breach of fiduciary duty claims
- Accounting disputes
- Non-judicial settlement agreements (NJSAs)
- Modification or termination of trusts
- Determination of heirship

David's litigation background and commitment to collaborative resolution mean he approaches TEDRA cases strategically — pursuing cost-effective outcomes while maintaining the ability to litigate effectively when necessary.`
    },
    {
      id: 'estate-planning',
      title: 'Estate Planning',
      icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg>`,
      summary: 'Wills, trusts, and advance directives that protect your family and carry out your wishes.',
      body: `Estate planning is one of the most important gifts you can give your family. A well-crafted estate plan ensures your wishes are carried out, minimizes potential for disputes, and eases the burden on loved ones during an already difficult time.

Birch Street Law provides:
- Last wills and testaments
- Revocable living trusts
- Durable powers of attorney
- Healthcare directives and living wills
- Beneficiary designation review
- Estate plan updates and amendments
- Planning for blended families and complex situations

Having witnessed the consequences of poorly-drafted estate documents, David designs plans that are clear, thorough, and tailored to each family's unique circumstances.`
    },
    {
      id: 'elder-protection',
      title: 'Elder & Vulnerable Adult Protection',
      icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/></svg>`,
      summary: 'Vulnerable Adult Protection Orders (VAPOs) and advocacy for those at risk.',
      body: `Washington law provides important protections for elderly and vulnerable adults who are at risk of abuse, neglect, exploitation, or abandonment. Birch Street Law helps families and individuals navigate these legal tools when it matters most.

We assist with:
- Vulnerable Adult Protection Orders (VAPOs)
- Financial exploitation claims
- Elder abuse and neglect proceedings
- Coordination with Adult Protective Services matters
- Emergency legal interventions

If you are concerned about the safety or welfare of an elderly or vulnerable loved one, contact us promptly. Time is often critical in these situations.`
    },
    {
      id: 'real-estate',
      title: 'Real Estate',
      icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>`,
      summary: 'Easements, boundary disputes, and real estate transactions in Washington.',
      body: `Property matters can be complicated, especially in rural and coastal Washington where easements and boundary issues are common. Birch Street Law helps homeowners, landowners, and buyers resolve real estate legal questions efficiently.

Services include:
- Easement disputes and access rights
- Boundary line disputes and quiet title actions
- Real estate transaction review and counsel
- Title issues and clouds on title
- Neighbor disputes with legal dimensions
- Real property aspects of estate and probate matters

David understands the deep attachment people have to their land and homes, and he works to protect his clients' property rights while keeping disputes from escalating unnecessarily.`
    }
  ];
</script>

<svelte:head>
  <title>Practice Areas — Birch Street Law PLLC</title>
  <meta name="description" content="Birch Street Law PLLC handles probate, guardianship, estate planning, TEDRA litigation, elder protection, and real estate matters in Washington State." />
</svelte:head>

<!-- Page Hero -->
<div class="page-hero">
  <div class="container">
    <h1>Practice Areas</h1>
    <p>We focus on the areas of law that matter most to families and individuals navigating life's transitions.</p>
  </div>
</div>

<!-- Quick nav -->
<div class="quick-nav-wrap">
  <div class="container">
    <nav class="quick-nav" aria-label="Jump to practice area">
      {#each areas as area}
        <a href="#{area.id}" class="quick-nav-link">{area.title}</a>
      {/each}
    </nav>
  </div>
</div>

<!-- Practice area detail sections -->
{#each areas as area, i}
  <section id={area.id} class="section" class:section--alt={i % 2 === 1}>
    <div class="container">
      <div class="area-layout">
        <div class="area-icon">
          {@html area.icon}
        </div>
        <div class="area-body">
          <h2>{area.title}</h2>
          <p class="area-summary">{area.summary}</p>
          <BirchDivider />
          <div class="area-content">
            {#each area.body.trim().split('\n\n') as para}
              {#if para.startsWith('-')}
                <ul>
                  {#each para.split('\n') as item}
                    {#if item.startsWith('- ')}
                      <li>{item.slice(2)}</li>
                    {/if}
                  {/each}
                </ul>
              {:else}
                <p>{para}</p>
              {/if}
            {/each}
          </div>
        </div>
      </div>
    </div>
  </section>
{/each}

<!-- CTA -->
<section class="section section--dark">
  <div class="container text-center">
    <h2>Questions About Your Situation?</h2>
    <p style="color: var(--gold-light); max-width: 540px; margin-inline: auto; margin-top: 0.75rem;">
      Every legal matter is unique. Contact Birch Street Law to discuss your specific circumstances 
      and learn how we can help.
    </p>
    <a href="/contact" class="btn btn-light mt-4">Get in Touch</a>
  </div>
</section>

<style>
  /* Quick nav */
  .quick-nav-wrap {
    background: var(--white);
    border-bottom: 1px solid var(--cream-dark);
    position: sticky;
    top: var(--nav-height);
    z-index: 50;
  }

  .quick-nav {
    display: flex;
    flex-wrap: wrap;
    gap: 0;
    overflow-x: auto;
    padding-block: 0.5rem;
  }

  .quick-nav-link {
    padding: 0.4rem 0.9rem;
    font-size: 0.8rem;
    font-weight: 500;
    color: var(--gray-warm);
    border-radius: var(--radius);
    white-space: nowrap;
    text-decoration: none !important;
    transition: color var(--transition), background-color var(--transition);
  }

  .quick-nav-link:hover {
    color: var(--navy);
    background-color: var(--cream);
  }

  /* Area layout */
  .area-layout {
    display: grid;
    grid-template-columns: 56px 1fr;
    gap: 2rem;
    align-items: start;
  }

  @media (max-width: 640px) {
    .area-layout {
      grid-template-columns: 1fr;
    }
  }

  .area-icon {
    width: 48px;
    height: 48px;
    color: var(--gold);
    margin-top: 0.5rem;
  }

  .area-icon :global(svg) {
    width: 100%;
    height: 100%;
  }

  .area-summary {
    font-size: 1.05rem;
    color: var(--gray-warm);
    font-style: italic;
    margin-bottom: 0.5rem;
  }

  .area-content {
    margin-top: 0.5rem;
  }

  .area-content :global(ul) {
    padding-left: 1.4rem;
    margin-bottom: 1rem;
  }

  .area-content :global(li) {
    margin-bottom: 0.35rem;
    color: var(--gray-dark);
  }
</style>
