# Building a Digital Home for Ogbemi Heymann

**An artwork-led portfolio and custom content management platform designed to reflect a contemporary artist's identity and support his evolving career.**

- **Client:** Ogbemi Heymann (via Uliuwa)
- **Role:** UI/UX Design & Full-Stack Development
- **Team Makeup:** Independent Designer & Developer, collaborating with Uliuwa's Curator
- **Timeline:** 2 months
- **Website:** [https://ogbemiheymann.com](https://ogbemiheymann.com)

<br>

# Overview

Ogbemi Heymann's artistic practice was well established, but his digital presence had yet to reflect the depth of his work and creative identity.

Working with artist management company Uliuwa, I led the end-to-end design and development of a dedicated portfolio website, translating the artist's creative direction into a refined, gallery-inspired digital experience.

Beyond showcasing his artworks, I developed a custom content management system and integrated his existing Airtable catalogue, giving Uliuwa the tools to independently maintain and evolve his online presence.

<br>

# The Problem

> **An Artistic Identity Without a Digital Home**

When Mr. Ogbemi approached Uliuwa, he was looking for a team to manage the business and marketing aspects of his career, allowing him to focus on creating art.

During our initial discovery, we identified a significant gap between his artistic practice and his online presence. His social media profiles were outdated, he had no dedicated website, and audiences primarily discovered his work through word of mouth and gallery exhibitions.

Uliuwa identified establishing a cohesive brand identity and digital presence as an immediate priority. We needed a solution that could:

- **Establish a digital presence:** Create a dedicated online destination for the artist and his work.
- **Communicate his identity:** Reflect his artistic vision, themes, and creative explorations.
- **Showcase his portfolio:** Present his artworks in a cohesive, accessible, and engaging format.
- **Improve discoverability:** Make his work more accessible to audiences beyond existing gallery networks and personal referrals.

The challenge was to create more than an online portfolio: a digital experience that meaningfully represented the artist and supported his long-term professional development.

<br>

# The Process

> **Translating Artistic Identity into a Digital Experience**

Working closely with Uliuwa's Curator, I led the website's design and development from concept through implementation, translating the artist's creative direction into a cohesive digital experience.

**01 — Discover & Define**

I began by consulting Uliuwa's Curator to understand the artist's identity, creative themes, and long-term aspirations. We established a clear objective: create a portfolio-led website with editorial capabilities, allowing visitors to explore both his completed works and the creative thinking behind them.

**02 — Research & Explore**

I immersed myself in the artist's digital catalogue, studying his body of work to develop a deeper understanding of his practice. I then researched artists exploring similar themes, examining how their websites presented artworks, structured content, and guided visitors. These insights informed my approach to the website's visual design and user experience.

**03 — Design & Refine**

Guided by the artist's preference for simplicity, I developed a minimalist visual direction that placed his artworks at the centre of the experience. Soft white backgrounds evoked the openness of a gallery, while restrained typography, minimal text, and subtle transitions created an understated interface that complemented, rather than competed with, the artwork.

**04 — Develop & Integrate**

I translated the Figma prototypes into a responsive React application and developed a custom CMS for managing website content. Rather than duplicating the artist's existing Airtable catalogue, I integrated it directly into the website, allowing Uliuwa to control which artworks and information were publicly displayed while maintaining a single catalogue.

<br>

# The Solution

> **An Artwork-Led Portfolio with Independent Content Management**

I developed a full-stack website that provides Mr. Ogbemi with a dedicated digital presence while giving Uliuwa the tools to manage its content independently.

**Artist Portfolio & Experience**

- Present the artist's creative themes through curated artwork and editorial content.
- Explore his body of work through a searchable, filterable archive and interactive gallery.
- Showcase available artworks, exhibitions, and publications.
- Facilitate enquiries and mailing list subscriptions.

**Content Management System**

- Create, edit, and publish articles through a custom block-based editor.
- Manage exhibitions, supporting artworks, and downloadable resources.
- Configure website settings and review visitor enquiries.
- Integrate the existing Airtable catalogue through configurable field mappings.

The result is a cohesive digital experience that balances artistic expression with practical content management, allowing the artist's team to maintain his professional presence without ongoing developer intervention for routine updates.

<br>

# A Peek into the Design Reasoning

> **Letting the Artwork Speak for Itself**

Mr. Ogbemi's practice is rich in symbolism, while his personal aesthetic favours simplicity and restraint. The challenge was to create an engaging digital experience without distracting from the artworks themselves.

I approached the website as a digital gallery, using generous whitespace, understated typography, and minimal interface elements to keep attention on the artwork. Subtle transitions introduced movement without compromising the experience's quiet sophistication.

**The Design Decision**

Rather than treating the website as a visual attraction in its own right, I designed the interface to complement the artist's work, allowing his creative identity to define the experience.

<br>

# A Peek into the Architectural Reasoning

> **One Artwork Catalogue. Multiple Applications.**

Uliuwa already maintained a comprehensive catalogue of the artist's work in Airtable. Recreating the master catalogue within the website's database would introduce unnecessary duplication and additional maintenance.

Instead, I developed an Airtable integration with configurable field mappings, allowing the website to retrieve and present artwork information from the existing catalogue.

**The Architectural Decision**

By preserving Airtable as the primary source of artwork records while using a dedicated CMS for website-specific content, I reduced duplicated data management and allowed Uliuwa to maintain its established cataloguing workflow.

<br>

# Technology & Architecture

I selected a full-stack architecture that balanced design flexibility, maintainability, and compatibility with the client's existing hosting infrastructure.

| Layer | Technology |
| --- | --- |
| UI/UX Design & Prototyping | Figma |
| Frontend | React, TypeScript, Vite, Tailwind CSS |
| Backend & API | Node.js, Express |
| Data Management | MySQL |
| Artwork Catalogue Integration | Airtable API |
| Email Notifications | Nodemailer, SMTP |
| Version Control | Git, GitHub |
| Deployment | cPanel, Node.js |

## Architectural Approach

The website separates public-facing experiences from administrative workflows, supported by an Express API connecting MySQL-managed content and Airtable artwork records.

The application is deployed on Uliuwa's existing cPanel-managed shared hosting infrastructure. I also retained Docker configurations and a GitHub Actions build workflow to support a potential future migration to dedicated hosting.

<br>

# Impact & Results

> **An Authentic Digital Identity. A Platform Built to Last.**

The website established a dedicated digital presence for Mr. Ogbemi, bringing his artworks, creative themes, and professional journey into a cohesive experience while giving Uliuwa independent control over its content.

### Creative & Brand Impact

**An Authentic Representation of the Artist**

Mr. Ogbemi expressed exceptional satisfaction with the finished website, describing it as a true reflection of his identity, artistic practice, and career. His continued appreciation reinforced the success of the design's central objective: allowing his work and creative identity to speak for themselves.

### Operational & Technical Impact

**Independent Content Management**

Uliuwa's team now actively maintains the website through the custom CMS. The interface has been well received for its simplicity and ease of use, with no operational difficulties reported to date.

**Preserved Existing Workflows**

The Airtable integration eliminated the need to duplicate the artist's master catalogue, allowing Uliuwa to continue managing artwork records through its established system.

**A Maintainable Digital Foundation**

The modular application architecture and reusable components provide a foundation for ongoing improvements, while the deployment configuration supports the client's current infrastructure and potential future migration.

**Beyond delivering a professional portfolio, the project successfully translated the artist's creative identity into a digital experience while equipping his management team with the tools to maintain and evolve it independently.**

<br>

# Website Demos

### [Check out Ogbemi Heymann's live website here](https://ogbemiheymann.com)

[![Ogbemi Heymann's site](/case-studies/ogbemi-heymann/assets/home-page.gif)](https://ogbemiheymann.com)

Editing and exhibition through the CMS
![Editing and exhibition through the CMS](/case-studies/ogbemi-heymann/assets/exhibitions-edit.gif)