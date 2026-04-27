---
template: dispatch.html
title: OpenAfterHours · After-hours dispatch
description: A personal dispatch from the maintainer of OpenAfterHours — open-source regulatory tools for the financial industry, built after hours.

# Masthead strip
issue: "№ 001 · Vol. I · 2026"
masthead_lead: The After-Hours
masthead_tail: Co.
dateline: London · GMT · MIT licensed

# Meta-row
tagline: A personal dispatch from the maintainer of OpenAfterHours
cadence: Published continuously · ☾ Written after dark

# Lede
deck: From the desk · Letter from the maintainer
headline_lead: "Capital adequacy is a"
headline_emphasis: public good
headline_tail: ". The software for it should be too."
intro_long: >-
  I build open-source regulatory tools for the financial industry —
  quietly, after the day job. The premise is simple: banks that hold the
  right capital and run the back-office cheaply can offer the public
  better products. The maths is well-defined; the software shouldn't be a
  moat.
intro_coda: >-
  A parallel practice, kept honest by being open, and kept warm by being
  shared.
byline: The Maintainer
read_time: 4 min

# // Now strip
now:
  - Working through PRA PS1/26 mapping for the SA module.
  - "Reading: Bank of England SS9/17, on internal model governance."
  - "Listening: shipping forecasts, mostly."

# Beliefs (4 columns, § 01 – § 04)
beliefs:
  - n: "01"
    head: Capital adequacy is a public good.
    body: >-
      Risk-Weighted Assets, IRB, the Standardised Approach — these define
      how safely a bank operates and how much it costs to hold a
      customer's mortgage. The arithmetic should be transparent and the
      implementations should be free.
  - n: "02"
    head: Cheap back-office, cheap products.
    body: >-
      Every line item that a bank pays a vendor for compliance computation
      is a line item the customer eventually pays. Open-source the
      computation, push the cost curve down, the saving lands somewhere
      real.
  - n: "03"
    head: Sustainable software, sustainable teams.
    body: >-
      Agile is not a ceremony — it's a way to ship for years without
      burning out. Small batches, honest tests, and code people are proud
      to maintain at 11pm on a Tuesday.
  - n: "04"
    head: Regulators are users, not adversaries.
    body: >-
      PRA, BCBS, EBA — these documents are an interface. Treat them like
      an API spec, write tests against them, and the rest follows.

# Project card
project:
  name: UK Credit Risk RWA Calculator
  tagline: High-performance Risk-Weighted Assets calculation for Basel 3.1 and CRR frameworks.
  repo_url: https://github.com/OpenAfterHours/rwa_calculator
  bullets:
    - { label: "Standardised + IRB", body: "F-IRB and A-IRB on top of the Standardised Approach." }
    - { label: "Polars-fast",        body: "50–100× over the equivalent pandas pipeline." }
    - { label: "~1,915 tests",       body: "Cross-checked against the regulator's worked examples." }
    - { label: "PRA PS1/26",         body: "Tracking the Basel 3.1 transposition for UK firms." }

# 8 formulas with their scatter positions, in render order.
# Each entry merges FORMULAS[i] with FORMULA_SCATTER[i] from the source.
formula_scatter:
  - { text: "K = LGD × Φ[√(1−R)⁻¹ × Φ⁻¹(PD) + √(R/(1−R)) × Φ⁻¹(0.999)] − PD × LGD", top: "6%",  left: "3%",  fs: 12, rot: -2.4 }
  - { text: "RWA = K × 12.5 × EAD",                                                  top: "14%", left: "62%", fs: 14, rot:  1.2 }
  - { text: "R = 0.12 × (1 − e⁻⁵⁰·ᴾᴰ)/(1 − e⁻⁵⁰) + 0.24 × [1 − (1 − e⁻⁵⁰·ᴾᴰ)/(1 − e⁻⁵⁰)]", top: "24%", left: "8%", fs: 11, rot: 2.0 }
  - { text: "b = (0.11852 − 0.05478 × ln(PD))²",                                     top: "32%", left: "42%", fs: 16, rot: -1.0 }
  - { text: "MA = (1 + (M − 2.5) × b) / (1 − 1.5 × b)",                              top: "40%", left: "74%", fs: 11, rot:  2.5 }
  - { text: "Φ(x) = ½[1 + erf(x/√2)]",                                               top: "48%", left: "2%",  fs: 13, rot: -2.0 }
  - { text: "EL = PD × LGD",                                                         top: "54%", left: "50%", fs: 10, rot:  1.5 }
  - { text: "RW = K × 12.5 × MA",                                                    top: "60%", left: "78%", fs: 12, rot: -2.5 }

# Recent dispatches — leave empty until the first post is filed.
posts: []

# Footer links
links:
  - { label: "github · personal",        url: "https://github.com/luckyphil122",                 external: true }
  - { label: "github · openafterhours",  url: "https://github.com/OpenAfterHours/rwa_calculator", external: true }
  - { label: "email",                    url: "mailto:hello@openafterhours.dev",                  external: false }
---
