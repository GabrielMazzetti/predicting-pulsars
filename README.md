# 🌌 HTRU2: Pulsar Detection through Machine Learning

## Overview

Pulsars are a rare type of neutron star that produce radio emission detectable here on Earth. As they rotate, their emission beam sweeps across the sky like a lighthouse, producing detectable patterns of broadband radio emission. Searching for these signals is a massive data challenge. Modern radio telescopes generate terabytes of data daily, making manual inspection impossible.

## The Problem

While searching for pulsars, scientists encounter a major obstacle: Radio Frequency Interference (RFI). Artificial signals from Earth (satellites, cell towers, and electronics) and cosmic noise often mimic pulsar signals. The challenge is to filter out the noise and identify the true pulsar signatures in a highly imbalanced dataset, where legitimate pulsars are extremely rare.

## The Data

The dataset used in this project is the HTRU2 (High Time Resolution Universe Survey). Instead of raw radio waves, the data consists of continuous statistical features extracted from two types of processed signals:

- The Integrated Profile (the folded pulse shape).
- The DM-SNR Curve (Signal-to-Noise Ratio over Dispersion Measure).

| Feature Type | Extracted Variables (Statistical Moments) |
| :--- | :--- |
| **Integrated Profile** | Mean, Standard Deviation, Excess Kurtosis, Skewness |
| **DM-SNR Curve** | Mean, Standard Deviation, Excess Kurtosis, Skewness |
| **Target** | `0` (Noise/RFI) or `1` (True Pulsar) |

## Project Objective

The goal of this project is to develop and evaluate a binary classification model capable of distinguishing real pulsar signals from background noise. Given the heavy class imbalance in the HTRU2 dataset, this project will focus heavily on specialized metrics (such as Recall, F1-Score, and PR-AUC) and resampling techniques rather than simple accuracy.
