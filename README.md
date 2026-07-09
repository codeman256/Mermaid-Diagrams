# Mermaid Diagrams

Example Mermaid diagrams to test out [mermaid-viewer-app](https://github.com/codeman256/mermaid-viewer-app) — meant to be cloned or bind-mounted in as its `diagrams-repo` so the viewer has something to display out of the box.

## Contents

- **`diagrams/`** — the `.mmd` files themselves. A few are intentionally saved in different text encodings (UTF-16, UTF-8 with BOM) to exercise the viewer app's encoding auto-detection in `server.js`.
  - `example.mmd`, `biggraph TD.mmd`, `biggraph LR.mmd` — basic flowcharts.
  - `chart with links.mmd` — demonstrates `click ... href "?file=..."` in-app navigation between diagrams.
  - `subfolder/test.mmd` — demonstrates that the viewer lists/serves `.mmd` files from nested folders too.
  - `dark mode contrast.mmd` — nodes with explicit light `fill:` colors (plus one dark one) to exercise the viewer's dark-mode node-contrast fix.
  - `parse error.mmd` — deliberately invalid Mermaid source (unclosed bracket) to demo the viewer's error-box rendering path.
  - `sequence diagram.mmd`, `class diagram.mmd`, `state diagram.mmd`, `er diagram.mmd`, `pie chart.mmd`, `gantt chart.mmd` — other Mermaid diagram types beyond flowcharts, for broader rendering coverage.

## TODO

- [x] Add a diagram (or two) that exercises the viewer's dark-mode node-contrast fix — i.e. nodes with explicit light `fill:` colors, since that's the one rendering edge case the viewer app specifically works around.
- [x] Add a diagram whose Mermaid source deliberately fails to parse, to confirm/demo the viewer's error-box rendering path.
