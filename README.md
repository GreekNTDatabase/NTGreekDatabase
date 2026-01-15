# Greek New Testament Vocabulary Dataset

This repository provides clean, structured Greek New Testament vocabulary
datasets designed for learners, teachers, and researchers.

The data is published as UTF-8 CSV files suitable for spreadsheets,
flashcards, and computational analysis, with a focus on transparency,
reusability, and learner-driven workflows.

---

## Project Background

This project began as a personal learning tool.

While studying New Testament Greek, I wanted a **simple and repeatable way to
build and maintain vocabulary flashcards directly from the text**—without
manually copying words, losing context, or relying on proprietary software.

In particular, I wanted:

- vocabulary ordered by *actual reading sequence*
- reliable identification of **first occurrences**
- clean data that could be freely sorted, filtered, and re-ordered
- a format that worked equally well in Excel, flashcard apps, and scripts
- a dataset I could re-upload or regenerate without friction

To solve this, I built a complete Greek New Testament vocabulary database for
my own study and flashcard uploads. Once the dataset was complete, stable,
and internally consistent, I decided to publish it openly so others could
benefit from the same workflow.

This repository is the result.

---

## Reading Order: *Greek for Life*

One set of datasets in this repository follows the reading order recommended
in:

**_Greek for Life: Strategies for Learning, Retaining, and Reviving New Testament Greek_**  
by Jonathan T. Pennington

📘 Amazon link:  
https://www.amazon.com/Greek-Life-Strategies-Retaining-Testament/dp/0801093201/

The book emphasizes reading-based vocabulary acquisition and long-term
retention rather than isolated memorization.

The **Reading Order** datasets reflect this approach by introducing vocabulary
in the order it is first encountered through the recommended reading sequence,
making them especially useful for learners building flashcards alongside
active reading.

---

## Dataset Variants

Four complementary datasets are provided. Each answers a different learning
or research question while sharing the same underlying data model.

### Canonical Order
- **Unique Forms**  
  Unique Greek word forms ordered by first occurrence in the traditional
  New Testament canonical sequence.
- **All Occurrences**  
  Complete corpus ordered canonically, preserving repetition.

### Reading Order (Greek for Life)
- **Unique Forms**  
  Unique Greek word forms ordered by first occurrence using the Greek for Life
  reading sequence.
- **All Occurrences**  
  All word occurrences ordered by the same reading sequence.

---

## Schema

Each CSV uses the following columns:

- `greek_word` — surface Greek text (polytonic Unicode)
- `english_translation` — interlinear gloss
- `parsing_abbreviation` — morphology code
- `strongs_number` — Strong’s Greek number
- `chapter_ref` — book and chapter of first occurrence
- `ordinal` — original row order index

### Ordinal Column

The `ordinal` column preserves the **original sequence of the dataset** prior
to any filtering, sorting, or deduplication.

This allows users to:
- sort or filter freely
- deduplicate safely
- restore the original order deterministically at any time

Ordinal values are 1-based, monotonically increasing, and stable within each
dataset.

---

## Encoding and Compatibility

All CSV files are encoded as **UTF-8 with BOM** to ensure compatibility with:

- Microsoft Excel
- LibreOffice
- Google Sheets
- Flashcard software (e.g., Flashcards Deluxe)
- Programming and data analysis tools

Note: CSV files may appear as plain text in a web browser. Download the files
and open them in a spreadsheet or flashcard application for proper formatting.

---

## License

This dataset is licensed under **Creative Commons Attribution 4.0 (CC BY 4.0)**.

You are free to use, share, and adapt the data with appropriate attribution.
See the LICENSE file for details.
