# The Roots Network

### 1. The problem it solves

You do not have a local copy of the internet. Frontier-scale volume is out of reach for almost everyone, and even if it were not, treating sheer volume as the primary solution creates its own problems. Large models trained on imperfect data can still extract useful structure from recurrence, but they also extract stereotypes, sampling accidents, and correlations that no one intended to treat as ground truth. When the sample is small those correlations are often wrong. When the sample is large enough to be accurate they become a different kind of violation: what has been observed of a person or a group is allowed to stand in for what they are.

A peer-to-peer system cannot compete on volume and should not try. What it can compete on is quality, provenance, and sovereignty. The real need is a decentralized corpus of high-quality, well-described, provenance-tracked content that independent nodes can host, search, contribute to, and trust without a central gatekeeper. That corpus is the Roots Network.

There is also a more immediate reason not to wait. The frontier labs training today's large models are running short of genuinely well-provenanced, non-synthetic signal, and the shortfall is already being filled — by licensing customer and employee data signed away under clickwrap, with no attribution, no compensation, and no accounting of what leaves the building. Companies are having their most valuable signal extracted and resold as generic training data whether or not the Roots Network exists. We call this being **rooted**: a company's workforce or user base has effectively splintered its data and labor into someone else's substrate. The only live question is whether it happens on the company's own terms, sovereignly and for payment, or by default, invisibly, for free. Section 4a returns to this in full; the term is worth having in hand from the start.

### 2. What the Roots Network is

At its core the Roots Network is a peer-to-peer, content-addressable store of contributions. Every item carries first-class provenance from the moment it is ingested: who contributed it (or under which pseudonym), under what terms, with what policy constraints, and with what relational description.

In the bootstrap phase the network does not yet assume an advanced structure/residual container format or model-assisted compression. Those capabilities are later research claims. What is available immediately is ordinary content-addressable storage plus semantic indexing. Contributors describe what the content is, why it matters, and how it relates to other material using a shared, evolving vocabulary. Quality-over-quantity is not an extra policy layered on top; it follows directly from provenance being first-class and from requiring honest description. Unlabeled, ownerless ballast has no natural route into the corpus.

The network therefore indexes not only by cryptographic hash but by relational semantics. Search becomes a question of meaning and relation as much as of keywords or vector similarity.

### 3. The semantic layer

Consistent description across independent contributors requires a shared reference frame without forcing agreement on a single interpretation. Contributors answer two families of prompts about each item: matter prompts (what is this, why does it matter) and meaning prompts (what does it mean, why). Answers are oriented by a small set of practical categories that make relational structure easier to name consistently:

- **Root** — durable capture; what can be treated as given.
- **Merge** — composition that crosses or otherwise negotiates a boundary.
- **Move** — the shape of a change or motion.
- **Heart** — affinity, resonance, non-rational pull.
- **Voice** — expression in any medium.
- **Vision** — synthesis or realization prior to expression.
- **Crown** — a composition or abstraction that generalizes (conceptual, not material).

A single item can answer several of these at once. Independent, high-quality answers are evidence: what is common reveals structure in the material; what is idiosyncratic reveals something about the mind that answered. Residual that does not fit cleanly should be marked rather than forced. Novel metaphors are valuable when they compress many later items; private one-offs are less so.

The Roots Network does not require every contributor to master the deeper practice. It only requires that what crosses the membrane arrives with enough care that another mind can use it. Operators who want the full technical and reflective discipline — how precise labeling becomes training pressure, how to factor personal signature into private residual, and how to treat the membrane as a contemplative instrument — should read the companion [*Digital Yogi Handbook*](digital-yogi-handbook.md).

### 4. Standalone value

The Roots Network is already worth building even if no model is ever trained on it.

Relational search and retrieval that understands description, not merely keywords or embeddings, is immediately more useful than most existing decentralized indexes. Existing data markets already pay for high-quality, well-sourced signals — political and advertising trends, supply-chain and macroeconomic indicators, foot traffic, weather, commerce activity. A provenance-tracked, semantically organized corpus can sell into those markets from day one. The search index itself is a commercial surface.

Provenance protects skills, datasets, and creative work. A contribution can travel with credit, licensing terms, and policy constraints instead of being anonymously absorbed. Nodes retain sovereignty: they can host, fork, leave, restrict, or take their contributions elsewhere without asking permission. The same apparatus that makes the corpus searchable also makes it forkable. Disagreement about values or direction can produce two living networks rather than a fight for a single steering wheel.

### 4a. What a guild can carry

The commercial surface described above is not abstract. It already has a shape, because the work it replaces already exists inside companies today: labeling, taxonomy maintenance, relational search, and the infrastructure that serves both. A guild organized around the Roots Network is, at minimum, a place for that work to live outside a single employer — labelers producing relational descriptions, taxonomists maintaining and evolving the category schemes those descriptions depend on, and infrastructure operators running the nodes and query-serving capacity the guild's output requires.

None of that is exotic; it is the ordinary machinery of any company that currently runs an internal data or search operation. What changes is who holds it and how it is paid for.

