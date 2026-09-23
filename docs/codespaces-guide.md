# GitHub Codespaces Guide

A **codespace** is a full development environment that runs in your browser, hosted by GitHub, attached directly to a repository. It is Visual Studio Code — the editor a large share of working developers use — with Java already installed.

There is nothing to download, nothing to configure, and no second account to create. If you have a GitHub account and a fork, you have an IDE.

---

## Opening a codespace

1. Go to **your fork** of the assignment repo on GitHub
2. Click the green **Code** button (top right, above the file list)
3. Click the **Codespaces** tab
4. Click **Create codespace on main**

Give it a minute the first time. When it finishes loading you are looking at VS Code, editing the files in your fork.

**Check the repo name before you click.** The page you open the codespace from must be *your* fork, with *your* username in the URL. A codespace opened from the teacher's repo will not let you push.

To get back to a codespace you already made: same **Code** → **Codespaces** menu, then click the existing codespace by name. You do not create a new one every session.

---

## The layout

| Where | What it is |
|---|---|
| Left sidebar, top icon | **Explorer** — your files. Click one to open it |
| Left sidebar, branching arrows | **Source Control** — stage, commit and push |
| Center | The editor |
| Bottom panel | **Terminal** — where you compile, run, and type input to your program |
| Bottom left corner | The codespace name, and the menu for stopping it |

If the terminal is not showing, press `` Ctrl + ` `` or use **Terminal → New Terminal** from the top menu.

---

## Running Java — two ways, both worth knowing

### The Run button

Open the `.java` file you want to run and click the **▷ Run** button at the top right of the editor. Output appears in the bottom panel.

Fast, and fine for most days.

### The terminal

In the terminal, from the folder your file is in:

```bash
javac Hello.java     # compile: Hello.java  ->  Hello.class
java Hello           # run the compiled class
```

Two commands, because those are two different things. `javac` turns your source code into bytecode and tells you about **syntax errors**. `java` runs that bytecode and is where **logic errors** show up. The Run button does both at once and hides the seam; the terminal makes it visible.

Note what you type after each command:

| Command | What you type after it |
|---|---|
| `javac` | the **file name**, with `.java` — `javac Hello.java` |
| `java` | the **class name**, with no extension — `java Hello` |

If your files are in a `src/` folder, `cd src` first.

---

## Committing and pushing

Git is already installed and already signed in as you — the codespace was created from your own fork, so it inherits your identity. There is no account to link and nothing to authorize.

### Using the Source Control panel

1. Click the **Source Control** icon in the left sidebar (the branching arrows)
2. Your changed files are listed — hover a file and click **+** to stage it, or click **+** on **Changes** to stage everything
3. Type a commit message in the box at the top
4. Click **Commit**
5. Click **Sync Changes** (or **Push**) to send it to GitHub

### Using the terminal

```bash
git status                       # what changed?
git add -A                       # stage everything
git commit -m "Your message"     # commit it
git push                         # send to GitHub
```

Either way, refresh your fork on github.com afterward. If your change is not there, it is not submitted.

---

## Stopping your codespace when you're done

GitHub gives personal accounts a **monthly free quota** of Codespaces hours and storage. A running codespace spends that quota even when you have walked away from it.

**When you finish working, stop it:**

- In the codespace: click the codespace name in the bottom left corner → **Stop Current Codespace**
- Or from GitHub: **Code** → **Codespaces** tab → **…** next to your codespace → **Stop codespace**

Stopping is not deleting. Your files stay exactly as you left them and the codespace restarts where you stopped.

---

## What survives and what doesn't

| What you do | What happens to your work |
|---|---|
| Closing the browser tab | Everything is fine. The codespace keeps running for a while, then idles out |
| Stopping the codespace | Everything is fine. Files and installed tools are still there when you restart it |
| Deleting the codespace | **Anything you did not commit and push is gone** |

A codespace is a workspace, not a backup. **Committing and pushing is the backup.** Push at the end of every work session, even if you are not finished — an unfinished commit is worth infinitely more than perfect work that only exists in one codespace.

---

## Shortcuts worth knowing

| Keys | Does |
|---|---|
| `Ctrl` / `Cmd` + `S` | Save |
| `` Ctrl + ` `` | Show or hide the terminal |
| `Shift` + `Alt` + `F` | Auto-format your code — **use this before every commit** |
| `Ctrl` / `Cmd` + `/` | Comment or uncomment the current line |
| `Ctrl` / `Cmd` + `F` | Find in file |
| `Ctrl` / `Cmd` + `Shift` + `P` | Command palette — type the name of any command |
| `Ctrl` + `C` (in the terminal) | Stop a running program |

---

## Troubleshooting

| Problem | Fix |
|---|---|
| Red errors when I compile | Read the **first** error only. The rest are usually knock-on effects. The line number is in the message |
| `class Hello is public, should be declared in a file named Hello.java` | Your file name must match your public class name exactly, capitals included |
| `Could not find or load main class Hello` | You are in the wrong folder, or you typed the file name instead of the class name. `java Hello`, not `java Hello.java`. Check `ls` to see what is actually in the folder |
| Program hangs and nothing happens | It is waiting for input. Click into the terminal and type |
| Infinite loop | Click into the terminal and press `Ctrl + C` |
| No Run button on the file | The Java extension is still starting up. Give it 30 seconds, or just use `javac` and `java` in the terminal |
| My changes aren't on GitHub | You committed but didn't push, or didn't stage the files. Open Source Control and look — unstaged changes are still listed there |
| `git push` is rejected | You are probably in a codespace opened from someone else's repo instead of your fork. Check the repo name in the bottom left |
| The codespace won't start / I'm out of quota | Check that you stopped your old ones (**Code → Codespaces**). Delete codespaces for assignments you have already pushed and submitted |
| I deleted my codespace and lost work | Anything pushed is safe on GitHub. Anything not pushed is gone. This is the reason we push often |

---

## Habits worth building now

1. **Format before you commit** — `Shift+Alt+F`. Readable code is graded code.
2. **Run often.** Don't write 60 lines and then run. Write 5, run, write 5, run.
3. **Read the first error.** Not the last one. The first.
4. **Commit at every milestone**, not once at the end.
5. **Push before you close the tab.** Every time.
6. **Stop your codespace when you leave.** It is your quota being burned.
