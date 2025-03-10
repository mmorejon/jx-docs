---
date: 2019-11-27T00:59:08Z
title: "jx step syntax validate pipeline"
slug: jx_step_syntax_validate_pipeline
url: /commands/jx_step_syntax_validate_pipeline/
---
## jx step syntax validate pipeline

Validates a pipeline YAML file

### Synopsis

Validates the pipeline YAML file in the current directory for the given context, or jenkins-x.yml by default

```
jx step syntax validate pipeline [flags]
```

### Examples

```
  # validates the jenkins-x.yml in the current directory
  jx step syntax validate pipeline
  
  # validates the jenkins-x-bdd.yml file in the current directory
  jx step syntax validate pipeline --context bdd
```

### Options

```
  -c, --context string   The context for the pipeline YAML to validate instead of the default.
  -d, --dir string       The directory to query to find the pipeline YAML file
  -h, --help             help for pipeline
```

### Options inherited from parent commands

```
  -b, --batch-mode   Runs in batch mode without prompting for user input (default true)
      --verbose      Enables verbose output
```

### SEE ALSO

* [jx step syntax validate](/commands/jx_step_syntax_validate/)	 - validate [command]

###### Auto generated by spf13/cobra on 27-Nov-2019
