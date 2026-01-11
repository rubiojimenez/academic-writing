---
geometry: margin=3cm
mainfont: Helvetica
fontsize: 12pt
---

<!--
Author: Jesús Rubio
Email: jesus@rubiojimenez.com
Modified: 2026-01
-->

# A personal VSCodium configuration

**Jesús Rubio**  

*2 September 2025, Guildford*

This document describes my personal VSCodium setup and is shared for illustration rather than as a universal recommendation.

## 1. Installed extensions

All currently installed extensions can be displayed by opening a terminal and running:

    codium --list-extensions

In my current setup, this yields the following list (alphabetised):

    davidanson.vscode-markdownlint
    ecmel.vscode-html-css
    hamza-aziane.obsidian-dark
    james-yu.latex-workshop
    mads-hartmann.bash-ide-vscode
    ms-python.debugpy
    ms-python.python
    ms-toolsai.jupyter
    ms-toolsai.jupyter-keymap
    ms-toolsai.jupyter-renderers
    ms-toolsai.vscode-jupyter-cell-tags
    ms-toolsai.vscode-jupyter-slideshow
    ms-vscode.live-server
    streetsidesoftware.code-spell-checker
    streetsidesoftware.code-spell-checker-british-english
    streetsidesoftware.code-spell-checker-spanish
    swmore.fortls
    tecosaur.latex-utilities
    the0807.uv-toolkit
    timonwong.shellcheck
    vv13.markdown-auto-preview        
    yzhang.markdown-all-in-one

## 2. Installing extensions

A single extension identified by ID can be installed as:

    codium --install-extension <extension-id>

For example, to install the Python extension:

    codium --install-extension ms-python.python

## 3. Working environment

A set of useful settings for `settings.json` is as follows:

    {
        "editor.minimap.enabled": false,
        "editor.wordWrap": "on",
        "editor.defaultFormatter": "yzhang.markdown-all-in-one",

        "workbench.startupEditor": "none",
        "workbench.statusBar.visible": true,
        "workbench.colorTheme": "Obsidian Dark",
        "workbench.editor.defaultBinaryEditor": "default",
        "workbench.editor.empty.hint": "hidden",

        "explorer.confirmDelete": false,
        "explorer.confirmDragAndDrop": false,

        "window.restoreWindows": "none",
        "window.restoreFullscreen": false,

        "files.hotExit": "off",

        "security.workspace.trust.untrustedFiles": "open",

        "git.enableSmartCommit": true,
        "git.confirmSync": false,
        "git.autofetch": true,

        "python.defaultInterpreterPath": "/your-path/python3",

        "latex-workshop.view.pdf.viewer": "tab"
    }

**Note:** Adjust the Python interpreter path placeholder to match your local installation.