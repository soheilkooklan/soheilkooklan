## Hi, I'm Soheil Kooklan

Biomedical engineer (M.Sc., Bioelectric) with a background in physics. I work on medical ultrasound, medical image analysis, and machine learning applied to vital physiological signals.

Most of what I publish here is research software, and it is written around one question: can the numbers it reports be trusted? Segmentation masks, EEG classifiers and heart-rate estimators all fail quietly, and a good score on a badly split dataset is worse than no score at all. The repositories below spend a fair amount of their code on saying when they do not know.

## Projects

Each repository is archived on Zenodo and citable by DOI. All of it is research software, not a medical device, and none of it is validated for clinical use.

**[Tumor-from-Ultrasound-Image](https://github.com/soheilkooklan/Tumor-from-Ultrasound-Image)** — Lesion segmentation, BI-RADS-aligned morphometry and uncertainty-gated reporting for B-mode breast ultrasound. Preprocessing built around ultrasound physics rather than generic denoising, five segmentation models including RDAU-Net with an ASPP bottleneck, automatic extraction of ACR BI-RADS descriptors from the predicted mask, and Monte Carlo dropout measured along the lesion boundary and converted into a reliability grade on each descriptor.
Python · PyTorch · OpenCV · DOI [10.5281/zenodo.21826922](https://doi.org/10.5281/zenodo.21826922)

**[Tumor-from-EEG](https://github.com/soheilkooklan/Tumor-from-EEG)** — Quantitative EEG biomarker extraction with subject-disjoint machine-learning evaluation. Version 2 is a rewrite. On a synthetic cohort with labels assigned at random, where the correct answer is ROC-AUC 0.500, the version 1 protocol scored far above chance because channels from one subject were split across training and test folds. The current version computes 81 documented qEEG biomarkers across five domains, selects among them by stability analysis, and evaluates classifiers under repeated nested subject-disjoint cross-validation with calibration, confidence intervals and significance testing.
Python · scikit-learn · MNE · DOI [10.5281/zenodo.21762151](https://doi.org/10.5281/zenodo.21762151)

**[HR-from-ECG](https://github.com/soheilkooklan/HR-from-ECG)** — Heart rate and HRV from single-lead ECG. Every quantity is reported as an interval with a distribution-free coverage guarantee, signal quality is learned from downstream estimation error rather than from waveform appearance, and the estimator abstains where the signal cannot support an answer. Version 1 returned a number for any input, including a flat line.
Python · NumPy · SciPy · DOI [10.5281/zenodo.21788945](https://doi.org/10.5281/zenodo.21788945)

## What I work on

- Therapeutic and diagnostic ultrasound, HIFU, image-guided intervention
- Medical image segmentation and quantitative descriptors
- qEEG and ECG biomarkers, uncertainty quantification and calibration in clinical machine learning
- Biomedical instrumentation: fault diagnosis and repair down to board level, calibration and precision measurement

## Background

M.Sc. in Biomedical Engineering (Bioelectric) and B.Sc. in Physics, Azad University, Science and Research Branch, Tehran. My master's thesis was on improving a high-intensity focused ultrasound transducer for tumor ablation: acoustic and thermal simulation in k-Wave, FOCUS and COMSOL, layered tissue models built in Mimics, fuzzy clustering for MRI tumor segmentation, and a delta parallel robot for positioning the transducer. Research assistant in the same department from 2017 to 2019, and teaching assistant for neural networks, fuzzy control and biological systems modeling.

## Tools

Python, C++, Java, MATLAB, COMSOL Multiphysics, Simulink, Mimics, SolidWorks, Arduino, Git.

## Contact

[LinkedIn](https://www.linkedin.com/in/soheilkooklan/) 

Questions about any of the repositories are welcome as issues, and so are pull requests. If you are working on uncertainty quantification for clinical models or on therapeutic ultrasound, I am glad to hear about it.

<!---
soheilkooklan/soheilkooklan is a special repository because its README.md appears on the GitHub profile.
--->
