# Higurashi and Umineko Syntax highlighters

vscode and npp language extensions for onscripter (vscode only) and mangagamer higurashi scripts (vscode and Notepad++)

## How to install and use the language extensions

### Visual Studio Code

**NOTE: double clicking the .VSIX file to install the extension WILL FAIL. You MUST follow the instructions below!**

- download the language extension package from the releases page
- open vscode
- click the "Extensions" button, or press CTRL-SHIFT-X
- click the 'three dots' menu button at the top of the left hand sidebar which popped up
- click install from VSIX
- after installation, you will be asked to reload vscode.
- NOTE: `.txt` files used by Higurashi won't have syntax highlighting by default and it has to be enabled manually. However, `.utf` and `.u` files will use the onscripter syntax highlighting by default. You can manually change the highlighting method by clicking on the "Select Language Mode" button at the bottom right of the vscode window

### Notepad++ (Only for Mangagamer Higurashi Scripts)

- Download [this User Defined Language xml file](https://github.com/07th-mod/script-syntax-highlighters/raw/master/higurashimg-npp/HigurashiMG-NPP.xml) for Mangagamer Higurashi scripts
- Click the "Language" button in the toolbar.
- Click "User Defined Language"->"Define Your Language..."
- Click the "Import..." button at the top left of the "User Defined Language" popup
- Find and choose the xml file downloaded earlier
- A new user language should appear as "HigurashiMG"
- Decide which of the two below options you want
    1. If you want all .txt files to open with this syntax highlighting, write `txt` in the "Ext." textbox (without the `.`). This might be useful if you exclusively use Notepad++ only for editing Higurashi.
    2. Otherwise, you will have to manually choose the syntax higlighting each time you open a script file by clicking "Language" in the top toolbar, then "HigurashiMG" at the bottom of the dropdown.

----

## For Developers Only

The below section is only for people modifying the syntax higlighters.

## Modifying Notepad++ Languages

Generally, the process involves opening the "User Defined Language" popup as per the installation instructions. Then you can modify each textbox to set each syntax highlighting activation keywords and styling.

The [npp user manual](https://npp-user-manual.org/docs/user-defined-language-system/) has more information.

## Modifying Visual Studio Code Languages

### How to modify and test

- Open the extension folder (higurashimg/onscripter) in visual studio code (as a whole folder).
- Hit F5 to start debugging. This will open a new vscode instance with the extension loaded.
- Edit the .tmLangauge.json file in the syntax folder
- Make sure vscode regonizes the .tmlLanguage.json file (eg it shows errors and syntax higlighting in the editor) otherwise it's hard to edit
- Remember that trailing commas in arrays are NOT allowed.

### How to export a language VSIX file

- Install npm for your system
- Install vsce: `npm install -g vsce`
- Run `vsce package` while inside the extension folder you want to export

Note that you don't need to properly 'publish' the file to the marketplace, as is described on this page: https://code.visualstudio.com/docs/extensions/publish-extension

### How to make a new laguage

- Follow the instructions on this page to install and run 'Yo Code': https://code.visualstudio.com/docs/extensions/yocode
- run `yo code` and choose `New Language Support`, then fill in the options you want.

Some information about the language is here, but be warned it's not quite exactly the same syntax (it's for TextMate, not vsCode JSON): https://www.apeth.com/nonblog/stories/textmatebundle.html
