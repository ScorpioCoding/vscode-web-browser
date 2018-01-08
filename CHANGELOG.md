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


## [Unreleased]
- Initial release