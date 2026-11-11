# Quick start

This guide gets the Markdown Basics runner open. The runner is a desktop window, so the tutorial needs no server, no browser, and no accounts. Once the runner is open, the lessons explain the rest.

## Quick setup with the script

The tutorial lives at [databankimx/training-markdown](https://github.com/databankimx/training-markdown).

`setup.ps1` does the whole setup. You can run it from anywhere. If it isn't inside the repository, it clones the repository into `C:\Development\training\training-markdown` and runs the cloned copy. It then:

- checks for Git, and installs it with winget if it's missing
- checks for Node.js 24 or later, and installs the LTS release with winget if it's missing
- checks for the C++ Build Tools, which are the fallback if Electron's download fails
- installs the runner's packages exactly as recorded in `lesson-runner\package-lock.json`
- makes sure the Electron binary is present, and if its download fails, rebuilds the native modules with the C++ environment and tries again
- runs the runner's tests, and stops at the first failure

It's safe to run more than once. Anything already in place is skipped.

Open PowerShell, and run:

```pwsh
powershell -NoProfile -ExecutionPolicy Bypass -File .\setup.ps1
```

The `-ExecutionPolicy Bypass` part lets this one script run. It doesn't change any setting on your machine.

The C++ Build Tools are about 4 to 5 GB and can take several minutes. They need an **Administrator** PowerShell. If you aren't an administrator, the script stops at that step and says so. Open PowerShell as Administrator, and run the script again.

If you only want to check your setup, without installing anything, add `-SkipInstall`:

```pwsh
powershell -NoProfile -ExecutionPolicy Bypass -File .\setup.ps1 -SkipInstall
```

When the script finishes, it prints a summary and the command to start the runner. Every line should say `ok`.

Installing uses winget. If winget isn't available, install **App Installer** from the Microsoft Store first. Company policy can block installs, in which case the script stops and you'll need IT.

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
