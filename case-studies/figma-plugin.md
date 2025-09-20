---
layout: case-study
title: Case study<span class="hilight">.</span>
masthead-pill: Walmart
masthead-intro: Leveraging AI to improve designer experience
masthead-description: Using Cursor (AI code editor) to build a Figma plugin, allowing designers to easily construct complex organisms..
masthead-image: work-landing-02.png
masthead-caption: Figma + Cursor
masthead-alt: Figma and Cursor logos
masthead-duration: Q1/Q2, FY26 (April 2025 - May 2025)
exclude: true
---

{% include section-title.html label="Background" %}

{% include copy-block.html copy="As we moved into FY26, Walmart's business leadership was encouraging design and tech teams to embrace AI tools, and find ways to use them to improve our workflows. A quarterly design summit was dedicated to the topic of new AI tools. Design leadership had given the design system team a directive to find ways to automate complex aspects of our systems, to improve user experience." %}

{% include case-study-h3.html label="My role & responsibilites" %}

{% include copy-block.html copy="Looking for an interesting way to leverage my previous front-end development experience, I decided that exploring Figma plugins would be an exciting way to approach the automated construction of complex components." %}

{% include figure.html image="case-studies/figma-plugin.png" caption="Figma plugin development" %}

{% include section-title.html label="Challenge" %}

{% include copy-block.html copy="One of the largest component sets in the PX Pattern Library, a Walmart Enterprise pattern library, is the Side Navigation component set, which we refer to as the 'SideNav' component. The SideNav component set is made up of multiple atoms, molecules, and organisms. It's highly flexible, and it's organized in the library in such a way that library maintainers can recreate variations of the SideNav for any product in Walmart's Enterprise business pillar." %}

{% include figure-big.html image="case-studies/figma-plugin-sidenav.png" caption="PX Pattern Library SideNav components" %}

{% include copy-block.html copy="The only downside of this component set, which is an aspect of any such complex component set, is that it requires time consuming collaboration with the pattern library team when someone needs a variation or iteration. To maintain library integrity, and to ensure that new variations are constructed correctly, users must:" %}

- File a ticket with the pattern library team.
- Submit a hierarchy of parent/child links requested in the new variation.
- Wait for the pattern library team to:
	- Build the new variation in a library branch.
	- Go through the review/approval/merge process for the work, in Figma.
	- Publish & release the new/updated components in the library.

{% include copy-block.html copy="Since engineers use the same atoms & molecules to construct a SideNav, in React, it's fortunately easy for them to follow design comps when parent and child links change. But the design process is slower than we'd like it to be." %}

{% include section-title.html label="Opportunity" %}

{% include copy-block.html copy="I saw this as a great candidate for Figma plugin exploration. If a user can fill in a form, in a plugin UI, and output the assembled component set to their design file, they would require no involvement on the part of the pattern library team. Designers can iterate as many versions of the SideNav as needed, and dispose of any previous versions. As long as they don't change its foundational structure (spacing, font sizes, etc.), engineers can use the system components in React." %}

{% include section-title.html label="Solutions" %}

{% include case-study-h3.html label="Step 1: The plugin development environment" %}

Figma provides extensive information in their [Plugin Quickstart Guide](link https://www.figma.com/plugin-docs/plugin-quickstart-guide/). I have enough experience with HTML/CSS, Node, JavaScript & TypeScript to spin up the skeleton of a basic plugin.
{: .mt4 .lh-copy .f5 .f4-m .f4-l }

{% include figure.html image="case-studies/figma-plugin-cursor-app.png" caption="Cursor App" %}

{% include copy-block.html copy="My first impression of Cursor was that it's a clone of VS Code with a built-in engineering partner. 🤓" %}

{% include section-title.html label="Solutions" %}

{% include case-study-h3.html label="Step 2: The plugin modal UI" %}

{% include copy-block.html copy="With some basic coding experience, getting the plugin modal UI set up is fairly easy. The HTML & CSS for this UI is very basic. I was able to add the necessary JavaScript to manipulate the DOM based on user input." %}

- User adds/removes as many parent-child navigation groups as needed.
- Enter link labels into the input fields.
- Click **Run plugin**.

{% include figure-big.html image="case-studies/figma-plugin-modal.png" caption="The Figma plugin modal" %}

{% include section-title.html label="Output" %}

{% include copy-block.html copy="Upon running the plugin, the user will get the following output, on their artboard:" %}

- One component set for each parent/child group, with variants for every possible active state of the parent and child links.
- The "MySideNav" component, which is made up of:
	- A "Home" link, which appears by default
	- The collapsed variant of each parent/child group
- The [PX] SideNav-MySideNav organism. This is the component designers would place into their template.

{% include figure-big.html image="case-studies/figma-plugin-output.png" caption="The Figma PX Sidenav plugin output" %}

{% include section-title.html label="Next steps" %}

{% include copy-block.html copy="I handed off this project when I left Walmart, as a result of their relocation mandate. There are a couple small but crucial details left to be completed:" %}

- The [PX] SideNav-MySideNav component has two variants: Expanded and Collapsed. The Collapsed variant needs to be output in the proper state to align with the existing library components.
- While the icons are very easy to change manually, it would be nice to include an additional form in the plugin UI, allowing the user to choose each leading icon variant.
- I have a small bug where the child links are not properly set to the active state in their variants. The debugging process with Cursor has been pretty easy, so it's a small issue to fix.

{% include section-title.html label="Learnings" %}

{% include copy-block.html copy="Overall, I'm pretty amazed at how easy it is to build a complex Figma plugin, using Cursor's conversational UI. I think it's definitely still a requirement that someone building a Figma plugin with Cursor have a comfortable level of knowledge of JavaScript, in order to write effective prompts. But it allowed me to complete this task without involving an engineering partner. I would want a qualified engineer to help with some debugging, and to review the code before shipping, but the ability to do this without taking up the design system's engineering resources was highly rewarding!" %}