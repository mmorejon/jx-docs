---
date: 2019-11-27T00:59:08Z
title: "jx step create pullrequest go"
slug: jx_step_create_pullrequest_go
url: /commands/jx_step_create_pullrequest_go/
---
## jx step create pullrequest go

Creates a Pull Request on a git repository updating a go module dependency

### Synopsis

Creates a Pull Request to change a go module dependency, updating the go.mod and go.sum files to use a new version 

Files named Makefile or Makefile. * will be updated

```
jx step create pullrequest go [flags]
```

### Examples

```
  # update a go dependency
  jx step create pr go --name github.com/myorg/myrepo --version v1.2.3 --repo https://github.com/jenkins-x/cloud-environments.git
  
  # update a go dependency using a custom build step (to update the 'go.sum' file)
  jx step create pr go --name github.com/myorg/myrepo --version v1.2.3 --build "make something" --repo https://github.com/jenkins-x/cloud-environments.git
```

### Options

```
      --base string        The branch to create the pull request into (default "master")
      --branch string      Branch to clone and generate a pull request from (default "master")
      --build string       The build command to update the 'go.sum' file after the change to the source (default "make build")
      --component string   The component of the git repo which caused this change; useful if you have a complex or monorepo setup and want to differentiate between different components from the same repo
      --dry-run            Perform a dry run, the change will be generated and committed, but not pushed or have a PR created
      --fail-on-build      Should we fail to create the Pull Request if the build command fails. Its common for incompatible changes to the go code to fail to build so we usually want to go ahead with the Pull Request anyway
  -h, --help               help for go
      --name string        The name of the go module dependency to use when doing updates
  -r, --repo stringArray   Git repo to update
      --skip-auto-merge    Disable auto merge of the PR if status checks pass
      --src-repo string    The git repo which caused this change; if this is a dependency update this will cause commit messages to be generated which can be parsed by jx step changelog. By default this will be read from the environment variable REPO_URL
  -v, --version string     The version to change. If no version is supplied the latest version is found
```

### Options inherited from parent commands

```
  -b, --batch-mode   Runs in batch mode without prompting for user input (default true)
      --verbose      Enables verbose output
```

### SEE ALSO

* [jx step create pullrequest](/commands/jx_step_create_pullrequest/)	 - create pullrequest [command]

###### Auto generated by spf13/cobra on 27-Nov-2019
