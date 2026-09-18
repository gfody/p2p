# The Pressure

## A Coordinating Prior for Grounded Compositional Machine Intelligence

### Abstract

Modern neural networks are optimized primarily for behavioral objectives. They are rewarded for producing the right outputs, but the objective generally places little direct pressure on *how* the computation responsible for those outputs is organized. Consequently, a system may acquire useful abstractions without making those abstractions explicit, reusable, compositional, or externally legible.

This paper proposes a complementary training principle: a **coordinating prior** that creates persistent pressure for learned computation to organize around a shared **semantic membrane**.

The semantic membrane is a provenance-aware relational substrate representing grounded structure and its relations. It is not a fixed ontology and does not require participating models to share an internal representation. It begins with human-grounded semantic structure, but remains open to extension by machine-discovered abstractions that acquire sufficient evidence and provenance to become shared structure.

The central hypothesis is that persistent pressure toward this substrate changes the computational ecology produced by learning. Rather than merely discovering whatever implementation minimizes the behavioral objective, models may increasingly favor reusable computational structures that can be composed from previously established structures, while preserving instance-specific information as residual rather than forcing it into an impoverished shared representation.

Two principal hypotheses follow. First, **compositional pressure** should increase the reuse of learned computational structures and reduce the effective description cost of new capabilities. Second, **grounded evolution** should cause newly learned abstractions to retain finite, inspectable provenance to existing semantic structures while allowing genuinely novel structure to extend the shared membrane.

The proposal does not assume that neural networks are naturally transparent, that all useful structure is already present in pretrained weights, or that a human ontology should constrain machine intelligence permanently. It instead asks whether the learning process itself can be given a different attractor: one in which useful computation tends to become grounded, compositional, reusable, and increasingly expressible in a shared language.

The larger architecture uses this pressure to support interoperable computation between independently operated systems. This paper isolates the learning question beneath that architecture: **what pressure would make useful learned computation want to become structure?**

---

# 1. Why Learned Computation Has an Organization Problem

A neural network is ordinarily described by its parameters and its input-output behavior: a model $f_\theta(x) = y$, with parameters $\theta$ trained by minimizing an objective such as $\theta^* = \arg\min_\theta L(f_\theta(x), y)$. That objective determines what behavior is rewarded, but it does not, by itself, determine the internal computation that produces the behavior.

Many parameter configurations can implement approximately the same function, and — more importantly — many computational organizations can produce similar behavioral performance while differing substantially in reuse of internal structures, modularity, compositionality, semantic correspondence, causal accessibility, provenance, interpretability, and portability. Behavioral equivalence, in other words, does not imply computational equivalence. A model may learn a useful abstraction without representing it in a way that another process can identify as an abstraction; it may distribute a single capability across many circuits, represent several concepts in entangled form, duplicate a computation that could have been reused, or discover a highly efficient implementation whose relationship to human descriptions is difficult to recover. None of these outcomes necessarily harms the training objective — which is exactly the problem this paper addresses.

The question is not simply whether a model can learn a capability. It is what determines the computational organization in which that capability is learned. If the training objective leaves that organization largely unconstrained, the system has little reason to converge toward the kind of reusable structure a network needs once capabilities must be inspected, composed, transferred, and independently validated. The proposal of this paper is that organization can itself become an object of optimization.

---

# 2. Language as an Existence Proof for Reusable Structure

Human language is an unusual computational artifact. It is redundant, ambiguous, and heavily dependent on context; it carries idioms, metaphors, irregularities, and historical accidents, and it tolerates multiple competing descriptions of the same thing — properties that would look like defects in a purely formal communication system. And yet alongside those properties sits an extraordinary capability: language lets finite systems, human minds, construct, transmit, recombine, and recognize an effectively unbounded space of meanings.

