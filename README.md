# EXAM-ASSESMENT

Offline **Computer-Based Test (CBT)** version of the NetClass *Quick assessment*
enrollment form (Cisco Networking · Emoji Digitals Academy · 2026 · Cohort 01).
Everything lives in one self-contained file — no internet, server, or installation required.

## Run it

Open `exam.html` in any web browser (double-click it). That's it.

## Features

- Student name + date captured on the start screen (date pre-filled, like the paper form)
- The 7 questions from the assessment form, one at a time, with Previous / Next navigation
- Progress bar and answered-count
- Warns about unanswered questions before submitting
- **Immediate result** after submission: score out of 7, percentage, PASS/FAIL badge
- Result header shows the student's name and date (prints with the result)
- Full answer review (your answer vs. correct answer for each question)
- Print result and Retake test buttons
- Works offline on desktop and mobile browsers

## Configure

Open `exam.html` in any text editor and edit `const CONFIG` at the top of the
`<script>` block:

| Setting           | Purpose                                                        |
| ----------------- | -------------------------------------------------------------- |
| `examTitle`       | Title shown on screen                                           |
| `subtitle`        | Line under the title (course / academy / cohort)                |
| `note`            | Intro note shown to the candidate                               |
| `passMarkPercent` | Pass mark in % (default 50)                                     |
| `showPassFail`    | `true` shows the PASSED/FAILED badge. The original paper form says the assessment "is not a pass-or-fail test" — set `false` for a purely diagnostic score |

## Edit questions

Questions live in `const QUESTIONS` just below the config. Each entry:

```js
{
  question: "What is 2 + 2?",
  options: ["3", "4", "5", "6"],
  answer: 1        // index of the correct option (0 = A, 1 = B, 2 = C, 3 = D)
}
```

Add, remove, or edit entries — the exam adapts automatically.

## Distribution

Copy `exam.html` to a flash drive or share the file directly. It runs anywhere a
browser runs. Results are shown on screen (and can be printed) but are not
stored after the page is closed.
