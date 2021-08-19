---
layout: page
title: About
permalink: /about/
---

### Introduction

The purpose of the study is to validate the efficacy of Neuroprint, a software pipeline which calculates and graphically renders deviations in regional cortical thickness from values observed in healthy control subjects. Specifically, the aim is to demonstrate that Neuroprint-rendered images (aka heatmaps) improve diagnostic accuracy of different types of neurodegenerative disease, including Alzheimer’s Disease (AD) and fronto-temporal dementia (FTD), and their subtypes compared to the corresponding unprocessed T1w MRI image in a clinical setting. A secondary objective is to show Neuroprint renderings improve reader classification of disease cases versus healthy controls.

### What is Neuroprint

Neuroprint is a pipeline/Flywheel gear for calculating statistical deviation in cortical thickness from expected values for a healthy individual of the same age and sex. These expected values are derived from a dataset of healthy controls (n=868) spanning the adult age range which were collected from various centers at Penn. The highest-quality T1w image was processed with the ANTs Cortical Thickness pipeline to calculate cortical thickness values in 200 cortical regions delineated by the Schaefer 2018 atlas. A linear regression was performed for each region based on that region’s mean cortical thickness value for the 868 subjects, with age and sex as covariates.

For a given patient, the gear takes the same regional cortical thickness values and the patient’s age and sex and calculates a w-score (essentially a weighted z-score) using the following formula. Note that the score is multiplied by -1 so that higher w-scores reflect greater degeneration.

w-score =-raw ct val - intercept - age\*agecoefficient - sex\*sexcoefficient standard error residuals
The result is a score for each region describing the difference in that region’s observed cortical thickness compared to that of a healthy control. The gear renders these scores in a 3D model.