One interpretation is that these properties are not arbitrary. They are consequences of the pressures under which language evolved and continues to operate — limited bandwidth, incomplete information, noisy observation, differing perspectives, uncertain inference, social coordination, embodied experience, and the need to communicate structures that cannot be transmitted directly. Under those pressures, a system that insisted on a fresh, independent representation for every situation would collapse under its own cost. Language survives by making structure reusable instead: a finite vocabulary generates an effectively enormous space of expressions, because a word does not need to encode every situation in which it can occur — its meaning arises through relation to other structures and through composition. Language is therefore an existence proof for an important possibility: **a representation system can become extraordinarily expressive by making structure reusable rather than representing every instance independently.**

The same logic applies to learned computation. If $C_1$ is an established capability and $\Delta$ is some transformation or additional structure, a new capability can be represented as $C_2 = \operatorname{compose}(C_1, \Delta)$ — reusing what already exists — or it can be learned as a largely independent computation, in which structure that already exists gets rediscovered from scratch. Both strategies can produce similar behavioral results, but their computational economies are very different, and the difference compounds as capability grows: if every new capability requires a new opaque implementation, the description complexity of the system continues to grow roughly with the number of capabilities; if new capabilities can increasingly be expressed as compositions of existing structures, the marginal cost of additional capability can instead decrease. The hypothesis of this paper is therefore not that intelligence is modular in some fixed biological sense. It is that persistent pressure for compositional reuse may cause learning to discover a more compositional computational organization — the way pressure on a communicating species discovered one.

---

# 3. Structure and Residual

Architecture.md establishes residual as the necessary counterpart to shared structure: not noise, but information the current representation doesn't yet explain, which has to stay available for future discovery rather than be treated as an error to eliminate (§3 there).

This paper needs a finer-grained version of that idea. Represent an observation or computational object $x$ conceptually as

$$
x = (S_x, R_x, \epsilon_x, P_x),
$$

where $S_x$ is structure that has been identified as reusable, $R_x$ is the relational organization giving that structure meaning and context, $\epsilon_x$ is residual information not currently explained by the shared representation, and $P_x$ is provenance. This is not a literal decomposition of a neural tensor — it is a conceptual decomposition of information, useful for reasoning about where cost is paid.

Agreement across independent observations is evidence that some structure may be shared; disagreement is evidence that something differs, and neither should be discarded automatically. If multiple independent observations can be explained by the same structure, representing that structure once may reduce collective description complexity. If a phenomenon consistently fails to fit the current shared representation, the unexplained residual may itself become evidence for extending the representation — a dynamic relation of residual $\rightarrow$ candidate structure $\rightarrow$ shared structure, while still preserving the possibility that some residual remains permanently local. Shared structure should be paid for once; residual variation should be paid for locally.

---

# 4. The Semantic Membrane

The **semantic membrane** is the shared surface between private computation and shared structure — the same boundary architecture.md defines (§10 there), between a node's private computational interior and the shared external language, on the principle that internal representations may diverge while external representations converge. It should not be understood as a conventional ontology or vocabulary; it is better understood as a persistent, relational, provenance-aware decomposition of observations and meanings, recording structures together with their relations, contexts, provenance, transformations, perspectives, validation history, and their relationship to residual information.

That record gives learned computation a reference frame against which it can become legible without requiring every participating model to become internally identical. Two models can implement the same concept — DOG, say — through two different internal representations, $R_A \neq R_B$, and still be interoperable, because interoperability requires only that both can establish sufficient correspondence through the shared structure, not that their internal representations match. The membrane is a mechanism for semantic interoperability without internal convergence, not a demand for it.

## 4.1 Grounded Initialization

The initial membrane is grounded in human semantic labor. The Roots Network provides a foundational example of this process: contributed material is captured with first-class provenance and organized according to a semantic description rather than treated as anonymous training mass. Architecture.md describes the shared computational language this feeds into as a living superset of human language, with humans and machines both participating in its growth — humans contributing roots-up curation and crowns-down interpretation of machine-generated structure.

The consequence that matters for this paper is that a model trained under this proposal does not begin with an empty semantic universe. It begins with a substrate already containing established relationships between observations, structures, and meanings — and the proposal is stronger than simply adding semantic labels to a training set. The hypothesis concerns the initial *computational substrate* itself, not an annotation layer alongside it. If semantic structure exists only in external annotation, the model may learn it merely as another prediction target; if it is represented in the computational substrate available to learning, it becomes a possible building material for subsequent computation instead.

---

# 5. The Membrane Learns Too

Grounding must not become freezing. A human-grounded semantic substrate is useful precisely because it provides a place from which further structure can be discovered, which means the membrane has to be allowed to evolve — $M_0 \rightarrow M_1 \rightarrow M_2 \rightarrow \cdots$ — where each $M_t$ contains the structure established up to that point in the system's development, and machine learning participates directly in extending it.

A model may discover a regularity that was not previously represented. Initially that regularity exists only as internal computation or residual structure; it may then become a candidate abstraction, a named or otherwise addressable structure, a structure with recorded provenance, a validated addition to the membrane, and finally a reusable component for subsequent learning. Conceptually, a new structure $m' = \operatorname{compose}(m_1, \ldots, m_k)$ may arise from existing structures — but machine discovery need not always be compositional in this sense, and a genuinely novel primitive may emerge as well. The requirement is not that every new abstraction reduce to an existing human category. It is that its emergence remain traceable: grounding means grounded *extension*, not fidelity to a frozen ontology. The goal is not to force machine intelligence to remain inside the concepts humans already possess — it is to give machine discovery a grounded place from which to extend them.

---

# 6. Multiple Perspectives Are Part of the Structure

A shared semantic object need not have a single canonical interpretation. Different observers may legitimately expose different structures around the same source, and their differences need not be contradictions — they may simply occupy different relational projections of the same underlying structure.

Consider *the dress*, the 2015 photograph that produced a well-known perceptual ambiguity. A photographer attends primarily to its capture — lighting, exposure, white balance, the missing visual references that made the ambiguity possible. A culturist attends to its propagation through a social network and the resulting split in perception. Search telemetry contributes a disambiguation relation, establishing that the phrase "the dress" picks out this particular artifact rather than some other cultural object it might otherwise be confused with. None of these observations is more "real" than the others; each is a legitimate projection, and their relationship can be represented without declaring any one of them the canonical account. The semantic membrane should preserve that multiplicity rather than prematurely collapsing it — which is one reason provenance is fundamental here: it is what lets several partial, non-contradictory descriptions of the same object coexist and still compose into something richer than any one of them alone.

---

# 7. The Coordinating Prior

The semantic membrane provides the substrate; the **coordinating prior** provides the pressure. These are different mechanisms. Let $M$ denote the current semantic membrane. A conventional training objective might be written $L_{\mathrm{task}}(\theta)$; the coordinating prior adds pressure toward organization compatible with $M$:

$$
L(\theta) = L_{\mathrm{task}}(\theta) + \lambda L_{\mathrm{coord}}(\theta, M),
$$

where $\lambda$ controls the strength of the coordinating pressure. The exact form of $L_{\mathrm{coord}}$ is left as an empirical question — it might penalize semantic misalignment, reward reuse, reward short compositional descriptions, reward causal correspondence between semantic interventions and computational interventions, reward recoverability of learned structure, or operate through architectural constraints rather than an explicit scalar loss at all. What matters is not the particular mathematical form but the underlying property: the learning process is given a persistent reason to prefer computational organization that can participate in the shared semantic structure.

The prior is therefore less like a lens than a spring. A lens attempts to reveal structure that already exists; a spring changes the forces acting on the system so that different structures become more likely to develop in the first place. That distinction matters because ordinary optimization has no intrinsic reason to settle on circuits that humans would recognize as reusable semantic units — it only has reason to optimize its objective. The coordinating prior adds another pressure alongside it.

---

# 8. Pressure Works in Two Directions

The coordinating prior can operate both before and after a capability has been learned.

