# Research Project M2 — Plane Identification of Rooftops from LiDAR data in France

This repository contains the work I carried out during my Master degree, focused on **plane identification in point clouds** using open-source LiDAR data from IGN.

The project is implemented in Python and consists of two main scripts:

- **Plane detection on real data**:  
  This script detects planes from LiDAR point cloud tiles covering 1 km² areas in France.

- **Algorithm robustness testing**:  
  This script evaluates the robustness of the detection algorithms using a generated point clouds with variable parameters.

## Data Source
The LiDAR data used in this project comes from open-source datasets provided by IGN.

https://cartes.gouv.fr/telechargement/IGNF_NUAGES-DE-POINTS-LIDAR-HD (web link tested on 24 march 2026)

## Utilisation

For practical reasons, the code has been adapted to run on **Google Colab**. Therefore, to test the code, the only data you will need to download locally is a LiDAR file of type `.laz` containing a raw point cloud of 1 km².

Visualization of the point cloud using **Open3D** is not supported in Google Colab, so some adaptations have been made to make the execution possible. As a result, you may notice some differences between the original Python script and the Colab notebook. In Colab, point cloud visualization will be performed using **Plotly**.

The following instructions assume you are testing the code on Google Colab. You will find a file named `Test.py` in this repository for this purpose.

---

## 1️⃣ First Step - SET UP

To test the code, upload the `.laz` file you downloaded from IGN to your Google Colab instance. You can download the file from the following link:  
[https://cartes.gouv.fr/telechargement/IGNF_NUAGES-DE-POINTS-LIDAR-HD](https://cartes.gouv.fr/telechargement/IGNF_NUAGES-DE-POINTS-LIDAR-HD)

Once on the website, select a tile where **buildings are visible** and download it.

<img width="1915" height="847" alt="image" src="https://github.com/user-attachments/assets/664cb6ea-9ed9-43ff-8919-fa7e9825b68a" />

You should obtain a  `.laz` file


**Point CLoud Classification done by the IGN**

<img width="601" height="246" alt="image" src="https://github.com/user-attachments/assets/3c57e7f5-b711-4d83-b1b5-260aa5dbf21c" />

source : https://geoservices.ign.fr/sites/default/files/2025-03/DC_LiDAR_HD_1-0.pdf

