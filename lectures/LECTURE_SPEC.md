# Lecture-note specification

## Audience

The notes are for graduate students in statistics, data science, economics,
and adjacent fields. Assume prior coursework in probability, mathematical
statistics, regression, linear algebra, and asymptotic notation. Explain
specialized causal-inference ideas carefully without re-teaching standard
mathematical prerequisites.

## Course-wide scope

The course is centered on causal inference for randomized experiments and on
design-based reasoning. Observational studies may be used for contrast or when
a lecture explicitly calls for them, but they should not silently become the
organizing perspective of the notes.

## How to interpret lecture briefs

Each `brief.md` is a concise, lecture-specific content specification. Treat its
scope bullets as requirements and emphases to be synthesized into a coherent
lecture—not as headings to reproduce or a sequence that the finished notes
must follow. Definitions, derivations, proofs, examples, counterexamples, and
interactive demonstrations should appear where they best serve the exposition.

Only three elements are expected in every brief: front matter, `# Lecture
scope`, and `# Literature`. A brief may also contain
lecture-specific examples, demonstrations, constraints, or unresolved
questions when the instructor chooses to specify them. Do not add the shared
audience, level, style, notation, or demonstration requirements to individual
briefs; those belong in the course-wide instruction files.

Keep literature entries minimal: author, year, title, and a stable link when
available. Do not pre-write assessments of a source or relevance
unless the instructor explicitly asks for them.

## Generation and revision

Each lecture has one canonical notes file, `index.qmd`. Before the first
generation it contains a placeholder and `generation-locked: false`. Initial
generation writes the lecture directly into that file, preserves the public
links to the brief and generation method, records `initial-draft-model` and
`initial-draft-date`, and changes the lock to `true`.

Once locked, `index.qmd` is human-owned. It may be edited in response to
specific instructor requests, but it must not be regenerated or wholesale
replaced unless the instructor explicitly requests an unlock and overwrite.
This is a generation guardrail, not a filesystem permission: it does not
restrict ordinary instructor editing.

Initial drafting may be iterative. Before the instructor begins substantial
line editing of `index.qmd`, the instructor may revise the brief and explicitly
request another full generation. Treat that request as permission to unlock and
replace the draft, then restore the lock and generation metadata. After direct
instructor edits begin, prefer specific revisions and never infer permission
for a wholesale regeneration from a changed brief alone.

## Intellectual level

- State the estimand before presenting an estimator.
- Separate identification, estimation, and inference.
- State the assignment mechanism and identify which quantities are fixed and
  which are random.
- Distinguish design-based, model-based, and superpopulation arguments.
- Make assumptions explicit and discuss what fails when they do not hold.
- Include derivations, counterexamples, and edge cases when they clarify the
  method.
- Connect theoretical results to experimental practice without turning the
  notes into a software manual.

## Teaching format

The notes will be available to students before class, but they should be
designed to support a paced, 115-minute blackboard lecture. They are a
preparation and reference document—not a slide deck, projected script, or text
to be read aloud in class.

The time limit applies to the material the instructor chooses to develop at the
board, not to the length of the written notes. Preserve a visible conceptual
spine that can guide the class meeting, but do not compress definitions,
motivation, transitions, derivations, or interpretation merely because every
sentence cannot be spoken in 115 minutes. The notes should be complete enough
to prepare students before class and to serve as a reference afterward. It is
acceptable—and often preferable—for the written treatment to be substantially
more expansive than the live lecture.

### Opening outline

Begin every lecture, immediately after its provenance link, with a compact
`Lecture outline` callout. This is the opening “tell them what you are going to
tell them” step: in three to five short bullets, preview the motivating problem,
the main conceptual progression, and where the lecture will arrive. Normally
keep the outline under 100 words.

The outline should describe an argument, not reproduce the table of contents or
inventory every subsection. Keep it intelligible before the lecture has begun:
avoid undeclared notation, unsupported technical claims, citations, and dense
lists of named methods. Do not include a minute-by-minute schedule unless the
timing itself is pedagogically important. If advanced material needs mention,
do so in one brief final bullet or sentence.

Where the lecture permits, close the main teaching path with a short synthesis
that returns to the opening problem and conceptual progression—the “tell them
what you told them” step. This need not be a second callout or a repetitive
summary.

- Organize the central argument into coherent units that can be developed and
  discussed at the board without rushing.
- Present major derivations in an order that can be reproduced line by line,
  introducing notation and assumptions before they are used.
- Prefer core examples and diagrams that can be reconstructed by hand and that
  create natural pauses for questions and interpretation.
- The written notes may include details or extensions that do not fit on the
  board, but the main conceptual and mathematical path should remain clear.
