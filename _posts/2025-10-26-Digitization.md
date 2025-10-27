---
  title: "Digitization"
excerpt_separator: "<!--more-->"
categories:
  - project1
tags:
  - OCR
  - python
  - digitization
image: images/my-image.jpg
---
1: At least one paragraph on the goal of the mini-project.

The goal of this mini-project was to understand and practice the full process of digitizing a physical book. By scanning the pages. The project introduces us to new tools and involves workflows and challenges that are related to digital humanities and text processing. Through this, we gained the advantage of experience with digitization technologies. Like OCR, metadata creation. Including GitHub, the main goal was to understand how training data for machine learning models contributes to improving OCR accuracy.

2: At least one paragraph on the book you digitized.

Our group selected a book for digitization from the Aga Khan Library collection, which was Two Ismaili Treatises, which includes early Ismaili texts that shed light on the philosophy, rituals, and history of the Ismaili branch of Shi’i Islam. As a part of the process, we referenced its metadata. This ensured that the digitized version could be properly listed and easily searched within digital archives.

3: At least one paragraph on the scanning process.

The first stage of the project involved scanning the book using the Aga Khan’s library high-resolution scanner. Each page was carefully digitized to maintain image quality, ensuring that the images were sharp and accurate and correctly aligned. After scanning, we cleaned the images by cropping unwanted parts, correcting the angles, and removing any blurred pages. We organized the images in a sequence and ensured the correct file naming. This stage puts more focus on the importance of accuracy and attention to detail in creating a clean data set for OCR processing.

4: A couple of paragraphs on the OCR process.

Four transcription models, developed by kraken for Arabic and Persian scripts, were tested on a three-page sample from the book.  Their performance, represented by CER (Character Error Rate) and WER (Word Error Rate) values, was measured with the usage of a Python script developed by instructors and students at the AKU-ISMC. The script also includes normalisation tables, which are used to further qualify the WER and CER results. Based on another Python script (built with the assistance of ChatGPT) involving basic and easily replicable functions – such as split and len– the highest-performing transcription model was concluded to be kraken-gen2-print-n7m5-union-ft_best. The results were then authenticated against calculations made on an excel spreadsheet.

5: At least one paragraph of reflections on the entire project.

This project was a good intersection to the start of digital humanities and machine learning.It shows how human expertise still matters in training and refinement. The process was also an exercise in collaboration, from maintaining a shared project log and cleaning data for testing and comparing OCR outputs.
One of the key lessons was the importance of normalization and documentation. Creating segmentation guidelines, using metadata templates, and creating files systematically to ensure that the work could be easily done and understood by group members.It also gives me a sense of understanding of how historical texts can be made accessible by scanning to OCR evaluation. 
