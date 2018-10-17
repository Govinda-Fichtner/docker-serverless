# Docker-Serverless
This Docker image contains NodeJS & NPM, the Serverless Framework and Python 3 & Pip.

To use this image locally as part of a development workflow it is convenient to define a (function) alias in your shell environment.
Add the following text snippet into a file like ~/.bash_profile or ~/.zshrc.

```
function sls() {
  docker run --rm -it --volume=$PWD:/workspace -v ~/.aws/credentials:/root/.aws/credentials gfichtner/docker-serverless:latest serverless "$@"
}
```

Afterwards you can call it with

```
$ sls --version
```

If you want to use a different version of the Serverless Framework just replace it with a different version tag.
