# Markdown Guide

Markdown is a way of writing formatted text using plain characters. Every README on GitHub, most documentation on the internet, and every written assignment in this class is written in it.

It takes about ten minutes to learn.

> **Tip that makes this click:** when editing on GitHub, there's a **Preview** tab next to **Edit**. Click back and forth constantly while you're learning. Instant feedback.

---

## Headings

```markdown
# Heading 1 — biggest
## Heading 2
### Heading 3
#### Heading 4
```

You need a space after the `#`. `#Heading` does not work. `# Heading` does.

---

## Emphasis

```markdown
*italic*  or  _italic_
**bold**  or  __bold__
***bold italic***
~~strikethrough~~
`inline code`
```

Renders as: *italic*, **bold**, ***bold italic***, ~~strikethrough~~, `inline code`

---

## Lists

**Bulleted:**
```markdown
- first
- second
  - nested (indent two spaces)
- third
```

**Numbered:**
```markdown
1. first
2. second
3. third
```

**Checkboxes:**
```markdown
- [ ] not done
- [x] done
```

---

## Code blocks

Three backticks, then the language name, then your code, then three more backticks.

````markdown
```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello!");
    }
}
```
````

Naming the language turns on syntax highlighting. Always name it.

---

## Tables

```markdown
| Column A | Column B | Column C |
|----------|----------|----------|
| row 1    | data     | data     |
| row 2    | data     | data     |
```

**The `|---|` separator row is required.** Leaving it out is the #1 Markdown mistake and it makes your whole table render as one ugly line of text.

**Alignment** (optional):
```markdown
| Left | Center | Right |
|:-----|:------:|------:|
| a    | b      | c     |
```

---

## Links and images

```markdown
[link text](https://example.com)

![alt text](path/to/image.png)
```

The only difference is the `!` in front for images.

---

## Blockquotes

```markdown
> This is a quote.
> It can span multiple lines.
```

> This is a quote.
> It can span multiple lines.

---

## Horizontal rule

```markdown
---
```

---

## Line breaks — the thing that confuses everyone

Markdown **ignores single line breaks.** These two lines:

```
Line one
Line two
```

...render as one paragraph: "Line one Line two"

**To get a real new paragraph, leave a blank line between them:**

```
Line one

Line two
```

---

## Cheat sheet

| I want... | I type... |
|---|---|
| Heading | `# Text` |
| Bold | `**text**` |
| Italic | `*text*` |
| Code inline | `` `text` `` |
| Code block | ` ```java ` ... ` ``` ` |
| Bullet | `- item` |
| Number | `1. item` |
| Checkbox | `- [ ] item` |
| Link | `[text](url)` |
| Image | `![alt](url)` |
| Quote | `> text` |
| Line | `---` |
| New paragraph | leave a blank line |

---

## Common mistakes

| Mistake | What happens | Fix |
|---|---|---|
| `#Heading` | Prints literally, no formatting | Add a space: `# Heading` |
| Table with no `\|---\|` row | Renders as one messy line | Add the separator row |
| Single line break for a new paragraph | Lines get joined | Add a blank line |
| Code block with no language | No syntax highlighting | Write ` ```java ` |
| Unmatched backticks | Everything after turns into code | Count your backticks |
