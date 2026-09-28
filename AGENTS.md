# Repository guidance for coding agents

This is the central documentation repository for service-product POCs. Application code may live in separate repositories.

1. Read the root README, the current workflow in `shared/workflow/workflow.md`, and only the relevant project README before changing project documents.
2. Treat `portfolio/project-catalog.md` as a list of candidates. Do not infer that its first row is selected. Create a project directory only when the user selects a project in a dedicated task/session.
3. Keep shared rules under `shared/` and product-specific requirements, designs, prompts, and decisions under that project's directory.
4. Keep one canonical current document per topic. Remove superseded drafts from the current tree after consolidating needed content. Git history retains earlier text.
5. For Base44 prompts, use the Salon Booking prompts as a quality reference: specify product context, exact scope, routes, locale, design system, data, behavior, responsive/accessibility expectations, exclusions, acceptance criteria, and a stop point. Do not copy salon-specific product behavior into another POC.
6. The user operates Base44 unless they explicitly ask the agent to operate it. Record only outputs and credit information that the user actually provides or that can be verified.
7. Do not mark a prototype pass reviewed or complete without evidence from its actual output.
