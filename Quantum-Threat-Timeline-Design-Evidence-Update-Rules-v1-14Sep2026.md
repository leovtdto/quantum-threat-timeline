# Quantum Threat Timeline --- Design, Evidence & Update Rules

**Canonical baseline at time of writing:** v41.9 --- 14 Sep 2026\
**Purpose of this file:** Preserve the design logic, evidence rules,
editorial standards, and update workflow for future **PQC Timeline Watch
/ Tracker Daily** updates so the site can be maintained consistently
even if a future editing session starts without the full project
history.

------------------------------------------------------------------------

## 1. Core purpose of the site

The Quantum Threat Timeline is not intended to be a news dump, vendor
tracker, or prediction of a single "Q-Day".

Its purpose is to be an **evidence-linked decision-support instrument**
that helps executives, policymakers, CISOs, practitioners and technical
reviewers answer three questions:

1.  **How is the cryptographic quantum threat changing?**
2.  **What does that mean for migration timing and action?**
3.  **What evidence shows that real organisations are actually
    migrating?**

The site should remain **Singapore-aware but globally evidenced**.

The central synthesis is currently expressed as approximately
**\~2033**, but this must always be described as a **central risk
estimate / convergence assessment, not a forecast date or prediction of
Q-Day**.

------------------------------------------------------------------------

## 2. Fundamental threat model: two primary trajectories

The core convergence model has two primary axes.

### A. Quantum computing capability ↑

Question:

> What can credible quantum-computing systems actually do, and how
> quickly is fault-tolerant capability advancing?

Track evidence such as:

-   measured hardware results;
-   quantum error correction (QEC);
-   logical-qubit demonstrations;
-   systems engineering;
-   control electronics;
-   connectivity/interconnects;
-   scaling/manufacturing;
-   credible vendor hardware roadmaps, clearly labelled as roadmaps
    rather than demonstrated capability.

### B. Resources needed to break cryptography ↓

Question:

> How much quantum computation does a serious cryptanalytic attack
> require?

Track evidence such as:

-   cryptanalytic algorithms;
-   logical resource estimates;
-   physical resource estimates;
-   QEC overhead reductions;
-   runtime reductions;
-   compilation improvements;
-   hardware-aware attack-resource estimates.

### Central convergence

The central estimate is an **assessment of where these trajectories may
overlap**.

Do not imply:

-   that a cryptographically relevant quantum computer exists today;
-   that \~2033 is a precise Q-Day;
-   that a vendor roadmap is measured capability;
-   that a resource estimate is a demonstrated attack.

------------------------------------------------------------------------

## 3. Executive presentation rule

The landing experience should answer, within the first few screenfuls:

> **Where are we? What changed? What should I do?**

Keep the **Executive Convergence Brief**, with three concise cards:

-   Quantum computing capability --- direction of travel;
-   Resources needed to break cryptography --- direction of travel;
-   Current synthesis --- central assessment.

Avoid large repetitive date badges inside this brief when the page
already contains a fact-check/update date elsewhere.

Detailed technical evidence should be progressively disclosed rather
than confronting an executive reader immediately.

**Do not remove technical evidence simply to shorten the page.** Prefer:

> State once → summarise elsewhere → link back to the evidence.

------------------------------------------------------------------------

## 4. Attack Resources section --- strict scope

### The question this section owns

> **How much computation does the attack require?**

This section is about the **cryptanalytic/resource side**, not a
comparison of quantum hardware modalities.

### Keep here

-   clean like-for-like historical resource trends;
-   algorithmic improvements;
-   logical-resource reductions;
-   QEC/resource-overhead developments;
-   resource-estimation methodology.

The strongest current like-for-like visual is the Gidney RSA-2048
comparison:

-   2019: about 20 million noisy qubits;
-   2025: fewer than 1 million noisy qubits;

under the same stated hardware assumptions.

This is valuable because it is a genuine longitudinal
resource-compression signal.

### Algorithm/logical evidence

Examples such as:

-   Regev;
-   Chevignard--Fouque--Schrottenloher;
-   Luo et al. (835 logical qubits for the cited 256-bit ECDLP
    construction);

belong naturally here because they reduce the **attack requirement**
without necessarily defining a directly buildable physical machine.

