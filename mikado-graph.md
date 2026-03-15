```
Create a single self-contained HTML file with an interactive learning artifact for the concept: "Mikado Method for Refactoring".

Context: I'm a full-stack engineer working on a legacy PHP codebase. I know what refactoring is but I struggle to manage large refactoring efforts without breaking things — the Mikado Method helps by mapping prerequisites as a tree before touching code.

Artifact type: Interactive diagram with clickable nodes (tree graph, buildable by the user)

Specific behavior I want:
- Start with an empty canvas and a root node labeled "Goal" (editable)
- User can click any node to add child prerequisite nodes (each with a name and optional note)
- Each node has three states: Todo (gray) → In Progress (blue) → Done (green) — click to cycle
- A node can only be marked Done if all its children are Done — show a warning if violated
- Nodes can be deleted (with their subtree)
- Show a progress bar at the top: X of N prerequisites done
- Draw connecting lines between parent and child nodes, re-layout automatically as nodes are added
- On hover, show a tooltip with the node's note
- Include a small legend explaining the Mikado Method in 3 bullet points at the bottom

Output: A single mikado-graph.html file I can open in a browser.
```
