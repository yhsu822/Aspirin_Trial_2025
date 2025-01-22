# Aspirin_Trial_2025
---
## About the project
This study quantitatively evaluated six biomarkers through two staining panels of 5-plex mIHC/IF using two formalin-fixed, paraffin-embedded (FFPE) tissue slides per rectal biopsy sample. The first panel included Ki67, BAX, TUNEL, pan-CK, and DAPI; the second included TRPM7, pMLKL, COX-2, pan-CK, and DAPI. The three fields of images per stained slide were taken at x100 amplification, and the exposure times were typically 200 microseconds for DAPI, 900 microseconds for Ki67, BAX, TUNEL, TRPM7, pan-CK, and 500 – 900 microseconds for COX-2 and pMLKL. Grayscale images from the 5-plex mIHC/IF were processed automatically using several image processing pipelines with the open-source CellProfiler (v3.1.5) software. 
### Pipelines that automatedly overlay grayscale images 
We established two pipelines that automatedly overlay grayscale images from the two mIHC/IF panels to generate RGB images (16-bit tiff format), with biomarkers in red, pan-CK in green, and nuclei in blue. Many images were batch-processed automatically and exported into designated folders on the local computer. A study pathologist performed a visual image quality check to exclude unspecific artifacts using the open-source ImageJ software 
### Pipelines for automated image quantification
The six quantitative measurement pipelines were established for six biomarkers. Each pipeline was validated using 50 control-TMA and sample images as a training set that typically showed negative, weak, moderate, and strong positive intensity, and randomly selected 100 sample images as validation sets for necessary threshold adjustment of the “IdentifyPrimaryObjects” module until quantitative scores and pathologist’s visual scores were well matched. The sample images were uploaded into established pipelines for automated high-throughput imaging quantification. A post-analytical quality check of 5% of images, especially those with high scores was performed to correct potential errors from low-quality images showing low signal/noise ratios. 
### Example images for all pipelines 
The images used for each pipeline are available from the remote repository URL https://github.com/yhsu822/Input.git. 
### Setting up folders for running the pipelines
After downloading pipelines, users must use CellProfiler v3.1.5 software (the latest version could not run the pipelines) and set up folders/subfolders on the local computer desktop before running the pipeline. 
#### First folder: Input
---
subfolders:1st Panel_RawImages 2nd Panel_RawImages BAX; subfolders: Bax_TraingSet; BAX_High Bkgd BAX_MergedImages COX2; subfolder: COX2_TrainingSetImages Cox2_MergedImages Ki67; subfolder: Ki67_TrainingSet Ki67_MergedImages pMLKL; subfolders: pMLKL_TrainingSetImages; pMLKL_2ndRun pMLKL_MergedImages TRPM7; subfolder: TRPM7_TrainingSet TRPM7_MergedImages; TUNEL; subfolders: TUNEL_TrainingSet; higherShresholdImages TUNEL_MergedImages.
---
#### Second folder: Output 
---
subfolders: Aspirin_BAX Aspirin_COX2 Aspirin_Ki67 Aspirin_pMLKL Aspirin_TRPM7 Aspirin_TUNEL
---
