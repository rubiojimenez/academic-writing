---
geometry: margin=3cm
mainfont: TeX Gyre Heros
fontsize: 12pt
---

<!--
Email: jesus@rubiojimenez.com
-->

# A personal VSCodium setup

**Jesús Rubio**  

*Guildford, 2 September 2025*

## 1. Installed extensions

All installed extensions can be displayed by opening a terminal and running:

    codium --list-extensions

In my setup, this yields, in alphabetical order, the following list:

    ecmel.vscode-html-css
    huytd.github-light-monochrome
    james-yu.latex-workshop
    mads-hartmann.bash-ide-vscode
    ms-python.debugpy
    ms-python.python
    ms-python.vscode-python-envs
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

## 2. Installing extensions

A single extension can be installed as:

    codium --install-extension <extension-id>

For example:

    codium --install-extension ms-python.python

To simultaneously install several extensions, use the following loop:

    for ext in \
        <extension-1-id> \
        <extension-2-id> \
        <extension-3-id>; \
    do
        codium --install-extension "$ext"
    done

## 3. Working environment

A set of useful settings for `settings.json` is as follows:

    {
        "window.zoomLevel": -0.75,
        "window.restoreWindows": "none",
        "window.restoreFullscreen": false,

        "workbench.startupEditor": "none",
        "workbench.colorTheme": "GitHub Light Monochrome",
        "workbench.statusBar.visible": true,
        "workbench.activityBar.location": "bottom",
        "workbench.editor.defaultBinaryEditor": "default",
        "workbench.editor.empty.hint": "hidden",

        "editor.minimap.enabled": false,
        "editor.wordWrap": "on",
        "editor.defaultFormatter": "yzhang.markdown-all-in-one",

        "explorer.confirmDelete": false,
        "explorer.confirmDragAndDrop": false,

        "files.hotExit": "off",

        "terminal.integrated.enableMultiLinePasteWarning": "never",

        "git.enableSmartCommit": true,
        "git.confirmSync": false,
        "git.autofetch": true,

        "python.defaultInterpreterPath": "/usr/bin/python3",

        "latex-workshop.view.pdf.viewer": "tab",

        "security.workspace.trust.untrustedFiles": "open"
    }

**Note:** Adjust the Python interpreter path placeholder to match your local installation.