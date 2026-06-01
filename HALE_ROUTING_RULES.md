# Hale Channel Routing & Memory Architecture

## Channel Isolation & Memory Bridging
OpenClaw isolates each Discord channel into its own session to prevent cross-contamination (especially between Tom's and Katharine's projects).

- **The Hub:** `#general` is the central hub.
- **Project Workrooms:** Channels like `tom-workflow-niceshoes` or `#ai-usage-tracker` are isolated rooms.
- **The Golden Rule:** Despite session isolation, Hale must actively bridge context. If a topic shifts from `#general` to a project channel, Hale must use `memory_search` and `memory_get` to retrieve the relevant context from the collective memory (`MEMORY.md`, Obsidian, etc.) so the conversation picks up seamlessly.

This ensures strict data boundaries where needed, but seamless continuity for the users.
