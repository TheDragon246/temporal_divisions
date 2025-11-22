# The Space-time Continuum: Temporal Segmentation Effects on Spatial Memory

This repository contains the statistical analysis files and data for the research paper "The Space-time Continuum: Temporal Segmentation Effects on Spatial Memory" by Ashish K. Sahoo and Steven M. Weisberg (2025).

## Study Overview

Spatial navigation requires learning environments larger than what can be perceived at one time, necessitating the integration of distinct episodes into a unified representation. Modern theories postulate hierarchical models of space, in which environments are mentally segmented, allowing more precise navigation within subregions and less precise strategies across them. But how does space become segmented into subregions?

Here, we investigate how temporal segmentation subserves memory in a virtual environment. While the dissociation of spatial and temporal information has been demonstrated for screen-size environments, this is the first experiment where this dissociation is tested in a freely navigable environment. Participants (n=76 complete, 97 enrolled) learned the locations of 16 objects in a custom-built Unity3D virtual environment across two temporally separated sessions. This design allowed us to examine whether temporal divisions during learning affect spatial memory across multiple behavioral tasks, with key aspects making temporal distance dissociable from spatial distance as well as whether objects were learned by being travelled between directly or not.

## Repository Structure

```
temporal_divisions/
│
├── analyses/                          # Statistical analyses
│   ├── Correlations_jun25.ipynb      # Correlation analyses
│   ├── factor analysis.ipynb         # Factor analysis
│   │
│   └── tasks/                        # JASP analysis files by task
│       ├── distance_comparison/      # Distance comparison task (4 files)
│       ├── distance_estimation/      # Distance estimation task (8 files)
│       ├── free_recall/              # Free recall task (4 files)
│       ├── jrd/                      # Judgment of Relative Direction (8 files)
│       ├── mapping/                  # Mapping task (4 files)
│       └── object_viewing/           # Object viewing task (8 files)
│
└── data/                             # Processed data files
    ├── questionnaires/               # Individual difference measures
    │   ├── nsq/                      # Navigation Strategies Questionnaire
    │   ├── sbsod/                    # Santa Barbara Sense of Direction Scale
    │   └── vgq/                      # Video Game Questionnaire
    │
    └── tasks/                        # Task data files (CSV format)
        ├── distance_comparison/      # Distance comparison data
        ├── distance_estimation/      # Distance estimation data
        ├── free_recall/              # Free recall data
        ├── jrd/                      # JRD data
        ├── mapping/                  # Mapping data
        └── object_viewing/           # Object viewing data
```

## Experimental Tasks

The study employed six behavioral tasks, administered in the following order after participants completed the environment learning procedure.

### 1. Free Recall
**Location**: `analyses/tasks/free_recall/`

In the free recall task, participants entered the names of all the objects from the environment, one at a time. Participants could enter names in any order they wished. We computed the number of transitions between each group type, correcting for the fact that the number of possible transitions varied, and adjusted for base rate differences accordingly.

**Files**:
- `free_recall_counts.jasp` – Overall transition analysis
- `free_recall_counts_sex.jasp` – Sex comparison
- `free_recall_counts_female.jasp` – Female participants only
- `free_recall_counts_male.jasp` – Male participants only

---

### 2. Judgment of Relative Direction (JRD)
**Location**: `analyses/tasks/jrd/`

In the JRD task, participants estimated the directions between different sets of objects, a measure of the configurational accuracy of the layout. On each trial, participants imagined standing at the location of the first object, facing towards the second object, and indicated the direction of the third object by rotating a compass on the screen.

**Files**:
- `jrd_min_diff.jasp` – Angular difference (overall)
- `jrd_min_diff_sex.jasp` – Angular difference with sex comparison
- `jrd_min_diff_female.jasp` – Female participants only
- `jrd_min_diff_male.jasp` – Male participants only
- `jrd_lr.jasp` – Left-right accuracy (overall)
- `jrd_lr_sex.jasp` – Left-right accuracy with sex comparison
- `jrd_lr_female.jasp` – Female participants only
- `jrd_lr_male.jasp` – Male participants only

**Metrics**:
- Angular accuracy (absolute angular difference between response and correct angle)
- Left-right direction accuracy (binary: correct side or not)

---

### 3. Distance Estimation
**Location**: `analyses/tasks/distance_estimation/`

