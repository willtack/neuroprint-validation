---
layout: page
title: About
permalink: /about/
---

### Introduction

The purpose of the study is to validate the efficacy of Neuroprint, a software pipeline which calculates and graphically renders deviations in regional cortical thickness from values observed in healthy control subjects. Specifically, the aim is to test the hypothesis that Neuroprint-rendered images (aka heatmaps) improve diagnostic accuracy of different types of neurodegenerative disease, including Alzheimer’s Disease (AD) and fronto-temporal dementia (FTD), and their subtypes compared to the corresponding unprocessed T1w MRI image in a clinical setting. A secondary objective is to show Neuroprint renderings improve reader classification of disease cases versus healthy controls.

### What is Neuroprint

Neuroprint is a pipeline/Flywheel gear for calculating statistical deviation in cortical thickness from expected values for a healthy individual of the same age and sex. These expected values are derived from a dataset of healthy controls (n=868) spanning the adult age range which were collected from various centers at Penn. The highest-quality T1w image was processed with the ANTs Cortical Thickness pipeline to calculate cortical thickness values in 200 cortical regions delineated by the Schaefer 2018 atlas. A linear regression was performed for each region based on that region’s mean cortical thickness value for the 868 subjects, with age and sex as covariates, creating a linear model for each region. 

For a given patient, the pipeline produces a score for each region, called a w-score, which denotes the number of standard deviations the patient's cortical thickness is below the expected value for a patient of that age and sex.   To get this score, the pipeline plugs the patient's mean cortical thickness in the given region, the patient's age, and patient's sex into the following formula: 


_w-score =-(raw ct val - intercept - age\*agecoefficient - sex\*sexcoefficient) / standard error residuals_

Note that the score is multiplied by -1 so that higher w-scores reflect greater degeneration. This calculation is repeated for all 200 regions in the atlas. The pipeline then renders these scores as different shades of color scale in a 3D projection of the cortical surface. The scores are thresholded at 1.5 for the rendering, so that only "clinically significant" differences are displayed. This threshold also means that areas of cortical thickening are not displayed (as they'd be negative). This is because we are focused on degeneration, and only displaying areas of cortical thinning makes the heatmaps easier to interpret. 
