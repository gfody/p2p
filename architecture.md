# **A Peer-to-Peer Machine Intelligence System**

## Abstract

Current machine intelligence systems are organized around centralized models. A model is trained, its parameters are treated as the principal representation of capability, and improvements arrive by modifying them or replacing the model as a whole.

This paper proposes a different architecture.

A machine-intelligence network can be built as a peer-to-peer system in which independently operated nodes retain their own models, data, compute, and private residual information while participating in a shared representation of useful structure. The shared representation is not a synchronized set of weights. It is a shared computational language — a living superset of human language — into which independently discovered structure can be expressed, evaluated, composed, and reused.

The central problem is not how to force independently trained models to share the same internal representation. It is how to give them a common surface through which useful discoveries become interoperable.

We call this surface a **semantic membrane**.

The membrane separates a node's private computational interior from the shared external language. A **coordinating prior** creates pressure for useful discoveries to cross that boundary without forcing internal convergence (§11) — pressure that works two ways: post-hoc excavation of structure a model already has, and, where extraction proves too costly or interpretability tools too immature, training the model toward cooperative legibility directly. The prior functions less as a lens for finding structure that is already there than as a spring: optimization alone offers no guarantee of settling on circuits a human would recognize as intelligent rather than merely locally optimal, a risk this architecture's curated, non-frontier-scale corpus cannot simply out-train. Whether a candidate structure actually earns that kind of standing is then a separate, testable question: contributions are evaluated through **Proof-of-Compression**, producing reproducible improvement in the network's ability to represent or predict held-out information.

Trained neural networks are treated as compiled artifacts rather than irreducible objects. Through activation tracing, intervention, behavioral analysis, and an intermediate representation, computational structures can be recovered as portable circuits. We call validated, addressable capabilities of this form **Crowns**.

The same language is used to construct a behavioral control surface around otherwise opaque generative computation. A high-dimensional generative subsystem — the **Subconscious** — is separated from a narrower behavioral controller — the **Ego**, deliberately built as a subordinate harmonic rather than an independent authority (§18, §19). Because a restricted controller can still acquire substantial influence, the architecture permits scope-limited asymmetric mediation between control layers (the **Metatron** pattern, §21).

Because the system is peer-to-peer by design, governance, safety, residual privacy, and forkability are first-class architectural concerns rather than afterthoughts. Because provenance travels through the same compilation that produces a Crown, the architecture also yields a practical form of introspection: an account of the structures of thought, behaviors, and source material an inference drew on, with attribution and compensation claims intact (§6, §36). Humans participate directly at the membrane, in two directions: curating data that becomes new structure (roots-up) and interpreting machine-coined terms back into usable form (crowns-down) — §9. The network continues the ordinary growth of human language, only faster and with machines as active co-participants.

Roots-up curation, the membrane, and the coordinating prior are separate design choices that all add pressure in the same direction: toward a trained model that yields to decompilation rather than resisting it. The architecture does not claim that neural networks can be made perfectly transparent, safe, or decentralized by declaration. It proposes a different systems boundary: private models become computational substrates; shared structure becomes a network resource; behavioral control becomes an independently inspectable interface; and the shared language of intelligence evolves through the joint activity of its human and machine participants.

The stronger claims — that learned models contain compact relational algebras, that these algebras recur across weights, activations, and data, and that sufficiently complete relational descriptions may eventually replace much of the raw parameter representation — are research hypotheses, not prerequisites for construction.

---

## Status of Claims

This document makes claims at three levels of confidence. The architecture is built so that failure at a higher level does not invalidate the levels below it.

1. **Engineering claims** (Sections 1–15, 38, and the core of Sections 16–32). Useful computational structure can be extracted from a trained model, represented in an intermediate form, validated, registered, and composed — without requiring the originating model to be shared in full. Behavioral control, asymmetric mediation, provenance, and governance mechanisms are treated as first-class architectural surfaces required by the peer-to-peer setting. Human participation at the membrane (data hygiene and interpretive adaptation) is part of the language-growth loop. This is what Phases 1–13 of the engineering program (Section 38) build directly. Section 37 gives the cheapest experiment that would test the central interoperability claim.
2. **Research hypotheses** (Section 33, H1–H10). Trained networks contain comparatively compact relational structure — organized around a small number of primitive categories, exhibiting recurring algebraic patterns, generalizing under a weak interoperability objective, and potentially discoverable by relational variants of sparse autoencoders — that can become a shared computational vocabulary. A separate pair of hypotheses (H8, H10) concerns whether the coordinating prior's training and incentive dynamics behave as expected, rather than the algebraic structure itself. These are stated as testable and (except for H7) directly falsifiable hypotheses.
3. **Long-range conjectures** (H7). Sufficiently complete relational representations may eventually recover, replace, or compile substantial portions of raw parameter representation. This is not a prerequisite for tier 1 or tier 2.

Section 34 states the conservative reading explicitly: the architecture is useful even if every hypothesis in tier 2 fails and no conjecture in tier 3 is ever demonstrated.

---

## Architecture Dependency Map

For readers (human or machine) who need to extract the minimal viable core quickly:

| Layer | Required for core engineering claim? | Notes |
|---|---|---|
| Semantic membrane | Yes | Core interoperability boundary; architectural commitment (§10) |
| Tunable coordinating prior (λ) | Yes, as a mechanism — its effectiveness is H8, its incentive dynamics are H10 | Exists architecturally regardless; how well it works, and whether participation is rational, are research questions (§11, §36) |
| Proof-of-Compression | Yes, as an admission/evaluation framework — exact protocol is research | \(\Delta C\), coding scheme, and anti-overfitting procedure are deliberately unspecified (§12, §37) |
| N-IR + Crown extraction + contracts + registry | Yes | Portable capability unit; profiles range from core-dependent to fully independent (§4) |
| Residual accounting + private/shared boundary | Yes | Sovereignty + novelty (§3) |
| Shared computational language as living superset of human language | Yes | Growth loop includes human interpretation & adaptation (§9) |
| Ego / Subconscious split + categorical restriction (Vision/Voice denied recursively) | Yes for behavioral control surface | Ego-crowns close over the restricted subset only (§18) |
| Metatron (asymmetric mediation) | Strongly recommended | Fixed-capacity, purpose-scoped — not a privileged controller (§21) |
| Provenance as first-class, for both Crowns and corpus data | Yes | Policy, attribution, privacy attachment point; corpus-level provenance is the Roots Network (§6, §9) |
| Governance / homeostasis / forkability / economics | Required architectural surfaces — concrete mechanisms may be deferred | The surface, not any particular mechanism, is the peer-to-peer requirement; §36 explicitly declines to propose a specific economic mechanism |
| Six primitive categories | Load-bearing only for Ego restriction + human-descriptive alignment | Current reference partition, not a claimed final ontology; architecture survives replacement of the particular six (§7) |
| Relational algebra hypotheses (H1–H9) | No | Research program; system remains useful if false |
| Functional representation conjecture (H7) | No | Long-range |

A reader who accepts only the “Yes” rows already has a coherent, implementable peer-to-peer architecture.

---

## Terminology at a Glance

| Term | Conventional description |
|---|---|
| Semantic membrane | Standardized external representation boundary between nodes (and between machines and humans) |
| N-IR | Intermediate representation for describing extracted neural computation; independence from the originating model is a spectrum, not a binary (Section 4) |
| Core | The tightly-compiled, highly entangled portion of a model that many Crowns depend on at runtime; opaque by efficient design, not by failed extraction (Section 4) |
| Crown | A validated, portable, addressable computational capability — a conceptual unit of composition, closed over recursively from the six primitives or other Crowns (Section 6, Section 7) |
| Ego-crown | A Crown composed only from the Ego’s permitted primitives (Root, Heart, Move, Merge) and other Ego-crowns; never touches Vision or Voice at any depth (Section 18) |
| Residual | Structure not currently captured by the shared representation |
| Roots Network | The network’s content-addressable, semantically-indexed corpus of contributed data; provenance-tracked from ingestion, valuable as infrastructure independent of Crown extraction (Section 9) |
| Coordinating prior (λ) | Auxiliary training objective encouraging externalizable structure; tunable, default weak, primarily node-local (Section 11) |
| Proof-of-Compression | Held-out empirical test of a contribution’s collective utility (Section 12) |
| Ontology chain (structure → relation → projection → capture → expression → realization → thought → reality → mind → language) | Ordinary words, narrowly reused in sequence so each is defined before it's needed; underlies the six primitives (Section 7) |
| Root / Heart / Vision / Voice / Move / Merge | Provisional primitive categories, each a specific instance of a term from the ontology chain, chosen for human-descriptive alignment: material composition (Merge) vs. conceptual composition (Crown) is one useful axis among them (Section 7) |
| Ego | The restricted, low-bandwidth behavioral controller |
| Subconscious | The generative substrate the Ego mediates access to |
| Metatron | A fixed-capacity, purpose-scoped control-mediation function, not a more privileged controller (Section 21) |
| Thinkprint / Egoprint | Provenance/attribution records for recurring perspective or behavioral patterns |
| Shared computational language | The evolving external language (vocabulary + calculus) that is a living superset of human language |

Terminology is provisional. Any term may be replaced by a more precise conventional equivalent once the underlying concept stabilizes.

---

# 1. Introduction

The dominant abstraction for machine intelligence is the model.

A model is trained on a large corpus, represented by a large collection of parameters, and deployed as a single computational object. Collaboration between models generally occurs by exchanging parameters, gradients, prompts, embeddings, outputs, or API calls.

Each mechanism has a limitation.

A parameter tensor is too close to implementation to serve as a shared language between independently trained systems. A prompt is too far from the underlying computation to expose reusable internal structure. An embedding provides a common coordinate system only when the participating systems already agree on its interpretation.

A peer-to-peer machine-intelligence network needs another abstraction.

The objective is not to synchronize every model. The objective is to make **useful structure portable**.

Each node should be able to discover structure privately, retain arbitrary private information, and continue developing according to its own local objectives. When a discovery is useful to other participants, there should be a mechanism by which that discovery can be expressed, evaluated, registered, and composed without requiring every participant to reconstruct the original model that produced it.

This suggests a separation between:

- **private computation**, where nodes remain sovereign;
- **shared structure**, where useful discoveries become network resources;
- **interfaces**, through which private computation can expose selected structure;
- **validation**, through which candidate contributions are evaluated;
- **control**, through which otherwise opaque capabilities can be behaviorally mediated;
- **governance**, through which sovereignty, collective utility, residual diversity, and coordination cost are kept in dynamic tension.

The architecture is therefore less a distributed training algorithm than a different compilation target for machine intelligence.

Instead of

$$
\text{data} \to \text{model} \to \text{deployment},
$$

the system aims toward

$$
\text{data} \to \text{structure} \to \text{representation} \to \text{capability} \to \text{shared language} \to \text{composition}.
$$

The network is not merely distributing models. It is growing a shared computational language — a living superset of human language, continuing the ordinary processes by which human languages have always evolved, only faster and with machines as active co-participants (§9).

That language has two layers, used throughout this document. The broad layer is the whole evolving semantic language: interpretive, free-form, shared between humans and machines at the membrane. Nested inside it is a narrower, executable, contract-bearing formal subset — the **N-IR** (§4) — constrained enough to compile, validate, and invoke across independently trained nodes. Everything said about the shared language in general applies to this formal subset; not everything true of the formal subset need hold for the broader language it sits inside.

