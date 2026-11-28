# Quick start

This guide gets the Markdown Basics runner open. The runner is a desktop window, so the tutorial needs no server, no browser, and no accounts. Once the runner is open, the lessons explain the rest.

## Quick setup with the script

### What gets installed

By default, the setup installs:

* Notepad++
* Git
* PowerShell 7
* Node.js 24 or newer
* VS Code
* Microsoft Visual C++ runtime

The C++ Build Tools aren't installed up front. The script installs them only if Electron's binary can't download.

The setup then runs these steps: Lesson runner packages; Lesson runner tests. At the end it opens the repository in VS Code and starts the lesson runner window (Electron).

### Getting started

There are three methods available to set up this tutorial. They are currently Windows-only.

#### Full Automation (if you don't have Git currently set up)

This process will install Git and copy the repository to a subfolder of `C:\Development\training` and install all necessary software and extensions for the tutorial's lesson runner.

1. Obtain the tutorial's GitHub slug name, which is `training-markdown`
2. Open PowerShell using "Run as Administrator"
3. Run the script below

```pwsh
# Obtain the load tutorial script
irm https://raw.githubusercontent.com/databankimx/training-shared-template/main/load-tutorial.ps1 -OutFile "$env:TEMP\load-tutorial.ps1"

# Perform automated setup
powershell -NoProfile -ExecutionPolicy Bypass -File "$env:TEMP\load-tutorial.ps1" -RepoUrl https://github.com/databankimx/training-markdown.git
```

#### Automated Setup from Local Repo (assumes you already have Git installed and set up)

In this process, you pull the existing repository and then run its setup script, which installs all necessary software and extensions for the tutorial's lesson runner.

1. Obtain the tutorial's GitHub slug name, which is `training-markdown`
2. Open PowerShell using "Run as Administrator"
3. If you will use the default base directory `C:\Development\training`, run the following:

```pwsh
# Create the base folder if it doesn't exist yet
New-Item -ItemType Directory -Force -Path C:\Development\training | Out-Null
```

4. Clone the repository. If you're using a different base directory, replace `C:\Development\training` with your path:

```pwsh
# Go there and clone the tutorial
cd C:\Development\training
git clone https://github.com/databankimx/training-markdown.git
cd training-markdown
```

5. If desired, edit the setup configuration, which determines what software is installed automatically (see "Change what gets installed" below)

```pwsh
# Optional: edit setup.json before installations
notepad setup.json
```

6. Save the configuration if you edited it, then run the setup script

##### If using the default base path, run this:

```pwsh
# Run the setup
powershell -NoProfile -ExecutionPolicy Bypass -File .\setup.ps1
```

##### If using a different base path, replace `<BASE_DIR>` with your path and run this:

```pwsh
# Run the setup
powershell -NoProfile -ExecutionPolicy Bypass -File .\setup.ps1 -BaseDirectory <BASE_DIR>
```

#### Manual Setup from Local Repo

If you want to do everything manually, you can pull the repository and set up software on your own.

1. Obtain the tutorial's GitHub slug name, which is `training-markdown`
2. Run the script below

```pwsh
git clone https://github.com/databankimx/training-markdown.git
```

3. Review README.md and QUICKSTART.md in the repository for instructions for manual setup.

### Switches and notes

* `-SkipInstall` checks what's installed and installs nothing.
* `-NoLaunch` runs the setup but doesn't open VS Code or start the runner.
* `-SkipTests` skips the course tests, which the setup runs by default.
* Installing uses winget. If winget isn't available, install **App Installer** from the Microsoft Store first. Company policy can block installs, in which case the script stops and you'll need IT.
* If an install needs administrator rights, the script stops before installing anything and asks you to run it again from an Administrator PowerShell window.

### Change what gets installed

The settings are in `setup.json`, in the repository folder. Open it in any text editor:

* Set an install's `"install"` to `true` to include it, or `false` to skip it.
* `"pinned"` sets the version. `"extensions"` lists the VS Code extensions to add.
* Save the file, then run `setup.ps1` again. It skips what's already installed.

## Requirements

- Windows 10 or 11
- Git, for cloning the repository. The script installs it if it's missing.
- Node.js 24 or later, for the runner. The script installs it if it's missing.
- The Visual Studio Build Tools with the C++ workload, the fallback for Electron's download. The script installs them if they're missing.

No editor is needed, although VS Code is convenient for writing your own Markdown.

## Start the runner

```pwsh
cd C:\Development\training\training-markdown\lesson-runner
npm start
```

The runner opens on the first lesson, "Why Markdown". It remembers the lesson you were on and opens there next time. Close the window normally to stop it.

Run `npm start` from the `lesson-runner` folder. The tutorial's root folder has no `package.json`, so `npm start` there fails.

## How the lessons work

- The **sidebar** lists the chapters, and the lessons in the chosen chapter. Use **Next** and **Previous** to move through the course in order.
- Read each lesson in the **Lesson** tab. Examples show the Markdown source, then a box labeled **Rendered** with the same text as it displays.
- Exercises use the **Source** tab. The first line of the page is usually given. Type the rest. The **Rendered** pane updates as you type, and the check reports whether your page matches the description. You don't need to press anything to check.
- A failed check shows a hint. A passed check shows a green message.
- **Show solution (spoiler)** opens one correct answer, read-only. Try the exercise first. The solution shows the rendered page, and **Hide solutions** returns you to your own text.
- **Reset** puts back the text the exercise started with.
- Press Ctrl and move the mouse wheel to change the size of the lesson text.
- Ctrl+Left and Ctrl+Right move to the previous and next lesson, unless the cursor is in the editor.
- Tab in the editor inserts spaces to the next four-column stop. Shift+Tab removes spaces from the start of the line.

The chapter called **Markdown Cheat Sheet** is a one-page reference. It has no exercises, and you can open it at any time.

## Your progress

The runner saves your progress as you go, in a file outside the repository, so it's never committed:

```
%APPDATA%\training-markdown-runner\
```

The saved progress includes which lessons you've visited, the spoiler solutions you've revealed, and the last lesson you opened. To reset it, press **Ctrl+Alt+Shift+Backspace** in the runner. The next start opens the first lesson.

Your exercise text is kept only while you're on the exercise. To keep your work, copy it into a file in your own folder.

## Troubleshooting

- **Setup says Git is missing and winget is not available.** Install **App Installer** from the Microsoft Store, or install Git from [git-scm.com](https://git-scm.com), then run the script again.
- **Setup says Node.js is too old.** Install the current LTS release from [nodejs.org](https://nodejs.org), open a new PowerShell window, and run the script again.
- **Setup says the C++ Build Tools need an Administrator.** Open PowerShell as Administrator, then run the script again.
- **Setup says `npm ci` failed.** Check your network access to the npm registry, then run the script again. Don't delete `package-lock.json` to get past the error.
- **Setup says the Electron binary still won't download.** Check your network access to github.com, and that the C++ Build Tools are installed. Then run the script again.
- **Setup says the tests failed.** The message names the failing check. Send the full output to the tutorial's owner, because the tutorial's own files need attention.
- **`npm start` fails with "package.json not found".** You're in the tutorial's root folder. Change to `lesson-runner` first.
- **The old exercise text shows after moving to another lesson.** Close and reopen the runner, and tell the tutorial's owner what you were doing.
