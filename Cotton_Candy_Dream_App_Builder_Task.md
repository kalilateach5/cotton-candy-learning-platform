# Dream Version App Builder Task

Create a production-grade, responsive Cotton Candy Math Review app using the attached student and teacher prototypes as visual and functional references.

## Required roles
- Student: can access only their own assessment and completion receipt.
- Teacher: can access all class results, filters, analytics, and exports.

## Authentication and data
- Use Microsoft 365 identity where available.
- Use Microsoft Lists as the centralized backend if supported.
- Never expose correct answers, answer-key fields, or other students' data to the student role.
- Save after every answer so progress can resume.

## Student features
- Required name, date, and period.
- 21 branching questions.
- Incorrect choices show hints without revealing answers.
- Correct choice unlocks the next question.
- Previous navigation and progress saving.
- 5 points on first try, subtract 1 per incorrect attempt, minimum 1 point.
- Track attempts, selected wrong choices, points, time per question, and rapid-guess flags.
- Badges at questions 7, 14, and 20.
- Completion receipt suitable for Canvas submission.

## Teacher dashboard
- Filters by period, student, completion date, and completion status.
- Student score, total attempts, rapid-guess flags, and completion timestamp.
- Per-question average points, average attempts, wrong-choice distribution, time distribution, and skill/standard grouping.
- Student detail drill-down.
- CSV export compatible with teacher review and Canvas grade preparation.
- Configurable rapid-guess threshold.

## Visual design
- Vivid cotton-candy palette: hot pink, sky blue, purple, mint, yellow, and white.
- Rounded cards, large accessible typography, clear contrast, responsive mobile layout.
- Celebrate progress without revealing answers.

## Canvas
- If direct Canvas integration is not supported, preserve downloadable completion receipts and CSV exports.

