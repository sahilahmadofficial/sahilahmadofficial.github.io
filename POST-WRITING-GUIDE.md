# Post Writing Guide
## Everything You Need to Write Great Blog Posts

---

## 1. Post Structure

Every post should follow this structure:

```
1. Front Matter (metadata)
2. Hook / Opening (grab attention)
3. The Problem (why this matters)
4. The Content (your actual knowledge)
5. Hands-on / Examples (prove it works)
6. Conclusion / What's Next
7. Resources (links for further reading)
```

---

## 2. Front Matter

Every post MUST start with front matter between triple dashes.

### Complete Front Matter Template

```yaml
---
title: "Your Post Title Here"
date: YYYY-MM-DD HH:MM:SS +0530
categories: [PrimaryCategory, SubCategory]
tags: [tag1, tag2, tag3, tag4, tag5]
description: "A compelling one or two sentence description of your post. This appears in Google search results and social media previews. Make it count."
image:
  path: /assets/img/posts/your-post-folder/cover.jpg
  alt: "Descriptive alt text for the cover image"
pin: false
---
```

### Field Explanations

**title:**
- Use title case
- Be specific and descriptive
- Include the main keyword naturally
- Good: "How SQL Injection Actually Works — Root Cause to Remediation"
- Bad: "SQL Injection Post"

**date:**
- Format: YYYY-MM-DD HH:MM:SS +0530
- +0530 is India Standard Time
- Example: 2026-06-10 10:00:00 +0530
- Must match the filename date

**categories:**
- Maximum two levels: [Primary, Sub]
- Use consistent naming across posts
- Examples:
  - [IAM, SailPoint]
  - [Security, Web]
  - [Security, HTB]
  - [Security, Network]
  - [Security, Tools]
  - [Journey, Learning]

**tags:**
- Lowercase, hyphenated
- 4-6 tags per post
- Be consistent — reuse tags across related posts
- Examples: sailpoint, iam, iga, cybersecurity, web-security, htb, sql-injection

**description:**
- 120-160 characters ideal
- Must be compelling — this is what Google shows in search results
- Include your main keyword
- Write it as a complete sentence

**image path:**
- Always use the post-specific folder
- Format: /assets/img/posts/post-folder-name/cover.jpg
- Dimensions: exactly 1200x630px
- File size: under 500KB

**pin:**
- Set to true only for your most important post
- Only one post should be pinned at a time

---

## 3. Markdown Syntax Reference

### Headings

```markdown
# H1 — Never use in posts (title is H1)
## H2 — Main sections
### H3 — Sub sections
#### H4 — Rarely needed
```

Rule: Start your content with H2. Never use H1 inside post content.

### Text Formatting

```markdown
**bold text**
*italic text*
***bold and italic***
~~strikethrough~~
`inline code`
```

### Horizontal Rule (Section Divider)

```markdown
---
```

Use between major sections for visual breathing room.

### Blockquote

```markdown
> This is a blockquote.
> Use for important quotes or key insights.
```

### Callout / Tip Box (Chirpy specific)

```markdown
> **Note:** Important information the reader should know.

> **Tip:** A helpful tip or shortcut.

> **Warning:** Something the reader must be careful about.

> **Info:** Additional context or background.
```

---

## 4. Lists

### Unordered List

```markdown
- First item
- Second item
  - Nested item
  - Another nested item
- Third item
```

### Ordered List

```markdown
1. First step
2. Second step
3. Third step
```

### Task List (Checklist)

```markdown
- [x] Completed task
- [ ] Incomplete task
- [ ] Another task
```

---

## 5. Code Blocks

Code blocks are critical for a security/technical blog. Use them for every command, script, and configuration.

### Inline Code

```markdown
Use `inline code` for commands, file names, and short snippets.
```

### Fenced Code Block with Language

Always specify the language for syntax highlighting:

````markdown
```bash
# Shell commands
sudo apt update && sudo apt upgrade -y
nmap -sC -sV -oA output 192.168.1.1
```
````

````markdown
```python
# Python code
import requests

response = requests.get("https://example.com")
print(response.status_code)
```
````

````markdown
```yaml
# YAML configuration
title: My Blog
theme: jekyll-theme-chirpy
```
````

````markdown
```json
{
  "name": "Sahil Ahmad",
  "role": "Security Engineer"
}
```
````