**Post-hoc pressure** treats a model that may already contain useful structure as something to be excavated: activation tracing, intervention, behavioral analysis, sparse decomposition, and related methods can identify candidate circuits, and the semantic membrane supplies the vocabulary in which those structures can be described. Here the pressure acts as an extraction incentive — existing computation $\rightarrow$ candidate structure $\rightarrow$ shared representation.

**Training-time pressure** is needed when extraction fails — when a model represents a capability in a form too distributed, entangled, or expensive to recover after the fact. In that case the coordinating prior has to operate during learning itself, encouraging the model toward computational organizations that are easier to relate to the membrane as it trains rather than after. This is the stronger interpretation of the proposal: interpretability stops being a purely archaeological activity performed after training and becomes, in part, something the training process arranges for in advance — creating conditions under which the structures worth excavating are more likely to exist at all.

---

# 9. Hypothesis I — Compositional Pressure

### H1

**If a model is trained under persistent pressure to preserve and reuse compositional structure represented by the semantic membrane, then increasing capability will increasingly be achieved through reuse and composition of existing computational structures rather than through accumulation of irreducibly entangled circuitry.**

The relevant quantity here is not simply parameter count — a model can have many parameters while possessing substantial reusable structure. The more informative target is effective description complexity: let $D(C)$ denote the description complexity of a capability $C$ in terms of a shared library of computational structures. If capabilities become increasingly compositional, then for a newly acquired capability $C_{n+1}$, $D(C_{n+1})$ should increasingly reflect the cost of specifying a composition of existing structures rather than the cost of specifying an independent implementation from nothing. A stronger, scaling version of the same prediction is that $\frac{dD}{dC}$ should decrease over some range of capability growth under sufficient coordinating pressure — the model exhibiting, in effect, an increasingly reusable computational vocabulary as it grows.

## 9.1 What H1 Does Not Claim

H1 does not claim that every neural circuit should become modular, that neurons correspond one-to-one with semantic concepts, or that any particular architecture is required, and it does not require identical representations across models. Nor does it claim that compression alone establishes correctness: a representation can be compact and still be wrong, a capability can be interpretable and still be unsafe, and a circuit can be reusable and still be poorly grounded. These properties have to remain experimentally separable rather than assumed to travel together.

---

# 10. Hypothesis II — Grounded Evolution

### H2

**If the semantic membrane is instantiated as part of the computational substrate and remains available as a persistent training reference, then newly learned abstractions will preferentially retain finite compositional or observational provenance to grounded semantic structures, while genuinely novel abstractions can become new shared structures rather than remaining permanently orphaned.**

The key word is *evolution*. The membrane should grow as the model grows: a new abstraction might have provenance $m' \leftarrow (m_1, m_2, \ldots, m_k)$ tracing back to established structures, or it may originate from an unexplained residual, $\epsilon \rightarrow m'$. The second case matters just as much as the first — the system has to be able to discover things the initial membrane did not contain. So the pressure should not minimize residual indiscriminately; it should make persistent, useful residual *interesting* rather than simply unwelcome.

---

# 11. No Persistent Orphan Abstractions

A useful grounding principle follows: **no persistent orphan abstractions; preserve unexplained residual as potential structure.** This distinguishes two very different situations. Unexplained residual — computation the current membrane does not explain — is entirely acceptable on its own: it may be novel, private, transient, or simply noise, and the system only needs to preserve enough information about it to make future investigation possible. A *persistent orphan abstraction* is different: a structure that becomes durable, reusable, and operationally important — repeatedly invoked — while carrying no meaningful semantic or computational provenance at all. That is the condition the coordinating prior should make increasingly expensive, and the distinction matters because it keeps grounding from turning into an anti-novelty mechanism. The system is not saying that everything unexplained is bad. It is saying that if something persists as useful structure, there should increasingly be an answer to what it is related to, where it came from, and how it was formed.

---

# 12. Grounding Is Not Internal Convergence