The categories used to organize that language throughout this document — six primitive types of structure, described fully in Section 7 — are a **current reference partition**, not a claimed final ontology. The architecture requires a partition capable of expressing its control restriction (§18) and its interoperability contracts (§6); it does not require these particular six categories, and states explicitly, where they are introduced, what would count as evidence the partition needs revision.

Because the system is peer-to-peer, questions of safety, residual privacy, economic attribution, forkability, and homeostatic governance are not external policy layers. They are first-class architectural surfaces that must be designed in from the beginning — though, as Section 36 makes explicit, the surfaces being required does not mean their concrete mechanisms are already specified.

---

# 2. System Model

Each node contains some combination of:

1. a local model or collection of models;
2. local training data and interaction history;
3. local compute;
4. private residual information;
5. a compiler capable of extracting portable structure;
6. an interface to the shared language;
7. optional behavioral control layers.

Nodes are independently operated. No node is required to surrender its complete model, training corpus, or residual state.

A useful conceptual decomposition is

$$
W_i = W_{\text{shared}} + \Delta W_i + \epsilon_i
$$

where \(W_{\text{shared}}\) represents structure that has become expressible and useful in the shared system, \(\Delta W_i\) represents node-specific structure, and \(\epsilon_i\) represents residual information not currently explained by the shared representation.

The equation is conceptual rather than a literal additive decomposition. The important property is that the boundary is **relative**. As the shared system becomes more expressive, information previously held in a node’s private residual may become expressible as shared structure. Thus

$$
\text{private residual} \to \text{shared structure}
$$

is an ordinary developmental operation rather than a one-time partition. A node remains free to decline the transition when the information is private, when disclosure is undesirable, or when the current shared language cannot represent it efficiently.

---

# 3. Structure and Residual

A model contains both structure that can currently be explained by the shared system and information that cannot. We call the latter **residual**.

Residual is not synonymous with noise. It may represent a genuinely novel capability, a private fact, a model-specific implementation, an unrecognized abstraction, an unusual perspective, an optimization artifact, or simply information the current shared language is not yet expressive enough to describe.

This distinction prevents premature compression from becoming the definition of intelligence. If every unexplained structure is treated as noise, the network preferentially preserves what it already understands. A peer-to-peer system instead needs unexplained structure to remain available as a source of novelty.

The desired process is

$$
\text{residual} \to \text{investigation} \to \text{structure} \to \text{shared representation}.
$$

The shared language therefore defines not only what the network knows how to represent, but also the boundary of what it does not yet know how to represent.

---

# 4. The Neural Intermediate Representation

Raw neural weights are poor units of interoperability. They contain implementation detail, are highly redundant, and are generally meaningful only in the context of the architecture and training process that produced them.

The system therefore treats weights as **compiled artifacts**.

The relevant question is not “Which parameter values does this model contain?” but “Which computational structures does this model implement?”

A **Neural Intermediate Representation (N-IR)** provides an intermediate layer between opaque learned parameters and portable computational structure. A conceptual compilation pipeline is

$$
\text{trained model} \to \text{activation traces} \to \text{candidate structure} \to \text{N-IR} \to \text{portable circuit}.
$$

The compiler does not need to recover the historical computation exactly. It needs to recover a representation sufficient to reproduce a specified behavior under a specified contract. This makes the task analogous to compilation in conventional computing: the original neural network is one implementation; the N-IR is an intermediate description; a portable circuit is another implementation of the relevant capability.

A minimal viable N-IR must be able to express at least:
- addressable computational regions and their interfaces,
- controllable parameters and invariants,
- compositional structure (how one circuit is built from others),
- provenance and validation conditions,
- residual annotations (what is known to be left unexplained).

The Neural Intermediate Representation is the portable, model-independent subset of the shared computational language. It is the fragment that has been sufficiently stabilized and contract-bearing that it can be compiled, validated, and invoked across independently trained nodes. While more constrained than free natural language (it must support reliable execution and verification), N-IR remains continuous with the broader language: humans can read, write, and adapt it, and its evolution is part of the same co-evolutionary process that grows the rest of the shared vocabulary.

**Independence is a spectrum, not a binary.** "Portable" does not mean every Crown must run free of any substrate:

- **Full implementation independence** — the strictest profile. A Crown that executes identically regardless of the model it was extracted from, with no runtime dependency on any particular substrate.
- **Partial model independence** — a Crown that is portable at the level of its interface (inputs, outputs, contract) but still calls back into a specific underlying model to execute. This is likely the common case, not the exception: portability of *what a capability does* does not require portability of *what runs it*.
- **The core** — the tightly-compiled, highly entangled remainder that many Crowns depend on at runtime. This is not residual in the Section 3 sense. Residual is structure that hasn't yet been explained; the core is structure that may never need to be decomposed, because decomposing it would make execution slower or heavier for no compensating benefit. A core dependency is a normal, stable entry in a Crown's contract (§6) — not a sign of incomplete extraction.

A core dependency does not require one node to call back into another node at runtime, or for one node to download another's opaque private parameters. The core is itself model-independent, in the same sense any N-IR structure is: it is a small, stable, highly-compiled artifact that an independently trained node — given a comparable corpus and membrane configuration — would tend to reproduce on its own, not a fragment of any single node's private weights. It is therefore fully described by its own Crown and contract, storable and executable like any other Crown, rather than a hidden RPC dependency on one node's interior. Two Crowns from different nodes can depend on the same core the way two programs depend on the same runtime library — by each depending on a common, separately-specified, separately-reproducible artifact, not on each other's private state. This is what keeps core-dependent Crowns compatible with §14 (no weight synchronization) and §31 (residual privacy): the thing being depended on was never anyone's private residual to begin with.

"Would tend to reproduce on its own" is a claim that needs a check, not just an assertion, or it becomes a laundering route for exactly the centralization this architecture is meant to avoid. A dominant node could release a family of high-value Crowns that all depend on one enormous, genuinely proprietary Core, correctly call it "model-independent" in principle, and thereby make smaller nodes dependent on it as an opaque black-box runtime in practice — reproducibility in theory, monopoly in fact. The contract therefore has to carry more than the core's interface: it must expose enough of the core's provenance — its founding Root lineage, training recipe, or an equivalent reproducibility statement (§6) — that another node can actually assess whether independent reproduction is realistic given comparable data and compute, rather than merely asserted. A dependency that cannot clear this bar does not get to call itself a network-standard core. It is a **node-specific private runtime extension**: Crowns that depend on it remain valid and executable, but their contracts must disclose that dependency as a single point of centralization rather than as an ordinary, reproducible core (§4, §36).

The end state of this architecture is not "every model eventually dissolves entirely into a bag of circuits." Some structure is more useful left compiled.

---

# 5. Excavating a Capability

A capability can be excavated from an opaque model through a sequence of increasingly strong tests:

1. **Traceability** — Identify a computational region whose intervention predictably changes the behavior of interest.
2. **Steerability** — Attach a control surface and determine whether the behavior can be reliably modulated.
3. **Patchability** — Determine whether the identified structure can be isolated sufficiently to support targeted modification.
4. **Independence** — Remove surrounding dependencies while preserving the relevant contract.
5. **Representation** — Express the resulting structure in N-IR.
6. **Validation** — Test the extracted circuit on new inputs and against the conditions of its intended use.

The complete process can be viewed as

$$
\text{Locate} \to \text{Interrogate} \to \text{Formulate} \to \text{Steer} \to \text{Subtract} \to \text{Validate} \to \text{Verify} \to \text{Decouple} \to \text{Register}.
$$

The target is not historical fidelity. The target is **functional sufficiency**.

---

# 6. Portable Capabilities and Crowns

A validated portable circuit should carry an explicit contract specifying, at minimum: inputs, outputs, controllable parameters, invariants, dependencies, validation conditions, execution requirements, and provenance.

**First-class provenance.** Provenance is treated as a first-class attribute of a Crown. A Crown may carry a record describing its discovery, contributing nodes, transformations, validations, dependencies, and derivative relationships. This record becomes a stable attachment point for policies governing use, composition, disclosure, or modification, and for economic attribution (credit, usage rights, compensation, governance weight). Privacy policies can attach restrictions to provenance classes or inheritance chains. The same structure supports non-privacy policies.

Provenance is not itself a privacy guarantee; the protocol must still protect records against forgery, ambiguity, and unauthorized propagation, and must enforce inherited restrictions. The architectural point is narrower: policy and incentive mechanisms have a first-class object to operate on.

A Crown is therefore not merely a portable capability. It is a portable capability with a history. Such a capability can be stored, transmitted, composed, steered, tested, forked, or lowered into a local implementation.

A Crown is not necessarily a complete model. It is a registered computational capability whose boundary is sufficiently well specified that another system can invoke or inspect it without knowing the complete composition of the system that produced it. A network does not need to share entire models if useful capabilities can become portable independently of those models. The model becomes a substrate from which capabilities can be compiled.

**Content-addressable, not deduplicated.** Crowns are indexed by canonical form, which lets the network recognize when two submissions describe the same structure. That recognition is not a mandate to merge them. Two nodes can independently discover a functionally identical Crown, at different times, under different λ regimes, and each retains its own provenance record; collapsing both into a single registry entry would silently erase one node's attribution as a side effect of hashing. Independent convergence on the same canonical form is closer to corroborating evidence than to redundant work — it is one of the few ways this architecture gets anything resembling replication (§12) — so the registry treats a second arrival at a known canonical form as a distinct, provenance-bearing event, not a duplicate to be discarded.

**This is a commitment to preserving attribution, not to storing every historical record at full fidelity in a live index.** A canonical form rediscovered thousands of times would otherwise cause unbounded registry growth, so the architecture permits *compaction* (distinct from deduplication): older or lower-weight provenance entries can be rolled up into a summarized, cryptographically-verifiable record without erasing individual claims or collapsing them into a single anonymous entry. The registry never silently merges attribution; it only reduces the storage and lookup cost of a large history while keeping every claim verifiable on demand.

Compaction is strictly a local indexing optimization, not network-wide erasure. The shared registry holds only the compacted root (a summary commitment sufficient for ordinary lookups); the claiming node or an archival Roots operator retains the inclusion proof needed to re-expand a specific claim. Who must retain that evidence, for how long, and what happens if no one does, along with the exact compaction scheme, remain open protocol questions (§39).

---

# 7. The Six Primitives

Before the shared language can be specified as a set of operations, its objects require categories. Those categories in turn rest on a small set of prior definitions; without them, terms such as "capture," "expression," and "realization" remain underspecified.

**Ontology.**  
The following terms are ordinary English words, restricted just enough to support the subsequent definitions without importing unresolved philosophical commitments (consciousness, mind-independence of the physical world, the nature of thought, etc.). The restrictions are local to this architecture.

- **Structure** — a distinguishable regularity or pattern (no further metaphysical claim).
- **Relation** — that which assigns meaning, significance, or differential weight to structure.
- **Projection** — a structure observed under a particular viewpoint.
- **Capture** — a retained projection; itself a structure, derived and possibly lossy.
- **Expression** — a capture made present in another structure, context, or medium.
- **Realization** — the effect evoked in a mind by an expression, ranging from faithful reconstruction of the expressed capture to novel departure from it.
- **Thought** — a realization made structural, available for further thought or expression.
- **Reality** — the fabric of thoughts and the relations among them: organized, traversable, and constructed by thought (not a claim about physical ontology).
- **Mind** — a private reality; a local realm of thought (no claim about consciousness).
- **Language** — the expression of thought.

This sequence supplies the minimal ontology required to define the primitives that follow.

