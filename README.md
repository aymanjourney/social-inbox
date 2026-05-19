# Social Inbox

A capture system for inspiring content found while browsing social media.

## Workflow

```
1. See an inspiring tweet / post
        │
        ▼
2. Create a new file in inbox/
   Copy TEMPLATE.md → inbox/YYYY-MM-DD_short-title.md
   Fill in: content, links, platform
        │
        ▼
3. Give me the file path
   "تفضل: social-inbox/inbox/2026-05-19_rlhf-tip.md"
        │
        ▼
4. I read it and respond with one of:
   ✅ Actionable  — clear benefit; I propose how to apply it
   🔬 Research    — worth logging in RESEARCH_LOG; not immediately actionable
   ❌ Skip        — redundant or incompatible with current architecture
        │
        ▼
5. Move the file to processed/ (or delete it)
   processed/ is the record of what was seen and decided
```

## File naming

```
inbox/YYYY-MM-DD_short-title.md
```

Examples:
```
inbox/2026-05-19_langgraph-checkpointing.md
inbox/2026-05-20_rlhf-paper-github.md
```

## Folder layout

```
social-inbox/
├── README.md          ← this file
├── TEMPLATE.md        ← copy this for every new entry
├── inbox/             ← unreviewed items (give me the path)
└── processed/         ← decided items (move here after review)
```

## What counts as a good capture?

- A tweet with a **GitHub link** to a tool/repo/paper worth evaluating
- A **methodology** described in a thread (prompt engineering, agent architecture)
- A **concrete technique** with code or a clear how-to
- A **research finding** from a paper or experiment

What to skip before even creating a file:
- Generic motivational content with no concrete technique
- Content you've already seen applied in the project
- Threads > 5 tweets with no clear thesis (too diffuse)
