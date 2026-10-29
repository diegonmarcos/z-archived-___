# z-archived-___

Registry index for the archived repos (every `z-archived_*`) - same model as `CG-___`, `DeepSc-___` and `cloudy-___`. This repo is an INDEX, not a container: it holds `repos.json` (a subset of _git-repos-master/repos.json), `clone.sh` (pick which repos to have locally) and one committed relative symlink per member (`<member> -> ../<member>`); the clones live as siblings in `~/git/`. In _git-repos-master these repos sit in `09.Archived/`.

## Members

- [z-archived_My-ai-memory](https://github.com/diegonmarcos/z-archived_My-ai-memory) (private) - Archived AI memory repo. Registered 2026-10-29 (#1291) so 09.Archived holds every z-archived_*.
- [z-archived_c3-infra-plugin](https://github.com/diegonmarcos/z-archived_c3-infra-plugin) (private) - Archived former c3-infra plugin repo; the plugin source of truth is cloudy-u-linux da_my-ai/data/claude/cloud-marketplace/c3-infra. Registered 2026-10-29 (#1291) so 09.Archived holds every z-archived_*.
- [z-archived_cloud-me-pub-data](https://github.com/diegonmarcos/z-archived_cloud-me-pub-data) - The owner's PUBLIC data (the public half of cloud-me). Added 2026-10-21 (#1073): cloud-drive seeded it but this registry did not list it.
- [z-archived_cloud-me-pvt-data-private](https://github.com/diegonmarcos/z-archived_cloud-me-pvt-data-private) (private) - Archived 2026-10-28: stale skeleton (per-app backups, AI sessions, Maps history, Financial), superseded by cloud-me-pvt-data; was cloud-me_data-private, registered then renamed z-archived_ the same day.
- [z-archived_cloud-me-pvt-legacy](https://github.com/diegonmarcos/z-archived_cloud-me-pvt-legacy) (private) - The original cloud-me repo (cloud-me family, near empty), kept as is under the pvt family. Registered 2026-10-28 (was unregistered_ok since #1073).
- [z-archived_front-data](https://github.com/diegonmarcos/z-archived_front-data) - Front-end content and data. Renamed z-archived_front-data 2026-10-23; to be archived on GitHub (owner click).
- [z-archived_front-feeds](https://github.com/diegonmarcos/z-archived_front-feeds) - Superseded 2026-10-25 (#1196): its projects moved into CG-circus; renamed z-archived_front-feeds, to be archived on GitHub (owner click)
- [z-archived_front-individual](https://github.com/diegonmarcos/z-archived_front-individual) - Superseded 2026-10-25 (#1196): its projects moved into cloud-me-pub-profiles-prf-prs (b_Profiles); renamed z-archived_front-individual, to be archived on GitHub (owner click)
- [z-archived_front-linktree](https://github.com/diegonmarcos/z-archived_front-linktree) - Superseded 2026-10-27 (#1217): linktree sources moved into cloud-me-pub-profiles-_lnktree (Lnktree); renamed z-archived_front-linktree. Originally split from diegonmarcos.github.io (#1072).
- [z-archived_front-media](https://github.com/diegonmarcos/z-archived_front-media) - Superseded 2026-10-25 (#1196): its projects moved into cloud-me-pub-profiles-prf-prs (b_Profiles); renamed z-archived_front-media, to be archived on GitHub (owner click)
- [z-archived_front-others](https://github.com/diegonmarcos/z-archived_front-others) - Superseded 2026-10-25 (#1196): its projects moved into CG-circus; renamed z-archived_front-others, to be archived on GitHub (owner click)
- [z-archived_front-projects](https://github.com/diegonmarcos/z-archived_front-projects) - Superseded 2026-10-24 by the 12 per-group front repos (#1072); renamed z-archived_front-projects, to be archived on GitHub (owner click).
- [z-archived_front-warehouse](https://github.com/diegonmarcos/z-archived_front-warehouse) - Superseded 2026-10-25 (#1196): its projects moved into front-endeavours; renamed z-archived_front-warehouse, to be archived on GitHub (owner click)

## Usage

```
./clone.sh                list what exists and what does not
./clone.sh <name>...      clone those, then link them
./clone.sh --all          clone every member
./clone.sh --link         relink whatever is already cloned
./clone.sh --relink       rewrite every link from the registry
./check-repos-sot.sh      verify repos.json against _git-repos-master
```

`repos.json` is a SUBSET of `~/git/_git-repos-master/repos.json` (the superset index of every repo this account owns): identical name/url/private/doc fields, checked by `./check-repos-sot.sh`.

## Hub submodule

This hub's parent is `_git-repos-master`, mounted as a git submodule at `0_hub/_git-repos-master` (one fixed path convention for every repo; URL https://github.com/diegonmarcos/_git-repos-master.git, pinned to its main). Every member mounts this hub at `0_hub/z-archived-___`. Only the upward link is a submodule; this hub keeps symlinks (not submodules) to its members, so there are no cycles. Source of truth: `repos.json` in _git-repos-master (`parent_hub` / `hub`, `_hub_submodule_doc`), guarded by `node repos-sot.js check-hubs`.