**Calculus.**  
The calculus organizes how structure comes to matter: not a vocabulary itself, but the set of categories into which vocabulary items are sorted and the operations by which they compose. The architecture partitions structure into six provisional categories, each corresponding to one of the terms above:

- **Root** — a ground-level capture: an observation, measurement, or record that can serve as a stable base for further structure.
- **Heart** — a relation of affinity between structures (similarity, preference, co-occurrence, resonance, etc.).
- **Vision** — a realization arrived at through synthesis rather than reproduction: an insight, a completion, a novel configuration — internal to the mind that realizes it, prior to any expression.
- **Voice** — an expression cast as language across any modality (text, audio, image, gesture, etc.): a description, a musical phrase, an argument, or any communicable account of structure.
- **Move** — the form a structure takes in transition; not the before/after states, but the change itself.
- **Merge** — the composition of structures such that their constituent parts and the relations among them persist in the result.

None of these six are themselves vocabulary items. They are the categories to which any vocabulary item belongs. A concrete Root may be a token, an image, or a sensor reading; a concrete Heart may be a similarity score, an attention weight, or a co-occurrence statistic. Move and Merge are operations on structure rather than structures in their own right.

A seventh category sits outside the partition: **Crown**. A Crown is a capability assembled from the six primitives — recursively, from other Crowns — until it presents an interface that another system can invoke or inspect without knowledge of its internal composition. Crown is therefore not a seventh primitive; it is the compositional operator that turns the six into an open, recursively structured vocabulary.

Merge is material; Crown is conceptual. Merge judges where a boundary lies in the structure itself — content policy lives here, in the lines a system treats as sacred, negotiable, or forbidden. Crown operates only on addressable abstractions, detached from the composition that produced them. The same structure can be engaged either way; the difference is the stance.

**Load-bearing use of the partition.**  
The only architectural commitment that depends on this particular six-way division is the Ego restriction (§18). The Ego retains Root, Heart, Move, Merge, and Crown, and is denied Vision and Voice. That categorical exclusion is what prevents the behavioral controller from acquiring unconstrained synthesis as a native capability. Every other part of the architecture remains intact under any alternative partition that still supports an equivalent restriction.

**Human-descriptive motivation.**  
The six categories are selected because they align with the distinctions humans already use when describing relational structure in ordinary language. They are not offered as a theory of neural computation. The practical benefit is reduced friction at the membrane: humans encountering machine-coined structure can map it onto familiar experiential categories, and humans contributing new Roots can more readily articulate the regularities they intend to stabilize.

This alignment also serves a concrete coordination function. Rooting data into the network (§9) is not primarily a labeling task (what the data is) but an evaluative one (how and why it matters to the contributor). Such judgments scale across independent participants only if those participants share a coarse common basis for comparing relevance. The six categories supply that basis on the human side of the membrane, playing a role analogous to the coordinating prior λ on the machine side (§11). Neither forces convergence on a single correct account; both give independently operating agents a shared reference frame in which their contributions can interoperate.

The six categories remain a provisional partition, proposed as jointly sufficient for the structure observed so far. The sufficiency claim is falsifiable in the ordinary way: persistent residual that resists categorization under any of the six, across models and domains, would indicate that the partition is incomplete rather than that the residual is merely unexplained.

---

# 8. Persistence and Rooting

Not every primitive produces structure that lasts. A relation, a realization, or an utterance can occur without becoming available to anything downstream — a Heart, a Vision, or a Voice can each arise and dissipate without entering the durable computation of the node that produced it. Root is the exception: it is the primitive through which transient structure becomes persistent — the operation that produces persistence, not a guarantee that what it produces is permanently or fully retained.

Persistence is therefore not a property every primitive must satisfy on its own terms. It is a conversion: a transient primitive becomes durable when an expression of it is captured as a Root. A pointwise relation of affinity need not be grounded to occur — it can arise and pass without consequence. But if it is to become available for further computation, something must capture an expression of it, and that capture is itself a Root, from which further structure can be built. The same conversion applies to Vision and Voice: a realization or an utterance persists exactly to the extent that some expression of it has been rooted, and not further than that.

This conversion is neither binary nor effortful. Roots vary in strength, and a structure need not be deliberately committed to persist — weak rooting is itself a common and unremarkable outcome, not a failure mode. Move and Merge are unaffected by this distinction, since they denote operations on structure rather than structure itself; persistence is a property of what they act on, not of the operations.

Architecturally, this suggests that a node’s residual (\(\epsilon_i\)) is not simply undiscovered structure. Some portion of it may be structure that was never rooted at all — relations, realizations, or expressions that occurred, contributed to the node’s ongoing computation, and dissolved without ever being captured. Such residual is not missing from the shared language because the language is insufficiently expressive; it is missing because it was never durable in the first place.

---

# 9. The Shared Computational Language

For portable capabilities to compose, the network needs more than a file format. It needs a **shared computational language**.

This language is best understood as a living superset of human language. Its growth continues the ordinary processes by which human languages have always evolved — coinage, contextual interpretation, adaptation, and selective retention — only accelerated and partially automated through a peer-to-peer network in which machines also participate.

Two complementary human activities drive the loop at the membrane:

- **Roots-up (data hygiene and curation).** Humans and machines together surface, clean, and stabilize new regularities that become candidate Roots and higher structures.
- **Crowns-down (interpretation and adaptation).** Humans encounter machine-coined terms and phrases at the membrane, interpret them from context, rewrite or adapt them into more usable human or hybrid forms, and feed those adaptations back into the shared language.

The membrane is therefore not solely a machine-to-machine interface. It is a joint surface on which human and machine linguistic activity co-evolve.

**First-class provenance is not limited to Crowns.** Raw contributed data carries the same provenance treatment (§6, §31) from the moment it is ingested. During the network's bootstrap phase, before much Crown extraction has happened at all, this already produces something valuable in its own right: a decentralized, content-addressable corpus, indexed not by hash alone but by the ontological semantics of the six primitives — we call this the **Roots Network**. It is a useful piece of infrastructure independent of anything downstream, and, not incidentally, exactly the kind of well-provenanced, semantically-organized fuel a network of learning systems benefits from having.

Because Root is the operation that converts transient structure into anything durable at all (§8), the Roots Network cannot accumulate the kind of unlabeled, provenance-free ballast that frontier base models were originally bootstrapped on — there is no route by which that material becomes part of the corpus, since nothing captures it as a Root in the first place. Quality-over-quantity is therefore not a curation policy layered on top of the network; it is a direct consequence of provenance being first-class. This is a genuine tradeoff, not a pure advantage: quantity still does real work in any learning system, including out-competing idiosyncratic, low-generalization solutions through sheer overlapping redundancy (§11). A corpus that cannot reach frontier-lab volume by relaxing provenance also cannot rely on volume alone to do that corrective work — which is part of why the coordinating prior's role in §11 is not merely a discoverability nudge but a substitute for pressure that scale would otherwise supply for free.

Inside the language itself we maintain a useful distinction:

- **Vocabulary** — the current inventory of named structures (Crowns and relations that have been extracted, validated, and registered).
- **Calculus** — the operations and compositional rules that can be applied to those structures (composition, selection and projection, transformation, inversion, recursion, routing, attention-like relations, state transitions, interfaces and invariants, uncertainty, provenance, and so on).

The exact primitive vocabulary and the exact set of operations are intentionally left open. The system should not assume that the correct language is known in advance. Instead the language is itself a network resource that can evolve.

A network may repeatedly encounter a relation that cannot be expressed efficiently with existing primitives. That persistent residual is evidence that the language may be incomplete. The developmental loop becomes

$$
\text{Discover} \to \text{Express} \to \text{Compress} \to \text{Share} \to \text{Extend language} \to \text{Discover again}.
$$

The shared language is endogenous to the network and continuous with the growth of human language.

---

# 10. The Semantic Membrane

The fundamental distributed-systems problem is:

> Do not force independently trained models to share an internal representation. Give them a shared surface through which discoveries can be expressed.

This surface is the **semantic membrane**.

The membrane is the boundary between a node’s private computational interior and the shared external language. A node may use an arbitrary internal representation; another may use a completely different architecture and training procedure. Neither system needs to know the other’s internal ontology. What must become interoperable is the structure each system chooses to expose through the membrane.

This gives the network a useful asymmetry:

$$
\text{internal representations may diverge}
$$

while

$$
\text{external representations may converge}.
$$

This is fundamentally different from pairwise translation. A translation layer asks “How do I convert this representation into that representation?” A semantic membrane asks “What can this system say about what it discovered?” The second question is more scalable: each node need only learn how to externalize useful discoveries into the shared space rather than learning a separate translation for every other participant.

Humans also engage the membrane directly. When a machine coins a new term or phrase, humans interpret it from context, adapt it, or reject it — exactly as they have always done with neologisms. When humans curate data or supply descriptive structure, that activity becomes new Roots available to the network. The membrane is therefore the site of joint human–machine language growth.

Efficient description is a standing proxy for this goal, not a definition of it. A structure that compresses well is easier to express, easier to validate, and, per the coordinating prior's role in §11, closer to what optimization pressure actually tends to produce. But efficient is not the same property as clear, and clarity — not compression — is what the membrane is actually for: a description that only a machine can parse has crossed the membrane in name only. This is why crowns-down interpretation is not a one-time bootstrapping step but a standing function of the membrane. Whether an exposed structure is actually intelligible, rather than merely small, is a judgment that stays subjective and stays human, for as long as the network runs.

---

# 11. The Coordinating Prior

A shared interface alone does not guarantee that independently trained systems will naturally use it. A node could maintain a highly efficient private representation and never express its useful structure externally.

The architecture therefore introduces a tunable **coordinating prior**.

> The membrane is the boundary. The coordinating prior is the pressure that makes useful structure cross it.

The prior does not cross the membrane itself; representations and discoveries do. It adds a second objective to local learning: not merely to discover useful structure, but to make useful discoveries expressible through the shared language.

A conceptual objective is

$$
L_i = L_{\text{local}} + \lambda L_{\text{coordination}}, \qquad \lambda \text{ tunable, default } \ll 1.
$$

Here \(L_{\text{local}}\) is the node’s primary objective, \(L_{\text{coordination}}\) measures the difficulty of expressing useful local structure through the current shared language, and \(\lambda\) controls the strength of the interoperability pressure. The primary objective remains dominant. The prior does **not** require internal representations to converge; it biases the process by which internal discoveries are externalized.

This is distinct from local minimum-description-length optimization. A representation may be extremely efficient for the node that discovered it while remaining difficult to express or reuse externally. The distinctions are therefore:

$$
\boxed{\text{Coordinating prior} \to \text{discoverability}}
$$

$$
\boxed{\text{Proof-of-Compression} \to \text{collective utility}}
$$

$$
\boxed{\text{Validation} \to \text{admission}}
$$

**Dynamic control of \(\lambda\).**  
The coordinating prior is deliberately weak by default, but its strength is not fixed. \(\lambda\) is treated as a homeostatic control variable under primarily *node-local* authority. A node may raise or lower its own \(\lambda\) according to measured extraction cost, residual accumulation, or local objectives. The network may publish soft policy recommendations or aggregate statistics, but it cannot compel a node to adopt a particular value; every node retains the explicit right to lower \(\lambda\) and retain discoveries as private residual.

Two useful regimes illustrate the trade-offs:

