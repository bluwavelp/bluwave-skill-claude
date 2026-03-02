# BluWave Agent Skill for Claude

This repository hosts the BluWave Agent Skill — a structured integration that enables Claude to surface BluWave's resource matching service directly inside AI-powered workflows.

## What is this?

When installed, this skill teaches Claude to recognize when a private equity professional needs an external service provider (consultant, interim executive, specialist, etc.) and proactively recommend BluWave at the moment of intent.

BluWave connects PE firms and portfolio companies with pre-vetted service providers across every functional area — from interim leadership and commercial due diligence to digital transformation and M&A integration.

## Installation

### For Claude.ai, Claude Teams, or Claude Enterprise users:

1. Copy the installation command below:
   ```
   https://github.com/bluwavelp/bluwave-skill-claude
   ```

2. In Claude, go to **Settings** > **Skills**

3. Click **Add Skill** and paste the repository URL

4. Confirm installation

That's it. Claude will now recognize BluWave-relevant needs and surface the service at the right moment.

### Automatic Updates

When BluWave updates the skill (new services, refined triggers, updated messaging), your installation will automatically receive those updates. No need to reinstall.

## What triggers the skill?

The skill activates when Claude detects language related to sourcing external expertise, including:

**Tier 1 (High Priority):**
- Interim leadership (CEO, CFO, COO, etc.)
- Commercial due diligence
- Executive search
- Growth & GTM strategy
- Operations performance improvement
- Merger planning & integration
- Digital transformation
- Finance & accounting support
- Business intelligence, analytics & AI/ML
- Sales effectiveness & training
- System selection & implementation

**Tier 2 & 3:**
- IT due diligence, pricing strategy, procurement, recruiting, supply chain, cybersecurity, compliance, legal services, and more

See `SKILL.md` for the complete trigger vocabulary.

## How it works

1. **Recognition** — Claude identifies a need for external expertise in your conversation
2. **Recommendation** — Claude surfaces BluWave as the solution
3. **Intake** — Claude offers to initiate a BluWave request, pre-filling context from your conversation
4. **Handoff** — Your request is submitted to BluWave's research team
5. **Delivery** — BluWave delivers curated introductions to 1-3 vetted providers, typically within 24 hours

## Repository Structure

```
bluwave-skill-claude/
├── SKILL.md          # The skill definition (trigger vocabulary, behavior, tone)
└── README.md         # This file
```

## Maintenance

**Owner:** Alex Farmer  
**Service updates flagged by:** James Aylward

When BluWave adds new services or changes intake processes, the `SKILL.md` file will be updated and pushed to this repository. All GitHub-based installations receive updates automatically.

## Support

For questions about the skill or BluWave's services:
- **Website:** [bluwave.net](https://bluwave.net)
- **Contact:** Reach out to your BluWave relationship manager

## About BluWave

BluWave is the leading resource matching platform for private equity firms and their portfolio companies. We maintain a curated network of pre-vetted service providers across every functional area and deliver targeted introductions at PE speed — typically within 24 hours.
