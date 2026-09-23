# The GitHub Workflow

This is the routine you will use for **every assignment** this year. Learn it once, use it thirty times.

---

## The five steps

```
   ┌─────────┐    ┌─────────┐    ┌─────────┐    ┌─────────┐    ┌─────────┐
   │  FORK   │ →  │  EDIT   │ →  │ COMMIT  │ →  │  PUSH   │ →  │ SUBMIT  │
   └─────────┘    └─────────┘    └─────────┘    └─────────┘    └─────────┘
    my copy of     make my        record what    send it to     paste link in
    the assignment changes        I changed      GitHub         Classroom
```

---

## The vocabulary

| Term | What it actually means |
|---|---|
| **Git** | The tool that tracks changes to files. It's the engine. |
| **GitHub** | A website that stores Git projects online. It's the parking garage. |
| **Repository (repo)** | One project, plus its entire history of changes |
| **Fork** | Your own personal copy of someone else's repo |
| **Commit** | A saved snapshot, with a message explaining what changed and why |
| **Push** | Uploading your commits from your computer to GitHub |
| **Clone** | Downloading a repo onto a computer |
| **Diff** | The view showing exactly what lines were added (green) and removed (red) |

---

## Step 1 — Fork

On the assignment repo page, click **Fork** (top right) → **Create fork**.

Confirm the URL changed to `github.com/YOUR-USERNAME/repo-name`.

**Fork once per assignment.** If you fork the same repo twice, GitHub will just send you back to your existing fork.

---

## Step 2 — Edit

**On GitHub directly** (fine for Markdown, fine early on):
- Click a file → ✏️ pencil icon → type → scroll down → commit

**In a codespace** (what you'll use once we're writing Java):
- On your fork, click **Code** → **Codespaces** tab → **Create codespace on main**
- Edit files in the editor, exactly like VS Code
- Use the **Source Control** panel in the left sidebar, or git in the terminal

---

## Step 3 — Commit

A commit is a save point with a note attached.

### Writing a good commit message

Finish this sentence: *"If applied, this commit will ____."*

```
✅ Add Rectangle class with area and perimeter methods
✅ Fix off-by-one error in loop counter
✅ Complete exercises 1 through 4
✅ Update README with build instructions

❌ stuff
❌ asdf
❌ changes
❌ done
❌ final version
❌ FINAL FINAL v3 actually final
```

### How often should I commit?

**Every time you finish a chunk of work that makes sense on its own.** Roughly: after each exercise, after fixing a bug, after adding a feature.

Not: once at the very end. If your entire assignment is one commit, you lose points, and more importantly you lose the ability to go back when you break something.

---

## Step 4 — Push

**On GitHub's web editor:** committing pushes automatically. Nothing to do.

**In a codespace:**
1. Open the **Source Control** panel (sidebar, the branching arrows)
2. Stage your changes (the **+** next to each file)
3. Type your commit message
4. Click **Commit**, then **Sync Changes**

Or, in the terminal: `git add -A`, then `git commit -m "Your message"`, then `git push`.

**Nothing to authorize.** The codespace was created from your own fork, so git is already signed in as you.

---

## Step 5 — Submit

1. Copy your fork's URL from the browser address bar
2. Google Classroom → the assignment → **Add link** → paste
3. Click **Turn In**

### The single most common mistake

Submitting **my** repo URL instead of **yours**. Before you hit Turn In, look at the link. Does it have your username in it? If not, it's wrong.

```
❌ github.com/flatbush-apcsa/apcsa-00-setup
✅ github.com/your-username/apcsa-00-setup
```

---

## Repo standards (graded from Session 5 onward)

Every submission needs:

- [ ] A `README.md` at the root with your name, the assignment, and what you built
- [ ] At least 3 commits with real messages
- [ ] No files named `Untitled.java`, `test2.java`, `Copy of ...`
- [ ] Consistent indentation
- [ ] Comments on every class and every non-obvious method

---

## Fixing things

| Problem | Fix |
|---|---|
| I edited the teacher's repo by accident | You can't — GitHub wouldn't let you. You were probably in your fork and got confused. Check the URL |
| I forked but can't find my copy | Click your profile picture → **Your repositories** |
| I made a typo in a commit message | Leave it. Not worth fixing. Write a better one next time |
| I deleted something important | It's in your commit history. Click **Commits**, find the version before the deletion, copy the content back |
| My codespace won't push | You almost certainly opened it from the teacher's repo instead of your fork. Check the repo name in the bottom left corner, then open a codespace on your fork |
| I want to start over | Delete your fork (Settings → scroll to bottom → Delete this repository) and fork again. You lose your work, so only do this if there's nothing to lose |
