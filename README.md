**Robocup2026 – Progress Object Classification with Computer Vision**

**Data used**

Work was done with three object classes selected due to the mechanical limitations of Colombia’s robotic gripper. The objects were chosen for their size.  
The classes used are:
- Tuna
- Sponge
- Golf Ball

Each category had approximately 60 initial images, obtained from open sources.

**Image processing**

A Python script was implemented to automatically process the image sets.  
The code performs the following steps:
- Unzips the .zip files for each class.
- Converts all images to .png format.
- Rotates the images at angles of 90°, 180°, 270°, and 360°, generating new views.
- Organizes the processed images into four separate folders according to their angle.
- Compresses the results again inside a general folder per class.

This procedure made it possible to increase the number of samples available for training and improve the variability of the dataset.  
Some images were not used due to resolution issues or visual redundancy.

**Dataset creation**

Once the images were processed, they were uploaded to the Roboflow environment. Each image was classified with its corresponding class, which carried the name of the objects.  
Three folders were generated corresponding to the three selected classes, with the following final counts:

| Class     | Uploaded images |
|-----------|------------------|
| Tuna      | 238              |
| Golf Ball | 240              |
| Sponge    | 254              |

Overall total: 732 images.

Version V2 of the dataset was created, which was automatically split by Roboflow into:
- Training set: 513 images
- Validation set: 146 images
- Testing set: 73 images

**Code generation and repository linkage**

In Roboflow, the Python code snippet for downloading the dataset in YOLOv8 format was automatically generated, which has already been incorporated into the GitHub repository.

This script allows direct access to the dataset from a Python environment, ensuring dataset traceability with Roboflow.

**Current training status**

Roboflow project link: https://app.roboflow.com/andesrobot/robocup2026-y7rar/annotate