````markdown
```sql
-- SQL queries
SELECT * FROM users WHERE username='admin'--';
```
````

### Supported Languages

```
bash, shell, sh       — terminal commands
python                — Python code
javascript, js        — JavaScript
yaml, yml             — configuration files
json                  — JSON data
sql                   — database queries
html                  — HTML markup
css                   — stylesheets
java                  — Java code
powershell            — Windows commands
ruby                  — Ruby code
go                    — Go code
c, cpp                — C and C++
text, plaintext       — plain text, no highlighting
```

### Terminal Output Style

For showing command output — use text or plaintext:

````markdown
```text
┌──(sahil㉿kali)-[~]
└─$ nmap -sV 10.10.10.1
Starting Nmap 7.94
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.9
80/tcp open  http    Apache 2.4.38
```
````

---

## 6. Links

### External Link

```markdown
[Link Text](https://example.com)
```

### Internal Link (to another post)

```markdown
[My Previous Post](/posts/post-title-here/)
```

### Internal Link (to a section in same post)

```markdown
[Jump to Section](#section-heading-in-lowercase-with-hyphens)
```

Example:
```markdown
[See the exploitation section](#exploitation)
```

### Link that opens in new tab

```markdown
[External Site](https://example.com){:target="_blank"}
```

### Reference-style links (for many links)

```markdown
This is [SailPoint][sailpoint] and this is [GitHub][github].

[sailpoint]: https://sailpoint.com
[github]: https://github.com
```

---

## 7. Images

### Basic Image

```markdown
![Alt text](/assets/img/posts/post-folder/image-name.jpg)
```

### Image with Caption

```markdown
![Alt text](/assets/img/posts/post-folder/image-name.jpg)
_This is the caption that appears below the image_
```

### Image with Custom Size

```markdown
![Alt text](/assets/img/posts/post-folder/image-name.jpg){: width="700" height="400" }
```

### Image Aligned

```markdown
![Alt text](/assets/img/posts/post-folder/image-name.jpg){: .left }
![Alt text](/assets/img/posts/post-folder/image-name.jpg){: .right }
![Alt text](/assets/img/posts/post-folder/image-name.jpg){: .normal }
```

### Clickable Image (opens full size)

Chirpy automatically makes images clickable with GLightbox — clicking opens fullscreen view. No extra syntax needed.

---

## 8. Tables

```markdown
| Column 1 | Column 2 | Column 3 |
|---|---|---|
| Data | Data | Data |
| Data | Data | Data |
```

### Alignment in Tables

```markdown
| Left | Center | Right |
|:---|:---:|---:|
| Left aligned | Centered | Right aligned |
```

### Example Security Table

```markdown
| Tool | Purpose | Cost |
|---|---|---|
| Burp Suite | Web app testing | Free/Pro |
| nmap | Network scanning | Free |
| Wireshark | Packet analysis | Free |
| Metasploit | Exploitation framework | Free/Pro |
```

---

## 9. Mathematics (LaTeX)

For any mathematical expressions:

### Inline Math

```markdown
This uses the formula $E = mc^2$ as an example.
```

### Block Math

```markdown
$$
\sum_{i=1}^{n} x_i = x_1 + x_2 + \cdots + x_n
$$
```

---

## 10. Video Embedding

### YouTube Video

```markdown
{% include embed/youtube.html id='VIDEO_ID' %}
```

Example (replace VIDEO_ID with actual ID from URL):
```markdown
{% include embed/youtube.html id='dQw4w9WgXcQ' %}
```

### Video File

```markdown
{% include embed/video.html src='/assets/img/posts/post-folder/demo.mp4' %}
```

---

## 11. Writing Style Guide

### Opening Hook (First 2-3 Lines)

Your opening must make the reader want to continue.

**Bad opening:**
```
In this post I will explain SQL injection.
SQL injection is a type of security vulnerability.
```

**Good opening:**
```
A single quote in a login form took down a Fortune 500 database.
Not a sophisticated attack. Not a zero-day. Just a missing check
on one input field — and years of customer data exposed in seconds.
This is SQL injection. Here is exactly how it works.
```

### Sentence Structure

