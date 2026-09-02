# Writing style for lecture notes

## Purpose and status

This is a working guide for writing lecture notes in a style compatible with
the instructor's research writing. It is distilled from papers spanning causal
inference, experimental design, statistical modeling, choice, networks, and a
more essayistic treatment of randomness. Those papers differ by venue, period,
technical level, and coauthor group. The principles below therefore describe
recurring tendencies, not a claim that every sentence or organizational choice
is uniquely attributable to one author.

Use these principles to shape exposition, not to imitate surface phrases. This
file is the required companion to the [`Expository style`](LECTURE_SPEC.md#expository-style)
section of `LECTURE_SPEC.md`, and should be read in full whenever that
specification is used to draft or substantively revise a lecture. The lecture
notes are a different genre from research papers: they need more pauses,
connective explanation, and opportunities to check understanding.

The instruction files have distinct, cumulative roles. The lecture brief
determines lecture-specific content and emphases; `LECTURE_SPEC.md` sets the
course-wide audience, scope, rigor, and teaching constraints; and this file
guides the explanatory realization of that material. If an apparent tension
remains, the brief and `LECTURE_SPEC.md` control content and scope, but that
precedence is not permission to ignore the expository principles here.

## Central principle: deliver the intuition

Intuition is not decoration placed after the formal result. It should explain
the mechanism:

- What is the underlying problem?
- Why does the obvious or standard approach fail?
- What conceptual move addresses that failure?
- Which feature of the new method produces the claimed benefit?
- What is traded away, assumed, or left unresolved?

Whenever possible, give the reader an informal model of the argument before
asking them to process its full notation. Then return to that model after the
formal result and explain what the mathematics has added or corrected. Do not
merely label a paragraph “intuition”; supply a causal, probabilistic, geometric,
or algorithmic mechanism the reader can reason through.

## Recurring expository principles

### Begin with the problem, not the machinery

Open a topic with a recognizable scientific or statistical problem. Establish
the object of interest and the practical or conceptual difficulty before
introducing specialized notation. A definition should feel like a response to
a need already visible to the reader.

Concrete settings are useful even in theoretical passages: an A/B test with
spillovers, a rare unit carrying a very large inverse-probability weight, a
truncated preference list, or a small randomized experiment can expose the
structure of the problem without lowering the intellectual level.

### Move deliberately from informal to formal

A common and effective progression is:

1. describe the problem in ordinary language;
2. isolate the key contrast or tension;
3. introduce the mathematical objects needed to express it;
4. state the result precisely; and
5. translate the result back into the original problem.

Use phrases such as “at a high level,” “formally,” “in other words,” or
“roughly speaking” only when they mark a real change in resolution. The
informal statement should be accurate enough to survive the formalization, not
a story that the mathematics later contradicts.

### Respect the reader's order of understanding

Exposition should be cumulative. A sentence, heading, or displayed equation
may build on ideas already established, but it should not require the reader to
understand an explanation that appears later. In particular:

- do not use notation before introducing the object it denotes, even in an
  opening example or motivational table;
- do not title a subsection by a phenomenon that the notes have not yet made
  visible—for example, explain the relevant variance before asking why a
  centered quantity appears in it;
- do not begin with a generic estimator when a concrete problem can naturally
  produce it; develop the need in the example, identify the useful move, and
  only then name and generalize the construction;
- do not rely on a technical word such as “level,” “normalization,”
  “calibration,” or “balance” to carry an unexplained argument; say what is
  being held fixed, matched, normalized, or moved toward what target; and
- make transitions explain why the next object enters. A transition should do
  more than announce a new topic.

An early preview should summarize the questions and conceptual sequence in
plain language. It should not become a compressed first presentation of the
lecture's formal machinery.

### Prefer explanatory completeness to artificial brevity

When brevity conflicts with understanding, expand the exposition. Supply the
missing motivation, define the notation locally, work through the consequential
algebraic step, and interpret the result. Strategic repetition is useful when a
symbol has not appeared for several pages or when its role changes between a
finite-population and superpopulation argument.

The written notes may contain substantially more material than can be spoken in
one meeting. The 115-minute constraint selects the instructor's blackboard
route through the notes; it is not a reason to compress away connective prose
or make the reader reconstruct unstated steps. Reserve `Advanced material` for
genuinely optional extensions, not for definitions or explanations needed to
understand the main argument.

### Explain through contrasts

Many ideas become clearest when placed next to a nearby alternative:

- complete versus Bernoulli randomization;
- Horvitz-Thompson versus Hájek normalization;
- point identification versus partial identification;
- fixed versus randomized clustering;
- a standard model versus the empirical pattern it cannot express.

State what the alternatives share before identifying where they diverge.
Follow the divergence to its consequence for the estimand, bias, variance,
identification, computation, or interpretation. Avoid comparison tables that
name differences without explaining why those differences matter.

### Use examples as parts of arguments

Examples should do intellectual work. A good example can:

- make a failure mode unavoidable;
- isolate the source of a variance or bias problem;
- show why an assumption is needed;
- reveal a distinction hidden by general notation; or
- make a tradeoff numerically or geometrically visible.

Prefer small examples that can be reconstructed at the blackboard. Introduce
the example before the most abstract derivation when it can help students
predict the result. Return to it afterward to check that the formal argument
matches the initial intuition.

### Decompose complicated questions

When a problem contains several mechanisms, separate them and name them. When
a method contains several contributions, identify the distinct roles they
play. Taxonomies are valuable when the categories are genuinely explanatory,
but should not become arbitrary lists.

For a technical lecture, useful decompositions often include:

- design, identification, estimation, and inference;
- target population, estimand, estimator, and estimate;
- direct effects, spillovers, and exposure assumptions;
- assumptions needed for validity versus assumptions used for efficiency; and
- statistical guarantees versus computational or practical considerations.

### Ask genuine organizing questions

Questions can expose the intellectual stakes and organize a transition: Can a
design help when the outcome model is already sophisticated? What exactly is
learned when overlap fails? Why should a random denominator reduce variance?
Use such questions sparingly and answer them. Do not use strings of rhetorical
questions as a substitute for committing to an explanation.

### Make tradeoffs and scope explicit

Benefits are rarely free. Explain which assumption, target, or operational
choice makes a result possible. Bias-variance, precision-relevance,
robustness-efficiency, and model-design tradeoffs should be treated as part of
the main idea rather than saved for a disclaimer.

Qualify claims at the right level. Distinguish what is proved, what is suggested
by a simulation or example, and what is a plausible interpretation. State when
a result depends on a particular metric, exposure model, target population, or
asymptotic regime. A useful limitation sharpens the contribution; it does not
apologize for it.

### Use history to clarify the intellectual problem

Historical material is most effective when it shows how a question or method
arose, recovers an overlooked idea, or reveals that two literatures use related
machinery. In the lecture spine, keep this history tied to the concept being
taught. Longer chronology and additional primary-source pointers belong in
`Further reading`.

## Writing technical passages

### Definitions

Motivate an object before naming it. State its domain, inputs, and role, then
give the formal definition. Immediately say what the definition includes,
excludes, or makes observable. If two definitions are easily confused, contrast
them at once rather than hoping the notation will keep them separate.

Define symbols at first use in the local discussion. State whether each object
is a scalar, vector, set, function, random variable, or realized value whenever
that distinction matters. For vector expressions, state the dimensions or
explain the operation in words; for indicator notation, identify the event
inside the indicator. A notation table supports consistency across lectures,
but it does not replace a local introduction for the reader.

### Equations

An equation should be prepared by prose and interpreted by prose. Before a
display, tell the reader what relationship is about to be expressed. After it,
identify the term, sign, scaling, or cancellation that matters. Do not narrate
algebra that is self-explanatory, but do explain the step where the argument
turns.

For an estimating equation or balance constraint, identify the target of the
equation and what each side represents before discussing its consequences. If
an expression is vector-valued, say whether equality holds coordinate by
coordinate. When weights are adjusted, explain which sample moments they are
being made to reproduce and why reproducing those moments helps with the
estimand at hand.

### Results and proofs

State assumptions close to the result and make clear which are structural,
design-based, or regularity conditions. Before a longer proof, provide a short
road map: what representation will be used, where randomness enters, and which
identity or bound does the real work.

After the proof, translate the conclusion. Useful questions include:

- What does the rate or sign say in ordinary terms?
- Which baseline does the result improve upon?
- Which feature of the design or estimator drives the improvement?
- Does the result describe bias, variance, identification, or all three?
- What happens at an edge case or when an assumption fails?

### Technical intuition

Use a toy calculation, limiting case, correlation argument, coupling,
geometric picture, or simple graph to reveal the mechanism. It is often useful
to give both a compact informal explanation and a derivation. Neither should be
asked to do the other's job.

When a method contains a tuning parameter or fitted coefficient, do not stop at
an oracle formula. Explain how it would be selected in practice, what data may
be used without compromising the argument, and what happens when the choice is
poor. The practical rule and the theoretical optimum should be distinguished,
not silently conflated.

### Literature

Use citations to locate ideas, not to replace exposition. Prefer the primary
source for a foundational result and mention cross-literature connections when
they genuinely illuminate the method. Avoid importing a research paper's long
literature review into the lecture spine.

## Writing less technical passages

Begin from something concrete: a historical episode, a familiar system, a
scientific decision, or an apparent paradox. Use it to expose a general tension,
then state the thesis clearly enough that the reader knows why the episode
matters.

Analogies should preserve structure. If randomization in art is compared with
experimental design, for example, identify what corresponds to the design,
the realization, and the act of selection. A memorable metaphor is useful when
it carries reasoning; it should not become an ornamental theme repeated after
its explanatory value is exhausted.

Nontechnical prose can be more expansive and historically textured, but should
retain the same habits of precision:

- move from example to claim rather than relying on assertion;
- surface the tension with “yet,” “however,” or a genuine question;
- acknowledge where the analogy or historical sample is limited; and
- return from the narrative to the statistical idea the lecture needs.

## Voice and sentence-level habits

- Prefer direct, developed prose over compressed textbook shorthand.
- Use active constructions when agency matters: a design assigns, an estimator
  reweights, an assumption permits, a model rules out.
- Use “we” to guide shared reasoning (“we now compare,” “we hold the potential
  outcomes fixed”), not to invent personal experience or attribute generated
  claims to the instructor.
- Let paragraph openings carry the argument. A reader scanning the first
  sentence of each paragraph should be able to recover the progression.
- Use descriptive headings and occasional bold lead-ins to orient the reader,
  but do not fracture a continuous argument into many tiny sections.
- Use bullets for taxonomies, comparisons, and recaps. Use paragraphs for
  explanation and argument.
- Favor calibrated words such as “can,” “under,” “in this setting,” and
  “suggests” when the evidence is conditional. Avoid hype and universal claims
  unsupported by the result.
- Vary sentence length. Longer sentences may carry a careful contrast or
  qualification, but the main claim should not be buried under several nested
  clauses.

## Writing complete notes for a 115-minute lecture

The research papers often need to establish novelty, survey adjacent work, and
state every contribution near the beginning. A lecture has a different job.
Preserve the problem-driven and intuition-rich reasoning, but replace the
research-paper contribution list with a teachable conceptual arc.

A useful local rhythm is:

$$
\text{problem}
\longrightarrow
\text{baseline}
\longrightarrow
\text{failure}
\longrightarrow
\text{new object}
\longrightarrow
\text{result}
\longrightarrow
\text{mechanism and limits}.
$$

This is a diagnostic, not a mandatory section template. Some topics should
begin with an example; others with an estimand, historical problem, or apparent
contradiction. Across the lecture as a whole:

- keep one visible conceptual spine that fits the blackboard session;
- treat that spine as the instructor's route through the notes, not as a word
  limit on the notes themselves; never sacrifice a needed definition,
  motivation, transition, or interpretation simply to make all written
  material speakable in one meeting;
- make derivations reproducible line by line without turning the notes into a
  transcript;
- use advanced sections for technical extensions;
- use Further reading for longer history and literature navigation; and
- let interactive demonstrations deepen an intuition already available from
  the prose, mathematics, and blackboard examples.

## Things to avoid

- Formula-first exposition in which the reader learns the purpose only after a
  page of notation.
- Headings that presuppose a result, mechanism, or vocabulary not yet developed
  in the preceding exposition.
- Undefined shorthand whose ordinary and technical meanings can diverge, such
  as “levels,” “balance,” or “adjusted weights.”
- Treating a cross-lecture notation table as permission to omit local
  definitions.
- Announcing that a result is intuitive without explaining its mechanism.
- Treating a simulation or anecdote as proof.
- Hiding a changed estimand or target population behind improved precision.
- Overusing “clearly,” “obviously,” or “trivially” where the reader needs an
  argument.
- Excessive callouts, canned summaries, or rhetorical questions.
- Transplanting research-paper contribution lists and literature surveys into
  lecture notes.
- Copying distinctive sentences, anecdotes, or metaphors from the source
  papers. The goal is continuity of reasoning and voice, not textual imitation.
- Forcing every lecture into the same structure. Consistency should come from
  explanatory principles, not identical headings.

## Drafting checklist

Before considering a lecture draft complete, ask:

1. Does the reader know the problem before encountering the machinery?
2. Is the estimand or target object stated before the estimator or algorithm?
3. Does each method arise from a visible need or concrete example before its
   generic formula and name are introduced?
4. Is there an informal model of the key argument that is accurate but simpler
   than the full derivation?
5. Have the nearest baseline and its failure been explained fairly?
6. Is every symbol introduced before use and locally reintroduced when needed?
   Are scalar, vector, random, and realized objects distinguishable?
7. Do headings and transitions rely only on concepts already developed?
8. Does every important equation have a purpose before it and an
   interpretation after it?
9. Are the design, assumptions, and sources of randomness explicit?
10. Is at least one example doing real explanatory work?
11. For tuning parameters or fitted coefficients, is practical selection
    explained alongside the theoretical choice?
12. Are tradeoffs, limitations, and changes of target stated in the main
   discussion rather than hidden at the end?
13. Can the central argument be taught at the board in 115 minutes without
    forcing all useful written exposition into that time budget?
14. Does the prose sound like a thoughtful technical guide rather than a paper
    abstract, a slide deck, or a cheat sheet?
