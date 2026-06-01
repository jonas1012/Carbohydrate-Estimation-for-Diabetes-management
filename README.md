# Carbohydrate Estimation for Diabetes Management

This repository contains the code and experimental pipeline for my thesis project on vision-based carbohydrate estimation from food images. The project investigates how different deep learning architectures and input modalities can be used to estimate dish-level carbohydrate content, with a particular focus on improving nutritional estimation for diabetes management.

## Project Overview

Accurate carbohydrate estimation is important for people with diabetes, as carbohydrate intake directly affects blood glucose regulation and insulin dosing. However, manual carbohydrate estimation is often uncertain and prone to error, increasing the risk of inaccurate insulin dosing and unstable blood glucose levels. This project explores whether computer vision models can estimate the carbohydrate content of meals directly from food images.

The project is based on the **Nutrition5K** dataset and compares several modelling approaches, including:

- CNN models trained from scratch
- Pretrained CNN models
- Vision Transformer-based models
- RGB-only models
- RGB-D fusion models using depth information
- Side-angle image models
- Oracle models using exact mass and ingredient information
- Fusion models using estimated mass and ingredient signals

The main prediction target is total carbohydrate content in grams.

## Research Aim

The aim of this project is to evaluate whether image-based deep learning models can estimate carbohydrate content from food images, and to investigate whether additional information such as depth, mass, and ingredients can improve prediction performance.

The project also explores whether practical single-image models can approach the performance of more information-rich multimodal systems.

## Dataset

The project uses the publicly available **Nutrition5K** dataset released by Google Research.

Nutrition5K contains images and metadata for approximately 5,000 dishes, including:

- Overhead RGB images
- Depth images
- Side-angle images
- Dish-level nutritional information
- Ingredient metadata
- Mass information

In this project, different subsets and modalities of the dataset are used depending on the experiment. The main experiments focus on dishes with available overhead RGB images and corresponding carbohydrate labels.

Due to dataset size and licensing considerations, the dataset itself is not included in this repository. Users must download the Nutrition5K dataset separately.

## Repository Structure

## Repository Structure

```text
Carbohydrate-Estimation-for-Diabetes-management/
│
├── Analysis of models/
│   ├── Carbohydrate dish bucket analysis.ipynb
│   ├── Heatmap Visualization.ipynb
│   ├── Ingredient Analysis.ipynb
│   ├── Mean baseline calculation.ipynb
│   ├── Own dataset difference analysis.ipynb
│   ├── PMAE calculation for select models.ipynb
│   ├── Testing Model 22 ingredient estimator.ipynb
│   └── Top 10 best and worst dishes analysis.ipynb
│
├── Dataset/
│   ├── Own dataset/
│   ├── Splitting of dataset test.ipynb
│   └── build_nutrition5k_dataset.ipynb
│
├── Models/
│   ├── Experimental Block 1/
│   ├── Experimental Block 2/
│   ├── Experimental Block 3/
│   ├── Experimental Block 4/
│   ├── Experimental Block 5/
│   └── Experimental Block 6/
│
├── Prediction scripts on own dataset/
│   ├── Model 22 prediction.ipynb
│   ├── Model 24 prediction.ipynb
│   ├── Model 3 V3 prediction.ipynb
│   └── Model 3 V5 prediction.ipynb
│
├── AI performance on nutrition5k test set.xlsx
├── AI performance on own dataset.xlsx
├── Performance of models.xlsx
├── TEHAI scorecard.xlsx
└── README.md
