# GDS open source web site

## How to update the list of projects and their data

Run:

```bash
bundle exec rake update_repo_data
```

You will then need to commit the updated data into Git:

```bash
git commit _data/repos.yml
```
