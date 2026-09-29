# OpenClaw Telegram Customer Inbox

Reusable OpenClaw skill and plugin for a Telegram customer-support inbox.

## Behavior

- Customer messages are mirrored to a staff group and AI replies remain enabled by default.
- Normal staff replies are routed directly to the customer without pausing AI.
- Staff can pause one customer with the `Tiếp quản` button or `/takeover`.
- Staff can resume AI with the `Trả lại bot` button or `/bot`.
- Exact staff IDs control group replies and button actions.

## Install

Read `SKILL.md`, then run the bundled installer in dry-run mode:

```bash
python3 scripts/install_customer_inbox.py \
  --openclaw-root ~/.openclaw \
  --workspace ~/.openclaw/workspace \
  --account-id <telegram-account-id> \
  --group-id <telegram-supergroup-id> \
  --staff-id <staff-user-id> \
  --dry-run
```

The target Telegram account must already have a secure `tokenFile`; this repository never contains a bot token.

See `SKILL.md` for verification, migration, repair, and rollback guidance.
