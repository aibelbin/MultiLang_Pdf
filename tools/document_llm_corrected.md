Here is the reformatted text in markdown:

# PS-05: Intelligent Multilingual Document Understanding

## General Description

With the explosion of digital technology, we have amassed a huge collection of documents in various formats. These documents are structured, visually rich, and multilingual—ranging from legal contracts, academic papers to business reports, government forms, and presentation decks, social media posts, and personal screen shots. These documents exist in diverse formats such as Word documents (DOC, DOCX), PDFs, PowerPoint slides (PPT), and scanned images (jpeg, png) and including handwritten documents, often containing mixed scripts (e.g., English-Arabic or Hindi-English, Chinese-English, etc.).

Traditional OCRs do not extract semantically correct text from various elements present in the documents. The elements may be Table, Image, Maps, Charts. The extracted text is inadvertently mixed/jumbled which is not conducive for downstream AIML-related tasks. Moreover, mixed scripts present in the document make the text extraction challenging.

The AI systems need to generate structured outputs from these documents for better indexing and maintaining document layout, enabling better multilingual keyword search and boosting performance of various downstream models such as machine translation, vector search, Named Entity Recognition, Retrieval Augmented Generation.

## The Challenge

Multilingual layout-aware document parsing across scripts, formats, and writing directions. The following languages will be present in the documents:

* English
* Hindi
* Urdu
* Arabic
* Nepalese
* Persian

Accurately extracting structured information from documents while preserving:

* Visual hierarchy (headings, sections)
* Semantic grouping (form fields, captions, references)
* Layout fidelity (table structures, image alignment, reading order)
* Embedded elements like charts, plots, maps, and figures

Representing the extracted content in a standardized, machine-friendly yet human-readable format.

A document may contain the following:

* Plain text (headers, paragraphs)
* Table
* Image
* Map
* Charts

## Solution Requirements

The solution should be able to:

* Localize the above components and convert them into natural language text
* Provide the output in json format with languages identified
* The output for the Table, Image, Map, Charts should be the natural language description of the contents

## Dataset

The indicative datasets would be used for preparing the first two stages for train/test datasets (not limited to):

* DocLayNet
* PubLayNet
* RvICdip
* ICDAR-MLT 2019
* HI-OCR
* FUNSD
* SROIE

In the third stage, organisation specific data would be used.

## Metrics for Evaluation

* Stage 1: Document Layout Mean Average Precision
* Stage 2:
	+ Document layout, text extraction, and
	+ MaP (Mean Average Precision) for Document layout
	+ CER (Character Error Rate)/ WER (word Error rate) for Text Extraction
	+ BlueRT + BertScore for Chart, Map
	+ T2T-Gen for Table to Natural Language Text
	+ Language Identification accuracy, precision, recall

## Dataset Arrangement for Stage-1

* Training Dataset (upto 10 GB): train_set.zip
* Mock Dataset (upto 10 GB): Mock_set.zip
* Shortlisting Dataset (upto 10 GB): short_listing_set.zip
* Holdout Test Set (upto 10 GB): After the Challenge deadline, a private ranking will be computed using this holdout set.

## Input/Output Instructions

* Input: The input to the participants would be jpeg/png images of documents. The datasets may also have rotated/blurred/noisy images also.
* Output: The participants needs to submit one json corresponding to each input image with the details of bbox in [x,y,h,w] and the class of the detected segments(including the rotated one also).

## Online Solution during Stage-1 (Mock Datasets)

* Solutions are expected to be submitted on Thursday from week commencing 15 Sep 2025, on the Mock Dataset.
* Leadersboard will be updated every Tuesday.
* Scores will be computed based on the evaluation metrics as under: -
	+ %Weight Category Criteria Description
	- Classification | 100
	- and Localization | Score

## Selection of 15-20 participants for offline-evaluation in Stage-1

* On 4 Nov 2025, the details of Shortlisting Dataset will be made available on the website. Results generated on the Shortlisting Dataset will be evaluated for final selection of 15-20 participants.
* The shortlisted participants will be published along with the cut-off score as per the evaluation criteria.

## Solution Evaluation at the end of Stage-1 Deadline (Holdout Dataset)

* ...

Please let me know if you have any further requests!Here is the reformatted text in markdown:

# Stage-1 Deadline (Holdout Dataset)

Shortlisted participants will be asked to demonstrate their solution at IIT Delhi on completion of stage-1 deadline.

# Evaluation Criteria

Participants will be allotted slots in which they need to run their solution on reference data provided by the organizers on given resources with following specifications:

* OS — Ubuntu 24.04 LTS
* CPU—48+ cores
* RAM— 256+ GB
* GPU - A-100, 40/80 GB

* Solution Demo Duration: 02 Hours for each selected participant

Based on the results from solution demonstration and presentation, final scores will be computed based on Evaluation Metrics as mentioned below:

### Evaluation Metrics

| Category | Criteria | Description | % Weight |
| --- | --- | --- | --- |
| Solution | Solution Score based on official | 50 |
|  | mAP Score metric on hidden hold-out test dataset |  |
| Solution | Solution Execution time | 10 |
|  | Robustness | Efficiency on hold-out test dataset (average per data point) | 5 |
| Solution | Solution Memory used | 10 |
|  | Resource Utilization |  |
| Approach | Methodologies | Start-up needs to present Solution Development approaches & proposed Architecture | 20 |
| Team | Technical Team Composition, Capabilities | Capabilities of Start-up Team | Experience and ability to complete the challenge end to end. | 10 |

d. Participants are free to use any language or development framework for the solution.

e. At most top 6 teams will be selected based on final score for Phase-2.

# Evaluation Criteria for Stage-2 and Stage-3

9. Evaluation Criteria for Stage-ll and Stage-Ill would be similar as above, only the metrics would change as per ‘Metric for evaluation’ in Para 3 above. The relative weightages of various parameters would be released before start of that stage. Apart from the languages given in para 2 a. above, a couple of more languages would be released for Stage-2 and Stage-3 participants.

# Sessions with Mentors/Experts

a. For Stage-1, the organisers plan to meet participants via online meet or email to resolve their doubts, if any. This provision will be made active from 15th August 2025 and details regarding interaction will be shared on this website. Kindly keep viewing this website regularly for updates on this.

b. There will be sessions with Mentors/Experts in Stage-2 and Stage-3 for the willing selected participants to help them in achieving the best solutions.