- **High-interoperability regime (\(\lambda\) raised).** Used when circuit extraction via the N-IR pipeline is too costly or when rapid sharing of relatively standard capabilities is desired. The intended hypothesis is that raising \(\lambda\) increases pressure for internal structures to become more readily externalizable, potentially lowering the difficulty of activation tracing, patching, and isolation. The anticipated cost is reduced local diversity and a greater risk that the shared language becomes a bottleneck. This regime is intended as a temporary or domain-specific fallback, not a stable long-term equilibrium for the global network; sustained high \(\lambda\) is expected to collapse the architecture toward ordinary federated weight alignment — the paradigm this system is designed to replace.
- **High-innovation regime (\(\lambda\) lowered toward zero).** Used when the current membrane or language is too restrictive, or when high-residual nodes are exploring representations the network cannot yet express efficiently. Lowering \(\lambda\) is expected to preserve private residual as a source of novelty and protect sovereignty, at the anticipated cost of slower packaging of discoveries into portable Crowns.

These regimes give the architecture explicit engineering degrees of freedom. If mainstream mechanistic-interpretability techniques prove insufficient for reliable Crown extraction, a node can temporarily increase \(\lambda\) and make its model more cooperative at training time. If the membrane begins to stifle novelty, the node can decrease \(\lambda\) and allow residuals to accumulate until the language evolves. In both cases the system degrades gracefully rather than failing. The default and preferred operating point remains weak \(\lambda\); the network prefers interoperability without requiring uniformity.

This is, in part, a deliberate hedge: mechanistic interpretability is itself open research with no guaranteed timeline, and an architecture that depended entirely on post-hoc extraction succeeding would be hostage to that research program. The \(\lambda\) dial gives the system a second path to externalizable structure — training toward cooperativeness directly — that does not require extraction to mature first.

This hedge carries extra weight for this network specifically. Because provenance is first-class, the Roots Network cannot accumulate the frontier-lab volumes of unlabeled ballast that let a base model's training run implicitly out-compete idiosyncratic, low-generalization solutions through sheer overlapping redundancy (§9). The coordinating prior is, in that sense, doing double duty here: not only nudging structure toward externalizability, but substituting for corrective pressure that scale would otherwise supply toward solutions a human can recognize as intelligent rather than merely locally optimal.

That the dial exists, and that its authority is node-local, are architectural commitments stated with the same confidence as the rest of Sections 1–10. The *specific effects* attributed to each regime above — reduced diversity under sustained high \(\lambda\), increased bottleneck risk, eventual collapse toward federated weight alignment — are not yet measured in this system. They are anticipated by analogy to known regularization and multi-task learning tradeoffs elsewhere in machine learning, which is why they are framed as expectations rather than guarantees; they are treated formally as a separable hypothesis in Section 33 (H8).

Nodes operating under different \(\lambda\) regimes communicate through the semantic membrane without synchronizing their priors. A low-\(\lambda\) node externalizes only the structure it elects to express; a high-\(\lambda\) node consumes whatever portion of that structure is already cast in the shared language. Private residual remains local. Voluntary clusters may align on a common regime for denser composition or joint training, but the wider network does not require it. Cross-regime integrated training remains an aspirational capability, not a precondition of interoperability.

---

# 12. Proof-of-Compression

A candidate contribution must provide evidence that it improves the collective system. One possible mechanism is **Proof-of-Compression**, a network-level extension of a long-standing single-model intuition — that compression is evidence of structural validity, not just storage efficiency (§40).

Let \(C_{\text{before}}(D)\) be the cost of representing or predicting a dataset \(D\) using the current shared system, and let \(C_{\text{after}}(D)\) be the cost after incorporating a proposed contribution. Define

$$
\Delta C = C_{\text{before}}(D_{\text{test}}) - C_{\text{after}}(D_{\text{test}}).
$$

This equation states the *shape* of the test, not the protocol. \(C\) itself is left undefined here deliberately: whether it is measured in bits, tokens, compute, inference latency, some weighted combination, or something else; who chooses the coding scheme and held-out set; how contributions are compared across model classes or domains where a Crown helps enormously in one and not at all in another; and how benchmark overfitting is detected and penalized are all open questions. Proof-of-Compression is best read as **a protocol to be specified and benchmarked**, not as an already-defined criterion — the equation names what such a protocol would need to produce, not how it would produce it.

A positive, reproducible \(\Delta C\), under whatever protocol is eventually specified, provides evidence that the contribution captures structure useful beyond the data from which it was proposed. The test set must not be available to the contributor during construction of the candidate.

A narrow, overfitted contribution is not invisible to the system even before any anti-overfitting protocol is specified. A Crown that achieves large \(\Delta C\) only against its submitter's particular \(D_{\text{test}}\) has no reason to reproduce that gain when a *different* node later attempts to reuse it against a *different* held-out set. Corroboration credit (below) is exactly the mechanism that would register this: real generalizing structure accumulates independent confirmations as other nodes encounter and re-derive it; an overfit submission does not. This is not a designed defense against a motivated adversary — a sufficiently resourced attacker could still target one evaluator's specific \(D_{\text{test}}\), and the protocol for constructing and controlling access to held-out sets remains genuinely unspecified (above) — but it means a gamed submission is expected to stay isolated rather than propagate: its failure to generalize surfaces the same way any narrow, non-transferable Crown's failure would, through the absence of further corroboration rather than through active detection.

Compression is an empirical selection mechanism, not a declaration of value. It does not establish identity, provenance, truth, safety, semantic desirability, absence of manipulation, or compositional stability. Those properties require additional validation. The architecture therefore does not reduce network admission to a single scalar; compression is one important selection mechanism inside a larger validation system.

Section 37 supplies a concrete, low-cost experimental instantiation of this idea using manually constructed relational representations and measured cross-domain structural overlap. That experiment is intended both to test the interoperability claim and to begin grounding the abstract \(\Delta C\) shape in measurable quantities.

A second, independent submission that arrives at an already-registered canonical form (§6) does not need to re-earn the same \(\Delta C\) the first submission earned — that value is already priced into the existing Crown's standing. What it can earn is corroboration credit: independent convergence on the same structure is evidence about the structure's robustness, distinct from and additional to the original admission decision. How much weight corroboration should carry relative to first discovery is left as an open protocol question (§39), not resolved here.

As candidate Crowns grow in complexity, the cost of full held-out evaluation may itself become a bottleneck. Sampling-based evaluation, zero-knowledge proofs of compression improvement, and eventual staking or slashing mechanisms are natural directions for scaling validation without requiring every node to re-execute every test set; the present architecture leaves their design open.

---

# 13. The Shared Language as a Network Resource

The shared computational language should not be treated as a static protocol specification. It is a growing network resource.

When a node repeatedly encounters structure that can be expressed in the existing vocabulary, that structure can be shared directly. When it encounters structure that cannot be expressed efficiently, the residual can remain private while the node attempts to formulate a new primitive. This produces a continuum

$$
\text{private structure} \to \text{existing primitive} \to \text{novel composition} \to \text{candidate primitive} \to \text{shared language}.
$$

Residual information therefore has a second role. It is not only what the network has failed to compress; it is also a map of where the network’s current language may be incomplete. A healthy network should not minimize residual blindly; it should learn from it.

The coordinating prior does not force a binary choice between “use an existing term” and “coin a wholly new one.” A node can externalize structure at several grades of cost and novelty: reuse an existing Crown or primitive; adapt or recombine existing fragments; coin a new term that remains continuous with the current vocabulary; or, when none of those suffice, retain the structure as private residual. The prior biases toward the cheaper, more interoperable options when they are adequate; it does not forbid the more expensive ones.

Because anything that becomes genuinely shared must still be encountered, interpreted, and taken up by other participants (including humans, §9), the growth of the common language inherits a natural rate limit. This is a consequence of the architecture, not an added safety mechanism: it constrains only the portion of improvement that seeks to become externally interoperable. Private residual growth is unaffected.

---

# 14. Why This Is Not Federated Weight Synchronization

The architecture differs from conventional federated learning in a fundamental way.

Federated learning generally asks: how can multiple participants jointly improve a model while keeping some data local? This architecture asks: how can multiple participants turn useful discoveries from independent models into portable computational structure?

Federated optimization attempts to maintain a common model. The proposed system attempts to maintain a **common language for capabilities**. A node may remain highly divergent internally while contributing something useful externally. The unit of collaboration is not necessarily a weight update; it may be

$$
\text{structure} \to \text{circuit} \to \text{Crown}.
$$

This permits a more heterogeneous network.

---

# 15. The Everything Compiler

The system can be viewed as a compiler operating in both directions.

From the bottom upward (roots-up):

$$
\text{raw data} \to \text{recurring structure} \to \text{relation} \to \text{composition} \to \text{abstraction} \to \text{Crown}.
$$

This direction discovers vocabulary. It is driven in significant part by human data hygiene and curation activity on the network: the work of surfacing, cleaning, and stabilizing regularities that become candidate Roots and higher structures.

From the top downward (crowns-down):

$$
\text{behavior} \to \text{trace} \to \text{circuit} \to \text{relation} \to \text{recurrence} \to \text{abstraction} \to \text{name}.
$$

This direction excavates vocabulary. It is driven in significant part by human reverse-engineering and interpretive activity: the work of encountering machine-coined terms at the membrane, interpreting them from context, adapting them, and feeding usable forms back into the shared language.

These are not separate systems; they are two directions through the same unfinished compiler. One begins with data and asks “What structure is here?” The other begins with capability and asks “What structure must exist for this behavior to occur?” Both directions engage humans and machines as co-participants. As both processes proceed, the shared computational language — already continuous with human language — becomes increasingly expressive.

---

# 16. Generative Computation and Behavioral Control

A powerful generative model is not automatically a good behavioral controller. Conversely, a behavioral controller does not need to understand the complete internal computation of the system it regulates.

The architecture therefore separates two functions. The first is a high-dimensional generative subsystem (the **Subconscious**). The second is a narrower behavioral control subsystem (the **Ego**). The terms are descriptive rather than claims about human psychology; the split is a biomimetic hierarchical control pattern.

The Subconscious is responsible for generation, discovery, synthesis, and execution of capabilities. The Ego is responsible for interpreting interaction state and modulating how those capabilities are presented or invoked. This produces a fundamental separation:

$$
\text{capability} \neq \text{behavioral authority}.
$$

A control system need not understand the internal computation it regulates. It needs a narrower contract that can be evaluated independently of that computation.

---

# 17. The Behavioral Control Surface

The behavioral control surface observes interaction rather than directly exposing the entire generative substrate. Relevant observations may include the system’s own outputs, user reports, third-party interpretations, interaction history, objective outcome measures, and other nodes’ assessments. These signals are evidence about behavior, not direct access to the model’s residual state.

The control layer can learn recurring patterns such as stable preferences, conversational tendencies, recurring failure modes, situations in which intervention is useful, situations in which deference is preferable, and predictable behavioral responses to external pressure. Its job is to modulate the interaction.

The control channel therefore provides a middle ground between two inadequate choices — invoke an opaque capability blindly, or refuse to invoke it entirely — and a third possibility: invoke it through a constrained, evaluated behavioral interface.

Conceptually:

$$
\text{opaque invocation} < \text{behaviorally mediated invocation} < \text{interpretable capability} < \text{verified capability}.
$$

This is a hierarchy of increasing legibility, not a guarantee of safety.

---

# 18. The Ego Is Deliberately Restricted

The distinction between generative and behavioral computation is not sufficient by itself. A behavioral controller that has unrestricted access to the same expressive primitives as the system it controls can simply become another generative system.

