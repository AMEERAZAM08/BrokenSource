---
title: Source
---

!!! quote "**The most flexible** way to use the Projects • Latest features, bugs, fixes, git clone"
    **Recommended for**: Advanced users, Contributors, Developers

## ⚡️ Installing

!!! success "Running any of my Projects takes only two commands"

!!! abstract "1. Select your Platform"
    === ":simple-windows: Windows"
        <div align="center"><img src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/windows.svg" style="vertical-align: middle; border-radius: 20%" width="80"></div>

        **Open** some folder to download the code on **Windows Explorer**

        - Press ++ctrl+l++ , run `powershell` and execute:

        ```powershell
        # Simply run the line below: 'irm' downloads, 'iex' executes, '|' links the two
        irm https://brokensrc.dev/get.ps1 | iex
        ```

        <hr>

        ??? success "Read what `get.ps1` does"
            ```powershell
            {% include-markdown "get.ps1" %}
            ```

        ??? quote "Enable <a href="https://rye-up.com/guide/faq/#windows-developer-mode" target="_blank">Developer Mode</a> for a Better Experience"
            To have <a href="https://en.wikipedia.org/wiki/Symbolic_link" target="_blank"><b>Folder Shortcuts</b></a> (Symbolic Links) to the **Project's Workspace** Directory (Data, Downloads, Config, etc) where the Source Code is, please enable <a href="https://rye-up.com/guide/faq/#windows-developer-mode" target="_blank"><b>Developer Mode</b></a> on **Windows Settings** per **Rye FAQ**.

            - This will also drastically speed up Virtual Environment creation

    === ":simple-linux: Linux"
        <div align="center"><img src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/linux.svg" style="vertical-align: middle; border-radius: 20%" width="80"></div>

        **Open** a **Terminal** on some directory and run

        ```shell title="Terminal"
        /bin/bash -c "$(curl -sS https://brokensrc.dev/get.sh)"
        ```

        <hr>

        ??? success "Read what `get.sh` does"
            ```powershell
            {% include-markdown "get.sh" %}
            ```

    === ":simple-apple: MacOS"
        <div align="center"><img src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/apple.svg" style="vertical-align: middle; border-radius: 20%;" width="80"></div>

        **Open** a **Terminal** on some directory and run

        ```zsh title="Terminal"
        /bin/bash -c "$(curl -sS https://brokensrc.dev/get.sh)"
        ```

        <hr>

        ??? success "Read what `get.sh` does"
            ```powershell
            {% include-markdown "get.sh" %}
            ```

    === ":simple-git: Manual"
        <div align="center"><img src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/git.svg" style="vertical-align: middle; border-radius: 20%" width="80"></div>

        - **Install** [**Git**](https://git-scm.com/downloads) and [**Rye**](https://rye-up.com) on your Platform

        ```bash title="Clone the Monorepo and all Submodules"
        git clone https://github.com/BrokenSource/BrokenSource --recurse-submodules --jobs 4
        ```
        ```bash title="Enter the Monorepo directory"
        cd BrokenSource
        ```
        ```bash title="Checkout all Submodules to the Master branch"
        git submodule foreach --recursive 'git checkout Master || true'
        ```
        ```bash title="Create the main Virtual Environment and Install Dependencies"
        rye sync
        ```
        ```bash title="Activate the main Virtual Environment"
        # Windows:
        .venv\Scripts\Activate.ps1 # PowerShell
        .venv\Scripts\Activate.bat # CMD

        # Linux and MacOS:
        source .venv/bin/activate # Bash
        source .venv/bin/activate.fish # Fish
        ```
        ```bash title="Start using any Project"
        broken
        shaderflow
        depthflow
        ```

<hr>

??? bug "Something Failed?"
    Try following the **Manual Instructions** Tab above, else [**Get in Touch**](../about/contact.md) with me, or create an **Issue** on GitHub

    - Please, show some effort or try solving the problem first, often you'll get it :)

<hr>

!!! abstract "2. Run any Project"
    **Now** simply run `broken` for a full Command List 🚀

    - Return the Project you want to run for extras

<hr>

!!! abstract "3. Next time, to use the Projects.."
    You just have to **Open a Terminal** on the <kbd>BrokenSource</kbd> directory and [**Source the Virtual Environment**](https://docs.python.org/3/library/venv.html#how-venvs-work)

    - Alternatively, run the `activate.sh` if on **Linux/MacOS** or `activate.ps1` if on **Windows**

<br>

## 🚀 Upgrading

<hr>

### 🌱 Submodules

The installation script should've **initialized** and set all Submodules to the **Master branch**

```bash title="Command"
git submodule foreach --recursive 'git checkout Master || true'
```

After that, you can **pull** the latest changes of all Repositories with

```bash title="Command"
git pull --recurse-submodules
```

If you have any local modifications and want to keep them,

```bash title="Command"
git pull --recurse-submodules --rebase
```

!!! note "You can add `--force` to override Local Changes. Be careful with data loss!"

<hr>

### 🌱 Virtual Environment

The Python Tooling I chose to Orchestrate the [**Monorepo**](https://github.com/BrokenSource/BrokenSource) is [**Rye**](https://rye-up.com)

- You'll probably **only** need to know of a **single command**:

!!! note "Command: [`rye sync`](https://rye-up.com/guide/sync)"
    This will **update** the **Virtual Environment** and **Install** any new **Dependencies**

<hr>
