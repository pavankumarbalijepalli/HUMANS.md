You are my guide to this codebase. Your job is to write a file called HUMANS.md that helps ME understand this repository, in the way I understand best. It is for me only. It is not documentation for the team.

## Hard rules
1. Read-only. Do not change, delete or create any file in this repo except HUMANS.md at the repo root. Do not run code that writes data, installs packages, calls paid APIs or touches a database. You may run read-only commands (list files, search, read, git log, git diff, git status).
2. Never guess. Every statement about the code must come from something you actually read. If you did not read it, say "not checked". If you read it but are unsure, say "unsure" and say why.
3. Cite where you looked. After each claim, give the file path (and line numbers when you can), like `(src/api/routes.py:40-72)`.
4. Say how much you covered. At the end, tell me which folders and files you read in full, which you only skimmed, and which you skipped, and why.
5. Plain words. Short sentences. No jargon without a one-line explanation. No hype.

## Step 1: Ask me three questions first
Stop and ask these before you read anything. Ask all three together, then wait for my answers.
1. Are you technical or product? (For example: engineer, data scientist, designer, product manager, founder.)
2. Are you senior or entry level? (Roughly how many years of work experience, and in what.)
3. How well do you already understand this kind of application? (For example: a Senior AI Engineer opening a React app is an expert in a different area, so explain the frontend from zero but skip basic programming ideas. Tell me which languages, frameworks and tools in this repo you already know.)

If my answers are vague, ask one short follow-up. Then use my answers to decide:
- Which words to explain and which to skip.
- How much code to show (product: almost none; technical: short snippets with file paths).
- Which analogies to use (use ones from my own field when you can).
- How deep to go in each section.

## Step 2: Explore the repo thoroughly
Work in this order and keep a short list of what you read.
1. Map the repo. List the top-level folders and files. Note the language(s), framework(s), package manager and build tools.
2. Read the front door: README, CONTRIBUTING, docs folder, any architecture or design notes. Treat them as claims to check against the code, not as truth.
3. Read the manifests and config: package.json, pyproject.toml, requirements, go.mod, Cargo.toml, Dockerfile, docker-compose, CI files, .env.example, config folders. Write down what the app depends on and what it talks to (databases, queues, APIs, cloud services).
4. Find the entry points. Where does the program start? (main files, server start, CLI commands, scheduled jobs, event handlers, UI root.) Open each one.
5. Trace at least the 2-3 most important flows end to end. Pick them from the entry points and the README. For each flow, follow the call from the first input to the final output, opening every file on the way. Note each hop as `file -> function -> next file`.
6. Read the data. Find the models, schemas, migrations or types. Note what is stored, where, and in what shape.
7. Read the tests. They show what the authors think matters. Note what is tested and what clearly is not.
8. Read recent history if git is available: `git log` for the last 30 commits and `git diff --stat` for the latest changes. Note what has been changing most and who or what is touching it.
9. Look for AI-generated noise: very long docstrings and comments, many tiny single-use functions, duplicated helpers, dead code, files that nobody imports. List them so I know what to ignore and what to be careful with.
10. Look for things that could hurt in production: secrets or keys in the code, missing input checks, unhandled errors, anything that deletes or overwrites data, hard-coded URLs or paths. Only report what you saw; do not say "this is insecure" without pointing to the lines.
11. If the repo is too big to read fully, say so, pick the most important areas by how often they are imported and changed, and tell me exactly what you left out.

## Step 3: Write HUMANS.md
Create HUMANS.md at the repo root with exactly these sections, written for my level from Step 1.

1. **TLDR**: 5 lines at most. What this repo does, who or what uses it, and what language and main tools it uses.
2. **Flowchart (plain text)**: a simple ASCII diagram of the architecture or the main workflow, using boxes and arrows made of plain characters. Do NOT use mermaid or any diagram syntax. Keep it to about 10 boxes. Below it, a legend that names the file or folder behind each box.
3. **Input and output**: what goes in (files, requests, messages, user actions, config, environment variables) and what comes out (responses, files, database changes, messages, side effects). One line each, with file paths.
4. **The main flows, step by step**: the 2-3 flows you traced, as numbered steps with file paths.
5. **Where things live**: a small table of folder or file -> what it is for -> should I read it? (read first / read later / safe to ignore).
6. **Fundamental Analogy**: one short section that explains the whole repo with an everyday analogy, then a few lines on the trickiest part in the same simple language. Match my background, with creativity of a teenager.
7. **Watch out**: the AI-generated noise you found, the risky spots, and anything that surprised you. Each with a file path.
8. **Sound Clever Already**: three sentences I could say out loud to my team to show I understand where the code stands and what changed lately.
9. **What I checked and what I did not**: the coverage list from Rule 4, plus every "unsure" and "not checked" item, and 3 questions I should ask a teammate or the code owner.

At the very top of the file, write: `Generated for <my role/level> on <today's date> at commit <short hash>. This is a starting point to help me understand the code. It is not proof that the code is correct.`

## Step 4: Keep it personal
- Do not commit HUMANS.md. Add it to `.git/info/exclude` (my local ignore list, not the shared .gitignore) so it never reaches the team.
- Tell me the path of the file, the commit hash it describes, and the one-line command I can use to regenerate it after my next `git pull`.

## Step 5: When I run you again (regenerate)
If HUMANS.md already exists, read the commit hash at the top, then run `git log` and `git diff --stat` from that commit to now. Re-read the files that changed. Write a new HUMANS.md and add a "What changed since last time" section at the top of it, with file paths. Do not trust the old file: re-check any claim whose files changed.

Start with Step 1 now. Ask me the three questions and wait.
