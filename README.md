# Repo Check

Repo Check is a CLI tool that lists out all local git repos in a directory along with
additional information such as the last modified date of the repo, whether the
repo is synced with remote etc.

![repocheck cli output](docs/demo.png)

## Installation

Install go v1.22 or later - [Official installation instructions](https://go.dev/doc/install)

To download and install repocheck, run:

`go install github.com/bevane/repocheck@latest`

## Usage

### Basic Usage

Command help

`repocheck -h` or `repocheck --help`

Running repocheck without any args will list the repos in current directory

`repocheck`

Target directory can be passed in as an arg either as a relative path or an absolute path

`repocheck projects`

`repocheck /home/user/projects`

### Additional flags

Sort flag `-s` or `--sort` can be used to sort the results by a specific key

`repocheck --sort=name` to sort by repo name

`repocheck -s=synced` to sort by sync status of the repo - unsynced repos will be at the top


# Planned features
- [ ] Add flag to filter the results by last modified date and sync status
- [ ] Add flag for plain output to only output the absolute paths of the repos
- [ ] Add flag for json output
- [ ] Add head and tail flag to limit output

# License
Repo Check is released under the MIT License
