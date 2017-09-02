# JuliaDockerfiles

[![CircleCI](https://circleci.com/gh/invenia/JuliaDockerfiles/tree/master.svg?style=svg)](https://circleci.com/gh/invenia/JuliaDockerfiles/tree/master)

This packages contains Dockerfiles for Julia used to build [invenia/julia](https://hub.docker.com/r/invenia/julia/) and [invenia/julia-ci-extras](https://hub.docker.com/r/invenia/julia-ci-extras/).
They are built using [Circle CI](https://circleci.com).
Unfortunately there is no way to trigger builds automatically, so nightly builds may not be up to date.

## `julia`

This image is based on Ubuntu 16.04 and only adds curl and Julia.

## `julia-ci-extras`

This image is based on the `julia` image and adds a full version of git, compiler tools, commonly-used libraries like `libhdf5`, and [Coverage.jl](https://github.com/JuliaCI/Coverage.jl).

## Tags

`0.5-latest`, `0.6-latest`, and `latest` (nightly) are the currently available tags. Please submit a pull request or open an issue if you would like other versions to be made available.
