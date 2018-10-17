# Docker-Serverless
This Docker image contains NodeJS & NPM, the Serverless Framework and Python 3 & Pip.

To use these image locally as part of a development workflow it is convenient to define a (function) alias in your shell environment:

```
function sls() {
  docker run --rm -it --volume=$PWD:/workspace -v ~/.aws/credentials:/root/.aws/credentials serverless:1.32.0 serverless "$@"
}
```

If you want to use a different version of the Serverless Framework just replace it with a different version tag.
