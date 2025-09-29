# KIP

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

- [KIP](#kip)
  - [Repository organization](#repository-organization)
  - [Metadata](#metadata)
  - [Verticalized content](#verticalized-content)
  - [How to cite](#how-to-cite)

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

## Repository organization

This repository contains:

* metadata for both speakers and conversations, in the [`metadata`](./metadata/) subfolder (see [metadata](#metadata) section below)
* descriptions of the set of transcription conventions used for this module ([Transcription conventions](./transcription-conventions.md))

For each conversation:

* `.eaf` file in [`eaf/`](./eaf/) folder: these files contain time-aligned Jefferson-style transcriptions
  and can be opened with [ELAN]() software
* `.txt` file in [`linear-jefferson/`](./linear-jefferson/) folder: linearized version of the
  Jeffersonian-style transcription
* `.txt` file in [`linear-orthographic/`](./linear-orthographic/) folder: linearized version of the
  transcription, retaining only orthographic words
* `.tsv` file in [`tsv/`](./tsv/) folder: this file containes a verticalized version of the transcription,
  with Jefferson-style information decoupled from text as features. See [verticalized-content](#verticalized-content) for more information.
  information

Both files in the [`linear-jefferson/`](./linear-jefferson/) and [`linear-orthographic/`](./linear-orthographic/) transcription contain one Transcription Unit per line, each line is composed of
two colums, the first containing the speaker code.
Transcription Units are sorted by their starting time.

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

## Verticalized content

Each file in the [`tsv/`](./tsv/) folder contains 12 columns, as follows:

1. `token_id`: unique token identifier within the conversation
2. `speaker`:
3. `tu_id`:
4. `span`:
5. `form`:
6. `type`:
7. `jefferson_feats`:
8. `align`:
9. `prolongations`:
10. `pace`:
11. `guesses`:
12. `overlaps`:


## How to cite

To cite this module please include

> Goria, E., & Mauri, C. (2018). Il corpus KIParla: una nuova risorsa per lo studio dell’italiano parlato. _CLUB Working Papers in Linguistics_, 2, 96–116

in your references

```bibtex
  @article{Goria_Il_corpus_KIParla_2018,
    author = {Goria, Eugenio and Mauri, Caterina},
    journal = {CLUB Working Papers in Linguistics},
    pages = {96--116},
    title = {{Il corpus KIParla: una nuova risorsa per lo studio dell’italiano parlato}},
    volume = {2},
    year = {2018}
  }
```

-----

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

<!-- [![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa] -->

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg