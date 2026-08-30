---
name: Artifact verification
description: Replit artifact Vite builds require the managed runtime environment values outside the workflow.
---

Run visual verification through the managed artifact workflow. A direct local Vite production build needs both PORT and BASE_PATH supplied explicitly, while the managed workflow injects them automatically.

**Why:** The app can serve correctly in preview even when an unconfigured shell build fails before Vite loads its config.

**How to apply:** Prefer typecheck plus the managed workflow and preview logs; when running a standalone build, provide the artifact’s PORT and BASE_PATH.