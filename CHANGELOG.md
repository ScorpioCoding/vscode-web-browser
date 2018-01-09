# Change Log
All notable changes to the "testeample" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.


## Branch - Hotfixes
1. added : added CHANGELOG.md to track changes made to git.Branches
2. changed : .gitignore : added package-lock.json
3. changed : .vscodeignore : added package-lock.json
4. changed : pachage.json : changed the devDependencies versions of
    * "vscode": "^0.11.0"       => "^0.11.18"
    * "typescript": "^1.8.5"    => "^2.6.2" 
5. added : extention.js - added by typescript-compiler tsc src/extention.ts --target ES5
6. changed : .vscode/launch.json changed deprecated config command outDir to outFiles which is an array
7. changed : .vscode/task.json changed deprecated config command "isWatching" to "isBackground"
8. changed : tsconfig.json command typscript compiler "target" from es5 to es6
    * got to change this to be able to update the devDependecy : typescript
9. changed : launch.json changed commands:
    * name : "Launch Extension" => "Extension"
    * name : "Launch Tests"     =>  "Extention Test"
    * preLaunchTask(both) : "npm"     =>  "npm watch"
    * outFiles :  ["${workspaceRoot}/out/src"]  =>   ["${workspaceRoot}/out/src/**/*.js"],
10. changed : package.json 
    * scripts : 
        - removed
            - "vscode:prepublish": "node ./node_modules/vscode/bin/compile",
            - "compile": "node ./node_modules/vscode/bin/compile -watch -p ./",
        - added
            - "vscode:prepublish": "npm run compile",
            - "compile": "tsc -p ./",
            - "watch": "tsc -watch -p ./",
    * engines
        - updated version "vscode": "^1.0.0" => "vscode": "^1.19.0"
11. Added new folder : Deprecated
12. Moved .vscode/task.json => deprecated/task.json
13. Added new .vscode/task.json version 2.0.0
14. Fixed error cannot find 'vscode' module in file extension.ts
    * Changed : package.json - changed devDependencies
        - "vscode": "^0.11.0"       => "vscode": "^1.1.10"
15. Issue : Compile Issue Ts Properties
    * File : src/extension.ts
    * [ts] Property 'startsWith' does not exist on type 'string'
    * [ts] Property 'push' does not exist on type '{}'
16. Fixed Ts Property issues
    * Issue is due to compile --target ES6 doesn't work
    * Changed tsconfig.json
        Changed "noLib": true => false
        Added "lLib": ["es5", "es6", "es7"]
17. Issue : Compile Issues Typings reference path not found
    * File : typings/node.d.ts
    * File : typings/vscode-typings.d.ts
18. Fixed Typings Reference path not found
    * Added : devDependecy "@types/node": "^9.3.0",
    * Changed : File : typings/node.d.ts
        - changed path from : path="../node_modules/@typings/node/index.d.ts"
        - changed path to : path="./../node_modules/@types/node/index.d.ts"
    * Changed : File : typings/vscode-typings.d.ts
        - changed path from : path="../node_modules/vscode/typings/index.d.ts"
        - changed path to : path="./../node_modules/vscode/vscode.d.ts"
19. Changed : File : extension.ts - Added Extra Important Styling to the iFrame
    * Added : top: 0; left: 0; position: fixed; background-color:white;
    * Important : cause without the iFrame doesn't show.
20. Changed : The Build, Watch, Debug process

### Test Build Hotfix
    - Build a test Version and installed it locally into my VSCode with success and it runs like a charm
    - ScorpioCoding has created an updated and working version







## [Unreleased]
- Initial release