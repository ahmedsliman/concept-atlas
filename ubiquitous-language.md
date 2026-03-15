```
Create a single self-contained HTML file with an interactive learning artifact for the concept: "DDD Ubiquitous Language".

Context: I'm a full-stack engineer building a payments product with DDD. I understand bounded contexts but I want a tool to build and maintain a shared glossary where the same word can mean different things in different contexts — and to make those conflicts visible.

Artifact type: Checklist / tracker — living glossary with per-context term management

Specific behavior I want:
- User can add Bounded Contexts (e.g. Billing, Identity, Notifications) as named tabs or columns
- Within each context, user can add terms with: Term name, Definition, and optional Example usage
- If the same term name exists in more than one context with different definitions, highlight it in red and show a "Conflict" badge — this is the core learning: same word, different meaning
- If the same term exists in multiple contexts with the same definition, show a "Shared" badge in green (Shared Kernel candidate)
- User can edit or delete any term inline
- A search bar filters terms across all contexts simultaneously
- A "Conflicts" view shows only conflicting terms side by side across contexts
- All data persists in localStorage so it survives page refresh
- Include a short explanation panel (collapsible) describing why ubiquitous language matters and what conflicts reveal about your model

Output: A single ubiquitous-language.html file I can open in a browser.
```
