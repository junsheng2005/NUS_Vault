---
title: "Systems Thinking — CLD, Stock & Flow Diagrams, and System Archetypes"
course: "UTC1702H"
tags:
  - systems-thinking
  - causal-loop-diagram
  - stock-and-flow
  - system-archetypes
  - vensim
aliases:
  - CLD SFD Archetypes
---

# Systems Thinking — CLD, Stock & Flow Diagrams, and System Archetypes

> [!abstract] Big picture
> **CLD → SFD → simulation → policy experiments.**
> A Causal Loop Diagram (CLD) is a **qualitative** representation of system structure and feedback. A Stock-and-Flow Diagram (SFD) turns that structure into a **quantitative, simulatable** model. System archetypes are recurring feedback structures that help diagnose persistent patterns and locate possible leverage points.

---

## 1. Causal Loop Diagrams (CLDs)

A **Causal Loop Diagram** is a qualitative tool for conceptualising a complex real-world issue. Its purpose is to make the modeller's **mental model / assumptions explicit**, so that the system's structure can be examined through cause–effect relationships and feedback loops.

### Four essentials

1. **Variables** — elements that can change over time; often nouns taken from the problem narrative.
2. **Arrows / causal links** — show that one variable influences another.
3. **Polarity** — each link is marked `+` or `−`.
4. **Feedback loops** — circular causal chains labelled **R** (reinforcing) or **B** (balancing).

![[obsidian_assets/cld_four_essentials.png]]

### Visual: feedback-loop notation
![[obsidian_assets/cld_feedback_loops.png]]

### Visual: worked CLD example
![[obsidian_assets/cld_example_motivation.png]]

### Visual: feedback structure → behaviour
![[obsidian_assets/cld_loop_behaviour.png]]

### Reading polarity

For a causal link `A → B`:

- **`+` (same-direction relationship):** if A increases, B increases *relative to what it otherwise would have been*; if A decreases, B decreases.
- **`−` (opposite-direction relationship):** if A increases, B decreases *relative to what it otherwise would have been*; if A decreases, B increases.

> [!warning] Causation ≠ correlation
> A causal arrow should represent a plausible **causal mechanism**, not merely two variables that move together. If the apparent relationship is produced by a third factor, make that intermediary variable explicit.

### Reinforcing vs balancing loops

| Loop | Core logic | Typical behaviour |
|---|---|---|
| **R — Reinforcing** | The effect comes back and **reinforces the original change** | Exponential growth **or** exponential decline |
| **B — Balancing** | The effect comes back and **opposes the original change** | Goal-seeking / movement toward equilibrium |
| **B + delay** | Corrective action is delayed | Oscillation can emerge |

A useful way to classify a loop is to **trace a change all the way around the loop** and ask what happens when it returns to the starting variable.

### Behaviour Over Time Graphs (BOTGs)

The course links system **structure** to characteristic behaviour:

- **Reinforcing feedback → exponential growth/decline**
- **Balancing feedback without delay → goal-seeking**
- **Balancing feedback with delay → oscillation**
- **Reinforcing + balancing feedback → often S-shaped / limits-to-growth behaviour**

BOTGs are useful for identifying recurrence, spotting warning signals, understanding the effects of past actions, and hypothesising future trends.

### CLD construction checklist

> [!tip] When drawing a CLD
> - Use variables that can **vary over time**.
> - Make intermediary concepts/processes explicit.
> - Give **every causal link** a polarity.
> - Close causal chains into meaningful feedback loops.
> - Label loops `R1`, `R2`, `B1`, etc.
> - Explain the **logic of each loop in words**.
> - Relate the structure to an expected BOTG.
> - Ask which loop is likely to **dominate at different times**.

### Limitation of CLDs

CLDs are strong for **qualitative understanding**, but the slides emphasise that they do not by themselves provide quantitative inference or accurate forecasts. With multiple interacting loops, the overall dynamics can be difficult to predict. This motivates the move from CLDs to **Stock-and-Flow modelling**.

---

## 2. Stock-and-Flow Diagrams (SFDs)

An SFD represents the system in terms of **accumulations** and the **rates that change those accumulations**.

### Stocks

A **stock (level)** is an accumulation or state that can be measured at a particular point in time.

Examples from the course:
- volume of water in a bathtub
- number of trees in a forest
- books in a library
- bank balance
- level of happiness
- amount of atmospheric CO₂

Stocks give systems **inertia and memory**, and accumulation can create delays between inputs and outputs.

### Flows

A **flow (rate)** changes a stock over time and therefore normally has units of **stock-unit / time**.

Examples:
- filling and draining water
- planting and cutting trees
- CO₂ emissions and removals

### Visual: flows change stocks
![[obsidian_assets/sfd_flows.png]]

### Visual: rise, fall and equilibrium
![[obsidian_assets/sfd_accumulation.png]]

### Principle of accumulation

For a stock:

`Net change = Σ inflows − Σ outflows`

Therefore:

