---
title: " OCR Evaluation."
excerpt_separator: "<!--more-->"
categories:
  - project1
image: images/OCR-Image.jpg
---

Analyzing Handwritten text recognition (HTR) systems usually relates to numerical numbers such as Character Error Rate (CER) 
and Word Error Rate (WER). CER includes the number of insertions, deletions, and substitutions that are required to change 
the system’s output into the correct text, divided by the total number of characters. This gives a percentage of
character-level error. Similarly, WER measures the errors at the word level: how many words are wrong, missing, 
or extra, compared to the total number of words. These numbers are helpful because they give clear, quantitative measures 
of performance; easy to calculate, compare across models, and record improvements over time. By applying these measures, 
we can standardize the HTR system and measure progress in an orderly manner.
<!--more-->

The good starting points are CER and WER. However, they are not sufficient for analyzing HTR in all real-world contexts. One limit is that they treat all errors equally and only focus on raw text differences, instead of meaning, structure, and usage. For example, an HTR system might misinterpret a date or a proper name, which can be important historically and legally, and CER might remain low because the few characters are wrong. In such cases, the error is major, but the numbers don’t convey its importance. Furthermore, these numbers acquire correct segmentation into lines, words, and characters. When dealing with handwritten documents, and most importantly, historical manuscripts with irregular layouts and annotations, the system might produce a text string with a few character mistakes but completely disordered segments; the rate of error looks acceptable even if the output is unusable.

Additionally, word-based metrics like WER struggle when word boundaries are ambiguous or absent, as in older scripts or in languages with no spaces between words, meaning WER may not capture meaningful error patterns. Also, both CER and WER offer little insight into which types of errors occur (e.g., confusion among visually similar characters, missing diacritics, and layout errors), which limits their value in root-cause analysis and targeted improvements. They don’t reflect whether the recognized text supports downstream tasks such as searchability, indexation, or semantic queries.

In addition, word-based numbers like WER face trouble when word boundaries are absent, as in older scripts and languages with no spaces between words.  WER doesn’t always capture meaningful error patterns. In short, CER and WER are valuable and quick measures of HTR accuracy; they should be complemented by qualitative evaluation and domain-specific assessments. For example, one might check the accuracy of critical fields (names, dates), check the structure correctness, or measure how it can be used and read in the intended workflow. In applications such as digitizing historical documents, manuscripts, or multilingual texts, evaluation should include usability, layout fidelity, and semantic correctness. Thus, numerical error rates are helpful but not sufficient on their own; they form the beginning of evaluation, not the full story.



