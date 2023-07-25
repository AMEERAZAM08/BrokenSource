👆【☰】Table of Contents

<div align="justify">

<div align="center">
  <img src="https://avatars.githubusercontent.com/u/110147748" style="vertical-align: middle; border-radius: 10%" width="140">

  <h2>Broken Source Software</h2>

  <i>Readme available in:</i>

  <!-- <a href="Readme pt-BR.md"><img src="https://hatscripts.github.io/circle-flags/flags/br.svg" style="vertical-align: middle;" width="50"></a> -->
  <a href="Readme.md">      <img src="https://hatscripts.github.io/circle-flags/flags/us.svg" style="vertical-align: middle;" width="50"></a>
</div>

<br/>

This _mono_-repository hosts the **shared library** called **Broken** ❤️‍🩹 (Rust and Python), a convenience script of the same name - `broken` - and **submodules** of **all our projects**

- **Broken** is a _Framework_ for all other projects, a solution to manage them all in a single place 🌟

- **Broken** does a lot of things automatically for you, spend more time **using** the projects 🚀

**Rust** projects might take longer to be developed and shall be the focus on the medium future, while **Python** projects are prototypes, mockups, proof-of-concepts or smaller projects and are the current focus

<sub>❤️‍🔥 We are Linux-first support 🐧</sub>


<br>
<br>
<br>

# 📦 Pre-compiled binaries

Head over to each project's **Releases** page and download the latest version for your platform if any available

Otherwise, you'll have to run from the source code, see below

- **Help needed**: Package managers for Linux and MacOS are welcome, you'll be credited ❤️

<sub><i><b>Warning for Windows:</b> Our binaries are 100% safe - you can read the source code - but are likely to be flagged dangerous by Windows Smart Screen, mistaken as a malware by your antivirus or blocked by Windows Defender, given enough people downloading and executing them. Code signing is expensive and we 1. Don't have a budget for it; 2. Are completelty Open Source, no shady between the lines stuff</i></sub>

<br>

Our **release binaries** follows the **naming convention** below:

- `$project_name-$operating_system-$cpu_architecture-$version.$extension`

where

<div align="center">

| **Variable**         | **Possible Values**         | **Notes**     |
|:--------------------:|:---------------------------:|:-------------:|
| `$project_name`      | Many                        | -             |
| `$operating_system`  | `linux`, `macos`, `windows` | _*1_          |
| `$cpu_architecture`  | `amd64`, `arm`              | _*1_          |
| `$version`           | `YYYY.MM.DD`                | _*2_          |
| `$extension`         | `.bin`, `.exe`              | Depends on OS |

</div>

We also provide a `.sha256` file for checksum for each binary for integrity verification

<sub><i>*1: We don't have the hardware to test on ARM or MacOS, so we can't provide binaries for those platforms. You likely can run from the source code</i></sub>

<sub><i>*2: Our versioning is based on a date format since most code is rolling release; we don't plan to have that many releases; they encode the rough timespan where the project was at and gets neatly sorted by name on file explorers</i></sub>


<br>
<br>
<br>

# 🔥 Running From the Source Code

Please read all instructions before executing them for tips and notes

**Common stuff** for all platforms:

