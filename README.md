# The Space-time Continuum: Temporal Segmentation Effects on Spatial Memory

This repository contains the statistical analysis files and data for the research paper "The Space-time Continuum: Temporal Segmentation Effects on Spatial Memory" by Ashish K. Sahoo and Steven M. Weisberg (2025).

## Study Overview

This study investigates how temporal segmentation affects spatial memory in virtual environments. Participants (n=76 complete, 97 enrolled) learned the locations of 16 objects in a custom-built Unity3D virtual environment across two temporally separated sessions. The study examined whether temporal divisions during learning affect spatial memory across multiple behavioral tasks.

### Key Findings

- **Temporal segmentation effects were task-dependent**, creating a gradient across different measures
- **Strongest effects**: Free recall (objects recalled together) and distance-based tasks (elongation, estimation accuracy)
- **Weakest effects**: Configurational tasks (JRD, mapping) requiring broader spatial knowledge
- **No effects**: Object viewing (perceptual control task), demonstrating divergent validity

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

### 1. Free Recall
**Location**: `analyses/tasks/free_recall/`

Participants typed object names in any order they wished.

**Files**:
- `free_recall_counts.jasp` - Overall transition analysis
- `free_recall_counts_sex.jasp` - Sex comparison
- `free_recall_counts_female.jasp` - Female participants only
- `free_recall_counts_male.jasp` - Male participants only

**Key Metric**: Weighted transition probabilities between object groups

**Main Finding**: ✓✓✓ **Strong temporal segmentation** - Objects from same Time Group recalled consecutively (TS > NS > ND transitions)

---

### 2. Judgment of Relative Direction (JRD)
**Location**: `analyses/tasks/jrd/`

Participants estimated directions between object triplets to measure configurational accuracy.

**Files**:
- `jrd_min_diff.jasp` - Angular difference (overall)
- `jrd_min_diff_sex.jasp` - Angular difference with sex comparison
- `jrd_min_diff_female.jasp` - Female participants only
- `jrd_min_diff_male.jasp` - Male participants only
- `jrd_lr.jasp` - Left-right accuracy (overall)
- `jrd_lr_sex.jasp` - Left-right accuracy with sex comparison
- `jrd_lr_female.jasp` - Female participants only
- `jrd_lr_male.jasp` - Male participants only

**Key Metrics**:
- Angular accuracy (absolute angular difference between response and correct angle)
- Left-right direction accuracy (binary: correct side or not)

**Main Finding**: ✓ **Weak temporal segmentation** - Left-right accuracy better for TS than ND; no effect on angular difference

---

### 3. Distance Estimation
**Location**: `analyses/tasks/distance_estimation/`

Participants estimated distances in feet between object pairs.

**Files - Elongation Measure**:
- `dist_est_elong.jasp` - Distance ratio (overall)
- `dist_est_elong_sex.jasp` - Distance ratio with sex comparison
- `dist_est_elong_female.jasp` - Female participants only
- `dist_est_elong_male.jasp` - Male participants only

**Files - Correlation Measure**:
- `dist_est_corr.jasp` - Correlation accuracy (overall)
- `dist_est_corr_sex.jasp` - Correlation with sex comparison
- `dist_est_corr_female.jasp` - Female participants only
- `dist_est_corr_male.jasp` - Male participants only

**Key Metrics**:
- Distance ratio (estimated distance / actual distance)
- Correlation (Pearson r between estimated and actual distances)

**Main Finding**: ✓✓✓ **Strong temporal segmentation**
- ND pairs perceived as MORE elongated (farther apart) than NS and TS pairs
- ND pairs showed BETTER correlation accuracy than NS pairs
- Suggests temporal boundaries help distance discrimination

---

### 4. Distance Comparison
**Location**: `analyses/tasks/distance_comparison/`

Two-alternative forced choice: which of two objects is closer to an anchor object?

**Files**:
- `dist_comp.jasp` - Overall accuracy
- `dist_comp_sex.jasp` - Accuracy with sex comparison
- `dist_comp_female.jasp` - Female participants only
- `dist_comp_male.jasp` - Male participants only

**Key Metric**: Accuracy (% correct choices)

**Main Finding**: ✓ **Weak temporal segmentation** - ND trials slightly more accurate than within-Time Group trials

---

### 5. Object Viewing (Control Task)
**Location**: `analyses/tasks/object_viewing/`

Perceptual control task: objects shown individually, tilted left/right or straight.

**Files - Accuracy**:
- `object_view_accuracy.jasp` - Overall accuracy
- `object_view_accuracy_sex.jasp` - Accuracy with sex comparison
- `object_view_accuracy_female.jasp` - Female participants only
- `object_view_accuracy_male.jasp` - Male participants only

**Files - Reaction Time**:
- `object_view_rt_correct_mean.jasp` - Mean RT for correct responses (overall)
- `object_view_rt_correct_mean_sex.jasp` - RT with sex comparison
- `object_view_rt_correct_mean_female.jasp` - Female participants only
- `object_view_rt_correct_mean_male.jasp` - Male participants only

