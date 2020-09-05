# React recipe

Install the adapter for Chrome: `:VimspectorInstall debugger-for-chrome` or `./install_gadget.py --force-enable-chrome` in vimspector folder

Create `.vimspector.json` file in the root of the folder with this configuration

```
{
  "configurations": {
    "launch": {
      "adapter": "chrome",
      "configuration": {
        "name": "Chrome",
        "type": "chrome",
        "request": "launch",
        "url": "http://localhost:3000",
        "webRoot": "${workspaceRoot}/src"
      }
    }
  }
}
```

Run the server with `npm start`

opem `nvim`, add `breakpoint` with `F9` wherever you want to test and run with `F5`
