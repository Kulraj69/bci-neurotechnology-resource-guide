# BCI and neurotechnology: a resource guide

This guide puts Neuralink's platform paper beside other implanted, endovascular and non-invasive brain-computer interface research. It is not a Neuralink endorsement or a claim of unrestricted thought reading. Human feasibility demonstrations and animal device experiments are labeled separately.

## Questions to carry through the reading

- What modality and task were used, and how many participants were studied?
- Was decoding online or offline? What calibration, language model or task constraint was used?
- Are results from held-out trials, sessions or people? Could preprocessing leak labels across splits?
- What are the device risks, failure modes, consent limits and limits on generalization?

## First useful projects

1. Reproduce a small EEG benchmark with subject/session-aware splits and fit preprocessing only on training data. Keep a dummy baseline and report uncertainty rather than only the best score.
2. Add a benchmark reporting card covering trial count, subject count, split unit, calibration, latency and participant-specific tuning.
3. Contribute a minimal failing test or a documentation correction to an established BCI tool after reading its current contribution policy. Synthetic examples are the first step, not a medical validation.

## Scope and provenance

Prepared 17 November 2026 from a selected 66-work reading library: 17 mind/emulation, 18 BCI/neurotechnology and 31 aging/rejuvenation works. The underlying selection covers foundational work and selected publications through 2025. This is not an exhaustive, latest or systematic review.

The source library checked journal bibliographic records and abstracts and direct repository abstracts for the six arXiv entries. Reading notes are short original summaries, not full-text critical appraisals. This guide preserves those limits; it does not imply every full text was read. Paper full texts are linked, not redistributed. Source titles and author names remain attributed to their authors.

`papers.json` is the reusable source, `papers.bib` is a citation export, and `validate.py` checks local metadata. Validation is structural, not a scientific peer review or a live link check. No clinical datasets or participant-level records are included.

## Evidence labels

- **Theory / review / philosophy / roadmap:** synthesis or argument, not an experimental demonstration of uploading or rejuvenation.
- **Computational:** simulation or modeling; judge the model's measured validation target, not its name.
- **Animal / tissue:** results for the stated organism or preparation, not proof of a human outcome.
- **Human cells / in vitro:** experiments on cells, not treatment of a person.
- **Human feasibility / pilot:** limited early human evidence; do not infer population-wide effectiveness.
- **Human trial / RCT:** inspect population, controls, sample size, endpoints and harms. A randomized biomarker analysis is still a biomarker analysis.
- **arXiv / report:** repository-hosted work; the label alone does not establish journal peer review.

## Use and improve this guide

```sh
python3 validate.py papers.json
python3 -m unittest -v test_validate.py
```

Keep limitations attached to the result they qualify. See `CONTRIBUTING.md` for the review checklist. Repository documentation and code are private review material at this stage. No license grant is made for third-party papers. Before a wider release, choose terms for the original guide/code separately from rights in cited works.

## Suggested reading path