**Key Metrics**:
- Accuracy (% correct orientation judgments)
- Reaction time (seconds for correct responses)

**Main Finding**: **No temporal segmentation effects** - As expected for non-spatial perceptual task (divergent validity)

---

### 6. Mapping
**Location**: `analyses/tasks/mapping/`

Top-down map placement: participants dragged objects to correct locations on a blank map.

**Files**:
- `mapping.jasp` - Distance ratio (overall)
- `mapping_sex.jasp` - Distance ratio with sex comparison
- `mapping_female.jasp` - Female participants only
- `mapping_male.jasp` - Male participants only

**Key Metric**: Distance ratio between placed and actual object locations

**Main Finding**: ✓✓ **Moderate temporal segmentation** - ND pairs more elongated than TS pairs, with NS in between

---

## Individual Difference Measures

### Questionnaires
**Location**: `data/questionnaires/`

Three questionnaires assessed navigation ability and experience:

1. **Santa Barbara Sense of Direction Scale (SBSOD)**
   - Location: `data/questionnaires/sbsod/`
   - 15-item self-report of spatial orientation ability (7-point Likert scale)
   - Good reliability and validity for predicting wayfinding performance

2. **Navigation Strategies Questionnaire (NSQ)**
   - Location: `data/questionnaires/nsq/`
   - 14-item measure of map-based vs. scene-based navigation preference
   - Mapping score = difference between map and scene responses

3. **Video Game Questionnaire (VGQ)**
   - Location: `data/questionnaires/vgq/`
   - Custom questionnaire on video game experience
   - Focus on navigational games (action-adventure, RPGs)
   - Time spent gaming (recent and lifetime)

**Key Finding**: VGQ (video game experience) was the strongest predictor of navigation performance, correlating with 7/8 navigation measures

---

## Python Analysis Notebooks

### Correlations_jun25.ipynb
**Location**: `analyses/Correlations_jun25.ipynb`

Comprehensive correlation analysis examining three key relationships:

1. **Overall Performance × Questionnaires**
   - How task performance relates to individual differences (SBSOD, NSQ, VGQ)
   - VGQ most strongly correlated with performance

2. **Temporal Segmentation Scores Across Tasks**
   - ND-NS difference scores (segmentation strength) correlated between tasks
   - Distance estimation segmentation correlated with JRD segmentation

3. **Overall Performance × Segmentation Strength**
   - Within-task correlation: does better performance relate to stronger segmentation?
   - Distance tasks showed strongest relationships

**Visualizations**: Correlation matrices with significance testing, heatmaps

---

### factor analysis.ipynb
**Location**: `analyses/factor analysis.ipynb`

Exploratory factor analysis on z-scored task performance using Oblimin rotation (allows correlated factors).

**Variables Analyzed**:
- JRD angular difference and left-right accuracy
- Distance estimation correlation and elongation
- Distance comparison accuracy
- Mapping distances

**Three-Factor Solution**:
1. **Factor 1**: JRD tasks (configurational spatial knowledge)
2. **Factor 2**: Distance comparison + distance estimation correlation
3. **Factor 3**: Distance estimation elongation + mapping

**Key Insight**: Tasks cluster by type of spatial representation required

---

## Experimental Design

### Virtual Environment
- Custom Unity3D environment (150×150 virtual meters square park)
- 16 objects on pedestals distributed across 4 quadrants
- Distal landmarks (mountains, trees) for orientation
- Adapted from Peer & Epstein (2021)

### Object Groupings

Objects were organized into groups to control temporal and travel-based learning:

- **Travel Groups**: Sets of 4 objects participants traveled between directly (one object per quadrant)
- **Time Groups**: Sets of 8 objects (2 Travel Groups) learned in one session

This created three types of object relations:

| Code | Name | Description |
|------|------|-------------|
| **TS** | Traveled & Same time | Same Travel Group and Time Group (traveled between directly, same session) |
| **NS** | Not traveled & Same time | Different Travel Groups but same Time Group (not traveled between, same session) |
| **ND** | Not traveled & Different time | Different Time Groups (never traveled between, different sessions) |

### Key Contrasts

1. **ND vs NS**: Tests temporal segmentation effect (controlling for travel)
2. **TS vs NS**: Tests travel effect (within same time)
3. **ND vs TS**: Combined temporal + travel effect

---

## Learning Procedure

1. **Session 1**: Learn 8 objects (Time Group 1) to criterion
   - 5 levels of learning
   - Level 5: complete 24 trials without errors

2. **Delay**: 15-30 minutes of questionnaires (creating temporal boundary)

3. **Session 2**: Learn remaining 8 objects (Time Group 2) to criterion

4. **Testing**: Six tasks in fixed order
   - Free recall
   - JRD (64 trials)
   - Distance estimation (128 trials)
   - Distance comparison (96 trials)
   - Object viewing (289 trials)
   - Mapping (16 objects)