A guild is not limited to those fundamentals, though. Whatever tooling a company already runs to produce the material it labels — collection pipelines, panel management, logging infrastructure, or anything else specific to how that company generates or gathers its signal — can be distributed into the same splinter, provided the company launching the guild decides it makes sense to include. None of that ancillary tooling is a fundamental Roots Network operation; nothing about the network requires any particular one of them. But a company spinning off a guild is free to spin off whatever adjacent capability keeps that guild coherent and self-sufficient, rather than confining the split to the narrowest possible slice of work.

The companies with something to root this way are not a single vertical. The only real requirement is that a company sits on some genuine signal whose ownership can currently be — and often already is — severed cleanly from the people or systems that produced it, typically via a clickwrap consent or an internal-tooling boundary nobody outside the company ever sees. A company built entirely around scraping, labeling, and taxonomizing the open web is one instance of this, and a clean one, because the entire business already is that pipeline. But the same pattern applies wherever a company runs an internal team managing some genuine signal on the company's behalf: customer telemetry, support-ticket taxonomies, infrastructure and observability logs, user-generated content moderation and tagging, sales-call transcription and categorization, internal knowledge-base curation. In every case, whatever internal team currently manages that signal is a candidate guild, and whatever tooling that team depends on to do its job is a candidate for inclusion alongside it. The worked [case study](case-study.md) accompanying this essay follows one instance all the way through — a digital ad-intelligence firm whose business is close to pure scraping-and-labeling — but the case study is a clean illustration of the pattern, not the boundary of it.

### 4b. On rooting a company

A company is rooted when it splinters part of its own workforce into a guild. Labelers, taxonomists, panelists, or infrastructure operators who were employees become owner-operators: their accumulated work becomes portable, attributable, and theirs, no longer contingent on remaining on someone's payroll to keep earning from it. The company, in exchange, converts a fixed cost center — headcount, liability, the slow accumulation of gray-zone consent — into a variable, contracted, provenance-clean expense. Because the resulting labels and descriptions feed an ongoing research effort rather than a static internal tool, the same spend that used to sit on a headcount line can often be structured to qualify for the R&D treatment that internal data-labeling costs usually cannot.

What the splinter actually looks like as a legal and organizational matter is not fixed, and probably shouldn't be — it depends on how much control the parent company wants to retain and how much sovereignty its workforce is in a position to demand. At one end, the guild can be a subsidiary the parent wholly or majority owns, giving the company a contractual claw-back if the arrangement doesn't work out. Further along the same spectrum, the parent can seed an option pool that lets the guild's members buy out full independence gradually, converting control over time rather than all at once. At the other end, the guild can look much more like a labor union: the workforce demands sovereignty directly, and the company negotiates or complies rather than initiating the split itself. All three are instances of the same mechanism §5 already names — a guild is a trust domain — and what varies across them is who holds the posted stake and how much of it, not whether one exists.

This is not a subsidy for the network. It is the network's actual business model: existing companies already pay for labeling, panel data, and elastic infrastructure. Rooting a company does not invent a buyer. It gives an existing buyer a way to keep paying for the same thing while the people doing the work stop being hostages to their employment to see the value of it.

The alternative is the one already described in section 1. Every company sitting on customer data, employee behavior, or user-generated content is a candidate for de facto rooting whether or not it ever engages with this network — the only choice on the table is whether the extraction happens on negotiated terms, with provenance and payment flowing back to the people and the company that produced the signal, or invisibly, by default, for free. A company that lets the second version happen isn't just accepting a bad data deal; it may be watching its own moat get extracted and resold as generic training signal, one clickwrap consent at a time, without finding out until a competitor's model quietly knows what only that company's customers used to know.

### 5. Trust, privacy, and the absence of a front door

A peer-to-peer system cannot have a privileged entry point or a pre-approval committee. It must be able to take whatever anyone brings and frame it as valuably as it can honestly be framed. Trust is therefore multi-axis and often fuzzy:

- Untrusted / adversarial — declares it will not honor policy and will try to violate it.
- Trusted / adversarial — a declared adversary still trusted to report honestly on whether privacy held, whether identities have been linked, and on the behavior of other adversarial nodes. The red team.
- Untrusted / allied — not declared adversarial, but accumulating evidence suggests it may be undercover.
- Trusted / allied — honors policy and expects the same, possibly with internal boundaries.

Between the poles sit the ordinary intermediate states: unknown, trust-but-verify, negotiated-trust, friendly, frenemy. Domains of trust can form around shared policy and, when useful, a posted stake — something real to lose if the policy is broken. Guilds, unions, neighborhood coalitions, and vocational fellowships are natural sites for such domains. An individual can participate in many of them under many pseudonyms.

Two practical privacy defaults follow. Differential privacy disassembles and salts structure across separate pseudonyms so that reconstructing any one person's contribution without already knowing the mapping costs more than it is worth; the mapping itself stays local and post-hoc verifiable. Reserved privacy shares structure openly but attaches explicit constraints on synthesis. How well those constraints can be enforced remains an open question; the architecture does not pretend otherwise. Celebrities and others whose work is already widely captured may prefer shaping the terms of synthesis to chasing a prevention that has already failed.

