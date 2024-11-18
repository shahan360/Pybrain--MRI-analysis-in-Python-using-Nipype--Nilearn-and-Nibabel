# Pybrain-MRI Analysis in Python using Nipype, Nilearn, and Nibabel

## Overview

This project is inspired by the **Pybrain Workshop** conducted by [Peer Herholz](https://github.com/PeerHerholz). The workshop focuses on using Python-based tools for neuroimaging analysis, particularly in the context of MRI data. This repository aims to replicate and extend the concepts learned during the workshop, using popular neuroimaging libraries such as **Nipype**, **Nilearn**, and **Nibabel**.

The goal of this project is to build a reproducible pipeline for preprocessing and analyzing fMRI data, leveraging these powerful Python libraries.

## Project Structure

The project is divided into several key components:

### 1. **fMRI Preprocessing with Nipype**
Using **Nipype**, we set up a preprocessing pipeline for fMRI data that integrates multiple neuroimaging tools (e.g., FSL, SPM). The pipeline includes the following steps:
- **Gunzip**: Unzipping the raw functional MRI images.
- **Slice Time Correction**: Correcting for differences in slice acquisition times.
- **Motion Correction**: Adjusting for subject motion during scanning.
- **Artifact Detection**: Identifying motion and intensity outliers.
- **Segmentation**: Segmenting anatomical images into gray matter (GM), white matter (WM), and cerebrospinal fluid (CSF).
- **Coregistration**: Aligning functional images with anatomical images.
- **Smoothing**: Applying Gaussian smoothing to the functional images.

The workflow is designed to run efficiently in parallel, leveraging Nipype's ability to execute tasks across multiple processors.

### 2. **Neuroimaging Data Manipulation with Nilearn**
Using **Nilearn**, we perform advanced image manipulation and visualization tasks on the preprocessed fMRI data. Key techniques include:
- **Resampling Images**: Adjusting image resolution to match templates or other images.
- **Smoothing**: Applying different levels of smoothing to brain images.
- **Signal Extraction**: Extracting time series data from specific brain regions using masks.
- **Independent Component Analysis (ICA)**: Decomposing fMRI data into independent components to identify brain networks.
- **Dictionary Learning**: A more stable alternative to ICA for extracting meaningful temporal elements from fMRI data.

Nilearn also provides powerful visualization tools such as glass-brain plots and 3D surface projections, which are used to visualize the results of our analyses.

### 3. **Image Handling with Nibabel**
Using **Nibabel**, we handle the low-level input/output operations for neuroimaging data. This includes:
- Loading and inspecting NIfTI images.
- Accessing image metadata such as headers and affine transformations.
- Visualizing slices of MRI data using matplotlib.
- Modifying image data (e.g., rescaling) and saving it back to NIfTI format while preserving important metadata.

Nibabel provides a flexible interface for working with various neuroimaging formats, making it an essential tool for preprocessing and preparing data for further analysis.

## Tools Used

1. **Nipype**: A Python library that interfaces with various neuroimaging tools like FSL, SPM, ANTs, etc., allowing users to create reproducible workflows for processing MRI data.
2. **Nilearn**: A high-level Python library focused on statistical learning and visualization of neuroimaging data, particularly fMRI.
3. **Nibabel**: A low-level Python library used for reading, writing, and manipulating neuroimaging file formats such as NIfTI.

## Current Status

This project is a work in progress. I am still learning how to fully utilize these libraries and concepts in neuroimaging analysis. The repository will be updated as I continue to explore new techniques and refine the pipeline.

Stay tuned for more updates!
