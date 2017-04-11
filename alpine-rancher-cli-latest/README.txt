# Alpine with the latest Rancher CLI via Github API

This checks with the Github API for the most current linux-amd64 build of the Rancher CLI,
retrieves it with curl and wget, and installs it to `/usr/local/bin/rancher`

## Docker Hub Image:
`cmosetick/alpine-base:rancher-cli-latest`


## Build Examples

#### If for example you have a Github token for Homebrew in your current shell's environment:

`docker build . --build-arg github_token=$HOMEBREW_GITHUB_API_TOKEN -t cmosetick/alpine:rancher-cli-latest`

#### If you want to manually pass in a Github token to your build process:

`docker build . --build-arg github_token=1234567 -t cmosetick/alpine:rancher-cli-latest`


## Caveats
Note that this image does not leave the Github API token in the docker image, but it does use the
token passed to `--build-arg` everytime a build is kicked off. Please be aware of this.


## Resources

https://github.com/settings/tokens

https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/

https://github.com/blog/1509-personal-api-tokens
