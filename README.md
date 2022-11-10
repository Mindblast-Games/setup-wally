# setup-wally
GitHub action to set [Wally](https://github.com/UpliftGames/wally) and Git credentials, and install packages.

## Usage
**Method 1:** Installing Wally with another action

```yml
steps:
  - uses: ok-nick/setup-aftman@v0.3
  - uses: Mindblast-Games/setup-wally@v1.0.0

# OR (deprecated)

steps:
  - uses: Roblox/setup-foreman@v1
  - uses: Mindblast-Games/setup-wally@v1.0.0
```

**Method 2:** Installing Wally in-action
```yml
steps:
  - uses: Mindblast-Games/setup-wally@v1.0.0
    with:
      install-aftman: true

# OR (deprecated)

steps:
  - uses: Mindblast-Games/setup-wally@v1.0.0
    with:
      install-foreman: true

# In either case, it is assumed wally has been added to an aftman.toml or foreman.toml file
```

### Parameters
|name|description|default|
|---|---|---|
|`install-aftman`| Should Aftman be installed |`false`|
|`install-foreman`| Should Foreman be installed |`false`|
|`install-packages`| Should `wally install` be run |`true`|
|`token`| Token for publishing packages or accessing private registries | - |
|`registry`| The registry endpoint to set an auth token for |https://api.wally.run/|
|`git-credentials`| Credentials to access private registry repositories | - |
