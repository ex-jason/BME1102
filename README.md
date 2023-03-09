# MRI Graphical Classification Interface

## Abstract

In the operating environment of magnetic resonance imaging (MRI), researchers have corresponding supporting software to classify and process the acquired data in real time, so as to efficiently judge the data status and adjust the scanning process. However, in the follow-up scientific research process, there is no corresponding software for graphical classification of the data obtained by magnetic resonance imaging. Generally, python or matlab is used to process the files, which reduces the efficiency of scientific research to a certain extent, and is not friendly to many  researchers who conducts MRI studies for the first time.

This project will use the python language to achieve the graphical classification and display of MRI data in ParaVision. We will learn the development of a python-based graphical interface, deeply understand the meaning of each part of MRI data, and use Linux+git+github to maintain the project.

## Introduction

**Magnetic resonance imaging** (MRI) is a procedure that uses radio waves, a powerful magnet, and a computer to make a series of detailed pictures of areas inside the body.

The **format** of the research data obtained by magnetic resonance imaging is ```.nii format. The Nifti (Neuroimaging Informatics Technology Initiative) file format is a voxel-level data format that is generally compatible with major neuroimaging analysis tools, and it is also the most common data format in neuroimaging research. It is a three-dimensional array (sMRI) or four-dimensional array (fMRI, dMRI), and then set a head data. The array contains the image voxel value data itself, and the header data contains spatial and voxel information. Matlab has introduced a special Nifti file analysis function since 2017b. SPM12 (Statistical Parametric Mapping, statistical parameter mapping), dpabi and other toolkits also provide a Nifti file analysis interface. NIfTI_20140122 is a special Nifti file analysis toolkit. Nibabel on python can parse brain image files such as Nifti, and nilearn is a tool that integrates parsing, processing, and analysis.

**paravision** is a preclinical imaging software. Using this software will make scanning more intuitive while maintaining full flexibility, enhancing scanning and analysis capabilities, allowing operators to focus on their research with confidence. But at present, this software is limited to use in the computer that supports the MRI machine, and cannot be installed and used in ordinary computers, so many of its processing, viewing, and analysis functions cannot be transferred and used. Under commonly used operating systems, to read MRI data in NII format, one of the mainstream methods is to use the NiBabel library in Python.

**NiBabel** is a Python library for reading and writing neuroimaging formats such as NIfTI and DICOM, with many convenient functions. However, the data directly derived from the code is too discrete to be displayed intuitively, and needs to be integrated in various ways to achieve unified research. Therefore, we want to use the Python language to realize the graphical classification and display of MRI data through this project, combined with the knowledge learned in the classroom, and further beautify the UI to improve the comfort of scientific research.

## Material & Methods

### Information contained in MRI data

* Information about the image matrix. Image size, image value range, etc.

* Image imaging information. Such as layer thickness, plane resolution, etc.;

* Image contrast information. Contrast information in MRI images is often used to distinguish different types of tissue. Contrast can be achieved by adjusting scan parameters such as TR and TE or by using different imaging sequences.

* Spatial location information. MRI images need some positioning techniques to determine the positional relationship of different tissues. Spatial location information can be obtained in different ways, such as methods based on magnetic field gradients and methods based on reference markers.

### Nibabel

NiBabel is a Python library for reading and writing data in neuroimaging formats, including common formats such as NIfTI, ANALYZE, MINC, MGH, and ECAT.

NiBabel provides many handy features such as:

* **Load and save neuroimaging format data. **NiBabel can load neuroimaging format data from disk and save it as a file in the corresponding format. It also supports reading and writing metadata of MRI data, including data type, data dimension and coordinate system, etc.
* **Data preprocessing and transformation.** NiBabel provides some methods for transforming MRI data into different spaces or coordinate systems, and supports preprocessing of MRI data, such as slicing and filtering.
* **Interactive data visualization.** NiBabel also supports interactive visualization of MRI data, including support for 3D volume rendering, slice viewing, selection of regions of interest, etc.

###  tkinter

Tkinter is one of the standard graphical user interface (GUI) toolkits for the Python programming language, which provides a rich set of GUI controls and utilities for creating Python applications with a graphical user interface. Tkinter is built on top of the Tk GUI toolkit, a cross-platform toolkit for creating graphical user interfaces.

Various GUI applications can be created using Tkinter, such as window applications, desktop applications, data visualization tools, and more. Tkinter provides many commonly used GUI controls, such as labels, buttons, text boxes, drop-down boxes, and so on. At the same time, Tkinter also provides layout managers to arrange controls and manage the appearance and behavior of GUI.

### tkinter Beautification

* **Use an appropriate layout manager.** Tkinter provides multiple layout managers, such as pack, grid, and place, and choosing the right layout manager can help you control the position and size of controls more easily.
* **Use appropriate colors and fonts.** You can add background and foreground colors to controls using Tkinter's built-in colors or custom colors. Likewise, using the proper font type, size, and color can make text more legible.
* **Use custom controls.** Using custom controls can help create a more personal and unique application. You can use Tkinter's Canvas class to create custom graphics, and Tkinter's Frame class to create custom containers.
* **Use external libraries.** In addition to the controls and functions provided by Tkinter itself, we can use the matplotlib library to create more complex data visualization controls.

### Material

* Project language: python_3.9(100%)

* Libraries expected to be used: numpy, tkinter, matplotlib, nibabel
* Test data source: mouse brain MRI data provided by BME1102

 ## Expected Result

The ParaVision interface is shown in the figure below.

![ParaVision](https://raw.githubusercontent.com/ex-jason/BME1102/main/image-20230226192012813.png)

This project will eventually realize most of this functions in the interface, including the display of various parameters, view axial plane, coronal plane and sagittal plane slices, etc., and realize the selection and switching of data positions.
