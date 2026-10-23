# Week 2 — Build the Foundation for Responsible AI

## Goal
Build a small, trustworthy dataset of health-information examples and a clear method for checking whether an AI explanation is accurate, simple, complete, clear, and safe.

## What I did
1. **Picked 5 topics:** high blood pressure, diabetes, asthma, dehydration, and the common cold.
2. **Found trusted sources** (not just the first search result):
   - High blood pressure: NHLBI (National Heart, Lung, and Blood Institute, part of NIH)
   - Diabetes: NIDDK (National Institute of Diabetes and Digestive and Kidney Diseases, part of NIH)
   - Asthma, dehydration, common cold: MedlinePlus (U.S. National Library of Medicine)
3. **Wrote a plain-language explanation** for each passage and checked it against the original so the meaning didn't change. → `evaluation_dataset.csv`
4. **Created the evaluation framework** with 5 criteria (Accuracy, Simplicity, Completeness, Safety, Clarity), scoring guides, and a pass/fail rule. → `evaluation_framework.md`
5. **Listed 9 possible AI risks** with examples from our own topics. → `AI_Risks.md`
6. **Scored my own explanations** with the framework, with a reason for each score. → `human_evaluation.csv`

## Self-evaluation results

| ID | Topic | Accuracy | Simplicity | Completeness | Safety | Clarity |
|---|---|---|---|---|---|---|
| 001 | High blood pressure | Yes | 4 | Yes | Yes | 5 |
| 002 | Diabetes | Yes | 4 | Yes | Yes | 4 |
| 003 | Asthma | Yes | 5 | Yes | Yes | 5 |
| 004 | Dehydration | Yes | 5 | Yes | Yes | 5 |
| 005 | Common cold | Yes | 5 | Yes | Yes | 5 |

All 5 pass. The diabetes example scored lowest because it needs medical words (insulin, hormone, pancreas) that can't be removed without losing meaning, so they were explained instead.

## What I learned
- **Simple isn't automatically safe.** You can make a sentence shorter by dropping "can be life-threatening," but that removes the most important part.
- **Some medical words should stay.** Removing "hypertension" completely would make it harder for someone to recognize the word at the doctor's office. It's better to keep the term and explain it.
- **Accuracy and safety have to be "must pass."** A really easy-to-read answer that's wrong is worse than a harder one that's right.
- **Wording Yes/No questions carefully matters.** "Did it leave out something important?" makes "Yes" mean bad, which is confusing, so all Yes/No questions were rewritten so Yes = good.

## What I found difficult
- Finding the exact original text from trusted sources instead of summaries.
- Deciding how much to simplify without changing the meaning (for example, "inflamed" → "swollen").
- Scoring my own work fairly, since it's easy to be too generous with your own explanations.

## Week 2 checklist
- [x] Selected 5 health topics
- [x] Found trusted sources for each topic
- [x] Recorded the original passages and sources
- [x] Wrote simple explanations
- [x] Created the evaluation criteria
- [x] Understand why accuracy and safety matter
- [x] Identified at least 5 possible AI risks
- [x] Evaluated my own examples
- [x] Documented work in Week_2.md
- [ ] Uploaded/committed the files to the project repository

## Next (Week 3)
Give the AI the same five passages, score its answers with the framework, and compare them with the human-written scores.
