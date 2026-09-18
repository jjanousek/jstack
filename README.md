# jstack

Writing skills for Cursor. Unslop is always on. The other three run on request.

## Install

1. Clone the plugin:

   ```bash
   git clone https://github.com/jjanousek/jstack.git ~/.cursor/plugins/local/jstack
   ```

2. Reload Cursor. In Customize, confirm the four skills and set the unslop rule to Always.

## Skills

| Invoke | Skill | What it does |
| --- | --- | --- |
| Always on | [unslop](skills/unslop/SKILL.md) | Everyday AI-tell filter, including replies |
| `/slopify` | [slopify](skills/slopify/SKILL.md) | Long-form audit, rewrite, voice match, or generate |
| `/kiss` | [kiss](skills/kiss/SKILL.md) | Restate the last message in plain language |
| `/next-action` | [next-action](skills/next-action/SKILL.md) | Action-first output, sticky for the session |

Use slopify on docs, decks, pages, and emails. Not on ordinary chat replies. Standalone skill: [jjanousek/slopify](https://github.com/jjanousek/slopify). jstack vendors it unchanged.

Turn off next-action with `stop next-action` or `normal mode`.

## Credits

Sources and licenses are in [NOTICE](NOTICE).

- unslop and kiss from [pstack](https://github.com/cursor/plugins/tree/main/pstack) by Lauren Tan
- next-action from [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) by Ayoub Ghriss
- slopify from [jjanousek/slopify](https://github.com/jjanousek/slopify)

## License

[MIT](LICENSE)
