# Sources and evidence ledger

This repository is intentionally conservative about attribution. The following ledger separates source-backed facts from opinion, synthesis, and hypothetical examples.

## A. Sourced facts

### 1) Palantir: Forward Deployed Engineers
- Title: Forward Deployed Engineers
- Organization: Palantir
- Named author or speaker: Not clearly identified on the public page.
- URL: https://palantir.com/careers/teams/forward-deployed-engineers/
- Publication date: Not clearly stated.
- Date actually checked: 2026-11-09
- Source type: employer description
- Claims it supports:
  - FDE work is tied to customer problems and product development.
  - The role is part of a delivery model that combines engineering with customer proximity.
  - FDE responsibilities are shaped by real deployment contexts rather than abstract product work alone.
- Limits, bias, or scope:
  - This is Palantir’s own description of its model, not proof that every employer uses the same role.
  - It reflects Palantir’s product and delivery philosophy.
- Access status: Accessible

### 2) Palantir Architecture Center overview
- Title: Architecture Center: Overview
- Organization: Palantir
- Named author or speaker: Not clearly stated on the page.
- URL: https://www.palantir.com/docs/foundry/architecture-center/overview
- Publication date: Not clearly stated.
- Date actually checked: 2026-11-09
- Source type: platform documentation
- Claims it supports:
  - Palantir describes the platform as an integrated operating environment with data, logic, and workflow services.
  - The architecture is designed to support enterprise workflows through a layered operating model.
  - The company frames feedback from customer problems into platform evolution.
- Limits, bias, or scope:
  - Platform documentation is product-oriented and describes a specific architecture, not a universal engineering standard.
- Access status: Accessible

### 3) Palantir + NVIDIA Sovereign AI reference architecture
- Title: The future of AI: Sovereign AI Operating System Reference Architecture with NVIDIA
- Organization: Palantir and NVIDIA
- Named author or speaker: Justin Boitano is quoted in the page, with the page itself not listing a single author.
- URL: https://www.palantir.com/sovereignaios/
- Publication date: Not clearly stated.
- Date actually checked: 2026-11-09
- Source type: platform documentation / joint reference architecture
- Claims it supports:
  - The page distinguishes infrastructure and model work from workflow and platform work.
  - It describes different FDE responsibilities depending on function: NVIDIA FDEs focus on infrastructure and model optimization; Palantir FDEs focus on workflow development and platform operation.
  - It shows a concrete example of employer-specific division of labor.
- Limits, bias, or scope:
  - This is a partnership marketing page and reference architecture, not an industry-wide taxonomy.
  - It demonstrates one company’s way of organizing work, not a universal standard.
- Access status: Accessible

### 4) OpenAI Forward Deployed Engineer job ad
- Title: Forward Deployed Engineer - Paris
- Organization: OpenAI
- Named author or speaker: Not clearly stated on the page.
- URL: https://openai.com/careers/forward-deployed-engineer-paris-paris-france/
- Publication date: Job posting appears current as of the checked date, but the page does not clearly list a posting date.
- Date actually checked: 2026-11-09
- Source type: employer description
- Claims it supports:
  - OpenAI describes FDE work as discovery, technical scoping, system design, build, and rollout.
  - It highlights customer delivery, production deployment, and product feedback loops into research and roadmap.
- Limits, bias, or scope:
  - Job listings change over time; the page reflects a current listing but not a permanent definition.
  - This is an employer-specific description, not a universal definition of FDE.
- Access status: Accessible

### 5) Anthropic: Building effective agents
- Title: Building effective agents
- Organization: Anthropic
- Named author or speaker: Erik S. and Barry Zhang
- URL: https://www.anthropic.com/engineering/building-effective-agents
- Publication date: 2024-12-19
- Date actually checked: 2026-11-09
- Source type: engineering guidance
- Claims it supports:
  - Anthropic distinguishes workflows from agents.
  - Workflows are predefined code paths; agents dynamically direct their own steps.
  - Simpler solutions are recommended before increasing system complexity.