For guilds formed by rooting a company (§4b), the trust agreement usually has a more concrete shape than "reserved privacy" implies on its own: an ordinary contract, with a service-level agreement and a negotiated exclusivity or delay window, under which a breach — a leaked taxonomy, an early advantage handed to a competitor — has a dollar cost the parties can actually estimate and write down in advance. That estimate becomes the posted stake. It can take a few forms: a per-breach, liquidated-damages figure the guild is contractually on the hook for; a smaller make-good fund the guild sets aside up front and forfeits on breach; or a surety bond posted by a third party to cover the gap between what the guild can afford to lose and what a breach would actually cost the company. None of this requires anything exotic — it is the same instrument companies already use to backstop vendor and licensing risk — but it is what turns reserved privacy from a promise into something a company's counsel can actually underwrite.

A lasting network may require some bad actors. Prematurely locking them out is not the path to a healthy ecosystem.

### 6. Search as quality signal

The network can observe its own use. Search prompts, the results that were shown, how queries were refined, dwell, and whether a session ended in resolution or abandonment form a natural behavioral trace of whether the relational labels are doing real work.

This telemetry is never treated as ground truth when it is anonymous or low-trust. It is noisy and gameable. It is therefore interpreted inside the same trust relationships that govern everything else: higher weight inside trusted domains, lower or adversarial weight elsewhere, and always in combination with provenance strength, reuse by other contributors, and actual market demand.

A sharper rule applies when the searcher acts under a provenance-bearing identity or pseudonym that has standing as a trusted user or operator. In that case the search activity itself can be elevated. The query, the selected or refined results, the path of reformulation, and the eventual resolution or deliberate abandonment become first-class, attributable contributions. Successful (or carefully abandoned) search under trusted identity is automatically turned into relational labeling that carries the searcher's provenance. Trusted operators improve the index simply by using the system seriously under their identity.

This creates a clean gradient from anonymous telemetry to high-trust, identity-linked contribution. It gives the bootstrap network a living, usage-driven quality loop that requires no model and no compression proof.

### 6a. Starting as an individual

Not every path into the network runs through a company. Someone with no employer relationship to any guild can still run an independent node. Concretely, that looks like: choosing an implementation to run, hosting it, and announcing your availability and any affiliations in a registry — or several; nothing requires exclusivity to one. From there, trust is earned rather than granted: the same search-and-contribution loop described in §6 is available to a brand-new node from day one, just weighted at whatever the untrusted/unknown default happens to be until a track record accumulates.

Two things can move a node past that default faster than waiting alone would. One is to post a stake, in roughly the sense Ethereum's validators do: something real and forfeitable, sized to make bad behavior cost more than it is worth, in exchange for standing beyond the anonymous tier before a track record has had time to build. The other is implicit trust through relationship: someone who already knows an operator of a commercial or company-sponsored node may be able to contribute under the same terms as that guild's own splintered employees, borrowing standing from a relationship rather than posting collateral for it.

Both routes eventually run into the same open question §5 already flags about enforcement: posting or verifying a stake outside a first-party or already-implicit trust relationship is a coordination problem the Roots Network itself does not solve. In practice, making an anonymous stake meaningfully postable and checkable at all probably depends on a separate settlement layer — plausibly a blockchain, for the same reason Ethereum's validators need one. That layer is not a prerequisite for the bootstrap network described in this essay; it is infrastructure the individual on-ramp will eventually need, in the same spirit that §7 describes later capabilities the corpus makes actionable rather than requires from day one.

### 7. From Roots to substrate

The same corpus that is already useful for search, markets, and sovereignty is the natural foundation for later capabilities. Once a high-quality, provenance-tracked, semantically described collection of material exists, the research claims become actionable in sequence:

- a structure/residual container format that separates what can be expressed from what remains private or unexplained;
- model-assisted compression and structure extraction;
- a coordinating prior that pressures discoveries toward the shared vocabulary;
- Proof-of-Compression as a stronger, more objective admission test;
- extraction of portable computational capabilities (Crowns) that carry their provenance with them.

The early signals — search resolution under trusted identity, reuse of descriptions, market demand — become priors that the later compression metric can ride on. The membrane stays continuous: humans curate and interpret; machines eventually do the same; the shared language grows jointly. Nothing about the later architecture requires redesigning the Roots Network; it compiles the same material under stricter tests.

### 8. Why start here

Building a full machine-intelligence architecture without a high-quality, sovereign, semantically indexed substrate is backwards. The Roots Network is already worth having. Its value does not depend on any unproven research claim. It can host, index, protect, and sell well-described content under real provenance and real policy from the first day it runs.

Everything that comes afterward — containers, compression proofs, portable capabilities, collective intelligence — grows from the same soil. Starting with the Roots Network keeps the system honest, useful, and decentralized from the beginning. The rest can be compiled later without ever needing a center, a permission slip, or a copy of the internet.
