# actions-copy-vc-runtime
GitHub Action: copy dependent VC++ runtime DLLs


## Requirements

* Windows runner
  * `windows-latest`, `windows-11-arm`, etc.
* MSVC environment (Developer Command Prompt)
  * `VCToolsRedistDir`, `VSCMD_ARG_TGT_ARCH`, etc.

Make sure to initialize MSVC before running this action:

```yaml
- uses: h20y60/actions-setup-msvc-env@v2
```


## Usage

### Inputs

```yaml
- uses: h20y6m/actions-copy-vc-runtime@v1
  with:
    # The target directory from which dependencies will be scanned and runtime DLLs will be copied.
    # Required.
    bindir:

    # File extensions to scan for dependencies.
    # Accepts comma or newline separated values.
    # Optional. Default is '.exe,.dll'.
    exts:

    # Additional directories from which dependencies will be scanned.
    # Accepts comma or newline separated values.
    # Optional.
    extradirs:
```