- The pre-requirements are having [Git](https://git-scm.com/downloads) and [Python](https://www.python.org/downloads) installed

<br>

## Linux and MacOS

<div align="center">
  <img src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/linux.svg" style="vertical-align: middle;" width="82">
  <img src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/apple.svg" style="vertical-align: middle;" width="82">

  **Linux** 💎 **MacOS**
</div>

<sub><i><b>Note:</b> For MacOS, use [Homebrew](https://brew.sh/) package manager if needed</i></sub>

- Open a Terminal on some directory and run:

```bash
# Clone and enter the repository directory
git clone https://github.com/BrokenSource/BrokenSource

# "Open" the repository folder
cd BrokenSource

# Install dependencies, activates virtual environment
python ./brakeit

# Clone submodules
broken clone
```

And done, you can now run `broken` and see all available commands: compile, release and run projects with ease!

<sub><b>Note:</b> On subsequent runs, open a terminal inside `BrokenSource` folder and execute `python ./brakeit` script again</sub>


<br>

## Windows

<div align="center">
  <img src="https://raw.githubusercontent.com/edent/SuperTinyIcons/master/images/svg/windows.svg" style="vertical-align: middle;" width="82">

  **Windows 10+**
</div>

A quick note based on the project language:

- Running the Python projects is **easy**, while Rust requires **extra steps**

- **Rust** is split in its own instructions to reduce micro-management and complexity


<details>
  <summary>
    ⚠️ Getting the error <i>"execution of scripts is disabled on this system"</i> ❓
  </summary>

  Open a PowerShell terminal as Administrator and run:

  ```powershell
  Set-ExecutionPolicy RemoteSigned
  ```
</details>

<br>
<br>

Depending on the **project language** you want to run, follow the **instructions below**


<br>

## • Python Projects

Have [Git](https://git-scm.com/downloads) and [Python](https://www.python.org/downloads) installed

<sub><b>Note:</b> Be sure to mark the option to add Python to PATH</sub>

- **Windows 10**: `Shift+Right Click` some empty space in Windows Explorer
  - Select `Open PowerShell window here`

- **Windows 11**: `Right Click` some empty space in Windows Explorer
  - Select `Open in Terminal`

Now run the same **Linux** and **MacOS** commands above

<br>

## • Rust Projects

**Rust** requires quite some **dependencies** to be **installed** for a Windows release

Compiling "natively" requires installing manually Python, Git, CMake, MinGW GCC and GFortran, Visual Studio C++ Build Tools, not really easy but **doable if you want to try**

Easiest way is using [MSYS2](https://www.msys2.org/) which provides an **Unix-like** environment for Windows, please install it

- Open a MSYS2 terminal and run:

```bash
# Install all required dependencies
pacman -S git python python-pip python-wheel mingw-w64-x86_64-toolchain libffi-devel zlib-devel
```

- Now follow the same **Linux** and **MacOS** instructions above

**Note**: Stuff will be downloaded to `C:\msys64\home\USERNAME\BrokenSource` on default configs

**Tip:** You can press `Shift+Insert` to paste stuff on the clipboard to MSYS2 terminal

<sub><i>Linux and terminal commands aren't that hard!.. see? 😉</i></sub>


<br>
<br>
<br>

# ❤️‍🩹 Contributing
Thanks for taking your time to contribute to Broken Source Software projects!!

- Apart from the usual "be nice", "be respectful", we have some guidelines to help you get started

## • Help Needed
- Designer needed for the logos and consistent art
- Packaging binaries on Linux and MacOS package managers

## • Reporting Issues
- **We do not** test enough or at all the code on Windows or MacOS
- Always give **minimal steps** to reproduce the error (instructions or code)
- Most projects deal with Audio or Video, issues may be file-specific
- **We only support the latest versions of any given project**, we are rolling-release
  - <sub>We'll still help troubleshooting older code or releases, just don't except back-porting</sub>

## • Suggesting Enhancements
- Rejection of ideas on Free and Open Source Software is a common and intimidating problem to newcomers, so we want to reduce the fear and cooperate with you
- Not all suggestions matches the project original idea
- No commentaries are criticizing your person, rather your *work*
- **Stuff needs time and effort to be implemented**
- Feel absolutely free to debate on choices and ideas for the projects


<br>
<br>
<br>

# 💎 Acknowledgements

All the infrastructure in **Broken Source Software's Framework** and **Projects** wouldn't be possible without many programming language packages, softwares we use and exponentially more **Open Source Contributors** that made it possible. **To all of you**, an **uncountable list of direct and indirect contributors**, we thank you for your time and effort to make the world a better place ❤️‍🩹

Below a list, **not ordered by importance or relevance**, of the most notable software and people.

### General
- [**FFmpeg**](https://ffmpeg.org): _"A complete, cross-platform solution to record, convert and stream audio and video."_ - and they are not lying!!
- [**Linux**](https://www.linux.org): Father of Open Source and all the things
- [**Visual Studio Code**](https://code.visualstudio.com): _"Code editing. Redefined."_
- [**Stability AI**](https://stability.ai): AI by the people for the people. Many products
- [**Huggingface 🤗**](https://huggingface.co): Central repository for AI models made easy with Diffusers, Gradio, Transformers
- [**Khronos Group**](https://www.khronos.org): For OpenGL, GLSL, Vulkan
- [**NVIDIA**](https://www.nvidia.com): Bittersweet one, but CUDA and the GPU's technology are undeniably amazing


### Python
- [**Python**](https://www.python.org): The programming language
- [**Poetry**](https://python-poetry.org): Package manager and virtual environments
- [**PyInstaller**](https://www.pyinstaller.org): A complete Python bundler for end user binaries
- [**Nuitka**](https://nuitka.net): A Python compiler to a redistributable portable binary
- [**ModernGL**](https://github.com/moderngl/moderngl): OpenGL made-easy wrapper
- [**GLFW**](https://www.glfw.org): Easy OpenGL window and input manager
- [**NumPy**](https://numpy.org): Numerical Python, the math behind the scenes
- [**Quaternion**](https://github.com/moble/quaternion): Built-in NumPy support for [Quaternions](https://www.youtube.com/watch?v=d4EgbgTm0Bg)<sup>Ew <a href="https://github.com/moble/quaternion/wiki/Euler-angles-are-horrible">Euler Angles</a></sup>
- [**DotMap**](https://github.com/drgrib/dotmap): Great and simple dot notation for dynamic dictionaries
- [**tqdm**](https://github.com/tqdm/tqdm): Progress bar for the terminal
- [**Rich**](https://github.com/Textualize/rich): Beautiful formatting in Python
- [**Loguru**](https://github.com/Delgan/loguru): Python logging made stupidly simple
- [**Forbiddenfruit**](https://github.com/clarete/forbiddenfruit): Monkey patching for builtins in Python
- [**Typer**](https://github.com/tiangolo/typer): Great Command Line Interfaces made easy
- [**Halo**](https://github.com/manrajgrover/halo): Beautiful spinners on the terminal
- [**Appdirs**](https://github.com/ActiveState/appdirs): Platform specific user directories
- [**Pillow**](https://github.com/python-pillow/Pillow): Complete Imaging Library for Python
- [**Aenum**](https://github.com/ethanfurman/aenum): Advanced enums in python
- [**TOML**](https://github.com/uiri/toml): Python [TOML](https://toml.io/en/) file support
- [**Schedule**](https://github.com/dbader/schedule): Python job scheduling for humans
- [**attrs**](https://github.com/python-attrs/attrs): Python classes without boilerplate
- [**intervaltree**](https://github.com/chaimleib/intervaltree): Timeline-like intervals made easy
- [**PyTorch**](https://pytorch.org): General AI and Machine Learning
- [**isort**](https://github.com/PyCQA/isort): _isort_ your imports, so you don't have to
- [**imgui**](https://github.com/ocornut/imgui): Bloat-free hacky-vibes user interface
- [**DearPyGui**](https://github.com/hoffstadt/DearPyGui): Awesome User Interfaces for Python
- [**SoundCard**](https://github.com/bastibe/SoundCard): A Pure-Python Real-Time Audio Library
- [**Imageio-FFmpeg**](https://github.com/imageio/imageio-ffmpeg): Bundling FFmpeg binaries so I don't have to
- [**mido**](https://pypi.org/project/mido): MIDI Files manipulation in Python

### Rust
- [**Rust**](https://www.rust-lang.org): The programming language
- _Incomplete list_

### Package Maintainers
Package managers for Linux and MacOS are welcome, you'll be credited ❤️

<br>
<sub><i><b>Note:</b> It is very likely that I've missed someone, contact me if you feel something should be here!</i></sub>

<br>
<br>
<br>

# ⚖️ License and Fair Use

**Basics**
- 📝 All projects have their own license; unless specified in the code, asset file or `Readme.md` on the project's root or some other directory, all files are subject to the `License.md` on their respective repository

- 📈 We embrace the **Open Source** philosophy; The **Free** part we hope that using more _"restrictive"_ licenses will help to keep the projects free from abuse. This being said, smaller projects tends to be MIT licensed since the effort is considerably lower


<br/>

**Legal Responsibilities**
- 🧨 We take **no responsibility** for any **damage** caused by the use of our projects on you or others, directly or indirectly

- 🖋 You are responsible for the **User Generated Content** you create, any copyright or law infringements are made by user inputs


<br/>

**Fair Use**
- 💝 Projects takes many human-hours to be created, consider retributing the favor by **donating** if you can or made money with them, do **share** the projects with others

- 💰 We are **not** against **Commercial** use, but we are against **abuse** of the projects and their code. Be fair, get in touch with us and we'll be happy to help both sides grow


<br/>

<sub>These are not legal advice, just our thoughts and intentions</sub>

</div>
