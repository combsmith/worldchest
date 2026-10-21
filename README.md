# WorldChest

Automatic backup, sync, restore and versioning for Minecraft Bedrock worlds, so
a kid's worlds survive a new phone, a cracked screen or a bad update, and can be
rewound to an earlier save without any technical work.

> NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG
> OR MICROSOFT. "Minecraft" is used only as a secondary title, never in the
> brand, domain, handles or packages, per the Minecraft Usage Guidelines.

**Status:** pre-code, graduated from the incubator. The brainstorm, market
research, decision brief, opportunity–solution tree and PRD live in
[`_bmad-output/planning-artifacts/`](./_bmad-output/planning-artifacts/) (seeded
from [combsmith/incubator discussion #5](https://github.com/combsmith/incubator/discussions/5);
working name BlockVault; brand decision 2026-10-19: WorldChest, `worldchest.app`).
The brief's recommendation is to buy evidence first; the PRD scopes that work.
The stack is not chosen yet; CI runs the org baseline checks until it is.

## What it will do

- **Backup** a device's whole local world library to the cloud, integrity-verified.
- **Restore** every world onto a new device with no cables and no corruption
  (the naive Smart Switch path crashes the game; the in-scope file set is known).
- **Version** saves so a player can rewind.
- **Tiered device access:** `.mcworld` share-sheet baseline for everyone, Shizuku
  (ADB, no root) power mode for automatic full-library backup, a desktop companion
  for big migrations, and the official Mojang API as the long-term goal.

## Working here

Read [`AGENTS.md`](./AGENTS.md) first. Frameworks such as BMAD are vendored from
`combsmith/.github-private` or `software-factory`, never installed per repo.

---

## 💼 Commercial Support & Enterprise Services

This project is open source and free for the community. For enterprise deployments, proprietary integration, and priority service, commercial support and custom engineering are provided through [CombSmith LLC](https://combsmith.com):

- **Standard SLA & Priority Support:** $199/month per organization
  - Guaranteed 24-hour issue triage
  - Dedicated private communications channel
  - Upstream bug-fix and security patch prioritization
- **Custom MCP Development & Architecture Advisory:** $250/hour
  - Custom tool, prompt, and resource connector implementation
  - Security audit and containerized deployment assistance
  - Tailored agentic workflow integration

For commercial invoicing, custom service agreements, or enterprise purchase orders, contact **support@combsmith.com** or visit [combsmith.com](https://combsmith.com).
