---
title: "pulumi preview"
aliases:
  - /docs/reference/cli/pulumi_preview/
---



Show a preview of updates to a stack's resources

## Synopsis

Show a preview of updates a stack's resources.

This command displays a preview of the updates to an existing stack whose state is
represented by an existing state file. The new desired state is computed by running
a Pulumi program, and extracting all resource allocations from its resulting object graph.
These allocations are then compared against the existing state to determine what
operations must take place to achieve the desired state. No changes to the stack will
actually take place.

The program to run is loaded from the project in the current directory. Use the `-C` or
`--cwd` flag to use a different directory.

```
pulumi preview [flags]
```

## Options

```
  -c, --config stringArray                    Config to use during the preview and save to the stack config file
      --config-file string                    Use the configuration values in the specified file rather than detecting the file name
      --config-path                           Config keys contain a path to a property in a map or list to set
  -d, --debug                                 Print detailed debugging output during resource operations
      --diff                                  Display operation as a rich diff showing the overall change
      --expect-no-changes                     Return an error if any changes are proposed by this preview
  -h, --help                                  help for preview
      --import-file string                    Save any creates seen during the preview into an import file to use with 'pulumi import'
  -j, --json                                  Serialize the preview diffs, operations, and overall output as JSON
  -m, --message string                        Optional message to associate with the preview operation
  -p, --parallel int                          Allow P resource operations to run in parallel at once (1 for no parallelism). (default 16)
      --policy-pack strings                   Run one or more policy packs as part of this update
      --policy-pack-config strings            Path to JSON file containing the config for the policy pack of the corresponding "--policy-pack" flag
  -r, --refresh string[="true"]               Refresh the state of the stack's resources before this update
      --replace stringArray                   Specify resources to replace. Multiple resources can be specified using --replace urn1 --replace urn2
      --show-config                           Show configuration keys and variables
      --show-policy-remediations              Show per-resource policy remediation details instead of a summary
      --show-reads                            Show resources that are being read in, alongside those being managed directly in the stack
      --show-replacement-steps                Show detailed resource replacement creates and deletes instead of a single step
      --show-sames                            Show resources that needn't be updated because they haven't changed, alongside those that do
      --show-secrets false                    Emit secrets in plaintext in the plan file. Defaults to false
  -s, --stack string                          The name of the stack to operate on. Defaults to the current stack
      --suppress-outputs                      Suppress display of stack outputs (in case they contain sensitive values)
      --suppress-permalink string[="false"]   Suppress display of the state permalink
      --suppress-progress                     Suppress display of periodic progress dots
  -t, --target stringArray                    Specify a single resource URN to update. Other resources will not be updated. Multiple resources can be specified using --target urn1 --target urn2
      --target-dependents                     Allows updating of dependent targets discovered but not specified in --target list
      --target-replace stringArray            Specify a single resource URN to replace. Other resources will not be updated. Shorthand for --target urn --replace urn.
```

## Options inherited from parent commands

```
      --color string                 Colorize output. Choices are: always, never, raw, auto (default "auto")
  -C, --cwd string                   Run pulumi as if it had been started in another directory
      --disable-integrity-checking   Disable integrity checking of checkpoint files
  -e, --emoji                        Enable emojis in the output
  -Q, --fully-qualify-stack-names    Show fully-qualified stack names
      --logflow                      Flow log settings to child processes (like plugins)
      --logtostderr                  Log to stderr instead of to files
      --memprofilerate int           Enable more precise (and expensive) memory allocation profiles by setting runtime.MemProfileRate
      --non-interactive              Disable interactive mode for all commands
      --profiling string             Emit CPU and memory profiles and an execution trace to '[filename].[pid].{cpu,mem,trace}', respectively
      --tracing file:                Emit tracing to the specified endpoint. Use the file: scheme to write tracing data to a local file
  -v, --verbose int                  Enable verbose logging (e.g., v=3); anything >3 is very verbose
```

## SEE ALSO

* [pulumi](/docs/cli/commands/pulumi/)	 - Pulumi command line

###### Auto generated by spf13/cobra on 23-Aug-2024
