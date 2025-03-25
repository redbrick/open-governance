---
id: Discord Bots
aliases:
  - Discord Bots
tags:
  - admins
  - webmaster
  - webgroup
  - webgroup-github
  - technical
created: 2024-01-18T19:49:29
modified: 2025-03-25T14:31:34
title: Discord Bots
---

# Discord Bots

Currently in Redbrick, we have 2 Discord bots:

- [Brickbot2](https://github.com/redbrick/brickbot2)
- [Blockbot](https://github.com/redbrick/blockbot/)

Brickbot is currently used only by the [admins](../admin/admins.md) to perform administrative operations (e.g. LDAP operations on user accounts).

Blockbot is a more modern discord bot written using [`hikari`](https://www.hikari-py.dev/), maintained by the [webmaster](../committee/webmaster/Webmaster.md) and the [webgroup](Webgroup.md). Blockbot is set to replace Brickbot2, once all the necessary admin utilities are ported over.

Unlike Brickbot, Blockbot *does not* and *will not* have direct access to LDAP. Instead, Blockbot interfaces with the redbrick API to perform administrative tasks. This ensures all sensitive data processing is kept within the API, maintained by the [admins](../admin/admins.md). Blockbot will have access to the redbrick API via a restricted account and all administrative tasks are restricted to the `@RBAdmin` role on discord. Additionally, any change to Blockbot code that edits code concerning the redbrick API will have to be signed-off by an [admin](../admin/admins.md) or [rootholder](../admin/Rootholders.md).

Once the [admins](../admin/admins.md) and [Webmaster](../committee/webmaster/Webmaster.md) decide Blockbot has reached feature-parity with Brickbot2 for administrative tasks, Blockbot may be renamed to Brickbot *(3?)*, will be re-branded accordingly, and Brickbot2 will be retired. The development version of Blockbot, BlockbotDev, may also follow this branding or remain as-is.

Blockbot is a [webgroup](Webgroup.md) project, and as such, encourages all members to contribute to it. It is documented extensively on [docs.redbrick.dcu.ie](https://docs.redbrick.dcu.ie/webgroup/blockbot/) to ensure ease of contribution.
