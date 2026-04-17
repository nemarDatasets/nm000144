[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.nm000144-blue)](https://doi.org/10.82901/nemar.nm000144)

# BNCI 2015-004 Mental tasks dataset

BNCI 2015-004 Mental tasks dataset.

## Dataset Overview

- **Code**: BNCI2015-004
- **Paradigm**: imagery
- **DOI**: 10.1371/journal.pone.0123727
- **Subjects**: 9
- **Sessions per subject**: 2
- **Events**: math=1, letter=2, rotation=3, count=4, baseline=5
- **Trial interval**: [0, 4] s
- **File format**: gdf
- **Data preprocessed**: True

## Acquisition

- **Sampling rate**: 256.0 Hz
- **Number of channels**: 30
- **Channel types**: eeg=30
- **Channel names**: AFz, F7, F3, Fz, F4, F8, FC3, FCz, FC4, T3, C3, Cz, C4, T4, CP3, CPz, CP4, P7, P5, P3, P1, Pz, P2, P4, P6, P8, PO3, PO4, O1, O2
- **Montage**: 10-20
- **Hardware**: g.tec
- **Reference**: left and right mastoid
- **Ground**: left and right mastoid
- **Sensor type**: active electrode
- **Line frequency**: 50.0 Hz
- **Online filters**: 0.5-100 Hz bandpass, 50 Hz notch
- **Cap manufacturer**: g.tec
- **Electrode type**: g.LADYbird active electrodes
- **Auxiliary channels**: EOG (2 ch, horizontal, vertical)

## Participants

- **Number of subjects**: 9
- **Health status**: CNS tissue damage
- **Clinical population**: stroke and spinal cord injury
- **Age**: mean=38.0, std=10.0, min=20, max=57
- **Gender distribution**: male=2, female=7
- **Handedness**: not specified
- **BCI experience**: naive
- **Species**: human

## Experimental Protocol

- **Paradigm**: imagery
- **Number of classes**: 5
- **Class labels**: math, letter, rotation, count, baseline
- **Trial duration**: 11.0 s
- **Tasks**: word_association, mental_subtraction, spatial_navigation, right_hand_imagery, feet_imagery
- **Study design**: Five mental tasks: word association (WORD), mental subtraction (SUB), spatial navigation (NAV), motor imagery of right hand (HAND), and motor imagery of both feet (FEET). Cue-guided paradigm with 7 seconds of continuous mental imagery per trial.
- **Feedback type**: none
- **Stimulus type**: visual cue
- **Stimulus modalities**: visual
- **Primary modality**: visual
- **Synchronicity**: synchronous
- **Mode**: screening
- **Instructions**: Participants were asked to continuously perform the specified mental imagery task for 7 seconds. For MI: kinesthetic imagination of movement (e.g., squeezing a rubber ball for hand, dorsiflexion for feet). For WORD: generate words beginning with presented letter. For SUB: successive elementary subtractions. For NAV: spatial navigation.

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  math
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Think
          └─ Label/math

  letter
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Think
          └─ Label/letter

  rotation
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine
          ├─ Think
          └─ Label/rotation

  count
    ├─ Sensory-event, Experimental-stimulus, Visual-presentation
    └─ Agent-action
       └─ Imagine, Count

  baseline
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Rest

```
## Paradigm-Specific Parameters

- **Detected paradigm**: motor_imagery
- **Imagery tasks**: right_hand, feet, word_association, mental_subtraction, spatial_navigation
- **Cue duration**: 1.0 s
- **Imagery duration**: 7.0 s

## Data Structure

- **Trials**: 40
- **Blocks per session**: 8
- **Trials context**: per_class_per_day

## Preprocessing

- **Data state**: filtered
- **Preprocessing applied**: True
- **Steps**: bandpass filter, notch filter, artifact rejection
- **Highpass filter**: 0.5 Hz
- **Lowpass filter**: 100.0 Hz
- **Bandpass filter**: {'low_cutoff_hz': 0.5, 'high_cutoff_hz': 100.0}
- **Notch filter**: [50] Hz
- **Artifact methods**: manual artifact rejection based on EOG
- **Re-reference**: left and right mastoid

## Signal Processing

- **Classifiers**: LDA
- **Feature extraction**: bandpower, temporal features
- **Frequency bands**: mu=[8, 12] Hz; beta=[13, 30] Hz

## Cross-Validation

- **Method**: 10-fold cross-validation
- **Folds**: 10
- **Evaluation type**: within_session, cross_session

## Performance (Original Study)

- **Accuracy**: 77.0%
- **Best Task Pair Gmac**: 77.0
- **Sub Vs Feet Gmac**: 77.0
- **Word Vs Hand Gmac**: 70.0
- **Hand Vs Feet Gmac**: 64.0
- **Between Day Word Vs Hand Gmac**: 82.0

## BCI Application

- **Applications**: communication, motor_function_restoration
- **Environment**: rehabilitation center
- **Online feedback**: False

## Tags

- **Pathology**: Stroke, Spinal Cord Injury, CNS Damage
- **Modality**: Motor, Cognitive
- **Type**: Motor, Cognitive

## Documentation

- **DOI**: 10.1371/journal.pone.0123727
- **License**: CC-BY-NC-ND-4.0
- **Investigators**: Reinhold Scherer, Josef Faller, Elisabeth V. C. Friedrich, Eloy Opisso, Ursula Costa, Andrea Kübler, Gernot R. Müller-Putz
- **Senior author**: Reinhold Scherer
- **Contact**: reinhold.scherer@tugraz.at
- **Institution**: Institut Guttmann
- **Department**: Institut Universitari de Neurorehabilitació adscrit a la UAB
- **Address**: 08916 Badalona, Barcelona, Spain
- **Country**: Spain
- **Repository**: BNCI Horizon 2020
- **Data URL**: https://bnci-horizon-2020.eu/database/data-sets
- **Publication year**: 2015
- **Funding**: FP7 EU Research Projects BrainAble (No. 247447); ABC (No. 287774); BackHome (No. 288566)
- **Ethics approval**: Comitè d'Ètica Assistencial de l'Institut Guttman
- **Keywords**: brain-computer interface, motor imagery, mental tasks, EEG, CNS tissue damage, stroke, spinal cord injury, binary classification

## References

Zhang, X., Yao, L., Zhang, Q., Kanhere, S., Sheng, M., & Liu, Y. (2017). A survey on deep learning based brain computer interface: Recent advances and new frontiers. IEEE Transactions on Cognitive and Developmental Systems, 10(2), 145-163.

Notes

.. note::

``BNCI2015_004`` was previously named ``BNCI2015004``. ``BNCI2015004`` will be removed in version 1.1.

.. versionadded:: 0.4.0
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb
