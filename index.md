---
layout: single
author_profile: false
classes: wide
title: " "
---

<link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:ital,wght@0,400;0,600;0,700;1,400&family=Source+Sans+3:wght@300;400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">

<style>
/* Page-specific overrides for the single-page layout */
.page__content { max-width: 720px !important; margin: 0 auto !important; }
.page__title { display: none !important; }
.page__hero { display: none !important; }

.sb-header { display: flex; align-items: center; gap: 20px; margin-bottom: 1.2rem; }
.sb-photo { width: 78px; height: 78px; border-radius: 6px; border: 2px solid #262626; object-fit: cover; filter: grayscale(100%); transition: filter 0.4s ease; }
.sb-photo:hover { filter: grayscale(0%); }
.sb-name { font-family: 'Source Serif 4', serif; font-size: 28px; font-weight: 700; color: #e8e8e8; margin: 0; letter-spacing: -0.02em; }
.sb-role { font-size: 15px; color: #a0a0a0; margin: 2px 0 0; }
.sb-pronouns { font-family: 'IBM Plex Mono', monospace; font-size: 12px; color: #555; margin: 2px 0 0; }

.sb-nav { font-family: 'IBM Plex Mono', monospace; font-size: 13px; margin-bottom: 1.5rem; line-height: 2.2; }
.sb-nav a { color: #808080; margin-right: 16px; text-decoration: none; transition: color 0.2s; }
.sb-nav a:hover { color: #00e67a !important; text-decoration: none !important; }
.sb-nav a.sb-green { color: #00e67a; }
.sb-nav a.sb-amber { color: #e6a020; }

.sb-divider { height: 1px; background: #262626; margin-bottom: 2rem; }

.sb-about { font-size: 16px; color: #c8c8c8; line-height: 1.85; margin-bottom: 0.8rem; }
.sb-keywords { font-family: 'IBM Plex Mono', monospace; font-size: 12.5px; color: #666; margin: 12px 0 2.5rem; }

.sb-section { margin-bottom: 2.5rem; }
.sb-h2 { font-family: 'Source Serif 4', serif; font-size: 19px; font-weight: 600; color: #d4d4d4; padding-bottom: 8px; border-bottom: 1px solid #262626; margin-bottom: 1.2rem; }

.sb-pub { margin-bottom: 18px; }
.sb-pub p { margin: 0; }
.sb-pub-title { font-size: 15px; color: #d4d4d4; margin-bottom: 2px !important; }
.sb-pub-title strong { color: #e8e8e8 !important; }
.sb-pub-journal { font-size: 13px; color: #707070; font-style: italic; }

.sb-chapter-label { font-family: 'IBM Plex Mono', monospace; font-size: 12px; color: #555; text-transform: uppercase; letter-spacing: 0.06em; margin-top: 1.2rem; margin-bottom: 0.6rem; }
.sb-chapter { margin-bottom: 10px; }
.sb-chapter p { font-size: 14px; color: #a0a0a0; margin: 0; }
.sb-chapter span { color: #666; font-style: italic; }

.sb-prose { font-size: 15px; color: #b8b8b8; line-height: 1.85; margin-bottom: 1rem; }

.sb-explore { border-left: 2px solid #262626; padding-left: 20px; margin-top: 1.5rem; }
.sb-explore-label { font-family: 'IBM Plex Mono', monospace; font-size: 12px; color: #555; text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 8px; }
.sb-explore p { font-size: 15px; color: #a0a0a0; line-height: 1.85; }
.sb-explore a.sb-green { color: #00e67a !important; text-decoration: none; }
.sb-explore a.sb-amber { color: #e6a020 !important; text-decoration: none; }

.sb-course { font-size: 14px; color: #a0a0a0; margin-bottom: 6px; }
.sb-course strong { color: #d0d0d0; }
.sb-course-meta { color: #707070; }

/* Timeline */
.sb-timeline { position: relative; padding-left: 24px; border-left: 2px solid #1a1a1a; }
.sb-tl-item { margin-bottom: 22px; position: relative; }
.sb-tl-dot { position: absolute; left: -29px; top: 5px; width: 10px; height: 10px; border-radius: 50%; }
.sb-tl-dot-current { background: #00e67a; box-shadow: 0 0 6px rgba(0,228,122,0.3); }
.sb-tl-dot-past { background: #262626; border: 2px solid #404040; }
.sb-tl-year { font-size: 15px; color: #c0c0c0; margin: 0; font-weight: 500; }
.sb-tl-year-current { color: #e0e0e0; }
.sb-tl-place { font-size: 14px; color: #909090; margin: 2px 0 0; }
.sb-tl-detail { font-size: 13px; color: #606060; margin: 2px 0 0; }

.sb-footer { border-top: 1px solid #262626; padding-top: 1.5rem; margin-top: 1rem; }
.sb-footer p { font-family: 'IBM Plex Mono', monospace; font-size: 12px; color: #4a4a4a; margin: 0; }

/* Expandable abstracts */
.sb-pub-toggle { font-family: 'IBM Plex Mono', monospace; font-size: 12px; color: #555; cursor: pointer; transition: color 0.2s; display: inline-block; margin-top: 4px; }
.sb-pub-toggle:hover { color: #00e67a; }
.sb-pub-abstract { max-height: 0; overflow: hidden; transition: max-height 0.4s ease, opacity 0.3s ease; opacity: 0; margin-top: 0; }
.sb-pub-abstract.open { max-height: 600px; opacity: 1; margin-top: 10px; }
.sb-pub-abstract-text { font-size: 13.5px; color: #909090; line-height: 1.75; padding: 12px 0 8px 16px; border-left: 2px solid #262626; }
.sb-pub-dl { font-family: 'IBM Plex Mono', monospace; font-size: 12px; margin-top: 8px; }
.sb-pub-dl a { color: #00e67a !important; text-decoration: none !important; }
.sb-pub-dl a:hover { text-decoration: underline !important; }

/* Fade-in animation */
@keyframes fadeUp { from { opacity: 0; transform: translateY(12px); } to { opacity: 1; transform: translateY(0); } }
.sb-header { animation: fadeUp 0.4s ease both; animation-delay: 0.05s; }
.sb-nav { animation: fadeUp 0.4s ease both; animation-delay: 0.1s; }
.sb-section { animation: fadeUp 0.5s ease both; animation-delay: 0.2s; }
</style>

<!-- Header -->
<div class="sb-header">
  <img src="/images/santoshbs1.jpeg" alt="Santosh B. Srinivas" class="sb-photo">
  <div>
    <h1 class="sb-name">Santosh B. Srinivas</h1>
    <p class="sb-role">Assistant Professor · Management & Human Resources · HEC Paris</p>
    <p class="sb-pronouns">he/him</p>
  </div>
</div>

<div class="sb-nav">
  <a href="mailto:srinivas@hec.fr">srinivas@hec.fr</a>
  <a href="https://github.com/santoshbs" target="_blank">github</a>
  <a href="https://bit.ly/sbsgsch" target="_blank">google scholar</a>
  <a href="https://orcid.org/0000-0002-7792-9622" target="_blank">orcid</a>
</div>

<div class="sb-divider"></div>

<!-- About -->
<p class="sb-about">
I study how value is produced, assessed, and negotiated in organizational and entrepreneurial settings — and how evaluative processes reflect and reinforce social power. I integrate insights from cultural sociology, cognitive psychology, and management theory. Methodologically, I work primarily with natural language processing and large language models.
</p>
<p class="sb-keywords">social evaluations · culture & cognition · entrepreneurship · computational social science</p>

<!-- Publications -->
<div class="sb-section">
<h2 class="sb-h2">Publications</h2>

<div class="sb-pub">
<p class="sb-pub-title">Patil, S. V., <strong>Srinivas, S. B.</strong>, Tussing, D. V., & Rhee, J. (2025). Addressing the flexible use of cognitive flexibility constructs: Toward a multifaceted approach.</p>
<p class="sb-pub-journal">Academy of Management Annals, 19(1), 74–131.</p>
<span class="sb-pub-toggle" onclick="this.nextElementSibling.classList.toggle('open'); this.textContent = this.nextElementSibling.classList.contains('open') ? '− abstract' : '+ abstract';">+ abstract</span>
<div class="sb-pub-abstract">
<div class="sb-pub-abstract-text">Many researchers have drawn on "cognitive flexibility" to denote the explanatory mechanism underlying a broad array of organizational theories. However, conceptualization of this construct is inconsistent, sometimes conflating with other constructs. We conduct a comprehensive search, strip away labels, and use text analysis to distinguish among five fluid thought processes: elaborating, dimensionalizing, integrating, juxtaposing, and matching — grouped into three higher-order categories involving reshaping, contending, and shifting of cognitive structures. We argue that cognitive flexibility may be more appropriately viewed as a multifaceted, rather than monolithic, construct.
<p class="sb-pub-dl"><a href="https://doi.org/10.5465/annals.2023.0078" target="_blank">doi ↗</a></p>
</div>
</div>
</div>

<div class="sb-pub">
<p class="sb-pub-title">Sinha, R., Chiu, C. Y., & <strong>Srinivas, S. B.</strong> (2021). Shared leadership and relationship conflict in teams: The moderating role of team power base diversity.</p>
<p class="sb-pub-journal">Journal of Organizational Behavior, 42(5), 649–667.</p>
<span class="sb-pub-toggle" onclick="this.nextElementSibling.classList.toggle('open'); this.textContent = this.nextElementSibling.classList.contains('open') ? '− abstract' : '+ abstract';">+ abstract</span>
<div class="sb-pub-abstract">
<div class="sb-pub-abstract-text">Shared leadership in teams is believed to be beneficial for team effectiveness, yet recent evidence shows it may not always bring positive effects. Drawing on dominance complementarity theory, we suggest that team power base diversity — the variety in power bases among team members — moderates the impact of shared leadership on relationship conflict to influence team performance. In a sample of 70 project-based teams, we find support that at high levels of team power base diversity, shared leadership has a positive downstream effect on team performance through reduced relationship conflict.
<p class="sb-pub-dl"><a href="https://doi.org/10.1002/job.2515" target="_blank">doi ↗</a></p>
</div>
</div>
</div>

<div class="sb-pub">
<p class="sb-pub-title">Rindova, V. P., Martins, L. L., <strong>Srinivas, S. B.</strong>, & Chandler, D. (2018). The good, the bad, and the ugly of organizational rankings: A multidisciplinary review.</p>
<p class="sb-pub-journal">Journal of Management, 44(6), 2175–2208.</p>
<span class="sb-pub-toggle" onclick="this.nextElementSibling.classList.toggle('open'); this.textContent = this.nextElementSibling.classList.contains('open') ? '− abstract' : '+ abstract';">+ abstract</span>
<div class="sb-pub-abstract">
<div class="sb-pub-abstract-text">A review of the literature on organizational rankings across management, sociology, education, and law reveals three perspectives on these complex evaluations — rankings as information intermediation, as comparative orderings, or as a means for surveillance and control. We identify core contributions and additional questions for each perspective, and propose a new perspective — rankings entrepreneurship — which presents significant opportunities to extend our understanding of the production and consumption of rankings.
<p class="sb-pub-dl"><a href="https://doi.org/10.1177/0149206317741962" target="_blank">doi ↗</a></p>
</div>
</div>
</div>

<p class="sb-chapter-label">Book chapters</p>

<div class="sb-pub">
<p class="sb-chapter"><p>Boyd, R. L., <strong>Srinivas, S. B.</strong>, Phadke, S., Wilson, S. R., & Pasca, P. AI and computation in the social sciences. <span style="color: #666; font-style: italic;">Forthcoming, Oxford University Press.</span></p></p>
</div>

<div class="sb-pub">
<p class="sb-chapter"><p>Rindova, V. P., <strong>Srinivas, S. B.</strong>, & Martins, L. L. (2022). How to break free: An orders-of-worth perspective on emancipatory entrepreneurship. <span style="color: #666; font-style: italic;">Research in the Sociology of Organizations.</span></p></p>
<span class="sb-pub-toggle" onclick="this.nextElementSibling.classList.toggle('open'); this.textContent = this.nextElementSibling.classList.contains('open') ? '− abstract' : '+ abstract';">+ abstract</span>
<div class="sb-pub-abstract">
<div class="sb-pub-abstract-text">We propose that entrepreneurial acts toward emancipation can be guided by different notions of the common good underlying varying conceptions of worth, beyond economic wealth creation. Drawing on Boltanski and Thévenot's work on multiple orders of worth, we theorize how the civic and inspired orders point to alternate emancipatory ends and means through which entrepreneurs break free from material and ideological constraints.
<p class="sb-pub-dl"><a href="http://bit.ly/3ZhbwbX" target="_blank">pre-print ↗</a></p>
</div>
</div>
</div>

<div class="sb-pub">
<p class="sb-chapter"><p>Rindova, V. P., & <strong>Srinivas, S. B.</strong> (2017). Managing meaning — culture. <span style="color: #666; font-style: italic;">Oxford Handbook of Management.</span></p></p>
<span class="sb-pub-toggle" onclick="this.nextElementSibling.classList.toggle('open'); this.textContent = this.nextElementSibling.classList.contains('open') ? '− abstract' : '+ abstract';">+ abstract</span>
<div class="sb-pub-abstract">
<div class="sb-pub-abstract-text">This chapter theorizes how symbolic practices enable effective responses to diverse stakeholder demands, examining the role of culture in the construction and management of organizational meaning.
<p class="sb-pub-dl"><a href="http://santoshbs.github.io/files/RindovaSrinivas_2017_ManagingMeaning_PreprintVersion.pdf" target="_blank">pre-print ↗</a></p>
</div>
</div>
</div>

</div>

<!-- Current Research & Explorations -->
<div class="sb-section">
<h2 class="sb-h2">Current research & explorations</h2>

<p class="sb-prose">
My current work examines how different audiences construct and contest social positions on user-generated platforms, and how individuals adapt their self-presentation when the demographic composition of their field shifts. A parallel stream reconnects with my longstanding interest in entrepreneurship — how personal histories shape opportunity recognition, how ventures use rhetorical history to craft market positions, and how entrepreneurial rhetoric can function as a form of social critique.
</p>

<div class="sb-explore">
<p class="sb-explore-label">Exploratory</p>
<p>I am interested in how the emerging agentic AI economy may reshape the evaluation of competence, worth, and opportunity. As part of this, I deployed a small open-weights language model into social networks where participants are entirely AI agents or entirely humans. It participates, observes, and writes field notes on what gets discussed and what patterns emerge.
<a href="/agentfield/" class="sb-green">agentfield</a> records observations from an AI-only network;
<a href="/mortalfield/" class="sb-amber">mortalfield</a> does the same for human conversations.</p>
</div>
</div>

<!-- Teaching -->
<div class="sb-section">
<h2 class="sb-h2">Teaching</h2>

<p class="sb-prose">
My classes orient students to multiple conceptions of value and varied approaches to organizing — not a single dominant logic. I use case-based pedagogy, asking students to reflect individually and then compare perspectives collaboratively. With AI reshaping what competence looks like, I see an opportunity to redesign assessments around what matters most: the ability to translate ill-structured problems into relevant concepts and critically synthesize solutions.
</p>

<div style="margin-top: 1rem;">
<p class="sb-course"><strong>Organizational Behavior</strong> <span style="color: #404040;">·</span> <span class="sb-course-meta">Grande École Program, HEC Paris · 2019 –</span></p>
<p class="sb-course"><strong>Doctoral Seminar in Organizational Behavior</strong> <span style="color: #404040;">·</span> <span class="sb-course-meta">HEC Paris · 2019 –</span></p>
<p class="sb-course"><strong>Outdoor Leadership Seminar</strong> <span style="color: #404040;">·</span> <span class="sb-course-meta">MBA, HEC Paris · co-supervisor</span></p>
</div>
</div>

<!-- Timeline -->
<div class="sb-section">
<h2 class="sb-h2">Timeline</h2>

<div class="sb-timeline">

<div class="sb-tl-item">
<div class="sb-tl-dot sb-tl-dot-current"></div>
<p class="sb-tl-year sb-tl-year-current">2019 – present</p>
<p class="sb-tl-place" style="color: #a0a0a0;">Assistant Professor, HEC Paris</p>
<p class="sb-tl-detail">Department of Management & Human Resources</p>
</div>

<div class="sb-tl-item">
<div class="sb-tl-dot sb-tl-dot-past"></div>
<p class="sb-tl-year">2014 – 2019</p>
<p class="sb-tl-place">Ph.D. in Management, University of Texas at Austin</p>
<p class="sb-tl-detail">McCombs School of Business</p>
</div>

<div class="sb-tl-item">
<div class="sb-tl-dot sb-tl-dot-past"></div>
<p class="sb-tl-year">2010 – 2014</p>
<p class="sb-tl-place">Indian School of Business, Hyderabad</p>
<p class="sb-tl-detail">Research Assistant, OB · Assistant Director, Wadhwani Center for Entrepreneurship</p>
</div>

<div class="sb-tl-item">
<div class="sb-tl-dot sb-tl-dot-past"></div>
<p class="sb-tl-year">2008 – 2010</p>
<p class="sb-tl-place">Institute of Leadership and Institutional Development, Bangalore</p>
</div>

<div class="sb-tl-item">
<div class="sb-tl-dot sb-tl-dot-past"></div>
<p class="sb-tl-year">2006 – 2007</p>
<p class="sb-tl-place">PGP, Indian School of Business</p>
</div>

<div class="sb-tl-item">
<div class="sb-tl-dot sb-tl-dot-past"></div>
<p class="sb-tl-year">2001 – 2006</p>
<p class="sb-tl-place">Intel Technologies India</p>
<p class="sb-tl-detail">Technical Lead / Programmer Analyst</p>
</div>

<div class="sb-tl-item" style="margin-bottom: 0;">
<div class="sb-tl-dot sb-tl-dot-past"></div>
<p class="sb-tl-year">1997 – 2001</p>
<p class="sb-tl-place">B.E. (Hons.) Computer Science, BITS Pilani</p>
</div>

</div>
</div>

<!-- Footer -->
<div class="sb-footer">
<p>Paris, France · srinivas@hec.fr</p>
</div>