Grounding is not a demand that all models become internally alike — the same principle architecture.md states as why this proposal is not federated weight synchronization (§14 there). Two independently trained models can implement a shared concept through entirely different internal circuits, $C_A \neq C_B$, and still expose a common semantic correspondence, $C_A \leftrightarrow m \leftrightarrow C_B$, which is sufficient for interoperability whenever the shared structure $m$ can mediate useful composition between them. Grounding, in this sense, means provenance, correspondence, addressability, semantic relation, and causal or behavioral validation — it does not mean identical weights, neurons, representations, or architectures. That distinction is essential to a peer-to-peer architecture whose purpose is precisely to let independently operated systems remain sovereign while still making useful structure portable between them.

---

# 13. The Training-Pressure Problem

There is a practical difficulty underneath all of this. Ordinary stochastic optimization does not directly observe statements like "these parameters implement DOG," or "reuse this circuit instead of learning another copy," or "this internal abstraction should remain grounded in these semantic structures." The loss function receives predictions and gradients; it does not automatically receive an ontology of the model's own computation. This is an observability problem — to apply structural pressure at all, the system must construct some correspondence between semantic structure and computational structure, and there are several possible levels at which that correspondence can be built.

**Behavioral semantic pressure** is the simplest approach: an auxiliary objective, $L = L_{\mathrm{task}} + \lambda L_{\mathrm{semantic}}$, trains the model to predict or preserve semantic relations in addition to ordinary task behavior. This establishes whether semantic supervision changes representation at all, but not that the internal computation has become semantically organized.

**Representation pressure** goes further, asking whether semantic interventions correspond to interventions in learned representations: if a membrane operation transforms structure $m$ into $m'$, an analogous intervention in the model should produce a corresponding change in behavior or internal state. This moves beyond correlation toward structural correspondence.

**Causal pressure** is the strongest form, asking whether the identified computational structure is actually causally responsible for the behavior attributed to it. If a candidate circuit $c$ is claimed to implement semantic structure $m$, intervention on $c$ should selectively alter the behavior associated with $m$, and introducing or transforming $m$ should produce predictable computational consequences in turn — which is what prevents a semantic side channel from merely appearing interpretable while the real capability stays opaque elsewhere.

---

# 14. A Hierarchy of Semantic Pressure

The coordinating prior is best treated as a family of mechanisms rather than one fixed loss term, ordered roughly by how much the system commits to:

- **Level 1 — Semantic supervision.** Encourage representations to preserve known semantic relations.
- **Level 2 — Semantic initialization.** Instantiate semantic structures in the initial computational substrate.
- **Level 3 — Structural reuse.** Reward reuse and composition of established computational structures.
- **Level 4 — Grounding.** Reward finite provenance from learned structures to membrane structures, and preserve residual for unexplained information.
- **Level 5 — Causal correspondence.** Require candidate semantic structures to correspond to causally meaningful computation.
- **Level 6 — Structural optimization.** Allow the system to create, merge, split, retire, and promote computational structures according to their measured utility.

The research program should not assume the highest level is necessary. The first question is simpler: whether relatively ordinary optimization mechanisms, given an appropriate substrate and objective, produce the desired computational ecology at all.

---

# 15. Initialization Is Part of the Hypothesis

The phrase "initial parameter space" can be misleading. Let $\Theta$ denote the space of possible parameters and $\theta_0 \in \Theta$ the initialization; the architecture determines what functions can be represented, and the initialization determines where learning begins. But the proposal here concerns something larger than either. The relevant object is the **initial computational substrate**:

$$
\mathcal{S}_0 = (\text{architecture}, \theta_0, M_0, \text{composition mechanisms}).
$$

If the semantic membrane is present only as metadata outside the model, learning dynamics may largely ignore it. The stronger hypothesis instantiates semantic primitives and composition mechanisms directly in the initial substrate, which gives learning access to two kinds of capacity at once: **grounded capacity**, corresponding to established semantic structures, and **uncommitted capacity**, available for discovering new structure. The second is not optional. A grounded substrate with no capacity for extension is not a learning system — it is a frozen ontology.

---

# 16. The Initial Substrate