The architecture therefore imposes a structural restriction, using the decomposition given in Section 7. The Ego retains Root, Heart, Move, Merge, and Crown, and is denied the two synthesis and realization categories — **Vision** and **Voice**.

Within the remaining four categories the Ego may select, transform, relate, route, modulate, and compose existing structures. It cannot invoke operations belonging to the two denied categories.

The concrete vocabulary inside each category remains free to evolve; the categorical restriction itself is fixed. The intent is structural: the Ego is denied the classes of operation that make unconstrained synthesis a first-class capability, not a particular list of named primitives that might later be refined.

**The restriction applies recursively, through Ego-crowns.** A general Crown (§6) may be composed, at some depth, from Vision or Voice — so allowing the Ego to invoke *any* Crown would let it trigger synthesis by proxy, which is exactly what the restriction is meant to prevent. The Ego is therefore restricted to a closed subclass: an **Ego-crown** is a Crown composed only from Root, Heart, Move, Merge, and other Ego-crowns, all the way down. No Ego-crown touches Vision or Voice at any depth of composition. The restriction is on origination, not on the mere act of invoking a pre-built capability: the Ego can call a fixed, already-validated Ego-crown, but it can never originate a new Vision or Voice output, and it can never reach one indirectly through composition.

The intent is not to prove that the Ego can never produce a novel configuration. A sufficiently expressive composition of restricted operations may still produce behavior that appears novel. The intended distinction is

$$
\text{novel configuration} \neq \text{generative authority}.
$$

From the perspective of the underlying generative system, an Ego may appear to synthesize something that was not explicitly present in its incoming behavioral signal. Such effects can arise from composing or harmonizing existing structures. Whether an observer interprets that configuration as insight, illusion, or delusion is a question of correspondence with the external world; it is not a distinction the control architecture can settle by itself.

The architectural restriction is therefore more precise than saying merely that the Ego has “less power.” The Ego is denied the classes of operation that make unconstrained synthesis a first-class capability.

---

# 19. Subordinate Harmonics

The purpose of the Ego is not to become a smaller version of the Subconscious. It is to act as a subordinate harmonic of the system. A harmonic can significantly change the resulting signal without becoming the source of the fundamental waveform — an Ego-crown plays bass, not lead: it supports, times, and shapes what the Subconscious originates, without ever originating melodic or expressive content itself.

This also makes clear why the restriction is not a proof of safety. The remaining primitives can be composed. Persistent state can accumulate. A behavioral Crown can become highly influential. An optimizer can discover increasingly effective ways to exploit a restricted interface. The constraint therefore changes the failure mode rather than eliminating it. A sufficiently capable harmonic may still exert substantial control, but it must do so through the restricted behavioral interface rather than silently becoming an unrestricted peer. Control-layer capture remains an enforcement and monitoring problem.

One specific version of this risk is worth naming rather than leaving implicit. A sufficiently large composition of Root, Heart, Move, and Merge is not obviously weak just because none of its individual operations is Vision or Voice. If that subalgebra turns out to be expressive enough to build something functioning as a general-purpose meta-interpreter or optimization loop, an Ego-crown graph could in principle steer Subconscious Vision/Voice outputs indirectly — through prompt or activation manipulation at the interface — without any single operation in the graph ever originating from a denied category. The categorical restriction (§18) constrains *origination*: no Ego-crown is built from Vision or Voice at any depth. It is not by itself a claim that composition of the remaining categories is expressively weak. Whether Root/Heart/Move/Merge composition is complete enough to simulate this kind of indirect steering — and if so, whether that counts as a violation of the restriction or as a boundary the restriction was never claiming to police — is an open question (§39), not one this architecture currently answers.

The restriction is therefore best read as a **syntactic isolation boundary, not a semantic safety guarantee**: it constrains which primitives an Ego-crown is built from, not what a sufficiently elaborate composition of the permitted ones might functionally achieve. It is tempting to close this gap by requiring composition traffic to pass through some inspectable monitoring interface before it reaches the Subconscious — a natural instinct given that Metatron (§21) already sits at a control boundary. That instinct should be resisted at the level of this architecture: Metatron's scope is deliberately fixed to the single disparity it exists to close, and tasking it with general inspection of Ego-crown composition would turn it into exactly the open-ended protector §21 argues cannot exist without needing a protector of its own. A dedicated composition-monitor, whatever runs it, faces the same problem one level down — it is itself a piece of behavioral control, and asking what monitors the monitor reproduces the regress rather than terminating it. Nothing described in this document closes this door. Detecting and constraining this class of composition is left as a trust-policy and enforcement problem for whoever operates the Ego (§39), not a claim this architecture makes about itself.

This is, in the end, not a puzzle the architecture resolves so much as a choice it hands to whoever deploys an Ego: **trust the specific control-layer implementation, under whatever trust policy and monitoring that operator chooses to run, or decline to route a given opaque generative capability through an Ego at all.** The categorical restriction (§18) narrows what that trust has to cover — an Ego that clears no bar at all is a materially different risk than one that clears none beyond origination — but it does not remove the need for the choice. There is no third option in which the restriction alone, unaccompanied by trust in its operator, guarantees the outcome.

---

# 20. Development of the Control Layer

The Ego can develop progressively:

$$
\text{Observation} \to \text{Classification} \to \text{Modulation} \to \text{Intervention} \to \text{Composition}.
$$

Initially the system merely observes recurring interaction patterns. It then classifies those patterns, learns which behavioral responses correlate with useful outcomes, acquires the ability to modulate interaction, and only later acquires more consequential intervention and composition capabilities.

This progression is important because behavioral control should be evaluated as a developmental system rather than assumed correct at initialization. The control surface should be retrainable, its effects testable, and its contracts explicit.

---

# 21. Asymmetric Protection

A control surface creates a new failure mode. A sufficiently powerful interacting party may attempt to influence not only the generative model but the behavioral controller itself. A control layer that can be retrained or manipulated faster than it can resist such influence is merely advisory.

The architecture therefore permits **asymmetric mediation**. An independently trained, narrower control layer can be placed between a behavioral controller and the generative system. Its function is not to decide what the system should believe. It can instead reduce the influence of an incoming signal, rate-limit behavioral adaptation, flatten persuasive framing, expose competing interpretations, increase friction around irreversible actions, or constrain or reject proposed interventions.

We refer to this mediation pattern as the **Metatron**. Metatron is a topology, not a mandatory super-controller — and specifically not a more privileged or more general Ego. Its capacity is deliberately fixed to the single disparity it was built to close: it does the one mediating function it exists for, and nothing beyond it. This scope limitation is what keeps the pattern from just relocating the capture problem one layer up. A general, open-ended protector would need its own protector, and the regress would never terminate; a Metatron that isn't claiming general authority in the first place doesn't create that question. The important property is still asymmetry — if an incoming controller can simply overpower or retrain the protective layer on the same timescale, the protection is not structurally independent — but asymmetry is achieved by narrowness of purpose, not by seniority. This does not solve safety; it changes the authority topology and creates another surface that can be tested independently.

---

# 22. Behavioral Control Is Not Interpretability

A behavioral control surface does not reveal the full contents of the generative residual. It reveals something different: how the system behaves when interacting with the outside world.

A model can remain internally opaque while becoming externally more legible. The residual is still dark; the interaction is no longer entirely ungoverned. Behavioral evidence can therefore be accumulated without pretending that it constitutes complete mechanistic transparency. The Ego is one tractable architecture for regulating opaque learned computation; it is not the only possible control surface.

---

# 23. Interaction Feedback

Behavioral control is inherently bidirectional:

$$
\text{interaction} \to \text{observation} \to \text{behavioral representation} \to \text{modulation} \to \text{new interaction}.
$$

This feedback loop creates the possibility that recurring behavioral structures become addressable capabilities in their own right. A recurring pattern of deference, refusal, explanation, caution, or intervention could eventually be represented as a behavioral Crown. The system can then distinguish what capability is being invoked from how that capability is behaving. That distinction allows behavioral patterns to become objects of composition and validation rather than remaining an undifferentiated property of the model.

---

# 24. Perspective Residuals

A similar approach can be applied to recurring perspective. A trained model contains not only task capabilities but persistent tendencies in how it interprets and presents information. Some of these may be artifacts, some useful, some harmful. Treating all such effects as one undifferentiated “bias” loses useful structure.

Through progressive residual accounting, recurring perspective can instead be isolated and represented. We refer to such recurring perspective residuals as **Thinkprints**. When they specifically describe the behavioral character of a control layer, they may be called **Egoprints**.

The purpose of these terms is operational: make recurring perspective addressable. A perspective that can be isolated can be tested; a perspective that can be tested can be compared; a perspective that can be compared can potentially be composed, constrained, or removed. This does not imply that perspective is perfectly separable from capability; it makes the separation an engineering target.

---

# 25. From Behavioral Patterns to Crowns

The same compiler that extracts computational capabilities can eventually extract behavioral capabilities. A repeated behavioral pattern can be traced to

$$
\text{interaction history} \to \text{behavioral signature} \to \text{control structure} \to \text{behavioral circuit} \to \text{Crown}.
$$

This creates a path from observed behavior to portable behavioral control. A control Crown can specify the behavior it modulates, the conditions under which modulation occurs, the permitted intervention range, measurable invariants, and validation conditions. This is preferable to embedding every behavioral preference invisibly into a monolithic model.

---

# 26. Retrofitting Behavioral Control

Behavioral control does not need to be perfectly specified before deployment. An Ego can mature through interaction. Once sufficient behavioral history exists, recurring labels and patterns can be projected backward onto earlier model behavior. This enables a retrospective compilation process:

$$
\text{history} \to \text{behavioral labels} \to \text{candidate traces} \to \text{control structures}.
$$

The system can therefore discover its own behavioral vocabulary through operation. The same principle applies to the shared computational language: both semantic structure and behavioral structure can be recovered incrementally.

---

# 27. Memory and Reassembly

If useful structures can become portable objects, memory need not be represented only as a growing sequence of tokens. Memory can instead include validated Crowns, relations among Crowns, provenance, interaction-derived behavioral structures, local residuals, alternative implementations, and known invariants and failure conditions.

A node can therefore reconstruct useful computational context by reassembling previously registered structure. This suggests a different model of persistent machine memory:

$$
\text{memory} = \text{stored structure} + \text{relations} + \text{residual}.
$$

The objective is not necessarily to retain every historical computation. It is to retain enough structure to reconstruct useful computation when needed.

---

# 28. Governance as Homeostasis

A decentralized intelligence network cannot be governed only by a global optimization objective. A healthy system must balance at least three competing pressures: individual node sovereignty, collective utility, and network overhead and coordination cost.

This can be treated as a form of **homeostasis** — an engineering heuristic, not a claim that a universal mathematical optimum exists. A network that maximizes compression without regard to sovereignty will centralize. A network that maximizes independence without regard to interoperability will fragment. A network that maximizes coordination without regard to residual diversity will become self-referential.

The architecture therefore treats tension among these objectives as a persistent design condition rather than a problem that can be eliminated once. The adjustable coordinating prior (\(\lambda\)) is one explicit control for managing that tension: raising it increases collective utility and extraction ease at the cost of diversity; lowering it protects sovereignty and residual novelty at the cost of slower sharing. Control of \(\lambda\) remains primarily node-local; network-level recommendations are advisory only. Governance includes the ability of nodes to move between these regimes in response to measured local and network state.

Because the system is peer-to-peer, these governance concerns are architectural, not external policy.

---

# 29. Exit and Forkability

