REACT RECIPE FOR VIMINSPECTOR

Install the adapter for go: `:VimspectorInstall vscode-go` in the terminal or `./install_gadget.py --enable-go` in the vimspector folder
Install devle `go get -u github.com/go-delve/delve/cmd/dlv`

Create `.vimspector.json` file in the root of the folder with this configuration

```
{
  "configurations": {
    "run": {
      "adapter": "vscode-go",
      "configuration": {
        "request": "launch",
        "program": "${fileDirname}/<path-of-your-test-file>.go",
        "mode": "debug",
        "dlvToolPath": "$HOME/go/bin/dlv"
      }
    }
  }
}
```

where `<path-of-your-test-file>` is the actual path of the file before the root folder of `.vimspector.json`

opem `nvim`, add `breakpoint` with `F9` wherever you want to test and run with `F5`