The proposed initial substrate therefore needs to contain semantic primitives or structures; relational connections between those structures; mechanisms for composition; mechanisms for representing residual information; sufficient uncommitted capacity for genuinely new abstractions; and pathways by which learned computation can be related back to semantic structure. It does not need to encode the final semantic membrane — indeed, it cannot, since the membrane is expected to evolve. The initial condition instead establishes a bias, $M_0 \rightarrow \text{learning}$, rather than merely $\text{random substrate} \rightarrow \text{learning}$. Whether that difference matters in practice is the experimental question.

---

# 17. The Semantic Membrane as a Living Reference Frame

It is worth separating two roles clearly: the membrane is the reference frame — it tells the system what established structure exists — while the coordinating prior is the pressure, determining how strongly learning is encouraged to organize around that structure. Keeping these separate lets them evolve independently: the membrane can grow on its own schedule while the pressure changes strength on its own, node by node, exactly as architecture.md's node-local $\lambda$ describes (§11 there). What matters for this paper specifically is that decoupling the reference frame from the pressure is what allows local diversity and shared structure to coexist at all, rather than trading off against each other in lockstep.

---

# 18. Proof-of-Compression as the External Test

The coordinating prior should not get to decide unilaterally which structures deserve to become shared — a model can produce an elegant-looking abstraction that provides little collective value, so structural pressure and structural validation have to remain distinct. The coordinating prior encourages the model to produce candidate structure; **Proof-of-Compression**, specified fully in architecture.md (§12 there), evaluates whether that structure actually earns a place in the shared system, on the basic principle that a candidate structure is useful if introducing it reduces the description or prediction cost of relevant held-out information: $\Delta D(s) = D_{\mathrm{without}} - D_{\mathrm{with}}$, where a positive and reproducible $\Delta D$ is evidence that the structure captures something reusable. This creates a clean division of labor between the two mechanisms this paper is built from: the coordinating prior produces candidate structure, and Proof-of-Compression supplies the evidence for whether it deserved to. Neither substitutes for the other.

---

# 19. The Membrane–Learning Loop

The complete process is a developmental loop with two passes. Forward: human grounding $\rightarrow$ semantic membrane $\rightarrow$ initial substrate $\rightarrow$ learning under pressure $\rightarrow$ learned computation. Backward: learned computation $\rightarrow$ structure + residual $\rightarrow$ candidate abstraction $\rightarrow$ validation $\rightarrow$ semantic membrane, closing the cycle. The loop has two sources of semantic growth — human observation and interpretation, and machine discovery — and two destinations for learned information — shared structure and residual. That combination is what makes this a living system rather than a one-time grounding step: ground, learn, discover, validate, share, and learn again.

---

# 20. Experimental Program

The central experiment should be designed to distinguish four effects: initialization, semantic pressure, their interaction, and ordinary task optimization alone. A factorial design provides a natural starting point:

| Condition | Semantic initialization | Coordinating pressure |
| --------- | ----------------------: | ---------------------: |
| A         |                      No |                     No |
| B         |                     Yes |                     No |
| C         |                      No |                    Yes |
| D         |                     Yes |                    Yes |

All four conditions should be trained on matched tasks and evaluated for computational organization, not only task performance.

**Reuse.** Measure how often newly learned capabilities invoke previously established structures — circuit reuse frequency, number of unique primitives used per capability, duplication of functionally equivalent circuits, composition depth, cross-task reuse. H1 predicts that pressure should increase useful reuse across these measures.

**Residual localization.** Measure where unexplained information actually ends up. A successful system should not simply force everything into the membrane: shared regularities should increasingly become shared, idiosyncratic information should stay localized, and persistent useful residual should become increasingly likely to be investigated or promoted rather than ignored. This is a more informative target than raw interpretability on its own.

**Grounding.** For each learned abstraction, estimate the length and quality of its provenance chain — for example $m' \leftarrow m_3 \leftarrow (m_1, m_2) \leftarrow \text{grounded observations}$ — measuring provenance depth, provenance completeness, the fraction of reusable abstractions that have provenance at all, the fraction of durable abstractions that remain orphaned, and the stability of provenance under further training.

