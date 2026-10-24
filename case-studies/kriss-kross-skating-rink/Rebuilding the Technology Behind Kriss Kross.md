# Rebuilding the Technology Behind Kriss Kross

**A purpose-built POS, management, and reporting solution designed to streamline operations and support long-term growth.**

- **Client**: Kriss Kross Skatium Synergy Limited
- **Role**: Solution Architecture, UI/UX Design & Full-Stack Development
- **Team Makeup**: Independent / Sole Developer
- **Timeline**: 2 months 

<br>

# Overview

Following a significant operational setback, Kriss Kross Skating Rink needed more than a fresh start. It needed a stronger technological foundation.

I led the end-to-end design and development of a custom POS and management platform, replacing an unreliable legacy system with a solution built around the business's operational needs, financial realities, and ambitions for growth.

<br>

# About Kriss Kross

Kriss Kross Skatium Synergy Limited is a company dedicated to providing quality skating experiences. Kriss Kross operates a 500sqm outdoor roller skating rink, as well as a mobile skating rink setup for corporate, school, private, and NGO events. 

<br>

# The Problem

> **Outgrowing a System That Was Holding Us Back**

Our existing WordPress and WooCommerce solution had served its purpose, but its limitations were becoming increasingly costly.

An outdated, unsupported POS plugin introduced inventory and accounting discrepancies, while missing functionality left critical operational processes dependent on manual intervention.

With reopening approaching, we needed a solution that could:

- **Improve reliability:** Eliminate recurring transaction and inventory inconsistencies.
- **Simplify operations:** Automate manual processes across sales, subscriptions, and stock management.
- **Adapt to the business:** Support complex pricing rules, multiple locations, and evolving operational needs.
- **Remain financially sustainable:** Deliver the required functionality without prohibitive recurring software fees.

The challenge was clear: build a robust, scalable foundation without compromising our reopening timeline or financial recovery.

<br>

# The Process

> **From Operational Challenges to a Working Product**

With just two months until reopening, I approached the project with a clear priority: solve the problems that mattered most, without overengineering the solution.

**01 — Discover & Define**

Working closely with my co-owner, I mapped existing workflows, documented operational bottlenecks, developed user stories, and researched comparable solutions to establish a clear set of requirements.

**02 — Evaluate & Prioritise**

After assessing third-party platforms, I determined that their recurring costs were not sustainable for the business. I chose to develop an in-house solution, prioritising business-critical functionality for the initial release and establishing a roadmap for future improvements.

**03 — Architect, Design & Build**

I translated our requirements into application workflows, interface designs, and technical specifications. Using Codex to accelerate implementation from my designs and pseudocode, I developed the frontend and backend within a tightly constrained schedule.

**The result:** A launch-ready solution completed four days before the rink reopened.

<figure>

```python
class Role(models.Model):
    """
    Role per portal, e.g. 'Admin', 'Manager', 'Cashier'.
    """

    portal = models.ForeignKey(Location, on_delete=models.CASCADE)  # portal_id
    role_id = models.IntegerField() # per-portal identifier
    name = models.CharField(max_length=70)
    description = models.TextField(blank=True)

    class Meta:
        unique_together = ("portal", "role_id")

    def __str__(self):
        return f"{self.portal.name} - {self.name}"

```

<figcaption>A code snippet from the user's roles & permissions model definition</figcaption>

</figure>

<br>

# The Solution

> **Two Applications. One Connected Operational System.**
> 

I developed two purpose-built applications designed to work together, giving frontline staff a simpler transactional experience while providing management with greater operational control.

**Customer-Facing POS**

- Process sales and automatically apply eligible discounts.
- Validate active subscriptions and redeem member passes.
- Record inventory transactions across business locations.

**Management & Reporting Dashboard**

- Configure products, ticket schedules, pricing, and multi-layered promotional rules.
- Manage inventory movements between warehouses and operating locations.
- Access centralised sales, inventory, and management reports.
- Administer subscriptions and other essential business operations.

Rather than forcing the business to adapt to a generic platform, the solution was designed around how Kriss Kross actually operates.

