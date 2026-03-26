# Research Project M2 — Plane Identification of Rooftops from LiDAR Data in France

**Last update:** 26/03/2026

This repository contains the work I carried out during my Master's degree, focused on **plane identification in point clouds** using open-source LiDAR data from [IGN](https://www.ign.fr/](https://cartes.gouv.fr/rechercher-une-donnee/dataset/IGNF_NUAGES-DE-POINTS-LIDAR-HD).

The project is implemented in Python and consists of two main scripts:

- **Plane Detection on Real Data**
  This script detects planes from LiDAR point cloud tiles covering 1 km² areas in France.

- **Algorithm Robustness Testing**
  This script evaluates the robustness of the detection algorithms using generated point clouds with variable parameters.

---

## 📌 Data Source

The LiDAR data used in this project comes from open-source datasets provided by IGN:

🔗 [IGN LiDAR HD Point Clouds](https://cartes.gouv.fr/telechargement/IGNF_NUAGES-DE-POINTS-LIDAR-HD)
*(Web link tested on 24 March 2026)*

---

## 🛠️ Utilisation

For practical reasons, the code for plane detection on real data has been adapted to run on **Google Colab**. The robustness testing work still needs refinement before being shared.

To test the code, the only data you need to download locally is a LiDAR file of type `.laz` containing a raw point cloud of 1 km².

### ⚠️ Note on Visualization
- **Open3D** visualization is not supported in Google Colab.
- Some adaptations have been made to enable execution in Colab.
- In Colab, point cloud visualization is performed using **Plotly**.

The following instructions assume you are testing the code on Google Colab. You will find a file named `Test.py` in this repository for this purpose.

---

## 1️⃣ First Step — Setup

### 📥 Download LiDAR Data
1. Upload the `.laz` file you downloaded from IGN to your Google Colab instance.
2. Download the file from the [IGN LiDAR HD Point Clouds](https://cartes.gouv.fr/telechargement/IGNF_NUAGES-DE-POINTS-LIDAR-HD) website.
3. Select a tile where **buildings are visible** and download it.

![IGN LiDAR Tile Selection](https://github.com/user-attachments/assets/664cb6ea-9ed9-43ff-8919-fa7e9825b68a)

You should obtain a `.laz` file.

### 📊 Point Cloud Classification (IGN)
![IGN Point Cloud Classification](https://github.com/user-attachments/assets/3c57e7f5-b711-4d83-b1b5-260aa5dbf21c)

**Source:** [IGN LiDAR HD Documentation (PDF)](https://geoservices.ign.fr/sites/default/files/2025-03/DC_LiDAR_HD_1-0.pdf)