## Question bank
```json
[
  {
    "id": 1,
    "standard": "Real numbers",
    "question": "Which number below represents an irrational number?",
    "options": [
      "0.625",
      "9/4",
      "√50",
      "-7"
    ],
    "answer": 2,
    "hint": "Check whether the square root is a perfect square."
  },
  {
    "id": 2,
    "standard": "Compare real numbers",
    "question": "Which number will NOT make √196 < x < 15 3/4 true?",
    "options": [
      "1450%",
      "0.125",
      "14.8",
      "√225"
    ],
    "answer": 1,
    "hint": "Convert each choice to a decimal and compare with 14 and 15.75."
  },
  {
    "id": 3,
    "standard": "Square roots",
    "question": "A square has area 484 square feet. What is its perimeter?",
    "options": [
      "22 ft",
      "44 ft",
      "88 ft",
      "1,936 ft"
    ],
    "answer": 2,
    "hint": "Find the side with √484, then multiply by 4."
  },
  {
    "id": 4,
    "standard": "Order real numbers",
    "question": "Which order is least to greatest: Ava 1/8, Ben 13%, Chloe 0.15, Diego 1/5?",
    "options": [
      "Ava, Ben, Chloe, Diego",
      "Ben, Ava, Chloe, Diego",
      "Ben, Chloe, Ava, Diego",
      "Diego, Chloe, Ben, Ava"
    ],
    "answer": 0,
    "hint": "Write every amount as a decimal."
  },
  {
    "id": 5,
    "standard": "Compare real numbers",
    "question": "Who has the largest answer: Maya 2.9, Ethan 14/5, Sofia √9, Liam 1 + √5?",
    "options": [
      "Maya",
      "Ethan",
      "Sofia",
      "Liam"
    ],
    "answer": 3,
    "hint": "Estimate √5 and convert 14/5."
  },
  {
    "id": 6,
    "standard": "Square roots",
    "question": "Will a √144-foot bookshelf fit in an 11-foot storage unit?",
    "options": [
      "Yes",
      "No"
    ],
    "answer": 1,
    "hint": "Evaluate √144 before comparing."
  },
  {
    "id": 7,
    "standard": "Scientific notation",
    "question": "Write 0.0000527 in scientific notation.",
    "options": [
      "5.27 × 10⁻⁵",
      "5.27 × 10⁵",
      "52.7 × 10⁻⁶",
      "0.527 × 10⁻⁴"
    ],
    "answer": 0,
    "hint": "The coefficient must be at least 1 and less than 10."
  },
  {
    "id": 8,
    "standard": "Estimate square roots",
    "question": "Between which consecutive whole numbers is √80?",
    "options": [
      "7 and 8",
      "8 and 9",
      "9 and 10",
      "10 and 11"
    ],
    "answer": 1,
    "hint": "Use nearby perfect squares 64 and 81."
  },
  {
    "id": 9,
    "standard": "Compare real numbers",
    "question": "Which set contains only numbers less than -0.4?",
    "options": [
      "-1/2, -1.2, -√1",
      "-0.35, 25%, -0.39",
      "-1/2, -0.35, -0.39",
      "25%, -1.2, -√1"
    ],
    "answer": 0,
    "hint": "Check signs and compare values on a number line."
  },
  {
    "id": 10,
    "standard": "Order real numbers",
    "question": "Which list is in ascending order?",
    "options": [
      "-2.5, -2, 280%, √8, 3.5 × 10²",
      "-2, -2.5, √8, 280%, 3.5 × 10²",
      "√8, -2.5, -2, 280%, 3.5 × 10²",
      "-2.5, 280%, -2, √8, 3.5 × 10²"
    ],
    "answer": 0,
    "hint": "Convert 280% to 2.8 and estimate √8."
  },
  {
    "id": 11,
    "standard": "Irrational numbers",
    "question": "Which statement about irrational decimals is true?",
    "options": [
      "They always terminate.",
      "They repeat forever.",
      "They neither terminate nor repeat.",
      "All decimals are irrational."
    ],
    "answer": 2,
    "hint": "Think about the decimal form of π."
  },
  {
    "id": 12,
    "standard": "Evaluate expressions",
    "question": "Evaluate -6x + y² when x = 5 and y = 8.",
    "options": [
      "34",
      "58",
      "94",
      "-34"
    ],
    "answer": 0,
    "hint": "Substitute first, then use order of operations."
  },
  {
    "id": 13,
    "standard": "Scientific notation",
    "question": "Which is NOT correct scientific notation?",
    "options": [
      "4.2 × 10⁵",
      "0.42 × 10⁶",
      "7.1 × 10⁻³",
      "9.8 × 10²"
    ],
    "answer": 1,
    "hint": "The coefficient must be from 1 up to, but not including, 10."
  },
  {
    "id": 14,
    "standard": "Real number system",
    "question": "Which number is misplaced in the irrational group?",
    "options": [
      "√225",
      "π",
      "√12",
      "None"
    ],
    "answer": 0,
    "hint": "Evaluate the perfect square root."
  },
  {
    "id": 15,
    "standard": "Order real numbers",
    "question": "Which runner order is fastest to slowest?",
    "options": [
      "Noah, Olivia, Emma, Lucas, Mia",
      "Olivia, Noah, Emma, Lucas, Mia",
      "Emma, Noah, Olivia, Lucas, Mia",
      "Mia, Lucas, Emma, Olivia, Noah"
    ],
    "answer": 0,
    "hint": "Convert the times to 42.5, 43, 43, 43.5, and 44.2 seconds."
  },
  {
    "id": 16,
    "standard": "Scientific notation",
    "question": "Write 8.04 × 10⁴ in standard form.",
    "options": [
      "804",
      "8,040",
      "80,400",
      "804,000"
    ],
    "answer": 2,
    "hint": "Move the decimal four places right."
  },
  {
    "id": 17,
    "standard": "Scientific notation",
    "question": "Write 5.6 × 10⁻³ in standard form.",
    "options": [
      "0.0056",
      "0.056",
      "560",
      "5,600"
    ],
    "answer": 0,
    "hint": "A negative exponent makes a number less than 1."
  },
  {
    "id": 18,
    "standard": "Estimate square roots",
    "question": "Which is the best estimate for √18?",
    "options": [
      "3.2",
      "4.24",
      "4.8",
      "5.2"
    ],
    "answer": 1,
    "hint": "√18 lies between √16 and √25."
  },
  {
    "id": 19,
    "standard": "Real number system",
    "question": "How are whole numbers W related to real numbers R?",
    "options": [
      "W is completely inside R.",
      "R is completely inside W.",
      "They are separate.",
      "They overlap only."
    ],
    "answer": 0,
    "hint": "Every whole number is a real number."
  },
  {
    "id": 20,
    "standard": "Evaluate expressions",
    "question": "Evaluate (-24 + √81 + 5³) ÷ [(3/4)(16) - 2].",
    "options": [
      "9",
      "10",
      "11",
      "12"
    ],
    "answer": 2,
    "hint": "Evaluate the numerator and denominator separately."
  },
  {
    "id": 21,
    "standard": "Scientific notation",
    "question": "Order 6.3×10⁻⁷, 6.3×10⁻², 6.3×10⁴, 6.3×10¹⁰ ascending.",
    "options": [
      "As shown",
      "Reverse order",
      "-2, -7, 4, 10",
      "-7, 4, -2, 10"
    ],
    "answer": 0,
    "hint": "The coefficients match, so compare the exponents."
  }
]
```
