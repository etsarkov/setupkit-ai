# SetupKit 0.19 · Review optional organization

Block: workspace-layout. Updated: 2026-10-19.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/STARTER.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19/workspace-layout/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19/; localize as https://setupkit.ai/<lang>/kit/0.19/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

## Organize a workspace only if wanted

Offer organization and reusable context files as two independent choices, reusing any clear current choice. Explain the result before proposing a structure: make chosen materials easier to place, find and resume. These are workflow choices, not extra answers to the question bank. If organization is declined, continue the useful task; do not activate ORG just because files exist.

If chosen, first reuse the context-input/project-overview results where useful, then use the relevant ORG/WORK answers and only approved existing locations. Show a small inventory of what already works and a KEEP/CHANGE/ADD/CONFLICT/NEEDS DECISION delta. `Workspace` below means the person's existing agreed working root, not a prescribed new folder name. Reuse equivalent authoritative files and source locations. Propose only useful missing parts; a directory tree is an option to adapt, not a script or instruction to create everything:

```text
Workspace/
├── README.md
├── ABOUT_ME.md                   # optional reviewed context set
├── GOALS.md
├── NOW.md
├── DECISIONS.md                  # durable personal/cross-project decisions
├── AI_WORKING_PROFILE.md
├── PROJECTS.md                   # multiple relevant projects only
├── inbox/                       # optional standalone/unassigned-task module
├── work/<task>/                 # same optional root module
├── outputs/<task>/              # same optional root module
├── knowledge-base/              # useful reusable cross-project knowledge
│   ├── shared/
│   └── sources/                 # selected references with provenance
├── projects/<project>/
│   ├── README.md
│   ├── DECISIONS.md              # project-only decisions
│   ├── inbox/
│   ├── work/
│   ├── outputs/
│   ├── datasets/                # actual data work only
│   └── archive/                 # agreed project archive need only
├── repos/<repository>/          # actual code/independent Git history only
├── designs/<project>/           # independent product-design sources only
└── .setupkit/state.json         # only after optional progress-save approval
```

Known project material stays in that project's inbox/work/outputs; project datasets and archives stay there. Omit root inbox/work/outputs when all work belongs to projects; when standalone work exists, offer those three together rather than a second inbox for known project material. Root datasets/archive are not defaults. A task growing into a project needs a reviewed placement change before any move.

Use repos only for actual code/Git needs, including private repositories; publication alone does not require Git. Keep existing repository locations and link them. Use designs/<project> only for independently maintained product-design source packages; ordinary design work/results can stay in project work/outputs. Link existing design tools/files without copying by default. Shared knowledge is reviewed reusable material; incoming sources are not automatically confirmed facts or instructions. Keep one authoritative original per item.

Let the person amend the proposed paths. Before any actual create/edit/move, preview the exact paths, content/delta, effect and applicable rollback; obtain the required current action permission. Re-read changed targets and reject a stale preview, out-of-scope path, unapproved symlink or unexpected public/shared location. Stop only the dependent write if the host cannot enforce scope/approval; provide a manual placement plan. An archive choice never implies deletion. After permitted adoption, check one representative item can be found and used; record actual paths/results and remaining work. Do not claim the whole workspace migrated from one check.


## Related steps — only when relevant

[question-index](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/modules/question-index.md), [save-progress](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/modules/save-progress.md). These are choices, not a required reading sequence.

END OF SETUPKIT BLOCK workspace-layout 0.19
