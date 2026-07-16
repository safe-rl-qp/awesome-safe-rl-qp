# Contributing

Thanks for building something on top of Acc-CBF-QP! To add your project to the **Community Controllers** table:

1. **Fork** this repo and create a branch for your addition.
2. Add a new row to the **Community Controllers** table in `README.md`, keeping the table sorted alphabetically by project name:

   ```markdown
   | [Your Project Name](https://github.com/you/your-repo) | Robot name (e.g. Unitree G1) | Your name or org | One short sentence describing what it does. |
   ```

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
