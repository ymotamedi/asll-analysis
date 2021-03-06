# Evolving artificial sign languages in the lab

The files in this repository include data files and analysis for data across 3 experiments of a study that looks at the roles that interaction between language users and transmission of language to new users play in the evolution of systematic linguistic structure.

Video data for the study can be found on the University of Edinburgh's DataShare, at https://datashare.is.ed.ac.uk/handle/10283/3191.

## Data files

There are separate data files for experiments 1, 2 and 3.

Each file contains the following columns

* **acc** - accuracy score for interaction trials (1 if correct, 0 if incorrect).
* **chain** - refers to transmission chain or pair. There are 5 chains in each condition of each experiment.
* **code_string** - gloss of gesture video provided by first coder.
* **condition** - which condition participant is assigned to.
* **director** - tag denoting which participant produced the gesture for that video. Note that this column is irrelevant for any analysis, and was included as a diagnostic check during data collection.
* **ent_type** - the functional dimension associated with the meaning; can be *person*, *location*, *object* or *action*.
* **generation** - which generation the participant was assigned to. Each chain is comprised of 5 generations. The seed gestures for each chain are tagged as generation 0.
* **guess_time** - for interaction trials only. Notes the time between the gesture being completed and the matcher selecting a response.
* **markerPres** - notes the presence or absence of a marker on the functional association (i.e. based on ent_type).
* **model** - notes which participant from the previous generation acted as a model for the generation given on each row.
* **participant** - participant identifier.
* **phase** - notes whether data shown is training or testing. Only testing data is shown here, and training data was not analysed.
* **selected** - notes which meaning was selected as a response by the matcher in interaction trials.
* **target** - the intended target meaning for that trial.
* **terminator** - notes which participant terminated the video stream in interaciton trials.
* **trial** - trial number.
* **verb** - binary variable categorising noun targets from verb targets.
* **vid_len** - length of gesture video recorded, in seconds.

In addition, the file **seed_info.csv** gives identifiers for seed videos, allowing linking between generation 0 in the data files and seed videos stored at the link given above. This file contains the following columns:

* **target word** - word the gesture is intended to represent
* **vid.length** - length of the video in seconds (approx. 7 seconds for all seed videos)
* **participant** - participant/video identifier
* **set** - two seed sets were recorded; this denotes which set the video belongs to
* **vid.name** - name of the video file as stored in the DataShare repository

## Analysis notebooks

The analysis notebooks are Jupyter Notebooks that run a Python 2.7 kernel and the rpy2 library, that allows cells in R to be inserted into a notebook using a Python kernel. Analysis is divided into three notebooks.

* **Efficiency results** - results pertaining to efficiency measures. This includes measures of gesture length and the frequency of repeated gestures.
* **Systematicity results** - results pertaining to systematicity measures. This includes measures of marker frequency and entropy of gesture sets.
* **Supplementary results** - results found in the supplementary materials of the written manuscript. This includes a plot showing frequency of handshapes in each chain and generation of experiment 1, measures of communicative accuracy, measures of alignment during interaction, and measures of transmission fidelity.
