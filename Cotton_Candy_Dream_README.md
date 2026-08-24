# Cotton Candy Math Review - Dream Version

## Included
- `student_app.html`: Student assessment with required name/date/period, branching hints, locked progression, 5-to-1 attempt-based scoring, time tracking, rapid-guess flags, badges, and JSON/CSV receipts.
- `teacher_dashboard.html`: Imports multiple student JSON receipts, filters by period/student, summarizes class scores, shows per-question analytics, flags rapid guessing, and exports a class CSV.
- `app_builder_task.md`: Production build specification for Microsoft Copilot App Builder.

## Current local workflow
1. Teacher posts `student_app.html` in Canvas or another approved location.
2. Student opens the app in a browser, completes it, and downloads the JSON receipt.
3. Student submits the JSON receipt in Canvas.
4. Teacher downloads all JSON receipts and opens `teacher_dashboard.html`.
5. Teacher imports all receipts at once.

## Important limitation
This prototype stores results locally and relies on student-uploaded receipts. It is not a secure centralized database. The production version should use authenticated student accounts and Microsoft Lists or another approved backend.