- Place conceptually optional technical extensions in clearly labeled
  `Advanced material` sections. Do not relegate explanation needed to
  understand the main argument to `Advanced material` merely to shorten the
  apparent teaching path; the instructor can select what to omit orally.
- Before initial generation, a lecture brief may identify which requested
  topics belong in the central teaching path, which should become advanced
  material, and which should be deferred or sidelined. Preserve those choices
  in the generated notes and make later-course connections explicit.
- Interactive demonstrations may supplement the notes, but the core lecture
  should remain teachable without projecting them.
- Do not adapt the content or organization to whether a particular meeting is
  in person or remote.

## Historical context and further reading

Historical context is part of the course's intellectual content. Include
concise history in the central lecture path when it clarifies why a concept was
introduced, how a problem was framed, or what an attribution means. Organize
longer chronology or literature discussion so it does not obscure the main
conceptual spine; this is an organizational distinction, not a length limit on
the written notes.

When a lecture has useful historical background, intellectual lineage, or
additional source pointers beyond that spine, include a clearly labeled
`Further reading` section near the end. Keep its annotations brief: identify
what question, development, or historical connection makes each source worth
following. It should orient an interested reader, not become a set of source
reports.

`Advanced material` and `Further reading` serve different purposes. Advanced
material develops technical extensions beyond the core lecture; Further
reading supplies history and routes into the literature. A source may support
an advanced section, but the two sections should not be treated as
interchangeable.

## Expository style

Read this section together with [`WRITING_STYLE.md`](WRITING_STYLE.md). The
writing-style guide is a required companion to this specification: whenever a
lecture is drafted or substantively revised under `LECTURE_SPEC.md`, read
`WRITING_STYLE.md` in full as well. The lecture brief determines the
lecture-specific content and emphases; this specification sets the
course-wide audience, scope, rigor, and teaching constraints; and
`WRITING_STYLE.md` governs how that material should be explained. These
instructions are cumulative rather than alternative.

The shared objective is a developed, problem-driven, intuition-rich lecture
narrative rather than a list of formulas. Intuition should expose the
mechanism behind a definition, method, or result, and the formal development
should then sharpen or qualify that intuition. At the scale of a lecture, the
following is one useful arc, but it is not a template and should be adapted,
reordered, or replaced to fit the material:

1. Motivating problem
2. Setup and estimand
3. Assumptions
4. Identification
5. Estimation
6. Inference
7. Failure modes
8. Worked example or simulation
9. Connections and extensions

At the scale of an individual topic, use the more detailed problem, baseline,
failure, new-object, result, mechanism, and limits rhythm described in
`WRITING_STYLE.md` when it clarifies the argument. Use bullets for genuine
comparisons, conditions, taxonomies, and recaps, not as a substitute for
exposition. Provide transitions between topics, motivate new mathematical
objects before naming them, and interpret important equations and results
after presenting them.

The tone should be more advanced than a typical undergraduate textbook. Avoid
cartoonish framing, excessive callout boxes, repeated remedial summaries, and
long digressions on prerequisites. At the same time, avoid cheat-sheet
terseness: important formulas need definitions, interpretation, context, and
an account of why they matter.

## Mathematical conventions

- Write inline math as `$...$` and display math as `$$...$$`.
- Use Quarto equation labels such as `{#eq-difference-in-means}` and references
  such as `@eq-difference-in-means`.
- Use Quarto theorem, proposition, definition, example, exercise, and proof
  blocks so numbering works in HTML and PDF.
- Never number equations, figures, tables, or theorems manually.
- Put reusable commands in the course-wide macro layer once their notation is
  established across lectures.
- Before defining notation in a new lecture, check `NOTATION.md`. Add newly
  established, course-wide conventions to that file during generation; do not
  add transient symbols used only inside one derivation or example.

## Sources

- Prefer primary sources and original papers, especially for historical
  attributions, foundational results, and the introduction of methods.
- Use reviews and textbooks selectively when they provide a genuinely useful
  synthesis, clarification, or exposition that is not well served by a single
  primary source. Do not substitute a recent textbook for a suitable original
  source by default.
- Tie substantive claims to a verified source.
- Do not infer bibliographic metadata from memory.
- Distinguish what a cited source proves from the interpretation supplied by
  the lecture notes.
- Flag unresolved source questions rather than silently filling gaps.
- Private reference materials may be consulted but must never be linked,
  copied, or redistributed with the notes. Cite the work and its draft status
  without publishing a private file path or download link.
- Write the exposition independently. Do not reproduce or closely paraphrase
  language from private drafts or other sources.

## Intended scale

Each lecture supports a 115-minute graduate class, but the notes are not
constrained to 115 minutes of readable prose. They are not a verbatim teaching
script: they should expose a teachable blackboard spine while retaining all
connective, motivational, and technical detail needed for independent reading
before and after the lecture.
