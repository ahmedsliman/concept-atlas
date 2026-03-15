```
Create a single self-contained HTML file with an interactive learning artifact for the concept: "DDD Bounded Context Relationships".

Context: I'm a full-stack engineer learning DDD for a payments product. I understand what a bounded context is but I want to practice sketching context maps and understanding the relationship patterns between them.

Artifact type: Interactive drag-and-drop diagram builder

Specific behavior I want:
- User can add named Bounded Context boxes to a canvas by clicking an "Add Context" button
- Boxes are draggable and resizable on the canvas
- User can draw a relationship between two contexts by clicking "Connect" then clicking two boxes
- When drawing a connection, a dropdown appears to pick the relationship type:
  - Shared Kernel
  - Customer / Supplier
  - Conformist
  - Anti-Corruption Layer (ACL)
  - Open Host Service
  - Published Language
  - Separate Ways
- Each relationship type renders differently (different line style or color) and shows a label on the edge
- Clicking a relationship line opens a side panel explaining what that pattern means, when to use it, and an example from a payments domain
- Clicking a context box lets the user rename it
- Include a legend showing all 7 relationship types with their colors/styles

Output: A single bounded-context-designer.html file I can open in a browser.
```
