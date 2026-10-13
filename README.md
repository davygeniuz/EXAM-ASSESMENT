# EXAM-ASSESMENT

Offline **Computer-Based Test (CBT)** version of the NetClass *Quick assessment*
enrollment form (Cisco Networking · Emoji Digitals Academy · 2026 · Cohort 01).
Everything lives in one self-contained file — no internet, server, or installation required.

## Run it

Open `exam.html` in any web browser (double-click it). That's it.

## Two parallel forms

The same exam exists in two interchangeable versions, so a cohort can be split
(seated neighbours get different papers) or retaken without reusing the same questions:

| File                | Form  | Questions                                                |
| ------------------- | ----- | -------------------------------------------------------- |
| `exam.html`         | Form A | Original NetClass "Quick assessment" items                |
| `exam-variant-b.html` | Form B | Brand-new parallel questions, same 10 skill areas        |

Both forms share the same settings (50% pass mark, 5-minute timer, question and
option shuffling) and the same question format, so they behave identically. No
question text or correct-answer text is shared between the two.

### Answer key

Question numbers below are the order in the file — the test shuffles them on each
attempt, so the review screen is the reliable place to check answers.

| #  | Skill area                 | Form A                                                  | Form B                                                        |
| -- | -------------------------- | ------------------------------------------------------- | ------------------------------------------------------------- |
| 1  | Number sequences           | 2, 4, 8, 16 → **32** (C)                                | 3, 6, 12, 24 → **48** (C)                                     |
| 2  | Categorical logic          | **Every router is a network device** (B)                | **Every switch is a network device** (B)                      |
| 3  | Hardware / devices         | Input device → **Keyboard** (C)                         | Output device → **Monitor** (D)                               |
| 4  | Operating systems          | **Manage hardware and applications** (B)                | **Managing files, memory, applications** (A)                  |
| 5  | Networking                 | **To share information and resources** (A)              | **Shares information, printers, internet** (B)                |
| 6  | Cybersecurity awareness    | **Do not share; verify via trusted channel** (D)        | **End the call; verify via official channel** (C)             |
| 7  | Troubleshooting            | **Check Wi-Fi / cable and network settings** (C)        | **Check printer power, cable/Wi-Fi and print queue** (A)      |
| 8  | Conditional reasoning      | **Device X connects different networks** (A)            | **File Z takes up less storage space** (B)                    |
| 9  | Problem solving            | **Split/compress or use cloud/USB** (C)                 | **Arrange a charger and test it beforehand** (C)              |
| 10 | Quantitative reasoning     | 3 : 5 with 24 boys → **40 girls** (C)                   | 4 : 7 with 28 desktops → **16 laptops** (B)                   |

If you would rather have a single, bigger pool of questions, copy the entries from
one form's `QUESTIONS` array into the other — the engine adapts to any count.

## Features

- Student name + date captured on the start screen (date pre-filled, like the paper form)
- 10 questions: the 7 from the assessment form plus logic, problem-solving and
  quantitative-reasoning questions — one at a time, with Previous / Next navigation
- **5-minute countdown timer** (turns amber under 1 minute, red under 10 seconds,
  auto-submits the test when it reaches zero)
- **Questions shuffled into a new order on every attempt/retake**
- Progress bar and answered-count
- Warns about unanswered questions before submitting
- **Immediate result** after submission: score out of 10, percentage, PASS/FAIL badge (pass mark 60%)
- Result header shows the student's name and date (prints with the result)
- Full answer review (your answer vs. correct answer for each question)
- Print result and Retake test buttons
- Works offline on desktop and mobile browsers

## Configure

Open `exam.html` in any text editor and edit `const CONFIG` at the top of the
`<script>` block:

| Setting               | Purpose                                                        |
| --------------------- | -------------------------------------------------------------- |
| `examTitle`           | Title shown on screen                                           |
| `subtitle`            | Line under the title (course / academy / cohort)                |
| `note`                | Intro note shown to the candidate                               |
| `passMarkPercent`     | Pass mark in % (default 60)                                     |
| `showPassFail`        | `true` shows the PASSED/FAILED badge. The original paper form says the assessment "is not a pass-or-fail test" — set `false` for a purely diagnostic score |
| `examDurationMinutes` | Countdown timer length in minutes (default 5, `0` = no timer)   |
| `shuffleQuestions`    | `true` shuffles question order on every attempt (default)       |

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
