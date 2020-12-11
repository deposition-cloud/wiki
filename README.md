# Wiki

The genesis repo.

It's git submodules all the way down.

## Workflow

Identify a folder that's been growing too much.

```bash
git clone <your_project> <your_submodule>
cd <your_submodule>
git filter-branch --subdirectory-filter 'path/to/your/submodule' --prune-empty -- --all
```

Probably not the brightest way to do it; however, a good way to keep perfect history.

## TODO

Automate submodule creation and publishing

Trigger could be size of content

## Questions to ponder

- [ ] What to do with data and images?
  - [ ] Keep them close to the content, or
  - [ ] Link to a dbpedia type of repo?


