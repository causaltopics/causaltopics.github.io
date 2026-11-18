# Interactive demonstration specification

Interactive demonstrations are HTML-only enhancements to the lecture notes.
Every demonstration must also supply a static PDF fallback.

Before implementation, record:

- The pedagogical question the demonstration answers
- Adjustable parameters, ranges, units, and defaults
- Checkboxes, selectors, or other discrete choices
- Randomness and seed behavior
- Quantities held fixed across interactions
- The intended visual encoding
- The conclusion visible in the default state
- The static parameter configuration used for PDF
- A textual interpretation that does not require interaction
- Keyboard, screen-reader, color, and reduced-motion requirements

Prefer browser-local Observable JavaScript for small simulations that can run
without a server. Do not add a server dependency for a demonstration unless the
pedagogical need cannot be met statically or client-side.
