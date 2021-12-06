---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<!-- <img src="/stages/stage2/subject1.png" width="250" align="right" margin-left="100px"  /> -->

<div align="center" style="margin-bottom:25px">
<img width="400" src="{{ '/stages/stage2/subject3.png' | relative_url }}"/>
</div>

**Design and Instructions**

In the study, you will view images, both raw T1w structural scans and rendered heatmaps of age- and sex-adjusted cortical thickness levels.

These heatmaps are a visualization of a patient's regional w-scores, a statistical score which denotes the number of standard deviations the patient’s cortical thickness is below the expected value for a patient of that age and sex. The pipeline calculates a w-score for each of 200 cortical regions (Schaefer 2018 atlas) by plugging the patient’s mean cortical thickness in the given region, the patient’s age, and patient’s sex into a model derived from >800 healthy subjects across the age range.

The pipeline then renders these scores as different shades of color scale in a 3D projection of the cortical surface. The scores are thresholded at 1.5 for the rendering, so that only “clinically significant” differences are displayed. This threshold also means that areas of cortical thickening are not displayed (as they’d be negative). This is because we are focused on degeneration, and only displaying areas of cortical thinning makes the heatmaps easier to interpret. Note that higher w-scores reflect greater degeneration.

Based on either the native T1w images or the heatmaps, you will make forced choice diagnostic decisions in 60 patients comprising healthy controls (n=20) as well as clinically diagnosed AD (n=20) and FTD (n=20) patients. You will first decide if the presented case is normal or abnormal and, if abnormal, choose among overarching disease categories (AD, FTDC, other), then among several potential subtypes depending on the choice of disease category, like so:

- Level 1: Normal vs Abnormal
- Level 2: If Abnormal, AD Spectrum vs. FTD Spectrum vs. Other Neurodegenerative
- Level 3: Additional subtype (e.g. logopenic PPA): Free text

The rater will also rate their confidence in their answer for Levels 1 and 2 as being 1) a guess, 2) low, 3) high.

The images will be unlabeled and will vary in order from stage to stage.

The study is divided into four stages:

1. Raters view raw T1w images and make diagnosis
2. Orientation: Raters view Neuroprint heatmaps but make no diagnosis.
3. Raters view Neuroprint heatmaps and make diagnosis
4. Raters view Neuroprint heatmaps alongside clinical context for that case and make diagnosis

--


## [Stage 1]({{ '/stage1/' | relative_url }})
## [Stage 2]({{ '/stage2/' | relative_url }})
## [Stage 3]({{ '/stage3/' | relative_url }})
## [Stage 4]({{ '/stage4/' | relative_url }})
