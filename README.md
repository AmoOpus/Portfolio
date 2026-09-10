<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Andrew Mo — Product Manager</title>
<meta name="description" content="Andrew Mo — Product Manager portfolio. Commercial partnerships, editorial platforms, and ad-tech delivery across News Corp, Yahoo Australia, and beyond.">

<!-- Tailwind CSS -->
<script src="https://cdn.tailwindcss.com"></script>
<script>
  tailwind.config = {
    theme: {
      extend: {
        colors: {
          paper: '#faf8f4',
          panel: '#ffffff',
          panel2: '#f4f2ec',
          line: '#e6e1d6',
          ink: '#181510',
          forest: {
            DEFAULT: '#047857',
            deep: '#065f46',
            tint: '#ecfdf5',
          },
          plum: {
            DEFAULT: '#7c3aed',
            tint: '#f3ecfe',
          }
        },
        fontFamily: {
          serif: ['"Fraunces"', 'Georgia', 'serif'],
          sans: ['"Inter"', 'system-ui', 'sans-serif'],
          mono: ['"JetBrains Mono"', 'monospace'],
        },
        maxWidth: {
          'measure': '68ch',
        }
      }
    }
  }
</script>

<!-- Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600;9..144,700&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">

<!-- FontAwesome -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<style>
  html { scroll-behavior: smooth; }
  body { background-color: #faf8f4; }

  ::selection { background: #047857; color: #faf8f4; }

  ::-webkit-scrollbar { width: 10px; }
  ::-webkit-scrollbar-track { background: #faf8f4; }
  ::-webkit-scrollbar-thumb { background: #e6e1d6; border-radius: 6px; }
  ::-webkit-scrollbar-thumb:hover { background: #d4cdbc; }

  .byline { letter-spacing: 0.02em; }

  .card-teaser {
    max-height: 0;
    opacity: 0;
    transition: max-height 0.35s ease, opacity 0.3s ease, margin 0.35s ease;
  }
  .card:hover .card-teaser {
    max-height: 6rem;
    opacity: 1;
    margin-top: 0.75rem;
  }
  .card {
    transition: transform 0.3s ease, border-color 0.3s ease, box-shadow 0.3s ease;
  }
  .card:hover {
    transform: translateY(-4px) scale(1.012);
    box-shadow: 0 12px 30px -12px rgba(24, 21, 16, 0.18);
  }

  #modal-backdrop { transition: opacity 0.25s ease; }
  #modal-panel { transition: transform 0.3s cubic-bezier(0.16, 1, 0.3, 1), opacity 0.3s ease; }

  .stat-figure { font-variant-numeric: tabular-nums; }

  .nav-link { position: relative; }
  .nav-link::after {
    content: '';
    position: absolute;
    left: 0;
    bottom: -4px;
    width: 0%;
    height: 1px;
    background: #047857;
    transition: width 0.25s ease;
  }
  .nav-link:hover::after { width: 100%; }

  #main-content {
    transition: opacity 0.5s ease, transform 0.5s ease;
  }

  input:focus, textarea:focus { outline: none; }

  .float-slow { animation: floaty 6s ease-in-out infinite; }
  .float-slow-delay { animation: floaty 6s ease-in-out infinite; animation-delay: 1.2s; }
  @keyframes floaty {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-10px); }
  }

  @media (prefers-reduced-motion: reduce) {
    * { animation: none !important; transition: none !important; }
  }
</style>
</head>

<body class="bg-paper text-ink font-sans antialiased">

<!-- ============ NAV ============ -->
<header class="sticky top-0 z-40 bg-paper/85 backdrop-blur border-b border-line">
  <div class="max-w-6xl mx-auto px-6 lg:px-8 flex items-center justify-between h-16">
    <a href="#top" class="font-serif text-xl font-semibold tracking-tight text-ink">
      Andrew Mo<span class="text-forest">.</span>
    </a>

    <nav class="hidden md:flex items-center gap-8 text-sm text-ink/70 byline">
      <a href="#about" class="nav-link hover:text-ink transition-colors">About</a>
      <a href="#portfolio" class="nav-link hover:text-ink transition-colors">Portfolio</a>
      <a href="#skills" class="nav-link hover:text-ink transition-colors">Skills</a>
      <a href="#contact" class="nav-link hover:text-ink transition-colors">Contact</a>
    </nav>

    <a href="#contact" class="hidden md:inline-flex items-center gap-2 rounded-full border border-forest/40 px-4 py-2 text-sm text-forest hover:bg-forest/10 transition-colors">
      Let's talk
    </a>

    <button id="menu-btn" aria-label="Open menu" aria-expanded="false" class="md:hidden text-ink text-xl">
      <i class="fa-solid fa-bars"></i>
    </button>
  </div>

  <!-- Mobile menu -->
  <nav id="mobile-menu" class="hidden md:hidden border-t border-line bg-paper px-6 py-4 flex flex-col gap-4 text-ink/80">
    <a href="#about" class="mobile-link">About</a>
    <a href="#portfolio" class="mobile-link">Portfolio</a>
    <a href="#skills" class="mobile-link">Skills</a>
    <a href="#contact" class="mobile-link">Contact</a>
  </nav>
</header>

<!-- ============ HERO (cover) ============ -->
<section id="top" class="max-w-6xl mx-auto px-6 lg:px-8 min-h-[88vh] flex items-center py-14">
  <div class="grid md:grid-cols-12 gap-12 items-center w-full">

    <!-- Left: intro -->
    <div class="md:col-span-7">
      <p class="byline text-forest text-sm mb-5">Product Manager · Publishing, Ad-Tech &amp; Financial Services</p>
      <h1 class="font-serif text-4xl sm:text-5xl lg:text-6xl leading-[1.08] text-ink">
        Delivery that keeps
        <br class="hidden sm:block">
        every stakeholder aligned.
      </h1>
      <p class="mt-6 text-lg text-ink/60 max-w-measure leading-relaxed">
        I turn ambiguous business objectives into clear delivery briefs — leading cross-functional teams
        across publishing, ad-tech, and fintech to ship commercial partnerships, editorial platforms,
        and AI-assisted products that hold up under real deadlines.
      </p>

      <div class="mt-9 flex flex-wrap gap-4">
        <a href="#portfolio" data-reveal class="inline-flex items-center gap-2 rounded-md bg-forest px-6 py-3 text-white font-medium hover:bg-forest-deep transition-colors">
          View portfolio
          <i class="fa-solid fa-arrow-right text-sm"></i>
        </a>
        <a href="#contact" data-reveal class="inline-flex items-center gap-2 rounded-md border border-line px-6 py-3 text-ink hover:border-ink/40 transition-colors">
          Contact me
        </a>
      </div>

      <dl class="mt-12 grid grid-cols-3 gap-6 max-w-md border-t border-line pt-6">
        <div>
          <dt class="text-xs text-ink/40 byline">Experience</dt>
          <dd class="font-mono text-xl text-ink stat-figure mt-1">10+ yrs</dd>
        </div>
        <div>
          <dt class="text-xs text-ink/40 byline">Ad revenue growth</dt>
          <dd class="font-mono text-xl text-ink stat-figure mt-1">10X YoY</dd>
        </div>
        <div>
          <dt class="text-xs text-ink/40 byline">2025 shortlists</dt>
          <dd class="font-mono text-xl text-ink stat-figure mt-1">2</dd>
        </div>
      </dl>
    </div>

    <!-- Right: illustration -->
    <div class="md:col-span-5 relative h-[420px] hidden sm:block">
      <div class="absolute inset-0 rounded-2xl bg-forest-tint border border-line"></div>

      <!-- main browser card -->
      <div class="absolute left-4 top-6 w-[78%] rounded-xl bg-panel border border-line shadow-xl p-4">
        <div class="flex items-center gap-1.5 mb-3">
          <span class="w-2.5 h-2.5 rounded-full bg-line"></span>
          <span class="w-2.5 h-2.5 rounded-full bg-line"></span>
          <span class="w-2.5 h-2.5 rounded-full bg-line"></span>
        </div>
        <div class="h-3 w-2/3 rounded bg-panel2 mb-3"></div>
        <div class="h-24 rounded-lg bg-forest-tint mb-3 flex items-end gap-2 p-3">
          <div class="w-3 rounded bg-forest/40" style="height:40%"></div>
          <div class="w-3 rounded bg-forest/60" style="height:65%"></div>
          <div class="w-3 rounded bg-forest" style="height:90%"></div>
          <div class="w-3 rounded bg-forest/50" style="height:55%"></div>
          <div class="w-3 rounded bg-forest/70" style="height:75%"></div>
        </div>
        <div class="h-2.5 w-full rounded bg-panel2 mb-2"></div>
        <div class="h-2.5 w-5/6 rounded bg-panel2 mb-2"></div>
        <div class="h-2.5 w-2/3 rounded bg-panel2"></div>
      </div>

      <!-- floating stat card -->
      <div class="float-slow absolute right-2 top-2 w-40 rounded-xl bg-panel border border-line shadow-lg p-4">
        <p class="text-[11px] text-ink/40 byline">YoY page views</p>
        <p class="font-mono text-2xl text-forest mt-1">+39%</p>
      </div>

      <!-- floating checklist card -->
      <div class="float-slow-delay absolute right-0 bottom-4 w-48 rounded-xl bg-panel border border-line shadow-lg p-4 space-y-2">
        <p class="text-[11px] text-ink/40 byline mb-2">Delivery status</p>
        <div class="flex items-center gap-2 text-sm text-ink/70">
          <i class="fa-solid fa-circle-check text-forest"></i> Requirements
        </div>
        <div class="flex items-center gap-2 text-sm text-ink/70">
          <i class="fa-solid fa-circle-check text-forest"></i> Stakeholder sign-off
        </div>
        <div class="flex items-center gap-2 text-sm text-ink/40">
          <i class="fa-regular fa-circle"></i> Launch
        </div>
      </div>
    </div>

  </div>
</section>

<!-- ============ MAIN CONTENT (revealed after "View Portfolio") ============ -->
<div id="main-content" class="hidden opacity-0 translate-y-4">

  <!-- ============ ABOUT ============ -->
  <section id="about" class="border-t border-line">
    <div class="max-w-6xl mx-auto px-6 lg:px-8 py-20 grid md:grid-cols-12 gap-10">
      <div class="md:col-span-4">
        <h2 class="font-serif text-3xl text-ink">About</h2>
        <p class="mt-3 text-sm text-ink/40 byline">10+ years · publishing, ad-tech &amp; fintech</p>
      </div>

      <div class="md:col-span-8">
        <p class="text-ink/70 leading-relaxed max-w-measure">
          I'm a Product Manager with over a decade of cross-functional delivery experience across publishing,
          ad-tech, fintech, and financial services. My focus is requirements gathering, stakeholder alignment,
          and translating business objectives into delivery briefs that engineering and design teams can
          actually build against.
        </p>
        <p class="mt-5 text-ink/70 leading-relaxed max-w-measure">
          At News Corp Australia, Yahoo Australia, and earlier in financial services, I've introduced repeatable
          workflows that reduce ambiguity, protect the reader and customer experience, and keep technical and
          non-technical stakeholders moving in the same direction — from offshore vendor delivery and commercial
          partnerships to the rollout of a newsroom's first consumer-facing AI feature.
        </p>

        <div class="mt-8 flex flex-wrap gap-2">
          <span class="rounded-full border border-line px-3 py-1 text-xs text-ink/60 byline">Requirements gathering</span>
          <span class="rounded-full border border-line px-3 py-1 text-xs text-ink/60 byline">Stakeholder alignment</span>
          <span class="rounded-full border border-line px-3 py-1 text-xs text-ink/60 byline">Delivery workflow design</span>
          <span class="rounded-full border border-line px-3 py-1 text-xs text-ink/60 byline">Commercial partnerships</span>
        </div>
      </div>
    </div>
  </section>

  <!-- ============ PORTFOLIO ============ -->
  <section id="portfolio" class="border-t border-line bg-panel2/60">
    <div class="max-w-6xl mx-auto px-6 lg:px-8 py-20">
      <div class="flex items-end justify-between flex-wrap gap-4 mb-10">
        <div>
          <h2 class="font-serif text-3xl text-ink">Selected work</h2>
          <p class="mt-2 text-ink/40 text-sm byline">Drawn from my roles at News Corp Australia and Yahoo Australia</p>
        </div>
      </div>

      <div id="portfolio-grid" class="grid sm:grid-cols-2 gap-5">
        <!-- Cards injected by JS -->
      </div>
    </div>
  </section>

  <!-- ============ SKILLS ============ -->
  <section id="skills" class="border-t border-line">
    <div class="max-w-6xl mx-auto px-6 lg:px-8 py-20">
      <h2 class="font-serif text-3xl text-ink mb-12">Skills &amp; toolkit</h2>

      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-10">

        <div>
          <h3 class="font-serif text-lg text-forest mb-4">Product &amp; delivery</h3>
          <ul class="flex flex-wrap gap-2">
            <li class="skill-tag">Requirements Gathering</li>
            <li class="skill-tag">Roadmap Planning</li>
            <li class="skill-tag">Agile Delivery</li>
            <li class="skill-tag">UAT &amp; Release Management</li>
          </ul>
        </div>

        <div>
          <h3 class="font-serif text-lg text-forest mb-4">Leadership &amp; comms</h3>
          <ul class="flex flex-wrap gap-2">
            <li class="skill-tag">Cross-functional Leadership</li>
            <li class="skill-tag">Presenting to Leadership</li>
            <li class="skill-tag">Change Management</li>
            <li class="skill-tag">Vendor &amp; Partner Management</li>
          </ul>
        </div>

        <div>
          <h3 class="font-serif text-lg text-forest mb-4">Customer &amp; commercial</h3>
          <ul class="flex flex-wrap gap-2">
            <li class="skill-tag">Stakeholder Management</li>
            <li class="skill-tag">Customer Experience</li>
            <li class="skill-tag">Commercial Partnerships</li>
            <li class="skill-tag">Data-Informed Decisions</li>
            <li class="skill-tag">Process Improvement</li>
            <li class="skill-tag">Workflow Design</li>
          </ul>
        </div>

        <div>
          <h3 class="font-serif text-lg text-forest mb-4">Software &amp; tools</h3>
          <ul class="flex flex-wrap gap-2">
            <li class="skill-tag">JIRA</li>
            <li class="skill-tag">Confluence</li>
            <li class="skill-tag">Trello</li>
            <li class="skill-tag">Salesforce Marketing Cloud</li>
            <li class="skill-tag">Google Analytics</li>
            <li class="skill-tag">Figma</li>
            <li class="skill-tag">WordPress</li>
            <li class="skill-tag">Adobe Creative Suite</li>
          </ul>
        </div>

      </div>
    </div>
  </section>

  <!-- ============ CONTACT ============ -->
  <section id="contact" class="border-t border-line bg-panel2/60">
    <div class="max-w-6xl mx-auto px-6 lg:px-8 py-20 grid md:grid-cols-12 gap-10">

      <div class="md:col-span-5">
        <h2 class="font-serif text-3xl text-ink">Get in touch</h2>
        <p class="mt-4 text-ink/60 leading-relaxed max-w-measure">
          Hiring for a product role, or want to talk through a delivery or stakeholder-alignment challenge?
          Send a note — I read every message myself.
        </p>

        <div class="mt-8 space-y-3 text-ink/60 text-sm">
          <p class="flex items-center gap-3"><i class="fa-solid fa-envelope text-forest w-5"></i> Mo.andrew@live.com.au</p>
          <p class="flex items-center gap-3"><i class="fa-solid fa-phone text-forest w-5"></i> 0432 121 477</p>
          <p class="flex items-center gap-3"><i class="fa-solid fa-location-dot text-forest w-5"></i> Sydney, Australia</p>
        </div>
      </div>

      <div class="md:col-span-7">
        <form id="contact-form" class="space-y-5">
          <div>
            <label for="name" class="block text-sm text-ink/50 mb-2 byline">Name</label>
            <input type="text" id="name" name="name" required
              class="w-full rounded-md bg-panel border border-line px-4 py-3 text-ink placeholder-ink/30 focus:border-forest transition-colors"
              placeholder="Jordan Lee">
          </div>
          <div>
            <label for="email" class="block text-sm text-ink/50 mb-2 byline">Email</label>
            <input type="email" id="email" name="email" required
              class="w-full rounded-md bg-panel border border-line px-4 py-3 text-ink placeholder-ink/30 focus:border-forest transition-colors"
              placeholder="jordan@company.com">
          </div>
          <div>
            <label for="message" class="block text-sm text-ink/50 mb-2 byline">Message</label>
            <textarea id="message" name="message" rows="4" required
              class="w-full rounded-md bg-panel border border-line px-4 py-3 text-ink placeholder-ink/30 focus:border-forest transition-colors resize-none"
              placeholder="Tell me a bit about the role or project..."></textarea>
          </div>
          <button type="submit"
            class="inline-flex items-center gap-2 rounded-md bg-forest px-6 py-3 text-white font-medium hover:bg-forest-deep transition-colors">
            Send message
          </button>
          <p id="form-status" class="text-sm text-forest hidden">Thanks — your message has been noted. I'll reply soon.</p>
        </form>
      </div>

    </div>
  </section>

  <!-- ============ FOOTER ============ -->
  <footer class="border-t border-line">
    <div class="max-w-6xl mx-auto px-6 lg:px-8 py-10 flex flex-col sm:flex-row items-center justify-between gap-6">
      <p class="text-sm text-ink/40 byline">© 2026 Andrew Mo · Product Manager</p>
      <div class="flex items-center gap-5 text-lg text-ink/50">
        <a href="https://linkedin.com/in/andrew-mo-46s" target="_blank" rel="noopener" aria-label="LinkedIn" class="hover:text-forest transition-colors"><i class="fa-brands fa-linkedin"></i></a>
        <a href="mailto:Mo.andrew@live.com.au" aria-label="Email" class="hover:text-forest transition-colors"><i class="fa-solid fa-envelope"></i></a>
        <a href="tel:0432121477" aria-label="Phone" class="hover:text-forest transition-colors"><i class="fa-solid fa-phone"></i></a>
      </div>
    </div>
  </footer>

</div>

<style>
  .skill-tag {
    @apply rounded-md border border-line bg-panel px-3 py-1.5 text-sm text-ink/70;
  }
  .mobile-link {
    @apply block py-1 text-base;
  }
</style>

<!-- ============ MODAL ============ -->
<div id="modal-backdrop" class="fixed inset-0 z-50 hidden items-center justify-center bg-ink/40 backdrop-blur-sm px-4 py-8 opacity-0">
  <div id="modal-panel" class="relative w-full max-w-2xl max-h-[85vh] overflow-y-auto rounded-lg border border-line bg-panel p-7 sm:p-9 opacity-0 translate-y-4 scale-[0.98] shadow-2xl">
    <button id="modal-close" aria-label="Close" class="absolute top-5 right-5 text-ink/40 hover:text-ink transition-colors text-xl">
      <i class="fa-solid fa-xmark"></i>
    </button>

    <p id="modal-category" class="byline text-forest text-xs mb-3"></p>
    <h3 id="modal-title" class="font-serif text-2xl sm:text-3xl text-ink pr-8"></h3>

    <div class="mt-6">
      <h4 class="text-xs byline text-ink/40 mb-2">Problem statement</h4>
      <p id="modal-problem" class="text-ink/70 leading-relaxed"></p>
    </div>

    <div class="mt-7">
      <h4 class="text-xs byline text-ink/40 mb-3">Key outcomes</h4>
      <div id="modal-metrics" class="grid grid-cols-1 sm:grid-cols-3 gap-4"></div>
    </div>

    <div class="mt-7 grid sm:grid-cols-2 gap-7">
      <div>
        <h4 class="text-xs byline text-ink/40 mb-2">Role</h4>
        <p id="modal-role" class="text-ink/70"></p>
      </div>
      <div>
        <h4 class="text-xs byline text-ink/40 mb-2">Tech &amp; tools</h4>
        <div id="modal-tools" class="flex flex-wrap gap-2"></div>
      </div>
    </div>
  </div>
</div>

<script>
  // ---------- Data (drawn from Andrew Mo's CV) ----------
  const projects = [
    {
      id: 'coles',
      icon: 'fa-solid fa-cart-shopping',
      category: 'Commercial Partnerships · News Corp Australia',
      title: 'Coles Click-to-Cart Commerce Integration',
      teaser: 'A direct, seamless path from editorial recipe content to purchase for News Corp\u2019s biggest commercial partner.',
      problem: 'The Coles partnership was Taste.com.au\u2019s most commercially significant collaboration, but delivery ran through an offshore development vendor and needed to sustain pace through a period of consolidated scope, all while keeping senior stakeholders confident in progress toward a seamless purchase path from editorial content.',
      metrics: [
        { value: '+39%', label: 'YoY page views to sponsored Dinner content' },
        { value: '#1', label: 'Commercial partnership at News Corp' },
        { value: 'On track', label: 'Delivery sustained through scope changes' },
      ],
      role: 'Product Manager — took a lead role coordinating an offshore development vendor and managing visibility for senior stakeholders throughout delivery.',
      tools: ['JIRA', 'Confluence', 'Salesforce Marketing Cloud', 'Google Analytics'],
    },
    {
      id: 'audience-protection',
      icon: 'fa-solid fa-shield-halved',
      category: 'Editorial Platform · News Corp Australia',
      title: 'Taste Audience Protection Project',
      teaser: 'Template redesigns, a consolidated data dashboard, and an AI-assisted editorial workflow uplift.',
      problem: 'Protecting and improving the reader experience required prioritising key template redesigns, consolidating fragmented reporting into a single data dashboard, and uplifting editorial workflows with AI assistance — all while requirements and scope kept evolving across a broad set of internal stakeholders.',
      metrics: [
        { value: 'Shortlisted', label: 'Mumbrella Publisher Awards 2025 — Relaunch of the Year' },
        { value: '1', label: 'Consolidated data dashboard shipped' },
        { value: 'AI-assisted', label: 'Editorial workflow uplift delivered' },
      ],
      role: 'Product Manager — led business requirements gathering and cross-functional prioritisation, maintaining delivery momentum through evolving scope.',
      tools: ['JIRA', 'Confluence', 'Google Analytics', 'Figma', 'WordPress'],
    },
    {
      id: 'ai-feature',
      icon: 'fa-solid fa-wand-magic-sparkles',
      category: 'Innovation · News Corp Australia',
      title: 'Consumer-Facing AI Feature Rollout',
      teaser: 'Directing the organisation\u2019s first consumer-facing AI feature from readiness through launch.',
      problem: 'Launching the organisation\u2019s first consumer-facing AI feature meant coordinating cross-functional readiness — engineering, editorial, and communications — with no internal precedent to draw on, while keeping stakeholders across the business informed ahead of a high-visibility launch.',
      metrics: [
        { value: 'Shortlisted', label: 'Mumbrella Publisher Awards 2025 — Innovation' },
        { value: '1st', label: 'Consumer-facing AI feature at the organisation' },
        { value: 'Org-wide', label: 'Stakeholder readiness coordinated' },
      ],
      role: 'Product Manager — directed post-launch rollout, coordinating cross-functional readiness and stakeholder communication.',
      tools: ['JIRA', 'Confluence', 'Google Workspace', 'Stakeholder comms plan'],
    },
    {
      id: 'yahoo-adtech',
      icon: 'fa-solid fa-bullseye',
      category: 'Ad-Tech · Yahoo Australia',
      title: 'Core Ad Product Line Rebuild',
      teaser: 'Rebuilding a global publisher\u2019s core ad product across dynamic creative, DSP, and ad-serving.',
      problem: 'Yahoo\u2019s core ad product line needed a rebuild spanning dynamic creative, DSP, and ad-serving integration, requiring tight coordination across design, data, and engineering to modernise the offering without disrupting revenue.',
      metrics: [
        { value: '+80%', label: 'Uplift in product consultations' },
        { value: '10X', label: 'YoY revenue growth' },
        { value: '3', label: 'Regions coordinated (SG, HK, India)' },
      ],
      role: 'Digital Producer — led requirements and delivery, coordinating design, data, and engineering across a distributed cross-regional team.',
      tools: ['JIRA', 'Trello', 'Google Analytics', 'DSP & ad-serving platforms'],
    },
  ];

  // ---------- Render portfolio grid ----------
  const grid = document.getElementById('portfolio-grid');

  projects.forEach((p) => {
    const card = document.createElement('button');
    card.type = 'button';
    card.className = 'card text-left rounded-lg border border-line bg-panel p-6 hover:border-forest/50 focus-visible:outline focus-visible:outline-2 focus-visible:outline-forest';
    card.setAttribute('data-id', p.id);
    card.innerHTML = `
      <div class="flex items-start justify-between">
        <span class="inline-flex items-center justify-center w-10 h-10 rounded-md bg-forest-tint text-forest">
          <i class="${p.icon}"></i>
        </span>
        <i class="fa-solid fa-arrow-up-right text-ink/25"></i>
      </div>
      <p class="byline text-xs text-ink/40 mt-5">${p.category}</p>
      <h3 class="font-serif text-xl text-ink mt-2">${p.title}</h3>
      <p class="card-teaser text-sm text-ink/50 overflow-hidden">${p.teaser}</p>
    `;
    grid.appendChild(card);
  });

  // ---------- Modal logic ----------
  const backdrop = document.getElementById('modal-backdrop');
  const panel = document.getElementById('modal-panel');
  const closeBtn = document.getElementById('modal-close');

  const modalCategory = document.getElementById('modal-category');
  const modalTitle = document.getElementById('modal-title');
  const modalProblem = document.getElementById('modal-problem');
  const modalMetrics = document.getElementById('modal-metrics');
  const modalRole = document.getElementById('modal-role');
  const modalTools = document.getElementById('modal-tools');

  let lastFocused = null;

  function openModal(project) {
    modalCategory.textContent = project.category;
    modalTitle.textContent = project.title;
    modalProblem.textContent = project.problem;
    modalRole.textContent = project.role;

    modalMetrics.innerHTML = project.metrics.map(m => `
      <div class="rounded-md border border-line bg-panel2 px-3 py-3 text-center">
        <div class="font-mono text-lg text-forest stat-figure">${m.value}</div>
        <div class="text-[11px] text-ink/40 mt-1 byline">${m.label}</div>
      </div>
    `).join('');

    modalTools.innerHTML = project.tools.map(t => `
      <span class="rounded-md border border-line bg-panel2 px-3 py-1.5 text-xs text-ink/70">${t}</span>
    `).join('');

    lastFocused = document.activeElement;
    backdrop.classList.remove('hidden');
    backdrop.classList.add('flex');
    requestAnimationFrame(() => {
      backdrop.classList.remove('opacity-0');
      panel.classList.remove('opacity-0', 'translate-y-4', 'scale-[0.98]');
    });
    document.body.style.overflow = 'hidden';
    closeBtn.focus();
  }

  function closeModal() {
    backdrop.classList.add('opacity-0');
    panel.classList.add('opacity-0', 'translate-y-4', 'scale-[0.98]');
    document.body.style.overflow = '';
    setTimeout(() => {
      backdrop.classList.add('hidden');
      backdrop.classList.remove('flex');
    }, 250);
    if (lastFocused) lastFocused.focus();
  }

  grid.addEventListener('click', (e) => {
    const card = e.target.closest('.card');
    if (!card) return;
    const project = projects.find(p => p.id === card.getAttribute('data-id'));
    if (project) openModal(project);
  });

  closeBtn.addEventListener('click', closeModal);
  backdrop.addEventListener('click', (e) => { if (e.target === backdrop) closeModal(); });
  document.addEventListener('keydown', (e) => {
    if (e.key === 'Escape' && !backdrop.classList.contains('hidden')) closeModal();
  });

  // ---------- Mobile menu ----------
  const menuBtn = document.getElementById('menu-btn');
  const mobileMenu = document.getElementById('mobile-menu');

  menuBtn.addEventListener('click', () => {
    const isOpen = !mobileMenu.classList.contains('hidden');
    mobileMenu.classList.toggle('hidden');
    menuBtn.setAttribute('aria-expanded', String(!isOpen));
    menuBtn.innerHTML = isOpen ? '<i class="fa-solid fa-bars"></i>' : '<i class="fa-solid fa-xmark"></i>';
  });

  // ---------- Reveal-on-demand: "View Portfolio" cover behaviour ----------
  const mainContent = document.getElementById('main-content');

  function revealContent() {
    if (mainContent.classList.contains('hidden')) {
      mainContent.classList.remove('hidden');
      requestAnimationFrame(() => {
        mainContent.classList.remove('opacity-0', 'translate-y-4');
      });
      return true; // content was just revealed, caller should wait before scrolling
    }
    return false;
  }

  document.querySelectorAll('a[href^="#"]').forEach(link => {
    const targetId = link.getAttribute('href').slice(1);
    if (targetId === 'top') return; // logo just scrolls to the cover, no reveal needed

    link.addEventListener('click', (e) => {
      e.preventDefault();
      const justRevealed = revealContent();
      mobileMenu.classList.add('hidden');
      menuBtn.setAttribute('aria-expanded', 'false');
      menuBtn.innerHTML = '<i class="fa-solid fa-bars"></i>';

      const target = document.getElementById(targetId);
      if (!target) return;
      setTimeout(() => {
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }, justRevealed ? 60 : 0);
    });
  });

  // ---------- Contact form (front-end only) ----------
  const form = document.getElementById('contact-form');
  const status = document.getElementById('form-status');

  form.addEventListener('submit', (e) => {
    e.preventDefault();
    status.classList.remove('hidden');
    form.reset();
    setTimeout(() => status.classList.add('hidden'), 5000);
  });
</script>

</body>
</html>
