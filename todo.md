- detect network up / network down
- detect registry down based on the target URL, so that you don't need to wait so long
- add support for fallback registries
- add support for alternative targets:
  - URLs ad dependencies (tarball target)
  - Git URLs as dependencies
    - git://github.com/user/project.git#commit-ish
    - git+ssh://user@hostname:project.git#commit-ish
    - git+ssh://user@hostname/project.git#commit-ish
    - git+http://user@hostname/project/blah.git#commit-ish
    - git+https://user@hostname/project/blah.git#commit-ish
  - GitHub URLs
    - user/foo-project

- more robust caching
  - during startup, iterate over cache content and list it
  - use minitask.cache for caching
  - allow querying cache by MD5 hash to avoid wasting disk space
  - make the cache use the first two chars to split files into folders to avoid issues with really large folders
