# Claude skills

Two small skills for Claude Code, shared by Paulina Espinosa. A skill is a plain text instruction file that teaches Claude how to do one job the same way every time. Read them first, they take a minute, and change them to fit how you work.

| Skill | What it does |
| --- | --- |
| `sync-prep` | Turns your meeting notes into a status draft or a prep note. It writes a draft only. It never posts or sends anything. |
| `refresh-browser` | Stops a stuck dev server, clears the cache folders and starts it again. |

## Install

Copy the folder of the skill you want into `~/.claude/skills/`, then start a new Claude Code session.

```bash
git clone https://github.com/Pecosa/claude-skills.git
cp -r claude-skills/sync-prep ~/.claude/skills/
cp -r claude-skills/refresh-browser ~/.claude/skills/
```

## Before you use refresh-browser

It stops whatever is running on ports 3000, 5173, 4321 and 8080, and it deletes cache folders such as `.next/`, `dist/` and `node_modules/.cache/`. Check that is what you want in your project.

## License

MIT. See [LICENSE](LICENSE).
