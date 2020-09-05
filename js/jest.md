# Jest recipe

Install the adapter for Node: `install_gadget.py --force-enable-node` in vimspector folder
(be sure to update the lasted vimspector and node)

Create `.vimspector.json` file in the root of the folder with this configuration

```
{
  "configurations": {
    "run": {
      "adapter": "vscode-node",
      "configuration": {
        "name": "Debug CRA Tests",
        "type": "node",
        "request": "launch",
        "runtimeExecutable": "${workspaceRoot}/node_modules/.bin/react-scripts",
        "args": ["test", "--runInBand", "--no-cache", "--watchAll=false"],
        "cwd": "${workspaceRoot}",
        "protocol": "inspector",
        "console": "integratedTerminal",
        "internalConsoleOptions": "neverOpen",
        "env": { "CI": "true" },
        "disableOptimisticBPs": true
      }
    }
  }
}
```

opem `nvim`, add `breakpoint` with `F9` in `.test` files you want to test and run with `F5`
