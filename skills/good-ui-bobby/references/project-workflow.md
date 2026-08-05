# Project workflow

Use this reference for project setup and temporary AI-assisted exploration.

## Git checkpoints

At the beginning of a new project:

1. Inspect Git status, branch, remotes, and existing history.
2. If the project is not yet under Git, initialize it before substantial implementation.
3. Check the global Git identity. Use it as configured; never replace it with a skill-specific name or email.
4. Ensure secrets, build output, and local-only files are ignored before the first commit.
5. Create a clean baseline checkpoint once the project is runnable.

During the work, commit coherent milestones such as system scaffolding, a working first surface, and a verified interaction pass. Do not include unrelated user changes or secrets in a commit.

## OpenRouter-backed features

Use OpenRouter only when an AI-assisted feature, image generation step, or project exploration tool materially benefits from it.

- Inspect the project's existing environment and server conventions before adding a client.
- Read `OPENROUTER_API_KEY` from the server-side environment. Never hardcode it, expose it to the browser bundle, print it in logs, or commit it.
- Add only a placeholder such as `OPENROUTER_API_KEY=` to an example environment file when the project convention supports one.
- Keep prompts and returned data scoped to the task. Do not send secrets, credentials, or unnecessary personal data.
- Handle timeout, rate-limit, authentication, empty, and provider-error states as product behavior.
- Make the feature removable or replaceable; do not make unrelated UI depend on a temporary model call.

## Temporary work

Keep generated images, test data, screenshots, and exploratory files out of production paths unless the user explicitly wants them shipped. Remove or gate temporary dev controls and provider integrations before declaring the work complete.