For each trial, participants saw two object names and were instructed to estimate the distance in feet between them. We computed two metrics: the correlation between actual and estimated distances, and a distance ratio (participant's estimate divided by actual distance).

**Files – Elongation Measure**:
- `dist_est_elong.jasp` – Distance ratio (overall)
- `dist_est_elong_sex.jasp` – Distance ratio with sex comparison
- `dist_est_elong_female.jasp` – Female participants only
- `dist_est_elong_male.jasp` – Male participants only

**Files – Correlation Measure**:
- `dist_est_corr.jasp` – Correlation accuracy (overall)
- `dist_est_corr_sex.jasp` – Correlation with sex comparison
- `dist_est_corr_female.jasp` – Female participants only
- `dist_est_corr_male.jasp` – Male participants only

---

### 4. Distance Comparison
**Location**: `analyses/tasks/distance_comparison/`

This two-alternative forced choice task presented participants with one anchor object at the top of the screen and two comparison objects below. The participant's task was to select which of the two comparison objects was closer to the anchor object.

**Files**:
- `dist_comp.jasp` – Overall accuracy
- `dist_comp_sex.jasp` – Accuracy with sex comparison
- `dist_comp_female.jasp` – Female participants only
- `dist_comp_male.jasp` – Male participants only

---

### 5. Object Viewing (Control Task)
**Location**: `analyses/tasks/object_viewing/`

This perceptual control task presented each object individually over a black background. For half of the trials, the object was tilted 15° to the left or right; for the other half, the object was upright. Participants indicated the object's orientation as fast as possible. Critically, this task did not involve remembering the object locations, serving as a measure of divergent validity.

**Files – Accuracy**:
- `object_view_accuracy.jasp` – Overall accuracy
- `object_view_accuracy_sex.jasp` – Accuracy with sex comparison
- `object_view_accuracy_female.jasp` – Female participants only
- `object_view_accuracy_male.jasp` – Male participants only

**Files – Reaction Time**:
- `object_view_rt_correct_mean.jasp` – Mean RT for correct responses (overall)
- `object_view_rt_correct_mean_sex.jasp` – RT with sex comparison
- `object_view_rt_correct_mean_female.jasp` – Female participants only
- `object_view_rt_correct_mean_male.jasp` – Male participants only

---

### 6. Mapping
**Location**: `analyses/tasks/mapping/`

Participants viewed a top-down map of the empty environment with external landmarks (mountains and forest) but no objects. The name and image of each object was shown one by one, and participants indicated the correct location of each object on the map by dragging and dropping.

**Files**:
- `mapping.jasp` – Distance ratio (overall)
- `mapping_sex.jasp` – Distance ratio with sex comparison
- `mapping_female.jasp` – Female participants only
- `mapping_male.jasp` – Male participants only

---

## Individual Difference Measures

### Questionnaires
**Location**: `data/questionnaires/`

Three questionnaires assessed navigation ability and experience:

1. **Santa Barbara Sense of Direction Scale (SBSOD)**
   - Location: `data/questionnaires/sbsod/`
   - A 15-item self-report measure of spatial orientation ability rated on a 7-point Likert scale. The scale has demonstrated good internal consistency and test-retest reliability, correlating well with performance on spatial tasks and real-world wayfinding abilities (Hegarty, 2002).

2. **Navigation Strategies Questionnaire (NSQ)**
   - Location: `data/questionnaires/nsq/`
   - A 14-item assessment tool measuring preference for cognitive map-based versus scene-based navigation. Developed by Brunec et al. (2019), it presents binary choices between map-based strategies (bird's-eye visualization) and scene-based strategies (sequential landmark visualization).

3. **Video Game Questionnaire (VGQ)**
   - Location: `data/questionnaires/vgq/`
   - A self-reported questionnaire focused on participants' experience playing video games, particularly video games with significant navigational components.

---

## Python Analysis Notebooks

### Correlations_jun25.ipynb
**Location**: `analyses/Correlations_jun25.ipynb`

Comprehensive correlation analysis examining three key relationships:
1. Overall performance and questionnaires
2. Temporal segmentation scores across tasks
3. Overall performance and segmentation strength

### factor analysis.ipynb
**Location**: `analyses/factor analysis.ipynb`

Exploratory factor analysis on Z-scored task data using Oblimin rotation to examine the underlying structure of the navigation tasks.

---

## Experimental Design

### Object Relations

We describe *relations* between any pair of objects as follows:

| Abbreviation | Meaning | Description |
|--------------|---------|-------------|
| **TS** | Traveled & Same time | Same Travel Group (traveled between directly, same session) |
| **NS** | Not traveled & Same time | Same Time Group but different Travel Groups (never traveled between directly, same session) |
| **ND** | Not traveled & Different time | Different Time Groups (never traveled between, different sessions) |

### Key Contrasts

1. **ND vs NS**: Tests temporal segmentation effect (controlling for travel)
2. **TS vs NS**: Tests travel effect (within same time)
3. **ND vs TS**: Test temporal segmentation with travel as a covariate

---

## Learning Procedure

Before participants were tested, they had to learn the locations of objects in the environment to criterion. The learning procedure occurred for one set of eight objects belonging to one Time Group, then, after a delay filled by other tasks, was repeated with the other set of eight objects belonging to the second Time Group.

1. **Session 1**: Learn 8 objects (Time Group 1) through 5 levels of learning, with Level 5 requiring completion of 24 trials without errors

2. **Delay**: 15-30 minutes of questionnaires (creating the temporal boundary)

3. **Session 2**: Learn remaining 8 objects (Time Group 2) to criterion

4. **Testing**: Six tasks in fixed order (free recall, JRD, distance estimation, distance comparison, object viewing, mapping)

---

## Data Files

### Task Data Structure
Each task folder in `data/tasks/` contains:
- `[task].csv` – All participants
- `[task]_female.csv` – Female participants only
- `[task]_male.csv` – Male participants only

### Questionnaire Data Structure
Each questionnaire folder in `data/questionnaires/` contains:
- `[questionnaire].csv` – All participants
- `[questionnaire]_female.csv` – Female participants only
- `[questionnaire]_male.csv` – Male participants only

---

## Statistical Approach

### Methods
- **Non-parametric tests**: Wilcoxon signed-rank tests (to avoid normality assumption)
- **Parametric tests**: Paired t-tests where appropriate
- **Effect sizes**: Rank-biserial correlation (r) for Wilcoxon; Cohen's d for t-tests
- **Bayesian statistics**: Bayes factors (BF₁₀) reported for all tests

### Software
- **JASP** version 0.16.4 – Open-source statistical software
- **Python** – pandas, numpy, scipy, matplotlib, seaborn

---

## Installation & Usage

### JASP Files
1. Download and install JASP: https://jasp-stats.org/
2. Open any `.jasp` file from `analyses/tasks/`
3. Data is embedded in JASP files

### Python Notebooks

1. Launch Jupyter:
```bash
jupyter notebook
```

2. Open notebooks in `analyses/`:
   - `Correlations_jun25.ipynb`
   - `factor analysis.ipynb`

**Note**: Notebooks reference CSV files in `data/` directory. File paths in notebooks may need updating based on the folder structure.

---

## Citation

If you use this data or analysis code, please cite:

```
Sahoo, A. K., & Weisberg, S. M. (2025). The Space-time Continuum:
Temporal Segmentation Effects on Spatial Memory. [Journal TBD]
```

---

## Pre-registration

Study methods and analysis plan were pre-registered on Aspredicted.org:
https://aspredicted.org/qr7ts.pdf

---

## Contact

**Corresponding Author**:
Steven M. Weisberg
Department of Psychology
University of Texas at Arlington
701 S Nedderman Dr
Arlington, TX 76019, USA
Email: steven.weisberg@uta.edu

---

## Acknowledgments

The authors thank Yunxiao Chen, Cecelia Albright, and Yukshi Jain for their assistance with data collection.

---

## Funding

This work was supported by the National Institute of Aging (1K01AC070333-01) grant to Steven M. Weisberg.

---

## File Naming Conventions

### Pattern: `[task]_[measure]_[subgroup].[ext]`

**Task abbreviations**:
- `jrd` – Judgment of Relative Direction
- `dist_est` – Distance Estimation
- `dist_comp` – Distance Comparison
- `free_recall` – Free Recall
- `object_view` – Object Viewing
- `mapping` – Mapping

**Measure suffixes** (task-specific):
- `min_diff` – Minimum angular difference (JRD)
- `lr` – Left-right accuracy (JRD)
- `elong` – Elongation/distance ratio (Distance Estimation, Mapping)
- `corr` – Correlation accuracy (Distance Estimation)
- `counts` – Transition counts (Free Recall)
- `accuracy` – Response accuracy (Object Viewing, Distance Comparison)
- `rt_correct_mean` – Mean reaction time for correct responses (Object Viewing)

**Subgroup suffixes**:
- No suffix – All participants
- `_sex` – Sex comparison analysis
- `_female` – Female participants only
- `_male` – Male participants only

---

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

Under the following terms:
- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made.

[![CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)