1. [An Integrated Brain-Machine Interface Platform With Thousands of Channels](https://doi.org/10.2196/16194) (2019) - Device / preclinical. Neuralink describes flexible electrode threads, insertion robotics and recording hardware. Limitation: The 2019 platform paper is not evidence of human mind uploading or current clinical efficacy.
2. [High performance communication by people with paralysis using an intracortical brain-computer interface](https://doi.org/10.7554/elife.18554) (2017) - Human / feasibility. Tests higher-performance intracortical communication in three people with paralysis. Limitation: Small clinical study; performance is not a universal user outcome.
3. [High-performance brain-to-text communication via handwriting](https://doi.org/10.1038/s41586-021-03506-2) (2021) - Human / feasibility. Decodes attempted handwriting into text in a participant with paralysis. Limitation: Single-participant demonstration; not general thought reading.
4. [A high-performance speech neuroprosthesis](https://doi.org/10.1038/s41586-023-06377-x) (2023) - Human / feasibility. Decodes attempted speech into text using intracortical arrays. Limitation: One participant; accuracy depends strongly on vocabulary and task.
5. [A high-performance neuroprosthesis for speech decoding and avatar control](https://doi.org/10.1038/s41586-023-06443-4) (2023) - Human / feasibility. Combines decoded speech text, synthesized audio and facial-avatar control. Limitation: One clinical-trial participant; trained task-specific decoding.
6. [An Accurate and Rapidly Calibrating Speech Neuroprosthesis](https://doi.org/10.1056/nejmoa2314132) (2024) - Human / feasibility. Demonstrates a rapidly calibrated speech prosthesis used in conversation. Limitation: One person with ALS; longer-term general use and broader populations need testing.
7. [A streaming brain-to-voice neuroprosthesis to restore naturalistic communication](https://doi.org/10.1038/s41593-025-01905-6) (2025) - Human / feasibility. Streams synthesized speech from cortical recordings in short increments. Limitation: Early clinical demonstration, not unrestricted access to private thoughts.
8. [Assessment of Safety of a Fully Implanted Endovascular Brain-Computer Interface for Severe Paralysis in 4 Patients: The Stentrode With Thought-Controlled Digital Switch (SWITCH) Study](https://doi.org/10.1001/jamaneurol.2022.4847) (2023) - Human / feasibility. The SWITCH study assesses an endovascular BCI and computer control. Limitation: Four analyzed patients and 12-month follow-up cannot establish rare-event or population-wide safety.

## Annotated bibliography

### P18. An Integrated Brain-Machine Interface Platform With Thousands of Channels

Musk E, Neuralink. (2019). *Journal of medical Internet research*.

**Evidence:** Device / preclinical.

**Why read:** Neuralink describes flexible electrode threads, insertion robotics and recording hardware.

**Limit:** The 2019 platform paper is not evidence of human mind uploading or current clinical efficacy.

[Primary record](https://doi.org/10.2196/16194) | [Open-text link](https://europepmc.org/articles/PMC6914248)

Verification: Bibliographic record and abstract checked.

### P19. High-performance brain-to-text communication via handwriting

Willett FR, Avansino DT, Hochberg LR, Henderson JM, Shenoy KV. (2021). *Nature*.

**Evidence:** Human / feasibility.

**Why read:** Decodes attempted handwriting into text in a participant with paralysis.

**Limit:** Single-participant demonstration; not general thought reading.

[Primary record](https://doi.org/10.1038/s41586-021-03506-2) | [Open-text link](https://europepmc.org/articles/PMC8163299)

Verification: Bibliographic record and abstract checked.

### P20. A high-performance speech neuroprosthesis

Willett FR, Kunz EM, Fan C, Avansino DT, Wilson GH, Choi EY, Kamdar F, Glasser MF, Hochberg LR, Druckmann S, Shenoy KV, Henderson JM. (2023). *Nature*.

**Evidence:** Human / feasibility.

**Why read:** Decodes attempted speech into text using intracortical arrays.

**Limit:** One participant; accuracy depends strongly on vocabulary and task.

[Primary record](https://doi.org/10.1038/s41586-023-06377-x) | [Open-text link](https://europepmc.org/articles/PMC10468393)

Verification: Bibliographic record and abstract checked.

### P21. A high-performance neuroprosthesis for speech decoding and avatar control

Metzger SL, Littlejohn KT, Silva AB, Moses DA, Seaton MP, Wang R, Dougherty ME, Liu JR, Wu P, Berger MA, Zhuravleva I, Tu-Chan A, Ganguly K, Anumanchipalli GK, Chang EF. (2023). *Nature*.

**Evidence:** Human / feasibility.

**Why read:** Combines decoded speech text, synthesized audio and facial-avatar control.

**Limit:** One clinical-trial participant; trained task-specific decoding.

[Primary record](https://doi.org/10.1038/s41586-023-06443-4) | [Open-text link](https://europepmc.org/articles/PMC10826467)

Verification: Bibliographic record and abstract checked.

### P22. An Accurate and Rapidly Calibrating Speech Neuroprosthesis

Card NS, Wairagkar M, Iacobacci C, Hou X, Singer-Clark T, Willett FR, Kunz EM, Fan C, Vahdati Nia M, Deo DR, Srinivasan A, Choi EY, Glasser MF, Hochberg LR, Henderson JM, Shahlaie K, Stavisky SD, Brandman DM. (2024). *The New England journal of medicine*.

**Evidence:** Human / feasibility.

**Why read:** Demonstrates a rapidly calibrated speech prosthesis used in conversation.

**Limit:** One person with ALS; longer-term general use and broader populations need testing.

[Primary record](https://doi.org/10.1056/nejmoa2314132) | [Open-text link](https://europepmc.org/articles/PMC11328962)

Verification: Bibliographic record and abstract checked.

### P23. A streaming brain-to-voice neuroprosthesis to restore naturalistic communication

Littlejohn KT, Cho CJ, Liu JR, Silva AB, Yu B, Anderson VR, Kurtz-Miott CM, Brosler S, Kashyap AP, Hallinan IP, Shah A, Tu-Chan A, Ganguly K, Moses DA, Chang EF, Anumanchipalli GK. (2025). *Nature neuroscience*.

**Evidence:** Human / feasibility.

**Why read:** Streams synthesized speech from cortical recordings in short increments.

**Limit:** Early clinical demonstration, not unrestricted access to private thoughts.

[Primary record](https://doi.org/10.1038/s41593-025-01905-6)

Verification: Bibliographic record and abstract checked.

### P24. A high-performance brain-computer interface for finger decoding and quadcopter game control in an individual with paralysis

Willsey MS, Shah NP, Avansino DT, Hahn NV, Jamiolkowski RM, Kamdar FB, Hochberg LR, Willett FR, Henderson JM. (2025). *Nature medicine*.

**Evidence:** Human / feasibility.

**Why read:** Decodes finger movements for virtual quadcopter game control.

**Limit:** One participant and a virtual task, not flight-safety evidence.

[Primary record](https://doi.org/10.1038/s41591-024-03341-8) | [Open-text link](https://europepmc.org/articles/PMC11750708)

Verification: Bibliographic record and abstract checked.

### P25. High performance communication by people with paralysis using an intracortical brain-computer interface

Pandarinath C, Nuyujukian P, Blabe CH, Sorice BL, Saab J, Willett FR, Hochberg LR, Shenoy KV, Henderson JM. (2017). *eLife*.

**Evidence:** Human / feasibility.

**Why read:** Tests higher-performance intracortical communication in three people with paralysis.

**Limit:** Small clinical study; performance is not a universal user outcome.

[Primary record](https://doi.org/10.7554/elife.18554) | [Open-text link](https://europepmc.org/articles/PMC5319839)

Verification: Bibliographic record and abstract checked.

### P26. Semantic reconstruction of continuous language from non-invasive brain recordings

Tang J, LeBel A, Jain S, Huth AG. (2023). *Nature neuroscience*.

**Evidence:** Human / decoding.

**Why read:** Reconstructs the meaning of language from non-invasive fMRI signals.

**Limit:** Cooperation and extensive subject-specific training matter; not a portable mind reader.

[Primary record](https://doi.org/10.1038/s41593-023-01304-9) | [Open-text link](https://europepmc.org/articles/PMC11304553)

Verification: Bibliographic record and abstract checked.

### P27. Towards decoding individual words from non-invasive brain recordings

d'Ascoli S, Bel C, Rapin J, Banville H, Benchetrit Y, Pallier C, King JR. (2025). *Nature communications*.

**Evidence:** Human / decoding.

**Why read:** Benchmarks word decoding from EEG and MEG across multiple datasets.

**Limit:** Stimulus/task and recording-device dependent; not evidence of arbitrary private-thought decoding.

[Primary record](https://doi.org/10.1038/s41467-025-65499-0) | [Open-text link](https://europepmc.org/articles/PMC12658044)

Verification: Bibliographic record and abstract checked.

### P28. A brain-spine interface alleviating gait deficits after spinal cord injury in primates

Capogrosso M, Milekovic T, Borton D, Wagner F, Moraud EM, Mignardot JB, Buse N, Gandar J, Barraud Q, Xing D, Rey E, Rey E, Duis S, Jianzhong Y, Ko WK, Li Q, Detemple P, Denison T, Micera S, Bezard E, Bloch J, Courtine G. (2016). *Nature*.

**Evidence:** Animal / intervention.

**Why read:** Links brain signals to spinal stimulation to improve locomotion in injured primates.

**Limit:** Non-human primate proof of concept; separate from the later human study.

[Primary record](https://doi.org/10.1038/nature20118) | [Open-text link](https://europepmc.org/articles/PMC5108412)

Verification: Bibliographic record and abstract checked.

### P29. Walking naturally after spinal cord injury using a brain-spine interface

Lorach H, Galvez A, Spagnolo V, Martel F, Karakas S, Intering N, Vat M, Faivre O, Harte C, Komi S, Ravier J, Collin T, Coquoz L, Sakr I, Baaklini E, Hernandez-Charpak SD, Dumont G, Buschman R, Buse N, Denison T, van Nes I, Asboth L, Watrin A, Struber L, Sauter-Starace F, Langar L, Auboiroux V, Carda S, Chabardes S, Aksenova T, Demesmaeker R, Charvet G, Bloch J, Courtine G. (2023). *Nature*.

**Evidence:** Human / feasibility.

**Why read:** A brain-spine digital bridge supports walking after chronic spinal cord injury.

**Limit:** An individual clinical demonstration, not a general cure for paralysis.

[Primary record](https://doi.org/10.1038/s41586-023-06094-5) | [Open-text link](https://europepmc.org/articles/PMC10232367)

Verification: Bibliographic record and abstract checked.

### P30. Restoration of reaching and grasping movements through brain-controlled muscle stimulation in a person with tetraplegia: a proof-of-concept demonstration

Ajiboye AB, Willett FR, Young DR, Memberg WD, Murphy BA, Miller JP, Walter BL, Sweet JA, Hoyen HA, Keith MW, Peckham PH, Simeral JD, Donoghue JP, Hochberg LR, Kirsch RF. (2017). *Lancet (London, England)*.

**Evidence:** Human / feasibility.

**Why read:** Brain-controlled muscle stimulation restores reaching and grasping in one participant.

**Limit:** Proof of concept with implanted electrodes and assistive support.

[Primary record](https://doi.org/10.1016/S0140-6736(17)30601-3) | [Open-text link](https://europepmc.org/articles/PMC5516547)

Verification: Bibliographic record and abstract checked.

### P31. A wireless millimetric magnetoelectric implant for the endovascular stimulation of peripheral nerves

Chen JC, Kan P, Yu Z, Alrashdan F, Garcia R, Singer A, Lai CSE, Avants B, Crosby S, Li Z, Wang B, Felicella MM, Robledo A, Peterchev AV, Goetz SM, Hartgerink JD, Sheth SA, Yang K, Robinson JT. (2022). *Nature biomedical engineering*.

**Evidence:** Animal / device.

**Why read:** Tests a small wireless endovascular peripheral-nerve stimulation implant.

**Limit:** Adjacent neurotechnology, not a cortical BCI; tested in rats and pigs.

[Primary record](https://doi.org/10.1038/s41551-022-00873-7) | [Open-text link](https://europepmc.org/articles/PMC9213237)

Verification: Bibliographic record and abstract checked.

### P32. Fully Implanted Brain-Computer Interface in a Locked-In Patient with ALS

Vansteensel MJ, Pels EGM, Bleichner MG, Branco MP, Denison T, Freudenburg ZV, Gosselaar P, Leinders S, Ottens TH, Van Den Boom MA, Van Rijen PC, Aarnoutse EJ, Ramsey NF. (2016). *The New England journal of medicine*.

**Evidence:** Human / feasibility.

**Why read:** A fully implanted BCI supports typing in a locked-in person with ALS.

**Limit:** One participant; slow communication, not speech restoration or uploading.

[Primary record](https://doi.org/10.1056/nejmoa1608085) | [Open-text link](https://europepmc.org/articles/PMC5326682)

Verification: Bibliographic record and abstract checked.

### P33. Neuroprosthesis for Decoding Speech in a Paralyzed Person with Anarthria

Moses DA, Metzger SL, Liu JR, Anumanchipalli GK, Makin JG, Sun PF, Chartier J, Dougherty ME, Liu PM, Abrams GM, Tu-Chan A, Ganguly K, Chang EF. (2021). *The New England journal of medicine*.

**Evidence:** Human / feasibility.

**Why read:** Decodes attempted words and sentences in a person with anarthria.

**Limit:** One participant and a constrained vocabulary; not silent omniscient mind reading.

[Primary record](https://doi.org/10.1056/nejmoa2027540) | [Open-text link](https://europepmc.org/articles/PMC8972947)

Verification: Bibliographic record and abstract checked.

### P34. High-performance neuroprosthetic control by an individual with tetraplegia

Collinger JL, Wodlinger B, Downey JE, Wang W, Tyler-Kabara EC, Weber DJ, McMorland AJ, Velliste M, Boninger ML, Schwartz AB. (2013). *Lancet (London, England)*.

**Evidence:** Human / feasibility.

**Why read:** Demonstrates multi-degree-of-freedom robotic-arm control after tetraplegia.

**Limit:** Individual proof of concept requiring surgical implants and training.

[Primary record](https://doi.org/10.1016/s0140-6736(12)61816-9) | [Open-text link](https://europepmc.org/articles/PMC3641862)

Verification: Bibliographic record and abstract checked.

### P35. Assessment of Safety of a Fully Implanted Endovascular Brain-Computer Interface for Severe Paralysis in 4 Patients: The Stentrode With Thought-Controlled Digital Switch (SWITCH) Study

Mitchell P, Lee SCM, Yoo PE, Morokoff A, Sharma RP, Williams DL, MacIsaac C, Howard ME, Irving L, Vrljic I, Williams C, Bush S, Balabanski AH, Drummond KJ, Desmond P, Weber D, Denison T, Mathers S, O'Brien TJ, Mocco J, Grayden DB, Liebeskind DS, Opie NL, Oxley TJ, Campbell BCV. (2023). *JAMA neurology*.

**Evidence:** Human / feasibility.

**Why read:** The SWITCH study assesses an endovascular BCI and computer control.

**Limit:** Four analyzed patients and 12-month follow-up cannot establish rare-event or population-wide safety.

[Primary record](https://doi.org/10.1001/jamaneurol.2022.4847) | [Open-text link](https://europepmc.org/articles/PMC9857731)

Verification: Bibliographic record and abstract checked.
