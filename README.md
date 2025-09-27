# KIP

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

The KIP corpus is part of the larger [KIParla collection](www.kiparla.it),
which can be freely queried through the [NoSketch Engine interface](https://kiparla.it/search/).

The KIP corpus was compiled within the framework of the LEAdhoC project – Linguistic Expression
of Ad Hoc Categories, funded by the Italian Ministry of Education, University and Research (MIUR)
under the SIR 2016 call.

It consists of approximately 70 hours of spoken data collected at the Universities of Bologna and
Turin. The interactions, recorded between 2016 and 2019, involved over 180 speakers, including
university students and professors from various regions of Italy, and took place in five different
types of communicative situations: lessons, exams, office hours, semi-structured interviews,
free conversations (among students).

The transcriptions have been anonymized.

Overall, the module is made up of 121 conversations and includes 184 speakers.

The KIP folder is available for download and contains:

For the entire module:

* A .csv file and a .json file with a list of speaker codes and their associated metadata
  (gender, age group, education level, profession, region of origin).
* A .csv file and a .json file with a list of conversation codes and their associated metadata
  (type of interaction, collection site, year).
* Set of conventions used in the module, .yml

For each conversation:

* Orthographic transcription in .txt format
* Transcription following Jefferson (2004) conventions in .txt format
* Transcription following Jefferson (2004) conventions in .eaf format

Due to GDPR restrictions, the pseudo-anonymized audio files in mp3 format are available under a
restricted-access license.
To gain access to the audio files, it is necessary to contact the corpus coordinators and follow
the procedure they will provide (link to KIP_audio).

## Metadata

Each participant and each conversation are associated to a series of metadata, that can be found in the
[`metadata/participants.tsv`](metadata/participants.tsv) and [`metadata/conversations.tsv`](metadata/conversations.tsv) fils.
Metadata is to be interpreted as follows:

1. Participants metadata:
    - `code`: unique anonymized 5-char identifier for each participant. Unknown, occasional participants
     to conversations are associated with a special `???` code.
    - `gender`: either `M` for masculine or `F` for feminine
    - `age-range`: 5 years range in which the age of the participant is included
    - `school-region`: Italian region[^1] where the participant has completed their school years.
     In case the participant completed school outside Italy, the label `estero` is used
    - `occupation`: either `student` or `intellectual`. In this module, participants whose occupation
     is `intellectual` are University professors.
	- Additionally, the [`metadata/participants.tsv`](metadata/participants.tsv) also contains a `conversations`
colum that summarizes the conversations in which the participant appears.
2. Conversations metadata:
   - `code`: unique identifier for conversation
   - `type`: type of interaction, possible values are `exam`, `free-conversation`, `lecture`, `office-hours` (i.e., professor - student meetings), `semistructured-interview`
   - `duration`: duration of the conversation, expressed in `hh:mm:ss` format
   - `participants-number`: number of participants to the conversation
   - `participants-relationship`: relation, either symmetric or asymmetric, holding among speakers
   - `moderator`: presence of a moderator
   - `topic`: either free or fixed
   - `year`: year of collection
   - `collection-point`: two letter code of the area where the conversation was collected. Possible values for this module are `BO` for Bologna and `TO` for Turin.
   - Additionally, the [`metadata/conversations.tsv`](metadata/conversations.tsv) also contains a `participants` field that recaps the codes of the participants to that conversation

[^1]: `abruzzo`, `basilicata`, `calabria`, `campania`, `emilia-romagna`, `friuli-venezia-giulia`, `lazio`, `liguria`, `lombardia`, `marche`, `molise`, `piemonte`, `puglia`, `sardegna`, `sicilia`, `toscana`, `trentino-alto-adige`, `umbria`, `valle-d-aosta`, `veneto`
-----

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

<!-- [![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa] -->

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg