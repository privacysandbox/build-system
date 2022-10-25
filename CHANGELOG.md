# Changelog

All notable changes to this project will be documented in this file. See [commit-and-tag-version](https://github.com/absolute-version/commit-and-tag-version) for commit guidelines.

## 0.1.0 (2022-10-25)


### Features

* Add --env flag to cbuild
* Add arg processing to cbuild script
* Add aws-cli helper script
* Add bazel-debian helper script
* Add builders/utils docker image
* Add hadolint to lint Dockerfiles
* Add optional flags to cbuild tool
* Add preliminary support for commit-and-tag-version and copybara
* Add the release-please tool
* Add toolchain short hash to bazel output_user_root path
* Add tools/lib/builder.sh
* **build:** Add GitHub CLI tool https://cli.github.com/
* Determine workspace mount point from docker inspect if inside docker container
* Inject clang-version as a bazel action_env
* Migrate generation of builders/release container image to Dockerfile
* Move image directories to images/ top-level directory
* Overhaul building on amazonlinux2
* Remove python build dependencies from bazel
* Set BUILD_ARCH env var in docker images
* Update release image to node v18
* Upgrade to bazel 5.3.2
* Upgrade to clang v14 on bazel-debian
* Use Packer to build AMI.


### Bug Fixes

* Add builders/tools/normalize-dist to chmod/chgrp/chown dist/ directory tree
* Add get_workspace_mount function to encapsulate code block
* Add python version to action_env
* Add/remove basic pre-commit hooks
* Adopt shellcheck
* Avoid installing recommended debian packages
* Avoid use of git rev-parse to determine tools path
* Bump to latest version of bazelisk
* Clean bazel_root for smaller docker image
* Correct argument handling in cbuild script
* Correct errors generating Amazon Linux 2-based builder image
* Define python3 toolchain
* Drop packer from build-debian image
* Ensure /etc/gitconfig is readable by all
* Improve cbuild help text
* Install bazel version as specified in .bazelversion
* Invoke addlicense for all text files
* Modifications as indicated by shellcheck
* Mount $HOME/aws in aws-cli container
* Move bazel env vars from comments to help text
* Move builder-related configs to builders/etc
* Move WORKSPACE definition to cbuild script global
* Only propagate AWS env vars into amazonlinux2 build container
* Pin version of bazelisk
* Pin version of libc++-dev
* Pin version of python3.8
* Print pre-commit version rather than help
* Remove container when get-architecture exits
* Remove debugging statement
* Remove dockerfile linter ignore and correct ENTRYPOINT
* Remove pre-commit config from build-debian
* Remove shellcheck from build-debian
* Remove unused nitro_enclave_image bazel rule
* Set bazel output_base to accommodate distinct workspaces
* Set bazel output_user_root in image bazelrc
* Set locale in build-debian
* Set WORKSPACE correctly from submodule
* Set WORKSPACE variable
* Switch from hardcoded arch to using dpkg --print-architecture
* Update normalize-dist to function inside build container
* Update pre-commit to use cbuild
* Use PRE_COMMIT_TOOL env var
* Various path-related fixes


### Build System

* Add arch to docker image tags
* Add get_builder_image_tagged tool to determine a content-based tag
* Add get-architecture helper script
* Add missing imports into nitro BUILD
* Add tools/pre-commit
* Correct propagation of quoted args in gh wrapper
* Move commit-and-tag-version into tools dir
* Move gh into tools dir
* Optionally build the AMI
* Propagate status code in exit functions
* Reduce redundant installation commands
* Remove release-please tool
* Rename builders/bazel to build-debian
* Simplify use of npm image in container_run_and_commit()
* Support GH_TOKEN env var


### Documentation

* Add top-level README.md
* Improve prose in README.md
* Move docker build instructions to README.md
* Reformat and lint markdown
