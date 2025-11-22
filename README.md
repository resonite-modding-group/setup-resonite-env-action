# Setup Resonite Environment Action
Github action to setup Resonite for building plugins and mods


## Usage
```yml
- name: Setup build environment
  id: build-env
  uses: resonite-modding-group/setup-resonite-env-action@v0.1.0
  with:
    steam-user: ${{ secrets.STEAMUSER }}
    steam-password: ${{ secrets.STEAMPASS }}
```

## Inputs

| Name              | Description                                                                              | Required | Default     |
| ----------------- | ---------------------------------------------------------------------------------------- | -------- | ----------- |
| `resonite-path`   | Path to where Resonite will be installed                                                 | no       | `/Resonite` |
| `steam-user`      | Steam username for SteamCMD (Provide via a secret: `secrets.STEAMUSER`)                  | yes      | —           |
| `steam-password`  | Steam password for SteamCMD (Provide via a secret: `secrets.STEAMPASS`)                  | yes      | —           |
| `branch`          | Branch of Resonite to use (`public`, `prerelease`, `headless`)                           | no       | `public`    |
| `branch-password` | Branch password if using a protected branch (Provide via a secret: `secrets.BRANCHPASS`) | no       |             |

## Outputs

| Name             | Description                                |
| ---------------- | ------------------------------------------ |
| `resonite-path`  | Path to the `Resonite` install directory   |
| `libraries-path` | Path to the `Resonite\Libraries` directory |