### Do not do this

Do **not** plot architecture-specific estimates such as neutral-atom,
trapped-ion, superconducting, cat-qubit and silicon-spin physical-qubit
counts as one continuous trend.

For example, do not create:

> 20M → \<1M → 26K

when the points change cryptographic target, architecture, QEC,
connectivity, runtime and physical assumptions.

That would create false precision.

### Bridge to Architecture Observatory

End the section with a short explanation:

> Architecture-specific physical-resource estimates differ substantially
> and are not placed on the like-for-like trend. They are analysed
> separately in the Architecture Convergence Observatory.

------------------------------------------------------------------------

## 5. Architecture Convergence Observatory --- strict scope

### The question this section owns

> **Can a particular quantum-computing architecture realistically supply
> the computation required by serious cryptanalytic estimates?**

This is the **hardware/modality side of convergence**.

The threat model must remain **architecture-neutral**. The tracker does
not need to predict which quantum-computing modality will "win". From a
security-planning perspective, the relevant question is whether **any
credible architecture** can close its cryptanalytic gap.

### Modalities currently tracked

At minimum:

1.  **Superconducting**
2.  **Trapped ion**
3.  **Neutral atom**
4.  **Bosonic / cat qubit**
5.  **Distributed silicon spin**
6.  **Photonic**

Topological/Majorana and other emerging modalities may be maintained as
watch/scenario evidence where appropriate, but should not be promoted to
equal evidential status without sufficient support.

### For every architecture, try to show

-   cryptographic target;
-   attack-resource estimate;
-   physical qubits, where provided;
-   logical qubits, where provided;
-   runtime;
-   QEC scheme/assumptions;
-   connectivity/architecture assumptions;
-   current measured hardware/QEC capability;
-   roadmap evidence, separately labelled;
-   remaining gap;
-   evidence confidence/status.

### Current attention logic

**High attention** is an editorial importance label, not a provenance
label.

Examples currently deserving high attention include:

-   superconducting;
-   neutral atom;
-   trapped ion;
-   bosonic cat qubits.

Distributed silicon spin remains useful but lower-confidence where the
relevant QRE is vendor-authored.

Photonic FTQC remains important, but if no modern directly comparable
target-specific physical cryptanalytic estimate is available, explicitly
show:

> **Insufficient comparable cryptanalytic evidence**

rather than inventing a number or trend.

### Critical comparison rule

> **Physical qubits are not fungible across architectures.**

20,000 trapped ions, 20,000 neutral atoms and 20,000 cat qubits are not
equivalent units of computational capability.

Always retain context including:

-   runtime;
-   cycle speed;
-   connectivity;
-   fidelity;
-   QEC;
-   decoding;
-   routing;
-   parallelism;
-   physical error assumptions.

Where useful and supportable, consider spacetime cost / qubit-time
measures, but never manufacture them from incompatible data.

### Do not calculate architecture-specific Q-Day dates without sufficient evidence

A modality may be labelled:

-   evidence improving rapidly;
-   resource estimate available;
-   hardware scaling evidence available;
-   gap narrowing;
-   uncertain;
-   insufficient longitudinal evidence.

Do not turn sparse evidence into a false convergence date.

------------------------------------------------------------------------

## 6. Special interpretation of neutral atoms

The Cain/Caltech neutral-atom work is important and deserves high
attention because it provides a striking architecture-specific
cryptanalytic resource estimate.

However:

-   it is not proof that a cryptanalytic neutral-atom machine exists;
-   trapped atoms are not equivalent to fault-tolerant computational
    qubits;
-   current atom-array scale must not simply be divided into the
    attack-resource estimate to claim a "distance to CRQC";
-   it must not replace the Gidney like-for-like RSA trend.

The correct watch question is whether experimental neutral-atom systems
progressively demonstrate the assumptions required by the resource
model:

> scale + fidelity + QEC + logical operations + reconfiguration +
> decoding + sustained circuit depth.

------------------------------------------------------------------------

## 7. Special interpretation of IonQ / trapped-ion evidence

IonQ deserves similar high attention when its work provides an
architecture-specific, end-to-end mapping from cryptanalytic workload
through QEC to a trapped-ion physical-machine estimate.

