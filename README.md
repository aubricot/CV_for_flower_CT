# CV_for_flower_CT
Computer vision for micro-CT datasets of flowers using UNETR and MONAI    
*Last updated 2 April 2025*    

The code in this repository is used to evaluate computer vision as a tool for analyzing floral micro-CT datasets of cacao (*Theobroma cacao*). It is built in Google Colab Notebooks with Python 3 and MONAI Core 1.5. Micro-CT datasets and labels were generated in 3D Slicer as .nrrd files. They are converted to NIFTI (.nii.gz) format and registered to eachother in [preprocessing_whole_flower_nrrd2nifti.ipynb](https://github.com/aubricot/CV_for_flower_CT/blob/main/preprocessing_whole_flower_nrrd2nifti.ipynb). UNETR is trained to recognize whole flower outlines from CT data in [Cacao_Whole_Flower_Seg_unetr_train.ipynb](https://github.com/aubricot/CV_for_flower_CT/blob/main/Cacao_Whole_Flower_Seg_unetr_train.ipynb). Results are visualized on input and output images to generate figures and interpret results in [Cacao_Whole_Flower_Seg_unetr_inspect_results.ipynb](https://github.com/aubricot/CV_for_flower_CT/blob/main/Cacao_Whole_Flower_Seg_unetr_inspect_results.ipynb).

<p align="center">
<a href="url"><img src="https://github.com/aubricot/CV_for_flower_CT/blob/main/images/unetr_pipeline.jpg" align="middle" width="900" ></a></p>   
<p align="center">
<sub><sup>Schema of CT training inputs and model ouputs for a cacao flower.</sup></sub>
  
<p align="center">
<a href="url"><img src="https://github.com/aubricot/CV_for_flower_CT/blob/main/images/thecac_fbg_cg_220622_05_masked.nii.gz_slice_176.png" align="middle" width="700" ></a></p>   
<p align="center">
<sub><sup>Sample model input image and label along with predicted output.</sup></sub>

<p align="center">
<a href="url"><img src="https://github.com/aubricot/CV_for_flower_CT/blob/main/images/Sketchfab_models.png" align="middle" width="700" ></a></p>   
<p align="center">
<sub><sup>Interactive 3D models of UNETR Model ground truth (label), output (raw), and output (post-processed) are available on <a href="https://skfb.ly/pvw6n">Sketchfab</a></sup></sub>

## Data and model availability
Three versions of the training datasets (micro-CT images of flowers and their corresponding segmentation files) are available on Zenodo ([masked training data used to train best models](https://doi.org/10.5281/zenodo.15123160), unmasked training data with cleaned segmentations and exclusion critera, [unmasked training data with original segmentations and no exclusion criteria](https://zenodo.org/records/15123180)). Train notebooks for the 5 best trianing attempts and their corresponding train graphs are available on [Zenodo](https://doi.org/10.5281/zenodo.15126203). Trained models will be made available soon.

## References

<a id="note1" href="#note1ref"><sup>1</sup></a>[Tomar 2021](https://medium.com/analytics-vidhya/what-is-unet-157314c87634). What is UNET? Medium, 15 March 2025.   
<a id="note2" href="#note2ref"><sup>2</sup></a>[Hatamizadeh et al. 2021](https://arxiv.org/abs/2103.10504). UNETR: Transformers for 3D Medical Image Segmentation. Accepted to IEEE Winter Conference on Applications of Computer Vision (WACV) 2022.   
<a id="note3" href="#note3ref"><sup>3</sup></a>[MONAI GitHub](https://github.com/project-monai/monai).   
<a id="note4" href="#note4ref"><sup>4</sup></a>[Cardoso et al. 2022](https://arxiv.org/abs/2211.02701). MONAI: An open-source framework for deep learning in healthcare. arXiv.   
<a id="note5" href="#note5ref"><sup>5</sup></a>[Kikinis et al. 2013](https://doi.org/10.1007/978-1-4614-7657-3_19). 3D Slicer: A Platform for Subject-Specific Image Analysis, Visualization, and Clinical Support.   
<a id="note6" href="#note6ref"><sup>6</sup></a>[3D Slicer Software](https://www.slicer.org/). 

## License
**Code**  
Code in this repository is released under the [MIT license](https://github.com/aubricot/CV_for_flower_CT/blob/master/LICENSE). More information is available at the [Open Source Initiative](https://opensource.org/licenses/MIT). Parts of Cacao_Whole_Flower_Seg_unetr.ipynb are listed under a different license.   
**Images**  
Images and their corresponding licenses will be updated shortly.
