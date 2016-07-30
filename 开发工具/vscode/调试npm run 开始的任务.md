1. Configure a new debug target in your .vscode/launch.json:
{
    "name": "Attach To npm",
    "type": "node",
    "request": "attach",
    "port": 5858,
    "address": "localhost",
    "restart": false,
    "sourceMaps": false,
    "outDir": null,
    "localRoot": "${workspaceRoot}",
    "remoteRoot": null
}
2. Config your npm to run the node with --debug-brk option:
"scripts": {
  "start": "node app.js",
  "debug": "node --debug-brk app.js"
  ...
3. Start your app from the shell as:
 $npm run debug
4. The program by default will be waiting in the port 5858 to attach the debugger
5. So, run the debugger in your visual code ("Attach To mpn").
6. Enjoy your debugger :)