- Limits, bias, or scope:
  - This is guidance for building agentic systems, not a definition of FDE roles.
  - It is a practitioner-oriented engineering post, not an industry standard document.
- Access status: Accessible

### 6) Anthropic: Demystifying evals for AI agents
- Title: Demystifying evals for AI agents
- Organization: Anthropic
- Named author or speaker: Mikaela Grace, Jeremy Hadfield, Rodrigo Olivares, and Jiri De Jonghe
- URL: https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents
- Publication date: 2026-01-09
- Date actually checked: 2026-11-09
- Source type: engineering guidance
- Claims it supports:
  - Agent evaluation includes task, trial, grader, transcript, outcome, and harness.
  - Deterministic, model-based, and human graders each play different roles.
  - Evals should be combined with production monitoring and human review rather than relied on alone.
- Limits, bias, or scope:
  - It is guidance from a vendor and reflects internal engineering experience, not a complete assessment of every deployment context.
  - It explicitly notes that evals are a part of a broader understanding of agent performance.
- Access status: Accessible

### 7) GitHub README guidance
- Title: About the repository README file
- Organization: GitHub
- Named author or speaker: No named author on the page.
- URL: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes
- Publication date: Documentation page; not clearly listed on the page.
- Date actually checked: 2026-11-09
- Source type: repository documentation guidance
- Claims it supports:
  - README files are used to explain what a project does and how to get started.
  - Relative links are preferred for an easier local clone experience.
- Limits, bias, or scope:
  - This is platform guidance for repository design, not evidence about the FDE role itself.
- Access status: Accessible

### 8) Google: Helpful, reliable, people-first content
- Title: Creating helpful, reliable, people-first content
- Organization: Google
- Named author or speaker: Not clearly stated.
- URL: https://developers.google.com/search/docs/fundamentals/creating-helpful-content
- Publication date: Not clearly stated.
- Date actually checked: 2026-11-09
- Source type: search quality guidance
- Claims it supports:
  - Content should be helpful, reliable, original, and clearly attributable.
  - People-first content is better than content designed only to manipulate rankings.
  - Trust and clarity are important for informational pages.
- Limits, bias, or scope:
  - This is search-quality guidance, not a proof of correctness for any specific repository topic.
- Access status: Accessible

## B. Attributed opinions

- Shyam Sankar’s interview with Stratechery is a practitioner perspective, not a universal definition. It is useful for understanding how Palantir describes the product strategy behind FDE work, especially its emphasis on customer-specific problems and the translation from narrow cases to reusable product improvements.
  - URL: https://stratechery.com/2026/an-interview-with-palantir-cto-shyam-sankar-about-the-ai-religious-war/
  - Date checked: 2026-11-09
  - Status: Accessible, but the page is a media interview and should be treated as an opinionated perspective rather than neutral fact.

## C. Editorial synthesis

The repository synthesizes the following lessons across multiple sources:
- FDE is best understood as a customer-proximity delivery model, not a single universal job title.
- The work often sits at the boundary between customer delivery and platform/product learning.
- The most robust AI deployments rely on system design, authorization, retrieval, evaluation, and operational discipline, not only model quality.
- A product feedback loop links customer pain to reusable platform improvements.
- Simpler workflows often outperform more complex agentic designs until evidence justifies added autonomy.

## D. Hypothetical examples

The support-assistant scenario, the evaluation cases, and the “product feedback loop” examples are illustrative examples built for clarity and teaching. They are not real customer engagements, claims of deployment success, or evidence of production readiness.

## Access notes

The following source type was not fully verifiable from the available materials and has therefore been treated cautiously:
- Stratechery interview: accessible through the public web page, but it is a media opinion piece and should not be treated as a neutral or comprehensive industry definition.

## Source usage policy

This repository does not claim universal consensus from these sources. The role descriptions and practitioner perspectives are used to support the explanations where appropriate, while the more general conclusions are labeled as guide-level synthesis.
