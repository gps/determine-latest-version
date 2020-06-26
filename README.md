# Determine Latest Version GitHub Action

This action looks at git tags in a repository that begin with `v`, and are of format `x.y.z`, where `x`, `y`, and `z` are integers that represent the major, minor, and patch versions respectively. It then sets an output with the latest `x.y.z` version.

## Inputs

### `gh_token`

The GitHub token used to authenticate with GitHub.

**Required**

### `tag_prefix`

Prefix to look for in version tags.

**Required**

**Default Value** 

If unspecified, assumed to be `v`.

## Outputs

### `latest_build_version`

Latest build version found.

## Example Usage

```yml
- name: Determine latest version
  uses: gps/determine_latest_version@master
  id: latest_version
  with:
    GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}
    TAG_PREFIX: v
```
