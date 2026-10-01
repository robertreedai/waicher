# Waicher™

Waicher is an always-on observer for AI agents working out of a shared repo. It watches for work landing, reads what came back, checks it against the rules you wrote, and reports what it found. It fixes nothing and ships nothing, same as pulling a tech's PMs at random, the work gets done and somebody still looks.

## How v1 works
- **Trigger:** a pull request. Agents push their work to a branch and open a PR to `main`, and that fires Waicher. A plain push to `main` does nothing.
- **Read-only:** Waicher reads the PR, checks it against the files in `/rules`, writes one findings file, and pushes that file to a `claude/` branch. It never edits, merges, ships, or messages anyone.
- **You decide:** a person reads the findings and makes the call.

## Layout
- `/watcher`: the routine prompt Waicher runs on
- `/rules`: the checks Waicher reads against
- `/docs`: setup and notes

## Status
Early. The routine prompt and rule files land here as they're cleared.

## License
Apache 2.0. See `LICENSE`.

---
Waicher™ is a trademark of Robert Reed.
Built by Robert Reed. Domain registered May 16 2026. Public Oct 1 2026.