- Short sentences. One idea per sentence.
- Vary length — short punchy sentences followed by longer explanatory ones.
- Active voice over passive voice.
- Good: "The attacker stole the credentials."
- Bad: "The credentials were stolen by the attacker."

### Technical Explanations

Always follow this pattern:
1. State what it is (1 sentence)
2. Explain why it matters (1-2 sentences)
3. Show how it works (example or code)
4. Show the defence (how to prevent or detect)

### Tone

- Write like you're explaining to a smart friend
- Honest about what you don't know
- Specific over vague — always
- Use "you" to address the reader directly

---

## 12. Post Length Guidelines

| Post Type | Word Count | Reading Time |
|---|---|---|
| Quick tip / tool note | 400-600 words | 2-3 min |
| Concept explanation | 800-1200 words | 4-6 min |
| HTB writeup | 800-1500 words | 4-7 min |
| Deep dive tutorial | 1500-2500 words | 7-12 min |
| Comprehensive guide | 2500-4000 words | 12-20 min |

**Rule:** Write exactly as long as the topic needs. Never pad. Never cut important content.

---

## 13. HTB Writeup Template

For HackTheBox writeups specifically:

```markdown
---
title: "HTB: MachineName"
date: YYYY-MM-DD HH:MM:SS +0530
categories: [Security, HTB]
tags: [htb, linux, web, privilege-escalation, specific-cve-if-any]
description: "Walkthrough of HackTheBox MachineName — a difficulty machine involving specific-vulnerability and privilege-escalation-method."
image:
  path: /assets/img/posts/htb-machinename/cover.jpg
  alt: "HTB MachineName"
---

## Machine Info

| Field | Details |
|---|---|
| Name | MachineName |
| OS | Linux / Windows |
| Difficulty | Easy / Medium / Hard |
| IP | 10.10.10.X |
| Release Date | DD Mon YYYY |
| Retire Date | DD Mon YYYY |

## Summary

Brief 2-3 sentence overview of the attack path without spoiling the details.

---

## Enumeration

### Nmap Scan

```bash
nmap -sC -sV -oA nmap/initial 10.10.10.X
```

```text
[paste nmap output here]
```

### What I Found

Explain what services are running and what looks interesting.

---

## Exploitation

### Vulnerability

Explain the vulnerability — root cause, not just the name.

### Payload / Method

```bash
[commands used]
```

Explain why this works.

---

## Post-Exploitation

### User Flag

How you got user.txt.

### Privilege Escalation

Explain the privilege escalation path — root cause.

```bash
[commands used for privesc]
```

### Root Flag

How you got root.txt.

---

## Lessons Learned

- What this machine taught you
- What you'd do differently
- Key concepts reinforced

---

## Tools Used

- Tool 1 — purpose
- Tool 2 — purpose

---

## References

- [CVE link if applicable]
- [Relevant documentation]

---

## 14. Checklist Before Publishing

Run through this before every post:

```
Content:
[ ] Front matter complete and accurate
[ ] Title is specific and descriptive
[ ] Description is 120-160 characters
[ ] Opening hook grabs attention
[ ] All sections flow logically
[ ] Code blocks have language specified
[ ] All commands tested and working
[ ] Links verified (not broken)
[ ] Spelling and grammar checked

Images:
[ ] Cover image is 1200x630px
[ ] Cover image is under 500KB
[ ] All images have alt text
[ ] Images are in correct folder

SEO:
[ ] Title contains main keyword
[ ] Description contains main keyword
[ ] Tags are relevant and consistent
[ ] Categories are correct

Final:
[ ] Read entire post out loud once
[ ] Filename matches date in front matter
[ ] Post adds genuine value — would you bookmark it?
```

---

## 15. Common Mistakes to Avoid

**Don't do these:**

- Starting with "In this post I will..."
- Using H1 inside post content
- Code blocks without language specification
- Images without alt text
- Publishing without a description in front matter
- Copying content from other sources
- Padding word count with filler sentences
- Writing a post you wouldn't personally want to read

**Do these instead:**

- Start with a hook — a scenario, a question, or a surprising fact
- Use H2 for all main sections
- Always specify language in code blocks
- Write alt text that describes the image meaningfully
- Always write a custom description — never leave it blank
- Only publish original content and genuine insights
- Write until the topic is done — then stop
- Ask: "Would I save this post to read again?" If no — improve it