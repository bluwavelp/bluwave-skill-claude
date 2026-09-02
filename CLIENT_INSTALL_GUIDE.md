# Installing the BluWave Projects Skill

This guide walks you through connecting BluWave to Claude or ChatGPT so the assistant can scope a provider need with you and submit it to the BluWave team without leaving the chat.

You will need two things: the **BluWave MCP connector** (which lets the assistant submit requests) and the **BluWave Projects skill file** (which teaches the assistant when and how to help). Download the skill file, `bluwave-projects.zip`, from [bluwave.net/bluwave-connectors](https://bluwave.net/bluwave-connectors).

---

## Claude

### Individual users

1. **Connect the MCP server.** In Claude, go to **Customize > Connectors**, click **+ Add custom connector**, and paste the BluWave MCP connector URL: `https://mcp.bluwave.app/mcp`. Complete the sign-in when prompted.
2. **Install the skill.** Go to **Customize > Skills**, click **Create Skill > Upload a skill**, and select `bluwave-projects.zip`.

### Organization admins

1. Go to **Organization settings > Connectors** and add the BluWave MCP connector URL: `https://mcp.bluwave.app/mcp`.
2. Go to **Organization settings > Skills**, click **+ Add**, and upload `bluwave-projects.zip`.

---

## ChatGPT

1. **Connect the MCP server.** In ChatGPT, go to **Settings > Connectors** (or **Apps & Connectors**), choose **Create** or **Add custom connector**, and paste the BluWave MCP connector URL: `https://mcp.bluwave.app/mcp`.
2. **Install the skill.** Go to **Skills**, click **Create**, choose **Upload from your computer**, and select `bluwave-projects.zip`.

If ChatGPT reports "Archive must include at least one SKILL.md file at the skill root," the file you downloaded has been re-zipped. Download a fresh copy from the link above, or contact BluWave.

---

## How it works

Once both pieces are installed, the assistant will:

1. **Recognize** when you are discussing a need for external expertise (interim executives, due diligence, consultants, and so on)
2. **Ask** a few quick questions to understand the situation, the way a PE-savvy peer would
3. **Submit** a structured brief to the BluWave team on your behalf
4. **Confirm** with a reference number. The team typically delivers curated provider introductions within 24 hours

---

## Updating

The MCP connector updates automatically. When BluWave releases a new version of the skill, download the new `bluwave-projects.zip`, remove the existing BluWave skill from your Skills settings, and upload the new file.

---

## Questions?

Contact your BluWave relationship manager or visit [bluwave.net/contact](https://bluwave.net/contact).
