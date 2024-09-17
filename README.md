# Tester: user manual

---

## **Table of Contents**

1. [Introduction](#1-introduction)
2. [System Requirements](#2-system-requirements)
3. [Installation](#3-installation)
4. [Getting Started](#4-getting-started)
5. [User Interface Overview](#5-user-interface-overview)
6. [Working with Images](#6-working-with-images)
   - 6.1 [Opening Images](#61-opening-images)
   - 6.2 [Image Manipulation](#62-image-manipulation)
   - 6.3 [Magnification Levels](#63-magnification-levels)
7. [Annotations](#7-annotations)
   - 7.1 [Creating Annotations](#71-creating-annotations)
   - 7.2 [Managing Annotations](#72-managing-annotations)
   - 7.3 [Exporting and Importing Annotations](#73-exporting-and-importing-annotations)
8. [Training Module and Dataset Generation](#8-training-module-and-dataset-generation)
   - 8.1 [Creating New Classes](#81-creating-new-classes)
   - 8.2 [Preparing Training Data](#82-preparing-training-data)
9. [Model Training](#9-model-training)
   - 9.1 [Selecting a Model](#91-selecting-a-model)
   - 9.2 [Training the Model](#92-training-the-model)
10. [Model Testing Toolkit](#10-model-testing-toolkit)
    - 10.1 [Running the Model on ROI](#101-running-the-model-on-roi)
    - 10.2 [Interpreting Results](#102-interpreting-results)
11. [Exporting Results](#11-exporting-results)
12. [Troubleshooting](#12-troubleshooting)
13. [Frequently Asked Questions (FAQ)](#13-frequently-asked-questions-faq)
14. [Support and Feedback](#14-support-and-feedback)
15. [Conclusion](#15-conclusion)

---

## **1. Introduction**

Welcome to **Tester**, a comprehensive digital pathology tool designed specifically for the analysis of testicular specimens. Tester enables pathologists and researchers to work with high-resolution slide images, annotate regions of interest, train machine learning models, and analyze results efficiently.

---

## **2. System Requirements**

- **Operating System:**
  - Windows 10 or higher
  - macOS 10.14 (Mojave) or higher
  - Linux (Ubuntu 18.04 or higher)

- **Hardware:**
  - **Processor:** Intel Core i5 or equivalent
  - **RAM:** 8 GB minimum (16 GB recommended)
  - **Graphics:** Dedicated GPU for model training (optional but recommended)
  - **Storage:** 1 GB of free disk space

- **Software Dependencies:**
  - The application includes all necessary dependencies bundled within the installer.

---

## **3. Installation**

### **Windows**

1. **Download the Installer:**
   - Obtain the `Tester_Setup.exe` file from the official website or distribution source.

2. **Run the Installer:**
   - Double-click the `Tester_Setup.exe` file.
   - Follow the on-screen instructions to complete the installation.

3. **Launch the Application:**
   - After installation, you can launch Tester from the Start Menu or desktop shortcut.

### **macOS**

1. **Download the Disk Image:**
   - Obtain the `Tester.dmg` file from the official website or distribution source.

2. **Install the Application:**
   - Open the `Tester.dmg` file.
   - Drag and drop the Tester app into the `Applications` folder.

3. **Launch the Application:**
   - Navigate to the `Applications` folder and double-click the Tester icon.

### **Linux**

1. **Download the Package:**
   - Obtain the `Tester.AppImage` file from the official website or distribution source.

2. **Set Execute Permission:**
   - Open the terminal and navigate to the download directory.
   - Run `chmod +x Tester.AppImage`.

3. **Launch the Application:**
   - Run `./Tester.AppImage` in the terminal or double-click the file in your file manager.

---

## **4. Getting Started**

Upon launching Tester, you will be greeted with the main interface. This manual will guide you through the basic functionalities to help you get started quickly.

---

## **5. User Interface Overview**

- **Menu Bar:**
  - **File:** Open slides, save projects, export data.
  - **Edit:** Undo, redo, preferences.
  - **View:** Adjust magnification, toggle toolbars.
  - **Tools:** Access image manipulation tools and annotations.
  - **Help:** Access help documentation and support.

- **Toolbar:**
  - Quick access to common functions like open, save, rotate, flip, zoom, and annotation tools.

- **Image Display Area:**
  - The central area where slide images are displayed and manipulated.

- **Annotation Panel:**
  - Manage annotations, classes, and view properties.

- **Status Bar:**
  - Displays information such as current magnification, cursor position, and operation status.

---

## **6. Working with Images**

### **6.1 Opening Images**

1. **Open a Slide Image:**
   - Click on **File > Open Slide** or use the **Open Slide** button on the toolbar.
   - Navigate to the directory containing your slide images.
   - Supported formats: OpenSlide formats (`.svs`, `.tif`, `.ndpi`) and standard image formats (`.jpeg`, `.png`).

2. **Viewing the Image:**
   - The selected image will load in the Image Display Area.
   - Loading time may vary depending on the image size.

### **6.2 Image Manipulation**

1. **Rotate Image:**
   - Click on **Tools > Rotate** or use the **Rotate** button.
   - The image will rotate 90 degrees clockwise each time you click.

2. **Flip Image:**
   - Click on **Tools > Flip** or use the **Flip** button.
   - Choose between **Flip Horizontal** or **Flip Vertical**.

### **6.3 Magnification Levels**

1. **Adjust Magnification:**
   - Use the zoom slider or mouse wheel to zoom in and out of the image.
   - Current magnification level is displayed in the Status Bar.

2. **Preset Magnification Levels:**
   - Click on **View > Magnification** and select from **5x**, **10x**, or **20x**.

---

## **7. Annotations**

### **7.1 Creating Annotations**

1. **Select an Annotation Tool:**
   - Choose from **Circle**, **Square**, or **Freeform** tools in the toolbar.

2. **Draw the Annotation:**
   - **Circle/Ovoid:**
     - Click and drag on the image to draw a circle.
   - **Square:**
     - Click and drag to draw a square or rectangle.
   - **Freeform:**
     - Click to start and draw the shape by moving the cursor.
     - Click again to close the shape.

3. **Set Annotation Properties:**
   - After drawing, a dialog will appear to set properties like **Class** and **Color**.

### **7.2 Managing Annotations**

- **Annotation List:**
  - View all annotations in the Annotation Panel.
  - Annotations can be sorted by class.

- **Editing Annotations:**
  - Select an annotation to move or resize it.
  - Right-click an annotation to edit properties or delete it.

- **Surface Area Calculation:**
  - The surface area of each annotation is displayed, using microns per pixel from image metadata if available.
  - Areas over 350 µm² are displayed in mm².

### **7.3 Exporting and Importing Annotations**

- **Export Annotations:**
  - Click on **File > Export Annotations**.
  - Save annotations in **GeoJSON** format for sharing or later use.

- **Import Annotations:**
  - Click on **File > Import Annotations**.
  - Load previously saved annotations into the current image.

---

## **8. Training Module and Dataset Generation**

### **8.1 Creating New Classes**

1. **Add a New Class:**
   - In the Annotation Panel, click on **Add Class**.
   - Enter a name for the class (e.g., **"Sertoli Cell"**).

2. **Annotate for Training:**
   - Use the annotation tools to label cells or regions corresponding to the new class.

### **8.2 Preparing Training Data**

1. **Dataset Generation:**
   - After annotating, click on **Tools > Generate Dataset**.

2. **Set Export Options:**
   - Choose export format (**JPEG**, **PNG**, etc.).
   - Set patch size (e.g., **256x256 pixels**).

3. **Export Dataset:**
   - The annotated regions will be exported as image patches, organized by class.

---

## **9. Model Training**

### **9.1 Selecting a Model**

- **Available Models:**
  - **U-Net:** Suitable for segmentation tasks.
  - **DeepLab:** Advanced model for semantic segmentation.

- **Select a Model:**
  - In the Training Module, choose between **U-Net** or **DeepLab**.

### **9.2 Training the Model**

1. **Prepare Training Data:**
   - Ensure your dataset is correctly generated and organized.

2. **Export to Keras/Google Colab:**
   - Click on **File > Export for Training**.
   - The data will be packaged for easy import into Keras or Google Colab.

3. **Training Outside Tester:**
   - Use the exported data to train your model in Keras or Google Colab.
   - Follow the specific instructions provided in the exported package.

---

## **10. Model Testing Toolkit**

### **10.1 Running the Model on ROI**

1. **Load Trained Model:**
   - Click on **File > Load Model**.
   - Select the trained model file (e.g., `model.h5`).

2. **Select Region of Interest (ROI):**
   - Use the annotation tools to define the ROI on the slide.

3. **Run Model:**
   - Click on **Tools > Run Model on ROI**.
   - Choose the classes you want to detect.

### **10.2 Interpreting Results**

- **Detection Results:**
  - The model will analyze the ROI and display detections.
  - Results include absolute numbers of detected cells or structures per class.

- **Performance Metrics:**
  - **Sensitivity** and **Specificity** are calculated based on model predictions.
  - **Surface Area** of detected regions is provided.

---

## **11. Exporting Results**

- **Export to Table:**
  - Click on **File > Export Results**.
  - Save results in CSV format for further analysis in Excel or other tools.

- **Result Contents:**
  - Includes counts per class, sensitivity, specificity, and surface areas.

---

## **12. Troubleshooting**

- **Image Loading Issues:**
  - Ensure the image format is supported.
  - Check that the image file is not corrupted.

- **Annotation Problems:**
  - If annotations are not saving, verify that you have write permissions to the save location.
  - Ensure that the annotation tool is correctly selected.

- **Model Training Errors:**
  - Confirm that the dataset is properly formatted.
  - Check compatibility of the model file when loading.

- **Performance Issues:**
  - Large images may slow down the application; consider increasing system RAM.
  - Close other applications to free up system resources.

---

## **13. Frequently Asked Questions (FAQ)**

**Q1:** *Can I use Tester with images other than testicular specimens?*

**A:** Yes, while Tester is optimized for testicular specimens, it supports standard image formats and can be used with other histological images.

**Q2:** *How do I update the application?*

**A:** Check the official website or use the built-in update feature under **Help > Check for Updates**.

**Q3:** *Is GPU required for model training?*

**A:** A GPU is recommended for faster training but is not strictly required. Training on CPU will be significantly slower.

**Q4:** *Can I customize the color schemes for annotations?*

**A:** Yes, you can change colors for individual annotations, classes, or all classes in the Annotation Panel.

---

## **14. Support and Feedback**

- **Documentation:** Access detailed documentation under **Help > User Manual** within the application.

- **Support Email:** For technical support, contact us at [support@tester.com](mailto:support@tester.com).

- **Feedback:** We welcome your feedback to improve Tester. Use the **Help > Send Feedback** option.

---

## **15. Conclusion**

Thank you for choosing Tester for your digital pathology needs. We aim to provide a powerful and user-friendly tool to assist you in your research and diagnostics. We encourage you to explore all the features and reach out to us with any questions or suggestions.

---

**Disclaimer:** Tester is intended for research and educational purposes. It should not be used as a sole tool for medical diagnosis. Always consult professional guidelines and standards in your field.
