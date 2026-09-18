# jstack

A Cursor plugin of writing skills. Four skills, one always-on rule.

| Skill | When it runs |
| --- | --- |
| unslop | Always. Everyday AI-tell filter. |
| slopify | On request. Long-form audit, rewrite, voice match, or generate. |
| kiss | On request. Restate the last message in plain language. |
| next-action | On request, then sticky for the session. Action-first output shape. |

Standalone Slopify lives at [jjanousek/slopify](https://github.com/jjanousek/slopify). jstack vendors that skill and does not change it.

## Install

```bash
git clone https://github.com/jjanousek/jstack.git ~/.cursor/plugins/local/jstack
```

Reload Cursor. In Customize, confirm the four skills and set the unslop rule to Always.

## Skills

### unslop

Already on. Cuts AI tells from everyday prose, including replies. You do not invoke it.

### slopify

`/slopify`

Use for long-form audit, rewrite, voice match, or generate of docs, decks, pages, and emails. Do not use it on ordinary chat replies.

### kiss

`/kiss`

Restate the last message in plain human language, with no jargon.

### next-action

`/next-action`

Stay in this output shape until you say `stop next-action` or `normal mode`. Replies lead with the next action, number the steps, and end with one concrete next action.

## Credits

Third-party skill sources and licenses are listed in [NOTICE](NOTICE).

- unslop and kiss draw from [pstack](https://github.com/cursor/plugins/tree/main/pstack) by Lauren Tan.
- next-action is adapted from [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd) by Ayoub Ghriss.
- slopify is copied from [jjanousek/slopify](https://github.com/jjanousek/slopify).

## License

MIT. See [LICENSE](LICENSE).