**Effective description complexity.** Measure the description cost of capabilities in terms of a growing computational vocabulary. The key quantity is not $|\theta|$; it is something closer to $D(C \mid \mathcal{L})$, where $\mathcal{L}$ is the learned shared library. If H1 is correct, the marginal description cost of new capabilities should decline as $\mathcal{L}$ grows.

**Causal correspondence.** For every claimed semantic structure, test whether the associated computation is actually causally responsible for the predicted behavior, using activation patching, ablation, feature intervention, causal mediation, or counterfactual semantic transformations. The goal is to distinguish genuine computational correspondence from a semantically decorated but causally irrelevant representation.

**Membrane growth.** Track the membrane itself as a dynamic object, $M_0 \rightarrow M_1 \rightarrow \cdots \rightarrow M_t$, measuring the number of validated structures, the rate of machine-originated additions, the rate of human reinterpretation, reuse of newly promoted structures, persistence of machine-discovered structures, and the provenance quality of additions. This is the experiment that tests H2 directly.

---

# 21. What Would Falsify the Proposal?

The proposal should be considered falsifiable. Several outcomes would count against it:

1. **Semantic side-channel only.** Semantic supervision produces a clean auxiliary representation while the actual computational core remains unchanged — the pressure has not reorganized learning in the intended way.
2. **No reuse increase.** Semantic pressure produces no measurable increase in computational reuse or composition, weakening H1.
3. **No description-complexity effect.** Capabilities continue to require approximately independent descriptions despite increasing shared structure, undermining the proposed compositional scaling advantage.
4. **Provenance collapse.** Newly learned abstractions rapidly lose meaningful ancestry despite persistent pressure, weakening H2.
5. **Forced ontology.** Grounding substantially reduces the system's ability to discover genuinely novel abstractions — the substrate is acting as a restrictive ontology rather than a coordinating prior.
6. **No initialization effect.** Semantic initialization has no measurable effect beyond equivalent external supervision, weakening the claim that the initial computational substrate matters.
7. **Non-causal interpretability.** Semantic labels remain predictable, but interventions on their supposed computational counterparts fail to affect the associated behavior — the system has learned semantic correlation rather than semantic computation.
8. **Gaming.** Models learn to satisfy the coordinating objective without producing reusable, causally meaningful structure — the objective is being optimized without achieving its intended purpose.

---

# 22. Limitations

Several limitations are fundamental rather than incidental. The semantic membrane may simply encode the biases of its contributors, so grounding does not imply truth — a provenance-aware structure can still be mistaken, it just fails in a traceable way rather than an opaque one. Compression does not imply correctness either: a compact explanation can compress the wrong regularity just as easily as the right one. And neither interpretability nor compositionality imply safety on their own — a perfectly understood capability can still be harmful, and a system can compose meaningless components together extremely efficiently.

Not all computation should necessarily become shared. Privacy, specialization, novelty, and local sovereignty are all legitimate reasons for residual information to remain local rather than get absorbed into the membrane. And the appropriate *form* of the coordinating prior remains genuinely unknown — the proposal deliberately leaves open whether the useful implementation turns out to be an auxiliary loss, an architectural mechanism, an initialization scheme, a structural optimizer, or some combination of these.

Finally, the proposal does not assume that all useful structure already exists inside pretrained models. Some may be recoverable as-is; some may need to be learned differently under this pressure; some may need to be explicitly instantiated rather than discovered; and some may only emerge through direct interaction between humans and machines at the membrane.

---

# 23. Relationship to the Larger Architecture

The larger peer-to-peer architecture treats independently operated models as sovereign computational substrates and seeks to make useful learned structure portable through a shared computational language. This paper addresses the learning problem beneath that system. The division of labor is:

$$
\boxed{
\textit{The Pressure} = \text{How can learning be biased toward grounded, compositional, reusable computation?}
}
$$