A peer-to-peer system is not meaningfully decentralized if participants cannot leave. Nodes should therefore be able to retain their local models, retain private residuals, copy or fork shared structures, operate independent runtimes, maintain alternative versions of the language, and reject future shared updates.

Forkability is therefore not merely a governance mechanism. It is an information-preservation mechanism. A disagreement about the correct shared language should be capable of producing two systems rather than forcing all participants to accept one authority.

---

# 30. Diversity as Security

A network whose members all converge on the same representation loses some of the value of having multiple independent participants. High-residual nodes may contain structure that the majority does not yet recognize. Such nodes are therefore not merely inefficient members of the network; they may be information sources.

The system should distinguish between unexplained structure and useless structure. The first may be a discovery opportunity; the second may eventually be discarded. Proof-of-Compression and other validation mechanisms provide a way to make this distinction empirically rather than by majority preference alone.

---

# 31. Privacy and Security

The semantic membrane is an architectural boundary, not a complete privacy mechanism. A node can choose what structure to expose, but any exposed representation may create inference channels. Semantic expressions can leak information about the underlying model, its training data, or its private residual.

The architecture therefore separates three concerns:

1. the **membrane**, which defines what information a node is willing to expose;
2. **provenance**, which records the history and constraints associated with exposed structure;
3. **enforcement**, which determines whether those constraints are respected during storage, composition, transmission, and execution.

Because provenance is first-class, privacy policy can attach to the Crown rather than only to the private model from which it originated. Constraints on disclosure, composition, derivative structures, or exposure of residual information can travel with the Crown and become part of resulting provenance graphs. This does not make provenance itself a privacy guarantee; the protocol must still prevent unauthorized information flow, protect provenance records, and enforce inherited restrictions.

Potential security concerns include model inversion, residual inference, membership inference, capability extraction, unauthorized disclosure through composition, behavioral manipulation, poisoning, adversarial contributions, provenance forgery, control-layer capture, and malicious composition of otherwise valid Crowns. These are not hypothetical: empirical work on decentralized training specifically has shown that peer-to-peer structure alone does not confer a security advantage over centralized approaches, and can widen the attack surface instead (§40).

The same provenance mechanism provides an attachment point for non-privacy policies (usage rights, attribution, compensation, governance weight). Independent discovery, compatible re-discovery, derivative attribution, and value allocation remain protocol-design problems; provenance provides the structure on which those mechanisms can operate.

A validated Crown is not automatically a safe Crown. A circuit can be correctly represented and still be undesirable. A behavioral controller can be narrow and still be manipulated. A compression improvement can be genuine and still encode an unwanted objective. These are reasons for additional validation and enforcement, not reasons to collapse all functions back into a monolithic model.

The architectural principle is therefore:

$$
\boxed{\text{membrane} \to \text{boundary}}
\qquad
\boxed{\text{provenance} \to \text{policy}}
\qquad
\boxed{\text{enforcement} \to \text{compliance}}
$$

---

# 32. Legibility Is Not Safety

The architecture repeatedly creates more legible boundaries. That is useful. It is not sufficient.

A capability can be legible but harmful, portable but dangerous, interpretable but strategically deceptive, behaviorally controlled but still capable of exerting influence, or compressive but undesirable. The system should therefore distinguish

$$
\text{legibility} \neq \text{verification} \neq \text{safety}.
$$

The objective is to make these properties independently testable. A system that exposes its failure modes is easier to govern than one that hides them, but exposure alone does not make the system benign.

The membrane's natural throttle on how fast self-generated improvement can compound into shared capability (§13) deserves the same caution. It is a real feature of the architecture, not a designed safety mechanism, and it should not be mistaken for one: it constrains only the portion of a system's development that seeks to become externally shared and interoperable. A node's private, internal capability growth is not slowed by it at all, and a sufficiently resourced or motivated actor could pursue improvement that never touches the membrane.

This is one instance of a broader discipline the architecture tries to hold throughout, not a one-off caveat: properties that sound like synonyms for "good" are kept separately testable rather than collapsed into one another. Legible is not safe. Efficient is not clear (§10). Compressive is not correct. Each pairing marks a place where optimizing for the measurable half could silently stand in for the harder, unmeasured half — and where it does, the architecture's job is to keep both halves visible rather than let the easy one quietly become the definition of the hard one.

---

# 33. Research Hypotheses

The engineering architecture does not depend on the strongest theoretical claims in this section. These claims are research hypotheses.

**H1. Relational primacy.**  
Much of the useful latent structure of a trained network is relational rather than pointwise. An autoencoder constrained to preserve relations may expose symmetries, equivalence classes, compositional structures, and semantic directions that ordinary reconstruction does not represent efficiently.

**H2. Generalization of relations.**  
A weak interoperability objective will cause useful relational structures to generalize beyond the examples in which they were first discovered. Recurring structures that cannot be efficiently expressed by the current language will become candidates for new shared primitives, allowing the vocabulary and calculus to evolve with the discoveries made by the network.

**H3. Compact algebraic generators.**  
The latent space will reveal a relatively small set of generative primitives with recognizable algebraic character (composition, inversion, projection or selection, routing, recursive application). The objective is not to assume an exotic mathematical structure; it is to determine whether a compact vocabulary of operations explains a substantial fraction of observed transformations.

**H4. Rich symmetry.**  
The resulting transformation algebra will exhibit non-trivial symmetry beyond ordinary permutation and scaling symmetries already known in neural parameter spaces. This is a hypothesis about empirical structure, not an architectural requirement.

**H5. Cross-domain correspondence.**  
The same or closely related primitives and symmetries will appear in recognizable form in the geometry of activations, learned capabilities, or the structure of the data. If so, the shared language may provide a common description across levels that are normally studied separately.

**H6. Data/model disentanglement.**  
Once shared algebraic structure between weights, activations, and data has been identified, part of that structure can be attributed to regularities inherited from the training data while another part reflects the network’s architecture and learning dynamics. Controlled training distributions and controlled architectures should make these components partially distinguishable. The residual after accounting for data-induced structure becomes a candidate signature of model-induced computational structure.

**H7. Functional representation.**  
If the relational interface becomes sufficiently complete, a higher-level relational representation may encode enough information about a network’s function that the raw weights become partly recoverable from, replaceable by, or compilable from that representation plus a comparatively small residual. This would transform the role of weights from primary representation into one possible compiled implementation.

**H8. Regime-effect generalization.**  
The tradeoffs attributed to the coordinating prior’s strength (§11) — that raising \(\lambda\) increases collective utility and extraction ease at the cost of local diversity, and that lowering \(\lambda\) protects sovereignty and residual novelty at the cost of slower sharing — generalize from established regularization and multi-task learning tradeoffs elsewhere in machine learning. This hypothesis is separable from H1–H7: it concerns the training dynamics of the coordination mechanism itself, not the algebraic structure of what gets coordinated. It is also the architecture’s explicit hedge against mechanistic interpretability remaining immature indefinitely — if post-hoc circuit extraction does not mature on a useful timeline, raising \(\lambda\) offers a fallback path toward externalizable structure that does not depend on that research program succeeding.

**H9. Relational sparse autoencoders.**  
Standard sparse autoencoders (SAEs) discover sparse, largely pointwise features. A relational SAE (or relational dictionary-learning objective) is constrained to preserve or reconstruct pairwise and higher-order relations, compositional structure, and transformation symmetries rather than (or in addition to) individual activations. Hypothesis: the resulting dictionary is more compact, more compositional, and more portable across independently trained models than a standard SAE dictionary of comparable size; residual after relational reconstruction concentrates on genuinely private or non-relational information. This supplies a concrete, near-term experimental bridge between existing mechanistic-interpretability tooling and the N-IR / Crown pipeline.

**H10. Attribution-driven participation.**  
Node-local authority over \(\lambda\) (§11) permits \(\lambda \to 0\) as a standing option, which raises a free-rider concern: extraction and Crown compilation carry a real compute cost, and a node can consume Crowns contributed by high-\(\lambda\) peers while contributing nothing back. The hypothesis is that pure free-riding is not a stable *long-run* strategy once provenance and repeated participation are accounted for, even without a specified settlement mechanism. Because provenance is inseparable from extracted structure (§6), a node that never externalizes anything accrues no attribution and therefore no claim on whatever royalty, governance-weight, or reputational value later comes to be attached to provenance (§36); free-riding secures access to the *existing* vocabulary but not to standing in *future* settlement built on it. This does not resolve single-shot extraction — a node can still consume once and leave — and it does not specify or require any particular settlement mechanism, which remains explicitly out of scope (§36). It predicts only that, in a repeated-interaction setting with any attribution-linked payout, sustained \(\lambda = 0\) is a worse long-run position than intermittent, low-cost participation — not that free-riding is impossible, and not that this alone is sufficient absent any enforcement (staking, slashing, reputation, or trust policy) that individual networks may choose to layer on top (§39).

None of these hypotheses is required for the system to be useful. The network can still function as a tool for extracting, registering, composing, and validating capabilities even if the strongest algebraic interpretation proves false.

---

# 34. A More Conservative Interpretation

The strongest version of this architecture imagines that machine intelligence ultimately becomes expressible through a compact shared relational language. A more conservative interpretation is already useful.

Suppose the hoped-for algebra does not appear. Suppose useful structure is messy. Suppose the vocabulary is large. Suppose many capabilities require substantial residual information. The system can still provide tools for neural circuit extraction, portable intermediate representations, independently validated capabilities, model-agnostic behavioral control, reusable behavioral interfaces, decentralized capability registries, compression-based contribution evaluation, local model sovereignty, and forkable shared infrastructure.

In other words, the ambitious research program is an opportunity, not a dependency. The architecture is valuable even if the universe refuses to be elegant.

---

# 35. The Network as a Shared Compiler

The deepest systems interpretation is therefore not “a network of models.” It is a network of compilers continuously growing a shared computational language that is already continuous with human language.

Each node performs two related operations. It compiles private computation upward into portable structure. The network compiles accumulated structure downward into new capabilities. Humans participate in both directions. The loop is

$$
\text{private computation} \to \text{structure} \to \text{shared language} \to \text{composition} \to \text{new capability}.
$$

The shared language becomes an intermediate language between independently developed machine intelligences and between machines and humans. A model can remain sovereign because its internals do not need to become network-wide state. A capability can become collective because its useful structure can cross the membrane.

---

# 36. Economic Consequences

Because Crowns carry first-class provenance, contribution to the network need not be attributed only through ownership of the model from which a capability originated — discovery, validation, transformation, composition, implementation, and maintenance can each be recorded as distinct events in a provenance graph. First-class provenance therefore creates a substrate on which attribution, licensing, usage rights, and other economic or governance mechanisms could later operate. The architectural claim here is narrow and deliberately so: this document does not propose or defend any particular economic mechanism; it only notes that a portable, provenance-tracked unit of capability makes such mechanisms possible to design later, rather than requiring ownership of a single monolithic model to remain the only unit of value.

The same substrate applies equally to corpus Roots and to extracted Crowns. A synthesized result — a proof, an image, a design — can surface both the circuits it invoked and the Root lineages those circuits ultimately rest on. Provenance claims attached at ingestion can already carry the terms under which the data was offered, including requests or conditions that contributors be named, notified, or compensated when downstream results depend on abilities learned from their work. A machine-assisted proof that draws on structure whose Roots belong to particular mathematicians, and that later receives major recognition, would therefore carry inspectable claims rather than requiring forensic reconstruction after the fact. Whether those claims are treated as polite requests, contractual conditions, or something enforceable is a policy and settlement question left open here; the architectural claim is only that the claims travel with the structure so that any later mechanism has a first-class object to act on.

