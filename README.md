# gz-mindload

A cognitive complexity scorer over CPython's `ast`, after G. Ann Campbell's
*Cognitive Complexity*. It never executes the code it scores.

```python
from gz_mindload import score_cognitive

for record in score_cognitive(source, "module.py"):
    print(record.name, record.line, record.score)
```

```bash
gz-mindload PATH...
```

## Provenance

Extracted as-is from [gzkit](https://github.com/tvproductions/gzkit) at commit
`a06a4f36a8e3fc538d8f20b61df91b9bf42d1ee7`: `src/gzkit/complexity/cognitive.py` and its tests. Only import paths
and the module named in the usage line changed.

## Development

```bash
uv sync --locked
uv run --locked python -m unittest discover -s tests -v
```
