Claude finished the response
Architected repository structure for awesome list project

Quick answers first:

    Description: something like "A curated list of robots, controllers, and projects built on the Acc-CBF-QP safety filter framework (mc_rtc-based, IROS 2026)."
    Template: no special repo template needed — awesome lists are just a README + a couple of support files, you can start from scratch.
    License: yes, add one. Convention for awesome lists (per the sindresorhus/awesome guidelines) is CC0 (public domain) for the list content itself — separate from whatever license your actual framework code uses (that's a code license question for the other repos, likely BSD/MIT/Apache, not this one).

Let me set up the files.
The user prompt is empty, so there is no primary language to identify. However, I'll provide a summary of the thinking block in English: Purged legacy state and rebuilt system architecture

Now the LICENSE — CC0, the standard for awesome lists:
Orchestrated file organization and presentation preparation

Four files, ready to drop straight into a new repo:

    README.md — the list itself, with sections for the core framework, getting-started (superbuild + template), community controllers table, and license. Three TODO-*-url placeholders for you to fill in once those repos exist, plus TODO-tag-name for the paper's release tag.
    CONTRIBUTING.md — submission steps and rules for what belongs on the list.
    .github/PULL_REQUEST_TEMPLATE.md — auto-fills when someone opens a PR, keeping submissions consistent.
    LICENSE — CC0, standard for awesome lists. Has one TODO-country-or-leave-blank you can delete or fill.

A few notes:

    I used Acc-CBF-QP as the framework's display name throughout (matching the paper), while keeping the repo name awesome-safe-rl-qp as you specified — adjust if you'd rather brand it differently.
    To search for TODO before you push: grep -rn TODO . in the repo root will find all of them.
    If you want the official "Awesome" badge/recognition later, this structure already satisfies most of sindresorhus/awesome's contribution guidelines (badge, TOC, contributing file, license) — worth submitting there once it has a few real entries.

Want me to do the superbuild, framework, or template repo files next?
Readme
Document · MD 
Contributing
Document · MD 
LICENSE
 
Pull request template
Document · MD 

I added the link and I don't think that Core Framework is the right title for this section as it's just the archive of the source code
## Core Framework

| Project | Description |
|---|---|
| [Acc-CBF-QP](https://github.com/safe-rl-qp/mc-safe-rl-qp) | The core framework: acceleration-based CBF-QP safety filter for mc_rtc. Includes the version used in the IROS 2026 paper (see the TODO-tag-name tag). |
Reconsidered section title and drafted alternative naming options

Good catch — that makes more sense given it's the frozen snapshot, not an actively developed "core framework" repo. A few naming options:

    Paper Implementation
    Reference Implementation (IROS 2026)
    Original Release
    Paper Code Release

I'd lean toward "Paper Implementation" — it's immediately clear this is the archived code tied to the publication, as opposed to something under active development (which is what the superbuild/template are for).
Edited a file, ran a command, read a file

Updated — section is now "Paper Implementation" with the description reworded to reflect it's an archived snapshot rather than an ongoing framework. Still left the TODO-tag-name placeholder for you to fill in once you cut that release tag.
Readme
Document · MD 

In this section 

## Community Controllers

Controllers, robots, and RL policies built on top of the framework by the community.

<!--
Please keep this table sorted alphabetically by project name.
Format: | [Project Name](link) | Robot | Author/Org | One-line description |
-->

| Project | Robot | Author | Description |
|---|---|---|---|

Is it possible to add automatically the date of the last commit on the repo?
Weighed automated workflow against dynamic badge solutions

Yes — the cleanest way is a shields.io badge that pulls live from the GitHub API, no workflow or script needed:

![Last Commit](https://img.shields.io/github/last-commit/OWNER/REPO)

It renders as a small badge showing "X days/months ago" and updates itself every time someone views the page — nothing to run or maintain on your end.

The alternative — a scheduled GitHub Action that queries each repo and rewrites the table with a literal date — is possible too, but it's real infrastructure (a script + workflow file you have to maintain) for something the badge already solves for free. I'd only go that route if you wanted more (e.g., auto-sorting entries by recency, or a table that doesn't depend on shields.io being up). For a "Last Updated" column, the badge is the standard approach — you'll see it all over other awesome-lists.

I've added a Last Updated column using it:
Add a "Last Updated" column with a live shields.io last-commit badge to the Community Controllers table

Now let me update the contribution guide so submitters know the exact syntax to use for that column:
Edited a file, ran a command, read a file

One thing to flag: shields.io badges only work for public repos and can occasionally rate-limit on unauthenticated GitHub API calls if hit very heavily — a non-issue at your scale, but worth knowing if the list ever grows to hundreds of entries.
Readme
Document · MD 
Contributing
Document · MD 


Claude is AI and can make mistakes. Please double-check responses.
Contributing · MD
# Contributing
 
Thanks for building something on top of Acc-CBF-QP! To add your project to the **Community Controllers** table:
 
1. **Fork** this repo and create a branch for your addition.
2. Add a new row to the **Community Controllers** table in `README.md`, keeping the table sorted alphabetically by project name:
```markdown
   | [Your Project Name](https://github.com/you/your-repo) | Robot name (e.g. Unitree G1) | Your name or org | One short sentence describing what it does. | ![Last Commit](https://img.shields.io/github/last-commit/you/your-repo) |
```
 
   The last column is a live badge (via [shields.io](https://shields.io)) that always shows the repo's most recent commit date — just replace `you/your-repo` with your GitHub `owner/repo`, no need to update it manually later.
 
3. Make sure your entry meets these guidelines:
   - The linked repository is **public** and **actually uses** the Acc-CBF-QP framework (link to the specific commit/tag if it's easier to verify).
   - The description is a **single sentence**, written in plain English, no marketing language.
   - No duplicate entries — if you're updating an existing entry, edit it in place rather than adding a new row.
4. Open a **pull request**. In the PR description, briefly say:
   - What robot(s) it runs on
   - Whether it's been validated in simulation, on hardware, or both
5. A maintainer will review and merge. We may ask for small wording tweaks to keep the table consistent.
## What belongs on this list
 
- Controllers or RL policies that build on the Acc-CBF-QP framework (core repo, superbuild, or template).
- Forks or extensions that add support for new robots.
- Tools or utilities specifically built to work with the framework.
## What doesn't belong here
 
- General mc_rtc controllers unrelated to Acc-CBF-QP.
- Unrelated RL or safety-filter projects (feel free to open an issue if you think an exception makes sense).
## Reporting issues instead
 
If you're not adding a project but found a broken link, outdated info, or a typo, feel free to just open an issue or a PR with the fix directly — no need to follow the full submission format above.
 