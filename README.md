# poe2-optimal-path

Pick multiple talents points on poe2 talent graph (1500+ nodes). Calculate the most optimal way to connect all of them. This is not the approximation, this is the perfect solution.

## Dependencies

Skill tree data is vendored as a git submodule:

- `poe2-skilltree-export/` — [grindinggear/poe2-skilltree-export](https://github.com/grindinggear/poe2-skilltree-export)
  - `data.json` — passive skill tree graph
  - `assets/` — tree rendering assets

Clone with submodules:

```bash
git clone --recurse-submodules https://github.com/EvgEvg/poe2-optimal-path.git
```

Update the skill tree data to the latest upstream release:

```bash
git submodule update --remote poe2-skilltree-export
```