Always distinguish:

-   the resource-estimate machine;
-   IonQ's actual/current hardware capability;
-   vendor roadmap statements;
-   independently measured results.

Never imply that the modelled attack machine exists today.

------------------------------------------------------------------------

## 8. Convergence accelerators and brakes

This material belongs under **Method**, not on the executive landing
section and not primarily under Counter-case.

Suggested heading:

> **What can move the convergence estimate?**

The two primary axes remain:

-   quantum computing capability;
-   attack-resource requirement.

Other technologies affect one or both axes rather than automatically
becoming a third clock.

### Potential accelerators

Examples:

-   QEC;
-   classical QEC decoding;
-   control electronics;
-   manufacturing yield;
-   modular interconnects;
-   compilers/scheduling;
-   algorithmic advances;
-   hardware--algorithm co-design;
-   AI/automation.

### Potential brakes

Examples:

-   logical error floors;
-   decoder latency;
-   fabrication/packaging;
-   interconnect loss;
-   cryogenic/optical scaling;
-   power/cost;
-   supply-chain constraints;
-   integration complexity;
-   roadmap slippage.

### AI rule

AI is currently treated as an **accelerator, not a third convergence
axis**.

Do not move the central estimate because of generic AI progress.

AI becomes decision-relevant only when AI-enabled work produces
measurable evidence such as:

-   improved calibration/control;
-   QEC decoding gains;
-   compiler optimisation;
-   algorithm discovery;
-   measurable capability increase;
-   measurable attack-resource reduction.

------------------------------------------------------------------------

## 9. Real-World PQC Adoption Observatory

### Purpose

Track **genuine independent PQC adoption**, not PQC deployment news.

The Observatory should remain deliberately selective.

### Fundamental inclusion rule

> **Independent adopter ≠ technology provider.**

The adopter should be identifiable and separate from the technology
provider.

### Include only when there is meaningful evidence of

-   named independent adopter;
-   actual implementation activity;
-   sufficiently clear use case;
-   sufficiently strong public evidence;
-   maturity that can be classified without inference.

### Maturity ladder

**Level 1 --- Selected**\
Technology/provider selected or implementation committed, but meaningful
validation not yet demonstrated.

**Level 2 --- Pilot / validation**\
PoC, experiment or implementation validation actually performed.

**Level 3 --- Production**\
Evidence supports sustained operational/production use.

**Level 4 --- Measured / independently corroborated**\
Operational use plus meaningful measurement or strong independent
corroboration.

Do **not** promote a successful PoC to "migration completed".

### Evidence quality

Recommended quality scale:

**A --- Adopter/authority primary source**\
**B --- Adopter + supplier corroborated**\
**C --- Supplier disclosure only**\
**D --- Secondary reporting only**

Only strong A/B evidence should normally contribute to headline
verified-adoption counts.

### Evidence date

Every Observatory case should visibly show its **public evidence date**.

Sort broadly newest-first.

Older cases remain useful but should be visibly identified as historical
where appropriate, e.g.:

> **Historical early adopter**

The Observatory is a **historical + current evidence base**, not a
latest-news feed.

### What is deliberately excluded from the independent adoption count

-   Google, Cloudflare, Meta and other technology providers deploying
    their own PQC capabilities;
-   anonymous supplier case studies;
-   generic product availability announcements;
-   pilots where the adopter cannot be identified;
-   announced contracts where completed implementation has not been
    demonstrated;
-   QKD-only deployments when the Observatory is specifically counting
    PQC migration.

These can remain useful elsewhere.

### Technology-provider self-deployment --- reference only

A compact subsection may retain one-line evidence-linked examples of:

-   Google;
-   Cloudflare;
-   Meta;
-   other major providers;

to show engineering feasibility and migration lessons.

Clearly state that they **do not count as independent adoption** because
the deploying organisation is also a technology provider.

### Do not target a desired number of cases

Six high-quality cases are better than twenty weak cases.

The scarcity of Level 3/4 public evidence may itself be a meaningful
finding.

------------------------------------------------------------------------

## 10. Evidence classification system

Every proposed new/update item should have **two separate visible
classifications**.

### Provenance status

