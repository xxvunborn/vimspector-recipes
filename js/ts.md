# Typescript recipe

Install the adapter for Node: `install_gadget.py --force-enable-node` in vimspector folder
This configuration is dependent of `ts-node`
(be sure to update the lasted vimspector and node)

Create `.vimspector.json` file in the root of the folder with this configuration

```
{
  "configurations": {
    "run": {
      "adapter": "vscode-node",
      "configuration": {
        "name": "Launch index.ts",
        "type": "node",
        "request": "launch",
        "runtimeArgs": ["-r", "ts-node/register"],
        "args": ["${workspaceFolder}/src/index.ts"]
      }
    }
  }
}
```

opem `nvim`, add `breakpoint` with `F9` in `.test` files you want to test and run with `F5`
