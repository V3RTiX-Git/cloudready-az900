# CloudReady — AZ-900 Exam Coach

An independent, local-first practice app for Microsoft Azure Fundamentals (AZ-900). Open `index.html` in a browser — there is no build step, backend, account, or API key.

CloudReady is not affiliated with or endorsed by Microsoft.

## What it does
- Original multiple-choice questions across all three AZ-900 skill domains: cloud concepts, Azure architecture and services, and management and governance
- Mixed quizzes (8 questions, drawn from all three domains) and topic quizzes (that domain's full set)
- Immediate check, correct-answer highlight, explanation, and a short "why not the others" note
- Session results with retry for questions missed in that session (including topic-specific quizzes)
- Dashboard stats based on each question's **latest** saved answer, so revisiting a question does not inflate the unique-answered count
- A readiness estimate that stays hidden until you have at least 8 unique answers and have practised all 3 domains. It is a rough in-app signal, not a prediction or guarantee of passing
- Progress stored in this browser's `localStorage` under `cloudready-v1`. If storage is blocked or data is malformed, the app still loads
- Reset asks for confirmation before clearing saved progress

## Run locally
1. Open the project folder.
2. Double-click `index.html`, or in this folder run:

```bash
python -m http.server 8000
```

3. Visit `http://localhost:8000`.

A Live Server (or similar) extension also works. Use a current Chromium, Firefox, or Edge browser.

## Publish
You can host the files as a static site (for example GitHub Pages):
1. Put `index.html` and `README.md` at the site root.
2. Deploy from the default branch, `/ (root)`.
3. Wait for the host to publish the URL.

## Manual test checklist
1. Overview → **Start practice** starts a mixed quiz.
2. Topic explorer → **Practise this domain** starts only that domain's questions.
3. Choose an answer → **Check answer** shows correct/incorrect state and explanations → **Next question** through the set → results.
4. From results, **Retry missed questions** (after a topic quiz too) only repeats that session's misses and keeps the topic scope.
5. Finish or skip retry, start another quiz, then **Dashboard** / Overview.
6. Answer the same question again later: unique answered count should not increase; latest answer should update accuracy.
7. **Reset** must show a confirm dialog; cancelling leaves data; confirming clears stats.
8. Practice quiz in the nav shows a chooser if no quiz is running, or resumes an in-progress / results screen.
9. Readiness stays **—** until 8 unique questions and all 3 domains have answers.

## Content note
Practice items are independently written. They are not official exam questions. Topics follow Microsoft's published AZ-900 skills measured outline as of July 20, 2026. Always use current Microsoft Learn material as the source of truth.

Official study guide: https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-900

## Disclaimer
CloudReady is an independent learning project. It is not affiliated with or endorsed by Microsoft. AZ-900 is a Microsoft certification.

## Privacy
Quiz activity stays in this browser. It is not synced across devices. Reset, clearing site data, or a private window without storage will drop progress.