---

## Summary of Results

### Temporal Segmentation Effects by Task

| Task | Effect Strength | Details |
|------|----------------|---------|
| **Free Recall** | ✓✓✓ Strong | Objects from same time recalled together (TS > NS > ND) |
| **Distance Est. (Elongation)** | ✓✓✓ Strong | ND pairs perceived farther apart than NS, TS |
| **Distance Est. (Correlation)** | ✓✓ Moderate | ND more accurate than NS; TS more accurate than NS |
| **Mapping** | ✓✓ Moderate | ND pairs more elongated than TS, NS intermediate |
| **Distance Comparison** | ✓ Weak | ND slightly more accurate than NS+TS |
| **JRD (Left-right)** | ✓ Weak | TS better than ND |
| **JRD (Angular)** | - None | No differences between groups |
| **Object Viewing** | - None | Control task (no spatial component) |

**Legend**: ✓✓✓ = Strong (BF₁₀ > 100), ✓✓ = Moderate (BF₁₀ 10-100), ✓ = Weak (BF₁₀ 3-10), - = No effect

### Gradient of Temporal Segmentation

The results show a **task-dependent gradient**:
- **Strongest**: Time-based tasks (free recall, distance estimation)
- **Moderate**: Combined spatial-temporal tasks (mapping)
- **Weakest**: Pure configurational tasks (JRD)
- **None**: Non-spatial tasks (object viewing)

This suggests temporal segmentation affects memory for "when" and "how far" more than "where" in an absolute sense.

---

## Sex Differences

### Overall Performance
Males showed advantages in:
- JRD angular accuracy (p = .009)
- Distance estimation correlation (p = .012)
- Distance comparison (p = .006)
- Object viewing speed and accuracy (p < .05)
- Video game experience (p < .001)
- Map-based navigation preference (p = .007)

### Segmentation Effects by Sex
- **JRD left-right**: Males showed ND vs NS effect; females did not
- **Mapping**: Females showed ND vs NS effect; males did not
- **Distance estimation**: Both sexes showed similar elongation effects

---

## Data Files

### Task Data Structure
Each task folder in `data/tasks/` contains:
- `[task].csv` - All participants
- `[task]_female.csv` - Female participants only
- `[task]_male.csv` - Male participants only

### Questionnaire Data Structure
Each questionnaire folder in `data/questionnaires/` contains:
- `[questionnaire].csv` - All participants
- `[questionnaire]_female.csv` - Female participants only
- `[questionnaire]_male.csv` - Male participants only

### Data Fields
- **Participant ID**: Unique identifier
- **Task-specific measures**: Varies by task (see individual task descriptions)
- **Group contrasts**: TS, NS, ND comparisons

---

## Statistical Approach

### Methods
- **Non-parametric tests**: Wilcoxon signed-rank tests (for non-normal distributions)
- **Parametric tests**: Paired t-tests where appropriate
- **Effect sizes**: Rank-biserial correlation (r) for Wilcoxon; Cohen's d for t-tests
- **Bayesian statistics**: Bayes factors (BF₁₀) reported for all tests

### Software
- **JASP** version 0.16.4 - Open-source statistical software
- **Python** - pandas, numpy, scipy, matplotlib, seaborn (see requirements.txt)

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
University of Florida
945 Center Drive
Gainesville, FL 32611, USA
Email: stevenweisberg@ufl.edu

---

## Acknowledgments

Data collection: Yunxiao Chen, Cecelia Albright, Yukshi Jain

---

## Funding

National Institute of Aging grant 1K01AC070333-01 (to S.M. Weisberg)

---

## File Naming Conventions

### Pattern: `[task]_[measure]_[subgroup].[ext]`

**Task abbreviations**:
- `jrd` - Judgment of Relative Direction
- `dist_est` - Distance Estimation
- `dist_comp` - Distance Comparison
- `free_recall` - Free Recall
- `object_view` - Object Viewing
- `mapping` - Mapping

**Measure suffixes** (task-specific):
- `min_diff` - Minimum angular difference (JRD)
- `lr` - Left-right accuracy (JRD)
- `elong` - Elongation/distance ratio (Distance Estimation, Mapping)
- `corr` - Correlation accuracy (Distance Estimation)
- `counts` - Transition counts (Free Recall)
- `accuracy` - Response accuracy (Object Viewing, Distance Comparison)
- `rt_correct_mean` - Mean reaction time for correct responses (Object Viewing)

**Subgroup suffixes**:
- No suffix - All participants
- `_sex` - Sex comparison analysis
- `_female` - Female participants only
- `_male` - Male participants only

**Examples**:
- `jrd_lr_sex.jasp` - JRD left-right accuracy with sex as factor
- `dist_est_elong_female.csv` - Distance estimation elongation data for females
- `mapping.jasp` - Mapping analysis for all participants

---

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose, even commercially

Under the following terms:
- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

[![CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)
