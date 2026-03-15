```
Create a single self-contained HTML file with an interactive learning artifact for the concept: "Gang of Four Design Patterns".

Context: I'm a full-stack PHP engineer who knows OOP well but hasn't internalized the 23 GoF patterns. I want a fast reference I can filter, scan, and drill into with real before/after code examples.

Artifact type: Filterable card grid with collapsible before/after code panels

Specific behavior I want:
- Show all 23 GoF patterns as cards, grouped by category: Creational, Structural, Behavioral
- Each card shows: pattern name, one-line intent, and a "Problem it solves" tag
- Filter bar at the top with buttons: All | Creational | Structural | Behavioral
- A search input to filter by pattern name or keyword
- Clicking a card expands it (accordion style) to show:
  - When to use it (2-3 bullet points)
  - Before code (bad/naive PHP code showing the problem)
  - After code (refactored PHP using the pattern)
  - A "Real-world in payments" note — e.g. Strategy pattern for payment method switching
- Only one card expanded at a time
- Cards have a subtle color accent per category (not just gray)
- A "Mark as learned" toggle on each card that persists in localStorage and shows a progress count at the top: "7 / 23 learned"

Output: A single pattern-cheatsheet.html file I can open in a browser.
```
