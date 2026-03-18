![Head](./Imag/Head.jpg)
<div align="center">


[![GitHub Stars](https://img.shields.io/github/stars/Muhammed-Maklad/Creating-CV-With-Latex?style=for-the-badge&logo=github)](https://github.com/Muhammed-Maklad/Creating-CV-With-Latex)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](http://makeapullrequest.com)

</div>

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Muhammed%20Gamal%20Maklad-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/muhammed-maklad/)

</div>

### You can use my template, which is available in the [**CV Template**](./CV%20Template.tex) file. Feel free to customize it according to your needs, or **read the tutorial**.

1. Go to **[overleaf.com](https://www.overleaf.com)**
2. Create a **free account**
3. Click **New Project → Blank Project**
4. Copy the code from the [**CV Template**](./CV%20Template.tex) paste it into your project, and replace the content with your own information 

<br>

> ### Lastly, don’t forget to review your CV for [ATS optimization](https://www.resumego.net/resume-checker/)

## 📚 Table of Contents

1. [Why use LaTeX?](#1-why-use-latex)
2. [Getting Started](#2-getting-started)
3. [The CV Document Structure](#3-the-cv-document-structure)
4. [Essential Commands for a CV](#4-essential-commands-for-a-cv)
   - [4.1 Text Formatting](#41-text-formatting)
   - [4.2 Sections and Headings](#42-sections-and-headings)
   - [4.3 Lists](#43-lists)
   - [4.4 Horizontal Lines](#44-horizontal-lines-dividers)
   - [4.5 Spacing](#45-spacing)
   - [4.6 Clickable Links](#46-clickable-links)
   - [4.7 Aligning Dates to the Right](#47-aligning-dates-to-the-right)
5. [Building Your CV Section by Section](#5-building-your-cv-section-by-section)
   - [5.1 Header](#51-header-name--contact-info)
   - [5.2 Summary / Objective](#52-summary--objective)
   - [5.3 Work Experience](#53-work-experience)
   - [5.4 Education](#54-education)
   - [5.5 Skills](#55-skills)
   - [5.6 Projects](#56-projects)
   - [5.7 Certifications](#57-certifications)
6. [Formatting & Layout Tips](#6-formatting--layout-tips)
7. [Recommended CV Packages](#7-recommended-cv-packages)
8. [Common Mistakes & Fixes](#8-common-mistakes--fixes)

---

## 1. Why use LaTeX?

LaTeX is a typesetting system used by engineers, academics, and researchers worldwide. Instead of clicking buttons to format text, you write commands  and LaTeX handles all the layout for you, perfectly, every time.

| Feature | LaTeX 🧾 | Microsoft Word 📝 |
|---|---|---|
| ✍️ Writing Style | Write **text + commands** | Click buttons & format manually |
| 🎯 Focus | Content & structure first | Design & appearance |
| 📄 Output Quality | Professional, consistent PDFs | Can vary across devices |
| 📐 Math Support | Excellent for equations | Limited & sometimes difficult |
| 🔁 Formatting | Automatic and consistent | Manual and error-prone |
| 📚 Best Use Cases | CVs, research papers, theses | Simple documents, notes |

### Why use LaTeX for a CV specifically?

| Benefit | Description |
|---|---|
| 🎯 **Pixel-perfect layout** | Everything lines up perfectly  dates, titles, bullet points |
| 💼 **Professional look** | Used by engineers, academics, and researchers worldwide |
| ✏️ **Easy to update** | Change content without ever breaking the design |
| 🆓 **Free templates** | Thousands of ready-made CV designs on Overleaf |

### How bold text works  a quick comparison

| Tool | How you make text bold |
|---|---|
| Word / Google Docs | Click the **B** button |
| LaTeX | Write `\textbf{this is bold}` |

---

## 2. Getting Started

### ✅ Recommended: Use Overleaf (No Installation)

Overleaf is a free, browser-based LaTeX editor. No installation, no terminal  just open and write.

**Step-by-step:**

1. Go to **[overleaf.com](https://www.overleaf.com)**
2. Create a **free account**
3. Click **New Project → Blank Project**

> 💡 **Tip:** Overleaf compiles your document instantly and shows a live PDF preview on the right side of the screen. No setup needed.

---

![Overleaf Interface ](./Imag/Interface%20of%20Overleaf.jpg)
## 3. The CV Document Structure

Every LaTeX CV file follows the same skeleton:

```latex
% a4paper = A4 page size | 11pt = font size (can be 10pt or 12pt)
\documentclass[a4paper, 11pt]{article}

% ── PREAMBLE ─────────────────────────────────────────────
% Load packages here (before \begin{document})
\usepackage{geometry}   % controls page margins
\usepackage{hyperref}   % makes links clickable in the PDF

% ── DOCUMENT BODY ────────────────────────────────────────
\begin{document}

  % Your CV sections go here

\end{document}
% Nothing written after \end{document} will appear in the PDF
```

### What does each part mean?

| Part | What it does |
|---|---|
| `\documentclass[a4paper, 11pt]{article}` | Sets page to A4 size, font to 11pt |
| `\usepackage{...}` | Loads extra features (margin control, clickable links…) |
| `\begin{document}` | Starts your actual CV content |
| `\end{document}` | Ends the document — nothing after this is printed |

---

## 4. Essential Commands for a CV

### 4.1 Text Formatting

```latex
\textbf{your job title here}        % Bold      — use for job titles, company names
\textit{your university name here}  % Italic    — use for institution names, dates
\underline{text}                    % Underline — use sparingly
\textbf{\textit{text}}              % Bold + Italic combined
```

| Command | Result | Best used for |
|---|---|---|
| `\textbf{text}` | **text** | Job titles, company names |
| `\textit{text}` | *text* | Institution names, dates |
| `\underline{text}` | <u>text</u> | Use sparingly |
| `\textbf{\textit{text}}` | ***text*** | Extra emphasis |

---

### 4.2 Sections and Headings

> ⚠️ **Always use `\section*{}` with the star (`*`) on a CV.**
> Without it, LaTeX prints "1. Experience", "2. Education" — which looks wrong on a CV.

```latex
\section*{Experience}    % ✅ correct — no number printed
\section{Experience}     % ❌ wrong for CV — prints "1. Experience"

\subsection*{Job Title}  % smaller sub-heading — also use * here
```

---

### 4.3 Lists

**Bullet list** (`itemize`) most common in CVs, use for responsibilities & achievements:

```latex
\begin{itemize}
  \item % write your first achievement or responsibility here
  \item % write your second achievement here
  \item % aim for 2–4 bullet points per role
\end{itemize}
```

**No-bullet list** — cleaner look, good for listing skills or tools:

```latex
\begin{itemize}
  \renewcommand{\labelitemi}{}  % this line removes the bullet symbol
  \item % skill or tool here
  \item % skill or tool here
\end{itemize}
```

**Description list** — best for the Skills section (label + content):

```latex
\begin{description}
  \item[Languages:]   % your programming languages here
  \item[Frameworks:]  % your frameworks here
  \item[Tools:]       % your tools and platforms here
  \item[Spoken:]      % e.g. Arabic (Native), English (Fluent)
\end{description}
```

---

### 4.4 Horizontal Lines (Dividers)

Use lines under section titles to visually separate CV sections:

```latex
\hrule          % draws a thin line across the full page width
\vspace{4pt}    % adds a small gap below the line so text isn't too close
```

---

### 4.5 Spacing

```latex
\vspace{6pt}    % pushes the next element DOWN by 6 points
\vspace{-4pt}   % pulls the next element UP — tightens a gap
\hspace{10pt}   % adds horizontal space inline
\noindent       % stops LaTeX from auto-indenting the paragraph
\newpage        % forces a new page — use for 2-page CVs
```

> 💡 `pt` = points. **1pt ≈ 0.35mm.**
> Common values: `4pt` (tight) · `6pt` (normal) · `10pt` (spacious)

---

### 4.6 Clickable Links

```latex
% ── In preamble ──────────────────────────────────────────
\usepackage{hyperref}
\hypersetup{colorlinks=true, urlcolor=blue}  % makes links blue and clickable

% ── In your document ─────────────────────────────────────
% \href{actual URL}{text shown to reader}
\href{mailto:your@email.com}{your@email.com}
\href{https://linkedin.com/in/yourprofile}{linkedin.com/in/yourprofile}
\href{https://github.com/yourusername}{github.com/yourusername}
```

---

### 4.7 Aligning Dates to the Right

Classic CV layout  job title on the left, date pushed to the far right:

```latex
\noindent
\textbf{your job title here} — \textit{Company Name, City}
\hfill                  % \hfill fills all empty space, pushing date to the right
\textit{Start Month Year – End Month Year}  % write "Present" for current job
```

---

## 5. Building Your CV Section by Section

### 5.1 Header (Name + Contact Info)

```latex
\begin{center}
  {\Huge \textbf{your full name here}} \\[4pt]
  % \Huge = very large font | \\[4pt] = line break + 4pt space

  {\large your job title or tagline here} \\[6pt]
  % \large = slightly bigger than normal text

  % Contact details on one line — \quad = medium space between items
  \href{mailto:your@email.com}{your@email.com} \quad
  your phone number here \quad
  your city, country here \\[2pt]

  % Online profiles
  \href{https://linkedin.com/in/yourprofile}{linkedin.com/in/yourprofile} \quad
  \href{https://github.com/yourusername}{github.com/yourusername}
\end{center}

\vspace{8pt}  % space between header and the divider line
\hrule        % horizontal line separating header from the rest of the CV
```

---

### 5.2 Summary / Objective

```latex
\section*{Summary}
% Write 2–3 sentences: your role, years of experience, and key strengths.
% Keep it concise — 3 lines maximum.
```

---

### 5.3 Work Experience

```latex
\section*{Experience}
\hrule
\vspace{6pt}

% ── Repeat this block for each job (most recent job first) ───
\noindent
\textbf{your job title here} — \textit{Company Name, City}
\hfill \textit{Start Month Year – End Month Year}
\begin{itemize}
  \item % describe an achievement — use numbers: "reduced X by 30\%"
  \item % another responsibility or achievement
  \item % aim for 2–4 bullet points per role
\end{itemize}

\vspace{4pt}  % small gap between job entries
% ── Paste the block above for your next job ──────────────
```

---

### 5.4 Education

```latex
\section*{Education}
\hrule
\vspace{6pt}

\noindent
\textbf{your degree here} — \textit{University Name, City}
\hfill \textit{Start Year – End Year}
\begin{itemize}
  \item GPA: your GPA here
  \item Graduation Project: briefly describe your project here
\end{itemize}
```

---

### 5.5 Skills

```latex
\section*{Skills}
\hrule
\vspace{6pt}

\begin{description}
  \item[Languages:]   % your programming languages here
  \item[Frameworks:]  % your frameworks here
  \item[Tools:]       % your tools, platforms, software here
  \item[Spoken:]      % spoken languages here
\end{description}
```

---

### 5.6 Projects

```latex
\section*{Projects}
\hrule
\vspace{6pt}

% ── Repeat this block for each project ───────────────────
\noindent
\textbf{your project name here}
\hfill \href{https://github.com/yourusername/project}{github.com/yourusername/project}
\begin{itemize}
  \item % what the project does and what technologies you used
  \item % a notable feature, result, or metric
\end{itemize}

\vspace{4pt}  % gap between projects
% ── Paste the block above for your next project ──────────
```

---

### 5.7 Certifications

```latex
\section*{Certifications}
\hrule
\vspace{6pt}

\begin{itemize}
  \item Certification Name — \textit{Issuing Organization, Year}
  \item Certification Name — \textit{Issuing Organization, Year}
\end{itemize}
```

---

## 6. Formatting & Layout Tips

### Page Margins

Default LaTeX margins are too wide for a CV. Tighten them:

```latex
% top/bottom = vertical margin | left/right = horizontal margin
\usepackage[top=1.5cm, bottom=1.5cm, left=1.8cm, right=1.8cm]{geometry}
```

### Font Size

```latex
\documentclass[a4paper, 10pt]{article}  % compact — fits more, good for 1-page CV
\documentclass[a4paper, 11pt]{article}  % standard — best readability (recommended ✅)
\documentclass[a4paper, 12pt]{article}  % large — easier to read, takes more space
```

### Remove Page Numbers

```latex
\pagestyle{empty}  % add to preamble — hides page numbers on all pages
```

### Change the Font

```latex
\usepackage{lmodern}  % clean modern font — recommended default ✅
\usepackage{times}    % Times New Roman style — traditional, formal
\usepackage{helvet}   % Helvetica style — clean, modern sans-serif
\renewcommand{\familydefault}{\sfdefault}  % switches the whole document to sans-serif
```

### Compact Bullet Lists

Default list spacing is too large for a CV. Fix it with `enumitem`:

```latex
% In preamble:
\usepackage{enumitem}

% Then use [noitemsep, topsep=2pt] on every list:
\begin{itemize}[noitemsep, topsep=2pt]
  % noitemsep  = removes space between bullet items
  % topsep=2pt = reduces space above the whole list
  \item your item here
  \item your item here
\end{itemize}
```

---

## 7. Recommended CV Packages

| Package | Purpose | How to use |
|---|---|---|
| `geometry` | Control page margins | `\usepackage[margin=1.5cm]{geometry}` |
| `hyperref` | Clickable links in PDF | `\usepackage{hyperref}` |
| `enumitem` | Compact, customizable lists | `\usepackage{enumitem}` |
| `fontawesome5` | Icons: email, phone, GitHub… | `\usepackage{fontawesome5}` |
| `titlesec` | Style section headings | `\usepackage{titlesec}` |
| `xcolor` | Colored text | `\usepackage{xcolor}` |
| `multicol` | Two-column layout | `\usepackage{multicol}` |
| `lmodern` | Modern clean font | `\usepackage{lmodern}` |
| `moderncv` | Full ready-made CV styles | `\documentclass{moderncv}` |

### Adding Icons with `fontawesome5`

```latex
% In preamble:
\usepackage{fontawesome5}

% In document:
\faEnvelope\  your@email.com \quad
\faPhone\     your phone number \quad
\faLinkedin\  your LinkedIn URL \quad
\faGithub\    your GitHub URL
```

### Coloring Section Titles

```latex
\usepackage{xcolor}
\usepackage{titlesec}

% Applies to every \section*{} heading in your document:
\titleformat{\section}
  {\large\bfseries\color{blue!70!black}}  % size | bold | color
  {}{0pt}{}[\titlerule]                   % \titlerule draws a line under the heading

% Change blue!70!black to any color: red, teal, gray!80, etc.
```

---

## 8. Common Mistakes & Fixes

| ❌ Problem | 🔍 Cause | ✅ Fix |
|---|---|---|
| Section shows "1. Experience" | Used `\section{}` without `*` | Change to `\section*{}` |
| Text goes off the page | Line too long | Use `\linebreak` or shorten the text |
| `%` disappears or causes issues | `%` starts a comment in LaTeX | Write `\%` to print a percent sign |
| `&` causes a compile error | `&` is reserved for tables | Write `\&` |
| Bullet points too spread out | Default list spacing is large | Use `enumitem` with `[noitemsep]` |
| Margins too wide | Default LaTeX margins | Add `\usepackage[margin=1.5cm]{geometry}` |
| Links are not clickable | `hyperref` not loaded | Add `\usepackage{hyperref}` to preamble |
| Font looks old-fashioned | Default Computer Modern font | Add `\usepackage{lmodern}` |

### Special Characters  Always Escape These

These symbols have a special meaning in LaTeX. Add `\` before them to print them as normal text:

| To print | Write in LaTeX |
|---|---|
| `%` | `\%` |
| `&` | `\&` |
| `$` | `\$` |
| `#` | `\#` |
| `_` | `\_` |
| `{` | `\{` |
| `}` | `\}` |

> 💡 **Rule of thumb:** If a character looks special in programming, it's probably special in LaTeX too. When in doubt, add a backslash `\` before it.


<div align="center">
 
---
 
## Show Your Support

If you find this repository helpful, please consider:

<table>
<tr>
<td align="center" width="33%">
⭐ <b>Star the Repo</b><br>
Help others discover it
</td>
<td align="center" width="33%">
🔀 <b>Contribute</b><br>
Add your solutions
</td>
<td align="center" width="33%">
📢 <b>Share</b><br>
Spread the word
</td>
</tr>
</table>

---


<div align="center">

### 🌟 **Thank You for Visiting!** 🌟

*"The only way to learn a new programming language is by writing programs in it."* - Dennis Ritchie

**Keep coding, keep learning, keep growing** 🚀

---

**Made with ❤️ by [Muhammed Maklad](https://github.com/Muhammed-Maklad)**

[![GitHub followers](https://img.shields.io/github/followers/Muhammed-Maklad?style=social)](https://github.com/Muhammed-Maklad)
[![GitHub stars](https://img.shields.io/github/stars/Muhammed-Maklad/Creating-CV-With-Latex?style=social)](https://github.com/Muhammed-Maklad/Creating-CV-With-Latex)

</div>