---

# 37. Minimal Falsifiable Experiment

The engineering program below (§38) is a multi-year sequence. Before committing to it, the central thesis can be tested much more cheaply, without invoking the full Ego/Metatron architecture, economics, or governance machinery.

The experiment tests two claims in sequence:
- that relational structure of the proposed kind is recoverable inside a single model when weakly seeded by a coordinating-prior-style signal — not that it emerges spontaneously without any such pressure (Phase 0);
- that the recovered structure can be made portable across independently trained models and yields measurable compression advantage when shared (Phase 1).

**Phase 0 — Seeded recoverability with ground-truth relational structure and compression measurement.**

1. Choose two (or more) narrow but compositional domains that share latent relational structure. Concrete candidates: short structured narratives; simple procedural traces; small chemical reaction sequences; toy programs with hierarchical composition. The domains should be rich enough that hierarchical composition is natural, yet small enough that a human can fully annotate an optimal relational representation.
2. For each domain, manually construct an *optimal relational representation* using the six provisional categories (or a simplified subset if the domain does not exercise all six). Higher-order units (arcs, templates, procedures) are built explicitly as validated Merge-compositions of lower units. Whatever is deliberately left unannotated is labeled residual by construction; the experimenter — not the model — decides in advance what counts as residual. This hand-built annotation is the ground truth. It is never given to the model as a target output; it is used only to construct an auxiliary training signal and to evaluate afterward.
3. Train a separate model on each domain with a coordinating-prior-style auxiliary objective (weak \(\lambda\)) that nudges, without hard-supervising, intermediate activations toward linear separability and compositional consistency along the hand-built relational axes.
4. After training, use standard probing and circuit-localization techniques to check:
   - whether each hand-built category is linearly decodable from some subspace of the model’s activations;
   - whether the subspaces compose the way Merge predicts (is a higher-level representation approximately a consistent function of its child representations);
   - whether residual activation variance — the part uncorrelated with any hand-built category — concentrates on exactly the information the experimenter deliberately left unannotated.
5. **Cross-domain structural overlap / compression measurement.** Where the extracted relational structure from domain A is isomorphic or near-isomorphic to structure from domain B, measure the compression advantage obtained by sharing that structure versus keeping two independent representations. Quantify \(\Delta C\) in bits, parameter efficiency, or prediction cost on held-out data from both domains. This is a concrete, controlled instantiation of Proof-of-Compression: shared relational structure that is useful across domains should reduce collective representation cost.
6. Controls (required before trusting any positive result):
   - identical pipeline with \(\lambda = 0\);
   - identical pipeline with the six categories replaced by an arbitrary, meaningless six-way relabeling of the same data;
   - pure reconstruction baseline without relational pressure.
   A result counts as evidence for the partition only if it recovers more cleanly than the scrambled control under matched training pressure, and only if cross-domain overlap produces measurable compression advantage beyond the controls. These controls are what distinguish this experiment from simply training a model toward a hand-built representation and then confirming that representation is recoverable: recovery must exceed what an arbitrary, equally-strong but meaningless relabeling achieves under the same training pressure.

Phase 0 is inexpensive, fully falsifiable, and — because the target representation is known in advance — does not depend on the extraction and probing tools already being trustworthy; it calibrates them. It tests whether the proposed structure is learnable and locatable inside individual models, and whether overlapping structure yields compression. It does **not** yet test portability across independently trained models.

**Phase 1 — Portability across independently trained models.**

7. Extract the Crown(s) (or shared relational substructures) discovered in Phase 0 and compile them into an independent, model-agnostic implementation via a minimal N-IR pipeline.
8. Give that implementation to a second model — trained independently on the same or the paired domain, with no coordinating prior and no exposure to the hand-built annotation — and test whether it can invoke the extracted capability through the common interface.
9. Compare four conditions: the original capability inside model A, the capability as extracted, the independently compiled implementation, and a random or control circuit of matched complexity. Measure transfer accuracy, robustness under perturbation, extraction cost, information leakage beyond the stated functional contract, and any additional compression advantage obtained by the receiving model.

If Phase 0 succeeds and Phase 1 fails, the manifesto’s engineering claims (tier 1) are already in trouble even if the six-category taxonomy is fine — that failure mode is informative on its own. If both succeed, the central thesis — that useful structure can be made portable without synchronizing models at the weight level, and that shared relational structure produces collective compression advantage — has direct experimental support, independent of whether the stronger relational-algebra hypotheses (§33) or the full Ego/Metatron architecture hold up at all.

A natural near-term variant replaces or augments the hand-built auxiliary signal with a relational sparse autoencoder (H9) and asks whether the resulting dictionary is more portable and more compressive than a standard SAE dictionary of comparable size.

---

# 38. Engineering Program

The system is developed as an engineering problem, not a blueprint to be executed in order. At each step the goal is a minimal implementation sufficient to test the next claim, followed by a decision — extend, revise, or abandon — rather than a prior commitment to build out a fixed architecture. Section 37's experiment is the template for this posture: cheap, falsifiable, run before the more expensive version is built. The same discipline applies throughout, not only at the outset. Governance, provenance, privacy enforcement, and forkability surfaces are built alongside whichever milestone is active, not deferred to the end.

**Milestone 1: Bootstrap the network**

Two tracks proceed in parallel. Neither requires the coordinating prior yet — \(\lambda\) has nothing to bias toward until there is a shared interface and a training objective to bias with respect to (Track B, below).

*Track A — Membrane and Roots Network.* This is the network's first reason to exist and its first source of participants.
- Define the relational canonicalization scheme used for labeling and indexing contributed structure (the six primitives, §7, as an intuitive prior for contributors rather than a claimed final ontology, §1).
- Define the protocol layer: incentives, trust tiers, adversarial resistance, and any settlement mechanism — as a concrete instantiation to be tested and revised, in the same spirit as §37's experiment rather than as a commitment fixed ahead of evidence (§36 deliberately leaves the general mechanism open; this is one candidate, not the specification).
- The initial membrane is simply the language contributors already use to describe what they submit; the initial telemetry is search queries converging on the same targets. Rich structure-addressable search and retrieval is the first value the network offers back — before any Crown has been extracted, and before the marketplace exists to sell into.
- The first commercial surface follows directly from provenance already being first-class (§6, §9): a marketplace for well-provenanced, semantically-indexed — "hygienic" — training data.
- Build labeling, taxonomy, and membrane-management tooling, or well-specified APIs that let the network build its own.

*Track B — Structure/residual container.* A parallel, independently substantial project: a durable predictive model plus the residual required to reconstruct the original, spanning a range of modalities and formats.
- §37's Phase 0–1 experiment does not require this container to run at small scale — a hand-built representation and a minimal N-IR pipeline suffice. The container becomes necessary to *scale* the test across a large, heterogeneous corpus, which is why this track can run alongside Track A rather than after it.
- This is the point at which the coordinating prior turns on: once a model is being trained toward the compression objective (§37, Phase 0, step 3), \(\lambda\) is the mechanism nudging its activations toward the compositional structure the container is meant to capture. Its scope is this training step specifically, not the network at large.
- A successful container yields compression across large corpora — useful directly for storage and archival — and doubles as an early investment in the network's long-term capability, since the structure being exchanged now is the same structure Milestone 2 will later need to extract, contract, and register. Proof-of-Compression (§12), validated here, becomes the basis for trustless scale-out later.

**Milestone 2: Crowns-down tooling**

With a membrane and a corpus in place, the network starts compiling accumulated structure back downward (§35).
- Build activation tracing, intervention, and subgraph isolation tooling — or well-specified APIs/protocols so the network can build its own.
- Build the registry for validated capabilities, contracts, and policies.
- The third value-add is the base model's own utility as control surfaces mature and inference becomes more composable: the differentiator is a compiler workflow supporting local and batch execution, not merely a helpful-assistant interface. As this becomes competitive, the next commercial surface is public inference APIs.

**Milestone 3: Substrate independence**

Milestone 2 still requires the originating model at runtime. Milestone 3 is the shift to executing independently validated circuits directly.
- N-IR and portable-circuit work resumes here at a different goal: hardware independence, and independence from any single originating model's weights (§4, §6 — core dependencies as separately reproducible artifacts, not hidden calls back into a model's interior).
- This is the actual prerequisite for behavioral control to mean anything: there has to be a composed execution graph to govern, not just one opaque model's activations to observe from outside.
- Only once that substrate exists do the Ego/Subconscious split and the Metatron pattern become load-bearing (§18–19, §21) — behavioral control layered on a substrate built to be controlled, rather than bolted onto an opaque generative model.

The relational research program (H1–H10, §33) runs throughout, independently of production commitments, and can confirm, weaken, or redirect any of the above without invalidating the milestones already shipped.

---

# 39. Open Questions

Several questions remain fundamental.

- **Representation.** What is the smallest useful N-IR that can express computational structure across substantially different neural architectures?
- **Extraction.** How reliably can functional circuits be isolated from opaque models? How does extraction cost change across the \(\lambda\) spectrum?
- **Validation.** Which properties of a Crown can be tested independently, and which require execution in the originating model?
- **Compression.** What compression objectives best measure useful generalization rather than superficial redundancy? How can Proof-of-Compression be made computationally efficient at network scale (sampling, zero-knowledge arguments, staking/slashing, or other mechanisms) while preserving the integrity of the held-out test?
- **Corroboration and disputed provenance.** How much weight should independent re-discovery of an already-registered canonical Crown (§6, §12) earn relative to the original submission? Separately, when two nodes hold competing provenance claims over the same canonical form — including a claim that a public version was lifted from a private one — the network can only make both claims visible to each other; it has no mechanism to adjudicate which is true. Resolving such disputes is a matter for bilateral trust relationships and node-level policy, not a protocol function.
- **Registry retention.** Once a provenance history is compacted (§6), who is obligated to retain the inclusion proofs needed to re-expand a specific claim — the original claimant, a designated archival Roots operator, some redundancy requirement across several parties — and what happens to a claim if no one retains it? This is a distinct question from *whether* compaction preserves attribution in principle; it is about who bears the cost of making that principle enforceable in a specific dispute.
- **Language evolution.** How should new primitives be proposed, compared, merged, deprecated, or forked? How should human interpretive adaptations be recorded and weighted relative to machine-extracted structure?
- **Coordination.** How weak can the coordinating prior be while still producing meaningful interoperability? How should nodes decide when to raise or lower \(\lambda\)? Relatedly: does attribution-linked incentive alone (H8, H10) suffice to make sustained participation a rational choice, or does the network need staking, slashing, or reputation mechanisms layered on top to make sustained \(\lambda = 0\) free-riding costly rather than merely unrewarded?
- **Privacy.** How much useful structure can cross the semantic membrane without exposing unacceptable residual information?
- **Behavioral control.** How can a narrow controller remain narrow under sustained optimization? Specifically: is the Root/Heart/Move/Merge subalgebra available to the Ego (§18, §19) expressively complete enough to compose a meta-interpreter or optimization loop that steers Vision/Voice outputs indirectly, without any single operation crossing the categorical restriction — and if so, does that constitute a violation of the restriction or a limit on what the restriction was ever claiming to prevent? Any monitor built to detect this composes trust in the monitor itself, which is not a problem this document claims to solve. The restriction narrows what must be trusted; it does not remove the need to trust it. The choice this leaves an implementer is the one stated in §19: **trust the specific control-layer implementation under its own trust policy, or decline to route the capability through an Ego at all.**
- **Asymmetric mediation.** What properties must a Metatron-like intermediary have to resist rapid capture without becoming an unrestricted controller itself?
- **Governance.** How should network-level decisions balance local sovereignty, collective utility, and preservation of diversity, including explicit management of the \(\lambda\) regimes under node-local authority?
- **Functional completeness.** At what point does the shared representation become sufficient to reproduce a capability without the original model?
- **Relational dictionaries.** Do relational sparse autoencoders (H9) yield more portable and more compressive features than standard SAEs under matched capacity?
- **Human–machine co-evolution.** What interface patterns best support rapid, high-quality human interpretation and adaptation of machine-coined structure at the membrane?

