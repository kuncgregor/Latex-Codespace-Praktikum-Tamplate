
1. Login or Sign Up to [GitHub]
2. Use this as template or Fork.

    - **Use as Template (Recommended):** just Click on `Use this template` and `Create a new Repository` 
    
    Or,
    
    - **Fork:** Fork this repository or just 
    
3. Give it a name and select **Create Fork / Create repository from template**
4. Select **<> Code** > **CodeSpaces** > **Create Codespace on Main**
    ![tutorial](https://user-images.githubusercontent.com/54777542/224550678-32a949ae-3a9b-4e8d-a0f1-ad30ec429908.gif)

5. It will start installing. **You Have to wait for 2 mins in the first time**. After that it will take 2/3 seconds to open up

## Where is my PDF?

Generated PDFs will be saved to **`/PDF`** directory

## Editor Instructions

1. Pressing `Ctrl+S` will save the document and generate PDF in the **PDF** folder
2. To check the generated PDF click on the PDF file. However **It will take 20/30 seconds to open the preview for the first time. So, do not panic**. After that, it will generate and preview the pdf instantly.
3. Your code will be automatically saved and the PDF will generate automatically each time you edit something
4. You can see all the error logs in the **Terminal > Output > Latex Compiler** as well as in the Latex Workshop sidebar
5. If it shows **Error showing PDF** or in case of any inconvenience, just reload the browser or press `Ctrl+R`
6. **Just use it as you use Visual Studio Code**
7. Do not delete the `devcontainer.json` file. However you can edit the properties there to customize many things!

## To use with LuaLatex or any other Tex program

Add this line to your main .tex file

```tex
%!TEX program = <tex_program>
```

For example, to use **`LuaLatex`**:

```tex
%!TEX program = lualatex
```

## GitHub Copilot

 Wonderful news, people! [GitHub Copilot](https://github.com/features/copilot) has been integrated with this tool, thanks to [@thodson-hugs](https://github.com/thodson-hugs). This program will suggest the next command, sentence and paragraph based on your document and previous writings.

![copilot](https://user-images.githubusercontent.com/54777542/224550711-9927d67f-e63e-445e-9ff0-db7674d7acef.gif)

To turn this off just **remove** or **comment out** the `"GitHub.copilot"` extension from the extensions list in `./.devcontainer/devcontainer.json` file.

  ```json
   "extensions": [
        "...",
        //"GitHub.copilot",
        "..."
        ]
  ```

## Grammarly

This editor has built-in [Grammarly](https://www.grammarly.com/) support for `.tex` files.

To disable grammarly, you can just **remove** or **comment out** the `"ms-vsliveshare.vsliveshare"` extension from the extensions list in `./.devcontainer/devcontainer.json` file.

  ```json
   "extensions": [
        "...",
        //"znck.grammarly",
        "..."
        ]
  ```

If you want to use Grammarly for other files, Go to `./.devcontainer/devcontainer.json` and add your file extension in the

  ```json
    "grammarly.files.include": ["*.md", ".YourFileExtension"]
  ```

And in case you do not want to use Grammarly for other files, add your file extension in the

  ```json
    "grammarly.files.exclude": ["*.md", ".YourFileExtension"]
  ```

You can use Grammarly in any file apart from `.tex` files. Just press `CTRL + SHIFT + P` and search for `Grammarly: Check text`.

This editor uses Grammarly Free account to check grammar and spelling. However if you want to use your Grammarly Premium account, simply press `CTRL + SHIFT + P` and search for `Grammarly: Login / Connect your account`.

## LanguageTools

This editor has built-in [LanguageTool](https://languagetool.org) support for `BibTEX`, `ConTEXt`, `LATEX`, `Markdown`, `Org`, `reStructuredText`, `R Sweave`, and `XHTML` documents but **it is disabled by default in favor of grammarly**. If you want to use LanguageTool instead of grammarly, just **uncomment** the following lines from `.devcontainer/devcontainer.json`

  ```json
  "extensions": [
      "...",
      "valentjn.vscode-ltex",
      "..."
    ]
  ```
  
  And the **remove** or **comment out** the `"znck.grammarly"` extension from the extensions list in `./.devcontainer/devcontainer.json` file. (Recommended)

  ```json
  "extensions": [
      "...",
      // "znck.grammarly",
      "..."
    ]
  ```

## Live Collaboration

> All about Live Collaboration: [Click Here](https://visualstudio.microsoft.com/services/live-share/)

Just click on the **Live Share** Sidebar button and you are good to go

![collaborate](https://user-images.githubusercontent.com/54777542/224550768-48997ac9-8747-425b-b7b4-05473f3ba944.png)

If you do not need the Live Collaboration at all, you can just **remove** or **comment out** the `"ms-vsliveshare.vsliveshare"` extension from the extensions list in `./.devcontainer/devcontainer.json` file.

  ```json
  "extensions": [
      "...",
      // "ms-vsliveshare.vsliveshare",
      "..."
    ]
  ```

## PDF Viewer Dark Mode

The pdf viewer will preview the pdf in Dark Mode by default if your Operating System is in Dark Mode. To view the pdf in Normal mode in os-wide dark mode just **remove or comment** these lines from `./.devcontainer/devcontainer.json`.

  ```json
    //"latex-workshop.view.pdf.color.dark.pageColorsBackground":"#171717",
    //"latex-workshop.view.pdf.color.dark.pageColorsForeground":"#FFFFFF",
    //"latex-workshop.view.pdf.color.dark.backgroundColor":"#171717",
  ```

## Configuration

- To change the output directory change the following properties in `./.devcontainer/devcontainer.json`

    ```json
    "latex-workshop.latex.outDir": "<YourDirectoryName>",
    "latex-workshop.latex.magic.args": ["-output-directory=<YourDirectoryName>"],
    ```

- Other configurations (e.g. PDF Generation Delay, Auto Saving etc.) can be modified in `./.devcontainer/devcontainer.json`. Check the [Wiki](https://github.com/James-Yu/LaTeX-Workshop/wiki)

## More Features and Configurations

There are a lot of features like

- [Intellisense (Citation, References)](https://github.com/James-Yu/LaTeX-Workshop/wiki/Intellisense)
- [Snippet and Shortcuts](https://github.com/James-Yu/LaTeX-Workshop/wiki/Snippets)
- [Linting](https://github.com/James-Yu/LaTeX-Workshop/wiki/Linters)
- [Formatting](https://github.com/James-Yu/LaTeX-Workshop/wiki/Format)
- [Code Folding](https://github.com/James-Yu/LaTeX-Workshop/wiki/ExtraFeatures#code-folding)

And a lot [more](https://github.com/James-Yu/LaTeX-Workshop/wiki/ExtraFeatures).

All of the features and configurations can be found [here](https://github.com/James-Yu/LaTeX-Workshop/wiki).

## Contribution

I am open to and request you to contribute to this project. You can just Create a new issue to let me know about your concern/requests or just send a pull request with your desired changes.

## Credits

- @James-Yu's [latex-workshop](https://github.com/James-Yu/LaTeX-Workshop) For all the Latex support.
- [danteev/texlive](https://github.com/dante-ev/docker-texlive) For Latex compilation.
- @znck's [Grammarly](https://github.com/znck/grammarly) for Grammarly support.
- [@thodson-hugs](https://github.com/thodson-hugs) for GitHub Copilot

## What's Next

1. Will optimize the backend to decrease installation time and PDF showing time for the first time
2. Documentation
3. Release: Export PDF as a release version
4. You tell me

## Contact

1. Send an email to `mail@sanjibsen.com`
2. [Facebook](https://www.facebook.com/sanjib.kumarsen.963/), [LinkedIn](https://www.linkedin.com/in/sanjibsen/)
