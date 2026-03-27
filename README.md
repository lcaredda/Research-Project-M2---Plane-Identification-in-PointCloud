# Research Project M2 — Plane Identification of Rooftops from LiDAR Data in France

**Last update:** 26/03/2026

This repository contains the work I carried out during my Master's degree, focused on **plane identification in point clouds** using open-source LiDAR data from IGN.

The project is implemented in Python and consists of two main scripts:

- **Plane Detection on Real Data**
  This script detects planes from LiDAR point cloud tiles covering 1 km² areas in France.

- **Robustness Testing**
  This script evaluates the robustness of the detection algorithms using generated point clouds with variable parameters.

---

## 📌 Data Source

The LiDAR data used in this project comes from open-source datasets provided by IGN:

🔗 [IGN LiDAR HD Point Clouds](https://cartes.gouv.fr/telechargement/IGNF_NUAGES-DE-POINTS-LIDAR-HD)
*(Web link tested on 24 March 2026)*

---

## 🛠️ Utilisation

For practical reasons, the code has been adapted to run on **Google Colab**.

To test the code, the only data you need to download locally is a LiDAR file of type `.laz` containing a raw point cloud of 1 km².

---

## Setup Instruction

### 📥 Download LiDAR Data
1. Upload the `.laz` file you downloaded from IGN to your Google Colab instance.
2. Download the file from the [IGN LiDAR HD Point Clouds](https://cartes.gouv.fr/telechargement/IGNF_NUAGES-DE-POINTS-LIDAR-HD) website.
3. Select a tile where **buildings are visible** and download it.

![IGN LiDAR Tile Selection](https://github.com/user-attachments/assets/664cb6ea-9ed9-43ff-8919-fa7e9825b68a)

You should obtain a `.laz` file.


Once your .laz file is downloaded, open the script in Google Colab using the "Open in Colab" button.

### 1st Part

Run the first code cell and upload your .laz file when prompted.
Note: This process may take 10–15 minutes to complete. Colab can run in the background, so you don’t need to stay on the page while waiting.
After the import finishes, use the second cell to verify that your file name appears in the output.
A `plot()` function is created  with plotly library to visualize the 3D point cloud process.

### 2nd Part

Make sure to replace the file name in the code with your actual `.laz` file name:
`las = laspy.read('your_file_name.laz')  # Replace 'your_file_name.laz' with your actual file name`
The IGN has already predone the work by classifying the raw data available in opensource. 
Since we want to calculate slope of planar rooftop, we will directly takes relevant points belonging to building by filtering with the coresponding categorie (categorie 6).

📊 ***Point Cloud Classification (IGN)***
![IGN Point Cloud Classification](https://github.com/user-attachments/assets/3c57e7f5-b711-4d83-b1b5-260aa5dbf21c)

**Source (link checked 26/03/2026) :** [IGN LiDAR HD Documentation (PDF)](https://geoservices.ign.fr/sites/default/files/2025-03/DC_LiDAR_HD_1-0.pdf)