**VERIFIED**\
Directly supported by a primary or authoritative source.

**REPORTED**\
Credible secondary reporting or a claim not yet independently/primarily
confirmed.

**ASSESSMENT**\
Interpretation or implication derived from verified/reported evidence.

### Evidence type

Examples:

-   HARDWARE
-   RESOURCE ESTIMATE
-   POLICY
-   STANDARD
-   DEPLOYMENT SIGNAL
-   MARKET NEWS
-   EXPERT OPINION
-   VENDOR ROADMAP
-   QUANTUM COMMUNICATIONS
-   RESEARCH / PREPRINT
-   PEER-REVIEWED RESEARCH

Do not confuse **importance/attention** with **provenance**.

For example:

> VERIFIED · RESOURCE ESTIMATE · HIGH ATTENTION

is valid because these labels answer different questions.

------------------------------------------------------------------------

## 11. Source and evidence-link rule

Every factual claim proposed for addition or revision must have a
**direct visible supporting internet source link near the relevant claim
or information block**.

Prefer, in order:

1.  peer-reviewed paper / original research publication;
2.  standards body;
3.  government/official authority;
4.  issuing organisation/adopter;
5.  primary company technical publication;
6.  credible secondary reporting where primary evidence is unavailable.

Where only secondary reporting exists:

-   label it **REPORTED**;
-   do not present it as independently verified primary evidence.

For vendor claims:

-   say that it is vendor evidence;
-   do not silently convert a roadmap or model into measured fact.

For major resource estimates, retain the technical paper as well as the
vendor/institutional announcement where both add useful context.

------------------------------------------------------------------------

## 12. Timeline inclusion rule

The Timeline must not become a catalogue of interesting quantum news.

A milestone should normally enter the public Timeline only if it
materially changes or informs at least one of:

-   quantum-computing capability;
-   attack-resource requirements;
-   migration timing;
-   standards/policy;
-   interpretation of the threat;
-   major deployment evidence.

Lower-value but credible developments can remain in **Tracker Daily /
Keep Watch**.

------------------------------------------------------------------------

## 13. Tracker Daily triage

Every candidate development should be assessed as one of:

### A --- Moves the needle

Could change:

-   quantum capability trajectory;
-   attack-resource trajectory;
-   central convergence assessment.

### B --- Changes migration picture

Could materially change:

-   standards;
-   regulation;
-   migration urgency;
-   implementation approach;
-   interoperability;
-   deployment feasibility.

### C --- Keep watch

Credible and potentially important but does not yet justify changing the
public decision layer.

### D --- Do not publish / low value

Interesting but insufficiently relevant, duplicative, weakly evidenced,
or commercially promotional.

The update question is no longer merely:

> "Is this new and relevant?"

It must also be:

> **"Does adding this make the site more useful than leaving it out?"**

------------------------------------------------------------------------

## 14. Counter-case rule

The Counter-case exists to preserve uncertainty and prevent alarmism.

Use it for evidence showing why headline progress does **not**
automatically imply imminent CRQC, for example:

-   resource estimate ≠ existing machine;
-   logical scaling remains difficult;
-   physical implementation overhead remains large;
-   benchmark advantage ≠ cryptanalytic capability;
-   vendor roadmaps can slip;
-   system integration can dominate;
-   QEC assumptions may not be realised at scale.

Do not use Counter-case as a dumping ground for every "brake". General
accelerators/brakes belong in Method.

------------------------------------------------------------------------

## 15. Method section

Method should explain **how the assessment is constructed**.

It should include:

-   architecture-neutral threat assessment;
-   distinction between measured results, resource estimates and
    roadmaps;
-   what can move the convergence estimate;
-   accelerators/brakes;
-   treatment of AI;
-   evidence hierarchy;
-   cross-architecture comparability limitations;
-   update/triage rules.

Important statement:

> The tracker does not assume which quantum-computing modality will
> ultimately achieve cryptographically relevant scale. It monitors
> measured progress and credible resource estimates across multiple
> architectures. Architecture-specific estimates are not treated as
> directly comparable unless their assumptions permit it.

------------------------------------------------------------------------

## 16. Presentation and information-density rules

The main editorial risk is now **too much good information**.

### General rule