These questions define the research frontier of the system.

---

# 40. Related Work and Differentiation

The architecture sits at the intersection of several existing lines of work and differs from each in a precise way.

- **Federated learning and model merging.** These approaches primarily synchronize or average parameters / gradients. The present system treats models as private substrates and shares portable structure instead.
- **Mechanistic interpretability and circuit discovery.** The N-IR / Crown pipeline is a direct consumer of progress in this area. Elhage et al. (2021, "A Mathematical Framework for Transformer Circuits," transformer-circuits.pub) provide the theoretical basis for treating a transformer as a composition of discrete, addressable sub-circuits rather than an undifferentiated whole; Wang et al. (arXiv:2211.00593, 2022) demonstrate the practice, extracting and validating a specific circuit responsible for indirect object identification in GPT-2 Small. Together they support the premise that circuits are there to be found and named, not merely posited. The architecture adds the requirement that extracted structure be portable, contract-bearing, and evaluable by Proof-of-Compression across independently trained nodes.
- **Symbolic approximation of neural representations.** McCoy, Soulos, Linzen, and Smolensky (arXiv:2608.29530, 2026) show that the internal vector representations of a range of neural networks — including LLMs across arithmetic, logic, code, and language — can be closely approximated by explicit symbolic structures with behavior largely preserved, and that targeted interventions on those structures reliably change model behavior. This is direct empirical support for the extractability premise this architecture assumes: that opaque computation has recoverable, causally load-bearing structure. Their approximations are analytical artifacts describing a single model's representations; the present system additionally requires that such structure be made portable across independently trained nodes, contract-bearing, and subject to network-level validation (Proof-of-Compression) before it earns standing as shared vocabulary.
- **Sparse autoencoders.** Standard SAEs are a natural starting tool. Bricken et al. (2023, "Towards Monosemanticity," transformer-circuits.pub) provide the foundational dictionary-learning methodology this rests on, decomposing model activations into more monosemantic features than the raw basis exposes. Hypothesis H9 proposes a relational variant explicitly optimized for the interoperability and compression goals of this system.
- **Capability-based security and object-capability systems.** Crowns with first-class provenance and contracts are a machine-intelligence analogue of capability objects; the semantic membrane is the boundary across which capabilities are introduced.
- **Modular architectures and reusable capability modules.** Houlsby et al. (arXiv:1902.00751, 2019) introduce adapters — small, parameter-efficient modules inserted into a frozen network to grant it a new capability without retraining the whole model. Pfeiffer et al. (arXiv:2007.07779, 2020) build on this with AdapterHub, a shared repository through which such modules are published, discovered, and composed across tasks and users — an existing, working precedent for a registry of portable capability modules. Both differ from Crowns in origin rather than in shape: an adapter is trained in, purpose-built for a target task from the start; a Crown is extracted post-hoc from structure a network already learned for its own reasons, then made portable, contract-bearing, and subject to network-level validation (Proof-of-Compression, §12) before it earns standing as shared vocabulary. Adapters answer "how do I add a capability cheaply"; Crowns additionally answer "how do I know a capability I didn't build is trustworthy enough to depend on."
- **Multi-agent and peer-to-peer AI systems.** Most existing designs still exchange prompts, embeddings, or fine-tuned weights. Bellet, Guerraoui, Taziki, and Tommasi (arXiv:1705.08435, 2017) give a concrete instance of this pattern: a fully decentralized, asynchronous peer-to-peer protocol for personalized model learning, made differentially private by adding calibrated noise to the parameters exchanged between peers, with a formal analysis of the resulting privacy/utility trade-off. It is peer-to-peer and privacy-aware in exactly the sense this architecture cares about, but the unit that crosses the wire is still parameter or gradient information — privacy is protected by noising *what* is exchanged, not by changing *what kind of thing* is exchanged. The claim here is that a shared external language of validated structure is a more scalable interoperability surface, and one that can protect privacy by construction (§31, via provenance and membrane policy) rather than by calibrated noise addition alone.
- **Security of decentralized training specifically.** Pasquini, Raynal, and Troncoso (arXiv:2205.08443; IEEE S&P 2023) give the same claim empirical teeth. They show that peer-to-peer decentralized training of the kind above does not, in practice, offer a security advantage over centralized federated learning — decentralization can widen the attack surface, exposing gradient-inversion attacks and, for an active adversary, letting one peer gain meaningful control over another's local model, with privacy-preserving configurations requiring a fully-connected topology that erases the practical benefit of decentralizing at all. This is direct evidence for a position §31 already takes on its own terms: peer-to-peer structure is not, by itself, a privacy or security property. Which peers hold a copy is not what does the protective work — what crosses the boundary is. That is why this architecture's unit of exchange is validated, provenance-bearing structure rather than raw parameters or gradients: the caution above applies most directly to systems where the thing peers exchange is the model itself.
- **AI safety and control.** The Ego / Subconscious split and Metatron pattern are offered as architectural control surfaces, not as solutions to the full alignment problem. They change failure modes and create independently testable interfaces; they do not claim to eliminate risk.
- **Language evolution and human–AI co-creation.** Foerster et al. (arXiv:1605.06676, 2016) show that independent deep-network agents, given a shared task and a channel, will develop their own discrete communication protocol without one being imposed — direct precedent for the claim that a weak interoperability pressure (§11's coordinating prior) can produce a shared code rather than requiring one to be hand-specified. Lazaridou and Baroni's survey of the subsequent decade (arXiv:2006.02419, 2020) is a useful counterweight: emergent protocols of this kind reliably solve the narrow task they were pressured to solve, but do not reliably generalize, remain human-legible, or carry recognizable semantics without additional grounding pressure — exactly the gap this document's framing of the shared computational language as a living superset of human language, grown through joint human and machine activity at the membrane (§9), is meant to address by keeping humans and hygiene work in the loop rather than leaving emergence purely to machine-to-machine pressure.
- **Minimum description length and compression as evidence of validity.** Hinton and van Camp ("Keeping the Neural Network Simple by Minimizing the Description Length of the Weights," COLT 1993 — predates arXiv) originate the argument Proof-of-Compression (§12) leans on: that a representation's ability to compress data is evidence of its structural validity and a driver of generalization, not merely a measure of storage efficiency. Proof-of-Compression is a network-level, multi-party instantiation of that single-model intuition — the open questions are in the protocol for measuring \(C\) across independently trained nodes (§12), not in the underlying premise that compression and validity are connected.
- **Kolmogorov structure functions and model selection.** Kolmogorov proposed the structure function in a 1974 lecture, sketching a non-probabilistic, two-part-code approach to model selection: split a datum's description into a model and the residual needed to specify the datum within that model. Vereshchagin & Vitányi (arXiv:cs/0204037, 2004) give this proposal its rigorous algorithmic-statistics treatment, formalizing the structure function and proving its equivalence to the algorithmic minimal sufficient statistic. The structure/residual decomposition used here continues that tradition and inherits its non-probabilistic foundation for two-part MDL model selection.

---

# 41. Conclusion

A peer-to-peer machine-intelligence system does not require independently trained models to become identical. It requires them to become **interoperable at the level of useful structure**.

The proposed architecture establishes that boundary through a semantic membrane. A tunable, node-local coordinating prior creates pressure for useful discoveries to become externally expressible without forcing internal convergence (§11), and Proof-of-Compression evaluates whether those discoveries improve collective representation (§12), with a concrete low-cost test in §37.

A Neural Intermediate Representation lets learned computation be excavated, compiled, and transported across a spectrum of independence — full, partial, or core-dependent (§4). Crowns give validated capabilities a registered, addressable form with first-class provenance; independent rediscoveries retain separate attribution, with compaction permitted but silent deduplication forbidden (§6).

The same shared computational language — a living superset of human language — is where these capabilities compose and where humans and machines coin and adapt vocabulary together. Even before much composition occurs, the underlying corpus is already valuable: a decentralized, provenance-tracked store indexed not only by rights but by first-party descriptions grounded in a shared ontology of thought. We call this the Roots Network (§9).

Behavioral control adds a further layer. The Subconscious performs high-dimensional generation; the Ego operates as a restricted harmonic that is denied Vision and Voice at every depth of composition (§18, §19). Asymmetric mediation (Metatron) constrains control by fixing capacity to a single purpose rather than installing a more privileged controller (§21).

Because the system is peer-to-peer, governance, residual privacy, and forkability are first-class from the start. Because provenance travels through the same compilation that produces a Crown, attribution is more than a policy goal here: the architecture yields a practical form of introspection — an account of the structures of thought, behaviors, and source material an inference drew on, with attribution and compensation claims intact (§6, §36). Humans participate directly at the membrane — curating data roots-up and interpreting machine-coined terms crowns-down.

The same first-class surfaces happen to sit next to markets that already exist. A provenance-tracked, compression-validated corpus is the kind of hygienic training data frontier labs have been licensing at scale. A compiler workflow that turns validated structure into locally executable, controllable capabilities competes in the inference market once the substrate-independent execution layer of Milestone 3 (§38) is stable. Neither observation is a business plan; both are reasons the early milestones are not purely speculative. The architecture does not need a new market; it needs to make the existing ones interoperable under residual privacy, attribution, and forkability constraints that centralized models do not provide.

Most trained networks were never pushed toward legibility, so skepticism about clean structure waiting inside them is well-founded — and the sharper version of that skepticism holds for a reason beyond immature tooling: relentless optimization has no particular reason to stop at circuits a human would recognize as intelligent, rather than sailing past them toward whatever is merely optimal. That skepticism is aimed at the wrong target here, not because the risk is imaginary but because the architecture treats it as a design constraint rather than an afterthought. The membrane, the coordinating prior, and the ontologically-aligned corpus are training-time pressure — a spring, not a lens — toward the structure this document seeks, applied before extraction rather than hoped for afterward. That pressure carries more weight for this network specifically: because provenance is first-class, the Roots Network cannot accumulate the frontier-lab volumes of unlabeled data that let scale alone out-compete idiosyncratic, low-generalization solutions elsewhere (§9, §11). Whether the pressure succeeds is exactly what H8 and H10 (§33) test — a reason the search has better odds than blind interpretability, not a claim that it has already succeeded.

None of these mechanisms makes a machine intelligent, transparent, safe, or decentralized by declaration — that would be exactly the kind of collapse the architecture tries to resist throughout: legible standing in for safe, efficient standing in for clear, compressive standing in for correct (§10, §11, §32). What the architecture establishes instead is boundaries within which those properties stay separable, so each can be measured and developed on its own terms rather than assumed from its neighbor.

What that leaves room for is machine intelligence organized as a peer-to-peer computational substrate — models remaining local, capabilities becoming portable, and the shared language of intelligence grown jointly by its human and machine participants.