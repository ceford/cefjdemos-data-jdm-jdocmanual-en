<!--
{
  "source": "https://jdocmanual.org/jdocmanual?article=jdm/data-management/data-entry-in-vscode",
  "title": "Data Entry in VSCode",
  "description": "Jdocmanual is a Joomla component designed for the display of multi-lingual technical information.", 
  "author": "Clifford E Ford"
}
-->

## About VSCode and VScodium

> From WikiPedia: Visual Studio Code, also commonly referred to as VS Code, is a source-code editor developed by Microsoft for Windows, Linux and macOS. Features include support for debugging, syntax highlighting, intelligent code completion, snippets, code refactoring, and embedded Git. Users can change the theme, keyboard shortcuts, preferences, and install extensions that add functionality.

[VSCodium](https://vscodium.com/) is a fork of [VSCode](https://code.visualstudio.com/) free of tracking data. These two applications are virtually identical. There is no need to mention any differences here. Where VSCode is mentioned just read VSCodium if that is your preference.

## Open the Repository Folder

The following screenshot shows the normal VSCode layout with the source tree of folders and files to the left and the edit area to the right:

![screenshot showing layout of vscode](../../../en/images/data-management/data-entry-in-vscode/00-vscode-layout.png)

## Preview

To see what your article will look like use the keyboard shortcut to open the preview tab. On a Mac that is `Shift+Command+V`.

![screenshot showing a rendered preview of a markdown file](../../../en/images/data-management/data-entry-in-vscode/01-vscode-preview.png)

## Markdown Edit

Markdown editing is intended to be simple! Hashes (`#`) at the start of a line for headings, 1-6 hashes for 1-6 level headings. Never use h1 as that is usually set in the overall layout. Start with h2 and use semantic markup (do not skip heading levels). Blank lines are used to separate paragraphs. Summary sheets for other markup features are available elsewhere.

## Autosave

VSCode has an enormous number of configuration options that you can change to suit yourself. A good one to use is to save content onFocusChange. Use the Code / Settings to find the Files: Autosave item and set it as you see fit.

## Git Commit & Push

In the left sidebar there is a Source Control icon. Try it! If you have not set up a Git repository you will see a button labelled **Initialize Repository**. Try it! Instantly you will see a list of *Untracked* files. At the top there is a box for entry of a short commit message. The Commit action list allows for a simple commit to the repository just created or a commit and push to a remote repository if one has been created.

![screenshot showing the source control column](../../../en/images/data-management/data-entry-in-vscode/02-vscode-source-control.png)

Enter a Commit message and select the Commit button. You will be prompted to confirm 