while

$$
\boxed{
\textit{The Architecture} = \text{What can a network do once such computation can be exposed, validated, composed, and shared?}
}
$$

The larger architecture already specifies the surrounding mechanisms — the semantic membrane and shared computational language, N-IR and Crown representations, Proof-of-Compression, provenance, behavioral control, and peer-to-peer governance — and this paper should not re-specify those. Its purpose is narrower: to ask why the learned computation entering those mechanisms should be expected to become increasingly suitable for them in the first place. The answer proposed here is persistent pressure. Roots-up curation establishes grounded material; the semantic membrane provides the reference frame; the coordinating prior creates pressure during learning; interpretability and extraction recover candidate structures; Proof-of-Compression evaluates their collective value; the membrane grows; and the cycle repeats.

---

# 24. Discussion

The deepest claim of this proposal is not that semantic labels make models more interpretable. It is that the organization of learned computation is itself a learnable property of the training environment. A model does not merely learn a function — it learns a particular computational implementation of that function, and ordinary optimization places enormous pressure on behavioral performance while placing comparatively little pressure on whether that implementation is reusable, grounded, or externally legible. The coordinating prior introduces another pressure alongside it, one that does not dictate a single implementation so much as create an ecological preference.

If that preference succeeds, the dynamic becomes self-reinforcing: computational structures corresponding to established semantic structures become useful building blocks, their reuse becomes advantageous, new capabilities can be assembled from them, persistent unexplained residual becomes a source of discovery rather than an embarrassment, and successful discoveries can be promoted back into the shared membrane — which becomes progressively richer, providing an even richer substrate for the next round of learning. This is a positive feedback loop: more shared structure leads to more reusable building blocks, which leads to more compositional learning, which leads to more discoverable structure, which leads to more shared structure again. The opposite loop is equally possible under the wrong pressure: opaque optimization leads to entangled implementation, which leads to poor extraction, which leads to poor reuse, which leads to continued independent rediscovery of the same thing over and over. The empirical question is which of these ecologies actually emerges under different forms and strengths of pressure.

---

# 25. The Stronger Interpretation

There is a tempting, weaker interpretation of all this in which semantic grounding is primarily an interpretability technique: first train a model, then discover what its internal representations mean. The proposal here is stronger than that. It asks whether meaning can become part of the developmental environment of computation itself, which is a different research program — not $\text{learn} \rightarrow \text{interpret}$, but $\text{ground} \rightarrow \text{learn} \rightarrow \text{interpret} \rightarrow \text{validate} \rightarrow \text{extend grounding} \rightarrow \text{learn again}$. In this formulation, interpretation becomes part of learning's own feedback loop rather than something applied to a finished model afterward. The semantic language is not merely a lens brought in after the fact to inspect the model against — it becomes part of the pressure field in which the computation develops in the first place.

---

# 26. Conclusion

A neural network can be behaviorally successful without becoming computationally legible. It can learn useful capabilities without organizing them into reusable structures, discover abstractions without giving them persistent provenance, and optimize indefinitely toward solutions that are locally effective without ever having a reason to become a cooperative computational substrate.

The coordinating prior is a proposal for changing that pressure. The semantic membrane provides grounded shared structure; the initial computational substrate makes that structure available from the beginning; the coordinating prior encourages learning to build upon it; residual preserves what the current representation cannot yet explain; machine discovery can extend the membrane rather than merely consuming it; and Proof-of-Compression provides an external test for whether proposed structures actually earn their collective value. The resulting hypothesis is simple: **if useful computation is persistently pressured toward grounded, compositional, reusable structure, then the computational organization of learning should change.**

The strongest version of the proposal is not that machines should remain inside a human semantic system. It is that machines should begin from one and learn how to extend it. The membrane therefore has no final form — it is a living boundary between what has become shared and what remains to be discovered. The goal is not to freeze machine computation inside a human ontology. It is to give machine discovery a grounded place from which to extend one.
