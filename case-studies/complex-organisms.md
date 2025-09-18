---
layout: case-study
title: Case study<span class="hilight">.</span>
masthead-pill: Walmart
masthead-intro: Complex organism component construction
masthead-description: Building complex organism components in Figma, in a way that optimizes maintenance while adhering to system best practices.
masthead-image: work-landing-05.png
masthead-caption: Component construction
masthead-alt: Component construction
masthead-duration: Part of the PX Pattern library project
exclude: true
---

{% include section-title-list.html label="Impact" %}

- Delivered complex organisms in Walmart's Enterprise business pillar to ~60 designers and ~200 web engineering partners.
- Replaced multiple Filter Panel components found in single-product subsystems, all with unique visual inconsistencies, managed by multiple teams.
- Estimating the removal of hours spent by individual teams building and owning custom Filter Panel components, the savings per year add up quickly. We don't have concrete data on this, but some "estimation math" can be enlightening.
	- ~60 designers and ~200 engineers in this business pillar
	- If ~5 designers & ~10 engineers, representing work in the 5 sub-pillars are each owning these patterns, spending 4 hours/week customizing and maintaining them...
	- It's reasonable to assume 960 hours/year (at $96K per year) is a **low** estimate of resources spent on inconsistent artifacts in design and code, for this one component.

{% include figure-big.html image="case-studies/complex-organisms-1.png" caption="Filter Panel organism" %}

{% include section-title.html label="Summary" %}

This is one example of the kind of complex, organism level components we shipped in the PX Pattern library, highlighted in my [pattern libraries]({% link case-studies/pattern-libraries.md %}) project.
{: .mt4 .lh-copy .f5 .f4-m .f4-l }

{% include case-study-h3-list.html label="Team" %}

- Product team
	- 1 senior director, 1 product design director, 1 product design lead, 2 product designers
- Specialized contributors
	- 1 design system lead, 1 accessibility lead
- Partners
	- Flexible group of dedicated React engineers
	- Several "pattern library ambassadors," representing all product teams who use this library, and who own the customization of complex organism components (more explanation below).

{% include case-study-h3-list.html label="My roles & responsibilities" %}

- Review component examples collected by product designers
- Analyze user flows and component behavior in production
- Build new Filter Panel components in accordance with Living Design processes and standards.
- Test Figma components with design partners to ensure features meet user needs
- Write engineering specs, and lead review sessions with engineers and accessibility partners.
- QA finished React components in Storybook

{% include section-title.html label="Challenge" %}

{% include copy-block.html copy="In addition to defining the list of necessary features this component needed, the primary challenge was delivering a complex component that designers could:" %}

- Easily pull from the library.
- Customize to suit their use-case without resorting to detaching.
- Maintain in their Figma files, over time, being able to make necessary changes based on product requirements.

{% include section-title-list.html label="Solutions" %}

{% include case-study-h3-list.html label="Step 1: Base Parts" %}

- Define the component's base parts.
- Use core system components when possible.
- Create new molecules only when necessary.

{% include figure-big.html image="case-studies/complex-organisms-2.png" caption="Filter Panel base parts" %}

{% include copy-block.html copy="👆🏼 Start with component molecules, and account for all possible filter types necessary for the applications in question." %}

{% include section-title-list.html label="Solutions" %}

{% include case-study-h3-list.html label="Step 2: Filter Groups" %}

- Use the base parts to build **Filter Groups** (Radio groups, Checkbox groups, etc.).
- As we move up in complexity, we define options for the user in Figma's component properties.

{% include figure-big.html image="case-studies/complex-organisms-3.png" caption="Filter Panel components" %}

👆🏼 The result is a single **Filter type** component. These **Filter type** blocks are assembled into the resulting Filter Panel.
{: .mt4 .lh-copy .f5 .f4-m .f4-l }

{% include section-title-list.html label="Solutions" %}

{% include case-study-h3-list.html label="Step 3: Filter Panel construction" %}

{% include copy-block.html copy="Note: Considering the level of component complexity, we will jump into a Figma file to discuss construction and intent in more detail. We keep detailed documentation in the pattern library file, as a resource for library maintainers." %}

{% include copy-block.html copy="Using the Figma frames and documentation below, for example, the pattern library team and the product ambassadors can collaborate to build customized versions of the Filter Panel. The ambassadors are then responsible to see that other designers on their team have the appropriate sources of truth needed in their product designs." %}

{% include figure-big.html image="case-studies/complex-organisms-4.png" caption="Filter Panel organism construction" %}

{% include section-title-list.html label="Solutions" %}

{% include case-study-h3-list.html label="Step 4: Pattern library ambassadors" %}

{% include copy-block.html copy="The pattern library team relies on library ambassadors (mentioned above). These are product designers, within the Enterprise business pillar, who have dedicated capacity to help other designers in their area use and customize these components. The ambassadors help maintain customized versions of our organism components." %}

{% include figure.html image="case-studies/complex-organisms-ambassadors.png" caption="We rely on library ambassadors to help with education and governance" %}

{% include section-title.html label="Learnings" %}

{% include copy-block.html copy="Approach complexity with caution. We know that we need to improve visual inconsistencies across the various product domains in the Enterprise business pillar. Further, we know how much design and tech debt are created if we don't do this. And we know this can't be accomplished just by building complex components, writing some documentation, and releasing them in Figma." %}

{% include copy-block.html copy="We need the support of product ambassadors, who are committed to the pattern library's intent and goals. We need collaborative learning and working sessions, and we need constant feedback to iterate these complex components. Also important, we need to work closely with all of our engineering partners to make sure they have all access to the same finished React components." %}
