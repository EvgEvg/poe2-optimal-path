# poe2-optimal-path

Pick multiple talents points on poe2 talent graph (1500+ nodes). Calculate the most optimal way to connect all of them. This is not the approximation, this is the perfect solution.

## Dependencies

Skill tree data is vendored as a git submodule:

- `poe2-skilltree-export/` — [grindinggear/poe2-skilltree-export](https://github.com/grindinggear/poe2-skilltree-export)
  - `data.json` — passive skill tree graph
  - `assets/` — tree rendering assets

The submodule tracks the `main` branch of the upstream repo (not a fixed tag).

### Clone

```bash
git clone --recurse-submodules https://github.com/EvgEvg/poe2-optimal-path.git
```

### Updating the skill tree data

Git submodules always record a **specific commit** in this repo. There is no built-in “always latest” mode — you choose when to bump that commit.

**Pull latest upstream data into your working tree:**

```bash
git submodule update --remote poe2-skilltree-export
```

Then commit the submodule pointer change if you want to save/share it:

```bash
git add poe2-skilltree-export
git commit -m "Update poe2-skilltree-export"
```

**When someone else already bumped the submodule** (you just want to match this repo):

```bash
git pull --recurse-submodules
```

**Convenience alias** — pull this repo and refresh the submodule to latest upstream `main`:

```bash
git config alias.pull-all '!git pull && git submodule update --remote --merge poe2-skilltree-export'
git pull-all
```

Optional: make submodule commands run automatically on every `git pull` in this repo:

```bash
git config submodule.recurse true
```
