# BluWave Projects Skill

This repository is the source of truth for the **BluWave Projects** agent skill. The skill teaches Claude and ChatGPT to recognize when a private equity professional needs an external service provider (interim executive, diligence firm, consultant, specialist, etc.), run a short discovery conversation, and submit a structured project brief to the BluWave team through the BluWave MCP connector.

## Repository structure

```
bluwave-skill-claude/
├── bluwave-projects/
│   └── SKILL.md              # The skill. Edit this file and nothing else.
├── .github/workflows/
│   └── release.yml           # Packages bluwave-projects/ into bluwave-projects.zip on every push to main
├── .claude-plugin/           # Manifest for the Claude Code plugin marketplace
├── CLIENT_INSTALL_GUIDE.md   # End-user install instructions
└── README.md
```

The `bluwave-projects/` folder is laid out exactly the way Claude and ChatGPT expect a skill archive to look: one top-level folder containing `SKILL.md`. Zipping that folder produces a valid upload with no further changes.

## Getting the packaged skill

**Preferred: download from Releases.** Every push to `main` that touches `bluwave-projects/` rebuilds the archive and publishes it as a release asset at a stable URL:

```
https://github.com/bluwavelp/bluwave-skill-claude/releases/latest/download/bluwave-projects.zip
```

The website's download link should point here (or the file should be re-uploaded from here) so the hosted copy never drifts from the repo.

**Manual alternative.** Pull the latest `main`, then zip the folder itself, not the files inside it:

```sh
# macOS / Linux
zip -r -X bluwave-projects.zip bluwave-projects

# Windows (PowerShell or Command Prompt)
tar -a -cf bluwave-projects.zip bluwave-projects
```

On Windows, avoid `Compress-Archive`. It writes backslash paths inside the zip, which some unzippers read as a single oddly named file instead of a folder.

Do not use Finder's right-click "Compress" on macOS. It adds a `__MACOSX` folder and, if used on an already-zipped file, produces a zip inside a zip that ChatGPT rejects with "Archive must include at least one SKILL.md file at the skill root." Open the finished zip and confirm it contains only `bluwave-projects/SKILL.md`.

## Installing the skill

See [CLIENT_INSTALL_GUIDE.md](CLIENT_INSTALL_GUIDE.md) for end-user instructions covering both the MCP connector and the skill upload.

## What triggers the skill?

The skill activates when the user expresses a need for external expertise, including:

- Interim leadership (CEO, CFO, COO, CTO, controller, fractional executives)
- Executive search and board recruitment
- Commercial, IT, operational, and HR due diligence; quality of earnings
- Growth and go-to-market strategy, pricing, sales effectiveness
- Operations improvement, merger integration, digital transformation
- Finance and accounting support, BI/analytics/AI/ML
- ERP/CRM selection, procurement, supply chain, cybersecurity, legal, HR, turnaround, staffing

It also triggers proactively on phrases like "we need help with," "looking for a consultant," or "just closed an acquisition." See the `description` frontmatter in `bluwave-projects/SKILL.md` for the full trigger vocabulary.

## How it works

1. **Recognize** a need for external expertise in the conversation
2. **Discover** the situation through a short, peer-level conversation (two questions per turn at most)
3. **Brief** the BluWave team by submitting a structured request through the MCP connector
4. **Confirm** with a reference number; BluWave typically delivers curated introductions to 1-3 vetted providers within 24 hours

## Making changes

1. Edit `bluwave-projects/SKILL.md` on a branch and open a PR to `main`.
2. When merged, the release workflow rebuilds `bluwave-projects.zip` automatically.
3. Notify the web team if the hosted download needs to be refreshed, or point the site at the release URL above so it never does.

## Maintenance

**Owner:** Alex Farmer
**Service updates flagged by:** James Aylward

## Support

- **Website:** [bluwave.net](https://bluwave.net)
- **Contact:** Reach out to your BluWave relationship manager

## About BluWave

BluWave is the leading resource matching platform for private equity firms and their portfolio companies. We maintain a curated network of pre-vetted service providers across every functional area and deliver targeted introductions at PE speed, typically within 24 hours.
