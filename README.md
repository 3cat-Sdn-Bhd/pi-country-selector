# pi-gato-knowledge-reader

Pi extension. It filters [gato-knowledge](https://github.com/3cat-Sdn-Bhd/gato-knowledge) content
for one country (`MY` default, or `PH`) before it reaches the model:

- the system prompt, so `AGENTS.md` and every skill description in the catalog are filtered.
  A skill whose description is written wholly as `my[...]` is absent from the catalog under `PH`.

Directive syntax:

- inline: `Price my[RM 100]ph[PHP 1000]`
- block: a `:::ph` line, content, then a `:::` line
- Nested or overlapping directives are an error. The extension shows a red notification and the
  model receives only the error text, never the unfiltered content.

`/country [MY|PH]` selects the country. Without an argument it opens a picker. The choice is
saved in the session and shown in the footer as `country: MY`.

## Install

In the Gato project `.pi/settings.json`:

```json
{ "packages": ["git:github.com/3cat-Sdn-Bhd/pi-gato-knowledge-reader"] }
```

## Test

```bash
npm test
```