- **Rise:** inflows > outflows
- **Equilibrium:** inflows = outflows
- **Fall:** outflows > inflows

> [!important] Stock–flow distinction
> A **stock** is a state/quantity at a point in time.  
> A **flow** is an action/rate that changes that quantity over a period of time.

### Auxiliary variables and constants

- **Auxiliary variables** are intermediate variables that are neither stocks nor flows. They can determine the "speed" of flows and may represent rates, formulas, probabilities, or decision rules. Their values depend on other model variables.
- **Constants / parameters** are baseline inputs that remain relatively stable during a model run and are treated as exogenous inputs.

### How to build an SFD

![[obsidian_assets/sfd_development_steps.png]]

The course gives a five-step workflow:

1. **Identify all stocks** (boxes), including units.
2. For each stock, identify all **inflows and outflows** (pipes), including units.
3. For each flow, identify the **parameters/constants and auxiliary variables** that determine it; draw the SFD skeleton.
4. For each auxiliary variable, form the required **connections and equations**.
5. Implement the model in **Vensim**, simulate it, and interpret the BOTG in relation to the model structure: **which feedback loops dominate, and when do key changes occur?**

### Example: Productive Opportunity Set (POS)

![[sfd_pos.png]]

### Additional SFD example: potential → active ecopreneurs
![[obsidian_assets/sfd_ecopreneur.png]]

This course example contains two stocks:

- **POS / Productive Opportunity Set**
  - inflow: `New Opportunity Identification`
  - influenced by `Innovation rate`
- **Funds**
  - inflow: `Income`
  - outflow: `Expenditure`

Auxiliary/parameter relationships connect POS to earnings and resource requirements. The key modelling lesson is that the SFD makes the **accumulations, rates, units, and equations explicit**, allowing the model to be simulated rather than merely hypothesised.

---

## 3. From CLD to SFD

Think of the two diagrams as different levels of the same analysis:

| CLD                      | SFD                                         |
| ------------------------ | ------------------------------------------- |
| Qualitative              | Quantitative                                |
| Variables + causal links | Stocks + flows + auxiliaries + parameters   |
| Shows feedback structure | Makes accumulation and rates explicit       |
| Hypothesises behaviour   | Simulates behaviour                         |
| Good for mental models   | Good for experiments / sensitivity analysis |

A practical workflow is:

**Problem narrative → variables → CLD → feedback loops → expected BOTG → identify accumulations → SFD → equations/units → simulation → compare BOTG with hypothesis → policy/sensitivity experiments**

---

## 4. Bass Diffusion: a useful CLD ↔ SFD example

The Bass Diffusion example models how **potential adopters become active adopters** through diffusion/contagion such as word-of-mouth.

The model demonstrates two interacting mechanisms:

1. **Reinforcing feedback:** more active subscribers create more opportunities for word-of-mouth contact, which creates more subscriptions.
2. **Balancing feedback:** as the pool of potential subscribers is depleted / the market approaches saturation, further growth becomes constrained.

The resulting stock behaviour is **S-shaped**: reinforcing feedback dominates early growth, then the balancing effect of market saturation increasingly dominates and growth flattens.

> [!example] Interpretation pattern
> Don't stop at "the graph is S-shaped." Explain **why**:
> - early period → reinforcing loop dominates;
> - transition → constraints become increasingly important;
> - later period → balancing loop / saturation dominates;
> - therefore the growth rate peaks and then declines while the stock approaches a limit.

---

## 5. System Archetypes

**System archetypes** are recurring system structures associated with commonly observed patterns of organisational behaviour and recurring problems. They help organise a complicated CLD into a recognisable structure and can point toward **leverage points**, counterproductive tendencies, counter-intuitive consequences, and limits to growth.

### Visual overview of the 10 archetypes
![[obsidian_assets/archetypes_overview.png]]

The course lists ten archetypes:

1. Limits to Growth / Limits to Success
2. Shifting the Burden
3. Eroding Goals
4. Escalation
5. Success to the Successful
6. Tragedy of the Commons
7. Fixes that Fail
8. Growth and Underinvestment
9. Accidental Adversaries
10. Attractiveness Principle

### Archetypes emphasised in the slides

#### Limits to Growth

![[obsidian_assets/archetype_limits_growth.png]]

**Structure:** a reinforcing process initially produces growth, but growth activates a **limiting condition** and a balancing loop that slows further improvement.

**BOTG:** growth accelerates and then slows/levels off; the course also connects combinations of reinforcing and balancing loops to an **S-shaped curve**.

**Diagnostic question:** *What constraint becomes stronger because we are succeeding?*

**Policy logic:** do not only push harder on the reinforcing engine; identify and address the limiting condition.

#### Fixes that Fail

![[obsidian_assets/archetype_fixes_fail.png]]

**Structure:** a fix reduces the problem symptom in the short term, but the fix also creates a delayed unintended consequence that eventually worsens the original problem.

