# BioPractice — Personal Biology MCQ Website

A mobile-friendly, browser-based Biology MCQ practice tool. It is designed for personal use and stores the question bank in IndexedDB on the current device.

## Included features
- Bilingual English + Hindi questions, options and explanations.
- NCERT-based and competitive-exam source labels.
- Chapter-wise practice and full-length Biology examinations.
- Five options (A–E), random or bank-order selection.
- Practice mode with immediate answer feedback.
- Exam timer, question palette, mark-for-review, positive and negative marking.
- Result analysis: score, correct, incorrect, unanswered, accuracy and chapter-wise breakdown.
- Add/edit/delete questions; import and export the question bank as JSON.
- Local session history and dark mode.

## Run on a phone or computer
1. Extract `BioPractice-Website.zip`.
2. Open `index.html` in a recent browser (Chrome, Edge or Firefox).
3. The first launch inserts a small sample question bank. You can add questions or import your own JSON bank.
4. Use **Export JSON** regularly to back up your question bank.

If opening the file directly is blocked by your browser, serve the folder using a simple local web server or publish the folder to a static hosting service. No account or backend is required.

## Question JSON format
Each item follows this structure:

```json
{
  "id": "unique-id",
  "subject": "Biology",
  "chapter": "Cell: The Unit of Life",
  "topic": "Cell organelles",
  "source": "NCERT",
  "difficulty": "Easy",
  "question": {"en": "Question in English", "hi": "प्रश्न हिंदी में"},
  "options": {
    "en": ["Option A", "Option B", "Option C", "Option D", "Option E"],
    "hi": ["विकल्प A", "विकल्प B", "विकल्प C", "विकल्प D", "विकल्प E"]
  },
  "answer": 1,
  "explanation": {"en": "Explanation", "hi": "व्याख्या"}
}
```

`answer` is zero-based: 0 = A, 1 = B, 2 = C, 3 = D, 4 = E. `source` should be `NCERT` or `Competitive`.

## Important limitations
- Data is stored in the browser on this device. Clearing browser site data can erase the question bank and history; keep JSON backups.
- The app does not sync between devices.
- This is a personal learning tool, not a secure examination system. A technically capable user can inspect client-side code and answer keys.
- Sample questions are starter examples only. Verify factual content against standard textbooks and authoritative references before relying on a question bank for formal assessment.
