# GitHub Action - Update Release

This GitHub Action wraps the [GitHub Release API](https://docs.github.com/en/rest/releases/releases), specifically the [Update a Release](https://docs.github.com/ko/rest/releases/releases#update-a-release) endpoint, to allow you to leverage GitHub Actions to update releases.

## Usage

### Inputs
For more information on these inputs, see the [Update a Release](https://docs.github.com/ko/rest/releases/releases#update-a-release)

- `github_token`: "Contents" repository permissions (write).
- `owner`: Owner of the repository if it is not the current one.
- `repository`: Repository on which to release. Used only if you want to create the release on another repository.
- `commitish`: Any branch or commit SHA the Git tag is created from, unused if the Git tag already exists.
- `tag_name`: The name of the tag. This should come from the webhook payload, `github.GITHUB_REF` when a user pushes a new tag.
- `prerelease`: `true` to identify the release as a prerelease. `false` to identify the release as a full release.