**BOTG:** apparent improvement followed by recurrence/worsening of the problem; unintended consequences accumulate.

**Diagnostic question:** *What side effect of today's solution recreates tomorrow's problem?*

#### Shifting the Burden

![[obsidian_assets/archetype_shifting_burden.png]]

**Structure:** a **symptomatic solution** provides relatively immediate relief, while a **fundamental solution** addresses the underlying cause. Reliance on the symptomatic solution can weaken attention to the fundamental solution, often through a side effect.

**Diagnostic question:** *Are we becoming dependent on a quick fix instead of building the capability that solves the root problem?*

#### Eroding Goals

**Structure:** a gap exists between a goal and actual performance. Instead of improving the actual condition enough, pressure is relieved by **lowering the goal**.

**Diagnostic question:** *Are we solving the gap by improving reality—or by redefining acceptable performance downward?*

#### Escalation

![[obsidian_assets/archetype_escalation.png]]

**Structure:** two actors compare themselves with one another. Each actor's actions increase the perceived threat to the other, encouraging further action and creating mutually reinforcing competition.

**Diagnostic question:** *Are our actions driven by relative position against another actor, creating an arms race?*

#### Success to the Successful

![[obsidian_assets/archetype_success_successful.png]]

**Structure:** two activities compete for limited resources. Early success causes more resources to be allocated to one activity, which improves its future success; the other receives fewer resources and falls further behind.

**Diagnostic question:** *Is past success determining resource allocation in a way that makes future success self-fulfilling?*

#### Tragedy of the Commons

![[obsidian_assets/archetype_tragedy_commons.png]]

**Structure:** multiple actors gain individually from using a shared resource. Their combined activity pushes against a common resource limit, reducing the benefit available to everyone.

**Diagnostic question:** *Does each actor have an incentive to consume a shared resource even though aggregate use damages the whole system?*

#### Growth and Underinvestment

![[obsidian_assets/archetype_growth_underinvestment.png]]

**Structure:** demand/growth increases, but capacity or performance does not keep pace. If investment is insufficient or delayed, performance deteriorates and eventually constrains growth.

**Diagnostic question:** *Is current growth creating a capacity requirement that we are failing to invest in early enough?*

---

## 6. How to identify an archetype from a case

Do **not** begin by choosing an archetype and forcing the case into it. Build the causal story first.

1. Define the focal problem and time horizon.
2. Identify variables and causal mechanisms.
3. Draw the CLD with polarities.
4. Identify the reinforcing and balancing loops.
5. Sketch the expected BOTG.
6. Compare the **loop structure + BOTG** against archetype patterns.
7. Name the archetype only when the structure fits.
8. Use the archetype to ask where a useful **leverage point** might be.

> [!warning] Archetype ≠ BOTG alone
> A similar graph can be produced by different structures. Identification should be informed by the **CLD structure**, not only the shape of the behaviour-over-time graph.

---

## 7. Exam / analysis framework

When given a case, use this sequence:

### A. CLD
- What are the variables?
- What causes what?
- What is the polarity of each link?
- Which loops are `R` and which are `B`?
- Are there important delays?
- What BOTG should this structure generate?

### B. Archetype
- Which recurring feedback structure does the CLD resemble?
- What is the **reinforcing engine**?
- What is the **balancing/limiting mechanism** or unintended consequence?
- What behaviour should emerge over time?
- Where might intervention change the structure rather than only the symptom?

### C. SFD
- Which variables are **stocks**?
- What **flows** increase/decrease each stock?
- What are the units?
- Which auxiliaries/constants determine each flow?
- What equations connect them?
- What initial values and simulation horizon are needed?

### D. Simulation
- What BOTG appears?
- Which loop dominates early, middle, and late?
- Do the simulated results match the CLD-based hypothesis?
- Which parameters should be varied in a sensitivity analysis?
- What policy levers follow from the model structure?

---

## 8. High-yield memory map

**CLD = why variables influence each other**  
↓  
**Feedback loops = why behaviour persists or changes**  
↓  
**BOTG = what behaviour the structure may generate**  
↓  
**Archetype = recurring configuration of loops**  
↓  
**SFD = where quantities accumulate + how fast they change**  
↓  
**Simulation = what the specified structure actually does over time**  
↓  
**Sensitivity/policy experiments = where intervention may change outcomes**

---

## 9. Quick self-test

- Can I explain `+` and `−` polarity without saying merely "good" or "bad"?
- Can I trace a loop and justify whether it is `R` or `B`?
- Can I connect `R`, `B`, and delayed `B` loops to typical BOTGs?
- Can I distinguish a **stock** from a **flow** using units?
- Can I write `net change = inflows − outflows`?
- Can I identify auxiliaries and constants?
- Can I convert a qualitative CLD into an SFD skeleton?
- Can I explain an S-shaped curve through **changing loop dominance**?
- Can I identify an archetype from its **feedback structure**, not just its name or graph?
- Can I propose a leverage point that addresses the structure rather than only the symptom?
