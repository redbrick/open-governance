---
title: Discord Bots
created: 2024-01-18T19:49:29
modified: 2024-01-18T20:12:16
tags:
  - admins
  - webmaster
  - webgroup
  - webgroup-github
  - technical
---
# Discord Bots

Currently in Redbrick, we have 2 Discord bots:
- [brickbot2](https://github.com/redbrick/brickbot2)
- [blockbot](https://github.com/redbrick/blockbot/)

Brickbot is currently used only by the [admins](../admin/admins.md) to perform administrative operations (e.g. LDAP operations on user accounts).

Blockbot is a more modern discord bot written using [`hikari`](https://www.hikari-py.dev/), maintained by the [webmaster](../committee/webmaster/Webmaster.md) and the [webgroup](Webgroup.md). Blockbot is set to replace brickbot2, once all the necessary admin utilities are ported over.

Unlike brickbot, blockbot *does not* and *will not* have direct access to LDAP. Instead, blockbot interfaces with the redbrick API to perform administrative tasks. This ensures all sensitive data processing is kept within the API, maintained by the [admins](../admin/admins.md). Blockbot will have access to the redbrick API via a restricted account and all administrative tasks are restricted to the `@RBAdmin` role on discord. Additionally, any change to blockbot code that edits code concerning the redbrick API will have to be signed-off by an [admin](../admin/admins.md) or [rootholder](../admin/Rootholders.md).

Once the [admins](../admin/admins.md) and [Webmaster](../committee/webmaster/Webmaster.md) decide Blockbot has reached feature-parity with brickbot2 for administrative tasks, blockbot may be renamed to brickbot *(3?)*, will be re-branded accordingly, and brickbot2 will be retired. The development version of blockbot, BlockbotDev, may also follow this branding or remain as-is.

Blockbot is a [webgroup](Webgroup.md) project, and as such, encourages all members to contribute to it. It is documented extensively on [docs.redbrick.dcu.ie](https://docs.redbrick.dcu.ie/webgroup/blockbot/) to ensure ease of contribution.
