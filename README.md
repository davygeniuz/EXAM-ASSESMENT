# EXAM-ASSESMENT

A simple **offline Computer-Based Test (CBT)** for the enrollment assessment.
Everything lives in one self-contained file — no internet, server, or installation required.

## Run it

Open `exam.html` in any web browser (double-click it). That's it.

## Features

- One question at a time with Previous / Next navigation
- Progress bar and answered-count
- Warns about unanswered questions before submitting
- **Immediate result** after submission: score, percentage, PASS/FAIL badge
- Full answer review (your answer vs. correct answer for each question)
- Print result button
- Retake test button
- Works offline on desktop and mobile browsers

## Edit the exam

Open `exam.html` in any text editor:

1. **Settings** — find `const CONFIG` near the top of the `<script>` block.
   Change the exam title, subtitle, and pass mark percentage.
2. **Questions** — find `const QUESTIONS` right below it. Each question looks like:

   ```js
   {
     question: "What is 2 + 2?",
     options: ["3", "4", "5", "6"],
     answer: 1        // index of the correct option (0 = first option)
   }
   ```

   Add, remove, or edit entries — the exam adapts automatically.

> ⚠ The questions currently in the file are **samples**. Replace them with the
> real enrollment assessment questions.

## Distribution

Copy `exam.html` to a flash drive or share the file directly. It runs anywhere a
browser runs. Note: results are shown on screen (and can be printed) but are not
stored after the page is closed.