The underlying product roadmap also accommodates future capabilities, including employee scheduling, third-party integrations, and merchandise assembly workflows.

<br>

# A Peek into the Architectural Reasoning

> **Designing a Discount Engine for Real-World Complexity**
> 

Promotional pricing in an entertainment business is rarely straightforward. Discounts can depend on what customers purchase, when and where they purchase it, and whether multiple offers can be combined.

Rather than hardcoding individual promotions, I designed a configurable, rules-driven discount engine that gives management control over three key aspects of promotional pricing:

**01 — Discount Mechanics**

Support for cart, item, and category discounts, expressed as percentages or fixed amounts, alongside Buy X Get Y and free-item redemption offers.

**02 — Conditional Eligibility**

Configurable conditions based on cart subtotal, item quantities, and category quantities, combined using AND/OR logic. Additional controls define product exclusions, eligible business locations, date ranges, and daily promotional schedules.

**03 — Application & Conflict Controls**

The engine evaluates eligible promotions and, where no priority is defined, automatically selects the discount offering the greatest customer saving. Configurable priority rules resolve equal-savings scenarios, while additional controls govern discount stacking, calculation order, usage limits, discount caps, and automatic application.

**The Architectural Decision**

By making promotional behaviour configurable rather than dependent on individual code changes, I created a pricing system that accommodates complex campaigns while reducing manual intervention and supporting future business requirements.

<br>

# Technology & Architecture

I selected a practical combination of established technologies that supported rapid development, operational reliability, and future extensibility.

| Layer | Technology |
| --- | --- |
| Product & Experience Design | Figma |
| Frontend Applications | React, Vite, Tailwind CSS |
| Backend & API | Django, Python |
| Data Management | MySQL |
| Containerisation & Deployment | Docker |
| Version Control | GitHub |
| Development & AI Assistance | VS Code, Codex |

<br>

## **Architectural Approach**

The solution separates customer-facing transactional workflows from administrative functions, with Django APIs and a relational data layer supporting the applications.

By retaining ownership of the software and its deployment, Kriss Kross gained greater flexibility to maintain and evolve the platform without depending on a third-party product roadmap.

<br>

# Impact & Results

> **Less Manual Work. Greater Control. Lower Costs.**
> 

The new platform addressed longstanding operational challenges, giving the team more time to focus on running the business rather than correcting its systems.

### Operational Efficiency

**Daily → At Most 6 Times Monthly**

Stock reconciliation, previously performed at the end of every operational day, is now required no more than six times per month.

**Up to 5 Minutes → Under 1 Minute**

Customer subscription lookup and verification now takes less than a minute, replacing a manual logbook process that could take up to five minutes per customer.

**Automated Promotional Pricing**

Complex discounts are applied according to configured rules, eliminating routine administrative price adjustments and reducing opportunities for human error.

### Management & Commercial Value

- Introduced structured inventory tracking across warehouses and business locations.
- Centralised reporting, improving visibility into sales, inventory, and operational performance.
- Avoided over **$200 per month** in third-party software subscription fees.
- Delivered the initial platform **four days before reopening**, within a two-month development window.

**Beyond the immediate improvements, the project established a technology foundation that Kriss Kross can continue to own, refine, and expand as the business grows.**

<br>

# POS Client Demos
POS client login demonstration
![POS client login demonstration](/case-studies/kriss-kross-skating-rink/assets/pos-login-demo.gif)

<br>

POS client checkout demonstration
![POS client checkout demonstration](/case-studies/kriss-kross-skating-rink/assets/pos-checkout-demo.gif)

<br>

POS client subscription lookup
![POS client subscription lookup](/case-studies/kriss-kross-skating-rink/assets/pos-customer-lookup-and-item-redemption.gif)

<br>

# Management & Reporting Dashboard Demos
Dashboard reporting view
![Dashboard reporting view](/case-studies/kriss-kross-skating-rink/assets/dashboard-demo.gif)

Dashboard dark/light theme toggle
![Dashboard dark/light theme toggle](/case-studies/kriss-kross-skating-rink/assets/dashboard-theme-toggle-demo.gif)

