# vscode-language-extensions
vscode language extensions for onscripter and mangagamer higurashi scripts

# How to install and use the language extensions
- download the language extension package from the releases page
- open vscode
- click the "Extensions" button, or press CTRL-SHIFT-X
- click the 'three dots' menu button at the top of the left hand sidebar which popped up
- click install from VSIX
- after installation, you will be asked to reload vscode.
- NOTE: all .txt files will use the mangagamer syntax, and all .utf files will use the onscripter syntax highlighting. you can manually change the highlighting method by clicking on the "Select Language Mode" button at the bottom right of the vscode window

# For Developers Only:

## How to modify and test
- Open the extension folder (higurashimg/onscripter) in visual studio code (as a whole folder).
- Hit F5 to start debugging. This will open a new vscode instance with the extension loaded.
- Edit the .tmLangauge.json file in the syntax folder
- Make sure vscode regonizes the .tmlLanguage.json file (eg it shows errors and syntax higlighting in the editor) otherwise it's hard to edit
- Remember that trailing commas in arrays are NOT allowed.

## How to export a language VSIX file
- Install npm for your system
- Install vsce: `npm install -g vsce`
- Run `vsce package` while inside the extension folder you want to export

Note that you don't need to properly 'publish' the file to the marketplace, as is described on this page: https://code.visualstudio.com/docs/extensions/publish-extension

## How to make a new laguage
- Follow the instructions on this page to install and run 'Yo Code': https://code.visualstudio.com/docs/extensions/yocode
- run `yo code` and choose `New Language Support`, then fill in the options you want.

Some information about the language is here, but be warned it's not quite exactly the same syntax (it's for TextMate, not vsCode JSON): https://www.apeth.com/nonblog/stories/textmatebundle.html