Do not continually add sections simply because useful evidence exists.

Prefer:

-   progressive disclosure;
-   concise executive summaries;
-   detailed evidence deeper in the page;
-   direct links between related sections.

### Avoid repetition

The following ideas naturally recur but should not be fully re-explained
everywhere:

-   capability is advancing;
-   attack resources are falling;
-   no demonstrated CRQC exists;
-   roadmap ≠ capability;
-   resource estimate ≠ machine;
-   \~2033 is an assessment;
-   migration should begin before CRQC exists.

Use:

> **State once. Summarise elsewhere. Link back.**

A future editorial pass may safely remove repetitive prose while
preserving evidence and meaning.

### Audience priority

Optimise primarily for:

1.  CISO/security leadership;
2.  policymakers/regulators;
3.  technical practitioners;
4.  technical management/researchers;
5.  executives.

Do not oversimplify merely to maximise accessibility to the general
public if that weakens decision usefulness.

------------------------------------------------------------------------

## 17. Terminology rules

Prefer:

**Quantum computing capability ↑**

rather than ambiguous "Quantum capability".

Prefer:

**Resources needed to break cryptography ↓**

rather than vague "Attack requirements".

For the centre:

**Estimated cryptographic risk window**

or equivalent wording that clearly avoids claiming a forecast Q-Day.

Where possible, reinforce:

> **Central risk estimate · not a forecast date**

------------------------------------------------------------------------

## 18. Date and currency rules

Keep distinct:

-   **Last fact-checked** --- date of substantive evidence audit;
-   **Last updated** --- only if needed and not duplicative.

Do not update the fact-check date merely because a cosmetic/layout edit
was made.

When adding an older historical item today, show the **actual
evidence/publication date**, not today's update date as if the event
were new.

------------------------------------------------------------------------

## 19. Quantum communications / QKD rule

Quantum communications should remain tracked as a separate evidence
class.

Distinguish:

-   QKD experimental result;
-   deployment;
-   network/interoperability result;
-   implementation-security research;
-   government/critical-infrastructure deployment;
-   vendor announcement.

Peer-reviewed QKD implementation-security work can be important even
when it does not change the CRQC convergence estimate, because it
informs the practical security interpretation of quantum-safe
communications.

Do not conflate:

-   PQC migration;
-   QKD deployment;
-   quantum networking research.

------------------------------------------------------------------------

## 20. Regulatory / government-product rule

Government-originated quantum-safe activity can have more than one
significance.

For example, a government-developed product portfolio may be:

-   a deployment/market signal;
-   government capability;
-   potentially relevant to the regulatory/national-policy clock.

Do not automatically classify a government product announcement as a
mandate.

Ask whether the source establishes:

-   policy;
-   requirement;
-   guidance;
-   procurement/deployment signal;
-   product availability.

Label accordingly.

------------------------------------------------------------------------

## 21. PQ authentication / implementation-risk rule

PQC migration is not only algorithm replacement.

Track developments showing deployment gaps in:

-   authentication;
-   certificates;
-   protocol integration;
-   hybrid modes;
-   interoperability;
-   configuration;
-   implementation;
-   cryptographic agility.

These are especially relevant because migration risk can shift from:

> "Are standardised algorithms available?"

toward:

> "Can organisations implement and integrate them correctly at scale?"

This is a useful bridge between standards maturity and
implementation/deployment risk.

------------------------------------------------------------------------

## 22. Hardware roadmap rule

Always distinguish:

### Measured hardware result

Something experimentally demonstrated.

### Vendor roadmap

A stated future target.

### Resource estimate

A model of what an attack would require.

Never place these on the same visual footing without explicit labels.

When a roadmap changes, update all dependent wording across:

-   landing/convergence;
-   capability section;
-   Timeline;
-   Method;
-   Counter-case;
-   Watch;
-   Sources.

This whole-site consistency check became necessary after the IonQ update
and should remain standard practice.

------------------------------------------------------------------------

## 23. Whole-site consistency audit after material updates

Whenever a significant item is accepted --- especially a new hardware
result or resource estimate --- search the **entire HTML** for affected
claims.

At minimum check:

