# File-Carving-HDF5-Recovery

# HDF5 File Recovery & Header Reconstruction

## Overview

This project demonstrates an investigation focused on recovering intentionally obfuscated **HDF5 (.h5)** files from a forensic disk image. It involved identifying altered file signatures, creating a custom PhotoRec signature, carving hidden files, hexadecimal analysis, reconstructing corrupted headers and validating the integrity of the recovered files.

## Scenario

An employee of MicroBotics company, Jonathan Boyle, is suspected of leaking company's AI training models and datasets. The company keeps those models and datasets in Hierarchical Data Format Version 5 (HDF5) files (https://support.hdfgroup.org/documentation/hdf5/latest/_f_m_t3.html#Superblock). These models are viewable through HDFViewer software (https://www.hdfgroup.org/downloads/hdf5) or online version (https://myhdf5.hdfgroup.org/). 

A drive was seized from the suspect and then acquired for forensic examination. A note was found stuck to the drive reading "First 3 bytes => +1". Initial file recovery attempts conducted by another agency did not reveal any evidence of dataset and model files having .h5 extension or HDF5 file format within the forensic image of the seized drive.

You as Digital Forensic Examiners of ICF Agency are tasked to find out if there are HDF files in the drive; carve all of them and rebuild the files (if necessary) in order to make them readable by the HDFViewer software. The company provided a sample h5 file 'suspect-corrupted-files' for helping the examination process. The hash value of the image file is given below.

SHA256: 4365CCF79D65A16E9418869A6EEB75FAEB964661FB57785C91CC39AF7FD98FE8

