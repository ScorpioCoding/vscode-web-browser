# Change Log
All notable changes to the "testeample" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.


## Branch - Issue-3 - Display Title
1. Changed : File : extensions.ts
    - Added an extra parameter to the return command
    - Changed from :         
        ```
        return vscode.commands.executeCommand('vscode.previewHtml', uri, col).then((success)
        ```
    - Changed to :
        ```
        return vscode.commands.executeCommand('vscode.previewHtml', uri, col, uri.toString()).then((success)
        ```
2. Changed : File : CHANGELOG







## [Unreleased]
- Initial release