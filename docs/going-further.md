# Going Further — Optional Challenges

Finished early? None of this is required and none of it is graded. All of it is genuinely useful.

---

## Challenge 1 — Your GitHub profile README ⭐ start here

GitHub has a hidden feature: if you create a repository whose name is **exactly your username**, the README inside it gets displayed at the top of your public profile.

1. GitHub → **New repository**
2. Name it exactly your username (`sarah-levy` → repo named `sarah-levy`)
3. GitHub will show a message: *"You found a secret! ... this special repository"*
4. Check **Add a README file**
5. Create, then edit the README
6. Visit `github.com/your-username` — it's there

Now make it good. Try:

```markdown
# Hi, I'm [Name] 👋

I'm a high school student learning Java and building things.

## Currently
- Taking AP Computer Science A
- Building [your project idea]

## Learning
`Java` · `Git` · `Markdown`

## Reach me
[email or leave this out]
```

---

## Challenge 2 — Add badges

Badges are the little colored labels you see on real projects. Get them free at [shields.io](https://shields.io).

```markdown
![Java](https://img.shields.io/badge/Java-17-orange)
![Status](https://img.shields.io/badge/status-learning-blue)
```

---

## Challenge 3 — Use Git from the command line

The web editor is training wheels. Real developers type these.

In your codespace, open the terminal (`` Ctrl + ` ``) and try:

```bash
git status                    # what has changed?
git add .                     # stage everything
git commit -m "Your message"  # commit it
git push                      # send to GitHub
git log --oneline             # see your history
```

`git status` is the single most useful command in Git. When you're confused, run it.

---

## Challenge 4 — Explore a real codebase

Pick a project you actually use and go read it. Suggestions that are readable:

- Any small utility library
- A game you like, if it's open source
- Your favorite app — search "[app name] github"

Look for: How is the folder structure organized? How long are their functions? What does their README say? How do they write commit messages?

You are not expected to understand the code. You are learning what real projects look like.

---

## Challenge 5 — Write a README for something you already have

Pick anything — a school project, a hobby, a club you're in. Write a README for it as if it were a software project:

- What is it?
- Who is it for?
- How do you use it?
- What would you add next?

This is the single most transferable writing skill in software.

---

## Challenge 6 — Try Java before Session 3

Open a codespace on your fork of `apcsa-00-setup` (**Code** → **Codespaces** → **Create codespace on main**). Make a new file called `Main.java` and type:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello!");
        System.out.println("I am " + 16 + " years old.");
        System.out.println(7 * 6);
    }
}
```

Then run it — click **▷ Run** at the top right, or in the terminal type `javac Main.java` and then `java Main`. Then break it on purpose: delete a semicolon and see what the compiler says. Getting comfortable with error messages early is worth more than getting code right early.

Stop the codespace when you're done.