-   landing/convergence graphic;
-   Executive Convergence Brief;
-   Attack Resources;
-   Architecture Observatory;
-   Timeline;
-   capability/hardware trajectory;
-   migration implications;
-   Counter-case;
-   Method;
-   Watch;
-   Sources;
-   glossary if terminology changed;
-   fact-check date.

Do not update only the section where the new evidence first appeared.

------------------------------------------------------------------------

## 24. HTML QA rules after every edit

Before declaring a new canonical version, check:

-   no duplicate HTML IDs;
-   no broken internal anchors;
-   no empty `href`;
-   external links preserved;
-   `_blank` links use `noopener`;
-   no accidental literal escape strings such as `\n`;
-   no malformed HTML introduced by scripted insertion;
-   no repeated blocks accidentally retained;
-   navigation and Contents include new major sections;
-   removed material is genuinely duplicate, not unique evidence.

Where possible, also perform visual/browser rendering QA.

If rendering cannot be performed, say so rather than claiming visual
verification.

------------------------------------------------------------------------

## 25. Evidence-preservation rule

When simplifying the site:

> **Reduce duplication, not evidence.**

Do not delete unique evidence simply to make the page shorter.

If a section is moved:

-   preserve its evidence links;
-   preserve provenance/evidence-type labels;
-   update internal navigation;
-   ensure no orphaned references remain.

A useful release check is:

> **No evidence lost / link-integrity check**

------------------------------------------------------------------------

## 26. Canonical-version discipline

Maintain one clearly identified latest working version.

At the time this guide was created:

> **v41.9 --- Separated Attack Resources & Architecture --- 14 Sep
> 2026**

Future edits should start from the latest canonical version, not from
older mock-ups or intermediate files.

Version names should describe the substantive change where practical.

------------------------------------------------------------------------

## 27. Recommended Tracker Daily notification format

When a potentially relevant development is found, report:

**What changed**\
Concise description.

**Date**\
Actual publication/event date.

**Affected site section**\
Or explicitly state **monitor-only**.

**Why it matters**\
Decision relevance.

**Provenance**\
VERIFIED / REPORTED / ASSESSMENT.

**Evidence type**\
HARDWARE / RESOURCE ESTIMATE / POLICY / STANDARD / etc.

**Migration urgency effect**\
Increases / decreases / no material change.

**Source**\
Primary or best authoritative source.

**Proposed HTML action**\
Add / revise / replace / monitor only / no change.

**Proposed wording**\
Only when an HTML change is warranted.

Do not silently modify the published HTML. The user reviews and accepts
changes first.

For automated/watch notifications, end exactly with:

> **ChatGPT can help to update. Please review the update and accept the
> change as the last step.**

------------------------------------------------------------------------

## 28. Decision hierarchy for future maintainers

When uncertain whether to add something, ask in this order:

1.  **Is the claim supported?**
2.  **Is the evidence type correctly identified?**
3.  **Is the provenance correctly labelled?**
4.  **Does it materially affect threat capability, attack resources,
    migration, policy, implementation or real adoption?**
5.  **Does it belong in an existing section rather than requiring a new
    one?**
6.  **Would adding it improve decision usefulness?**
7.  **Does it duplicate something already explained?**
8.  **Could the visual presentation imply more certainty than the
    evidence supports?**
9.  **Does this change require updates elsewhere in the HTML?**
10. **Have all relevant evidence links and dates been preserved?**

If the answer to usefulness is weak, keep it in Watch rather than
expanding the public page.

------------------------------------------------------------------------

## 29. The overarching editorial principle

The tracker should aim to become progressively **more selective as the
evidence base grows**.

Its value comes from:

> **curation + evidence quality + explicit uncertainty + decision
> relevance**

---not from the number of quantum developments it contains.

The strongest future version is therefore not necessarily the one with
the most entries. It is the one in which a senior reader can quickly
understand the decision, while a technical reviewer can drill down and
verify every important claim.

------------------------------------------------------------------------

## 30. One-sentence identity of the tracker

> **An evidence-linked, architecture-neutral decision-support tracker
> that connects measured quantum-computing progress, cryptanalytic
> resource reductions, migration deadlines and independently evidenced
> PQC adoption without treating vendor roadmaps, models or headlines as
> demonstrated fact.**
