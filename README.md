# remotion-best-practices (mirror)

Auto-synced mirror of [@am-will/remotion-best-practices](https://clawhub.ai/am-will/skills/remotion-best-practices) on ClawHub.

This repository is **not** the upstream source. The original skill is published by
`am-will` on ClawHub; this repo exists so `zsy2099` has its own git-controlled copy
that tracks the author automatically.

## Upstream

- Author: [@am-will](https://clawhub.ai/am-will) (GitHub: [am-will](https://github.com/am-will))
- Canonical skill: [`@am-will/remotion-best-practices`](https://clawhub.ai/am-will/skills/remotion-best-practices)
- Duplicate alias: [`@am-will/remotion`](https://clawhub.ai/am-will/remotion)

## How sync works

A GitHub Actions workflow (`.github/workflows/sync-clawhub.yml`) runs every day at
00:00 UTC. It re-fetches every file from the ClawHub file API and commits any
diff to this repo. You can also trigger a manual sync from the Actions tab
("Run workflow").

The mirror stays byte-identical with the upstream skill content. **Do not commit
personal edits here** — put them in a separate, independent repository (see
below).

## Layout

```
SKILL.md                                  # skill entry
rules/                                    # 31 best-practice rule files
  3d.md  animations.md  assets.md  audio.md  ...
rules/assets/                             # 3 reusable .tsx examples
.github/workflows/sync-clawhub.yml        # daily ClawHub sync
```

## Using the mirrored skill locally

The skill is already deployed at `~/.workbuddy/skills/remotion/` on your machine.
To refresh from this mirror instead of SkillHub/ClawHub directly:

```bash
cd ~/.workbuddy/skills/remotion
rm -rf ./*
git clone https://github.com/zsy2099/remotion-best-practices-mirror.git _mirror
cp -r _mirror/. .
rm -rf _mirror
```

Or just rerun the SkillHub install — both paths resolve to the same upstream.

## Publishing your own skills (independent repos)

Any skill you author or customize should live in its **own separate GitHub
repository** under `zsy2099`. This keeps them independent from the mirror and
guarantees the upstream sync can never conflict with your work.

Suggested naming:

| Kind                          | Repo pattern                              |
| ----------------------------- | ----------------------------------------- |
| Mirror (this one)             | `remotion-best-practices-mirror`          |
| Your fork / variant of author | `remotion-best-practices-<your-suffix>`   |
| Brand-new skill you authored  | `<your-skill-slug>`                       |