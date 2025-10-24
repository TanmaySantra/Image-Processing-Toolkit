# Image Processing Toolkit

A Python-based interactive toolkit for performing common image processing operations such as **Gaussian Blur**, **Edge Detection**, **Color Detection**, **Binary Image Conversion**, and **Grayscale Conversion**. Users can provide inputs at runtime to customize processing.

---

## **Features**

1. **Gaussian Blur**

   * Apply a Gaussian blur to an image.
   * Adjustable **kernel size** and **sigma**.

2. **Edge Detection**

   * Detect edges using the **Laplacian filter**.
   * Converts the image to grayscale for edge detection.

3. **Color Detection**

   * Highlight specific pixel colors in an image.
   * User can provide **multiple target colors** and a **highlight color**.

4. **Binary Image Conversion**

   * Convert an image to binary (0–255) using a **pivot value** (0–1).

5. **Grayscale Conversion**

   * Convert an image to grayscale using the **simple averaging method** of RGB channels.

---

## **Installation**

1. Clone the repository:

```bash
git clone <repository_url>
```

2. Install required dependencies:

```bash
pip install pillow numpy scipy
```

3. Ensure your input images are placed in a valid directory (e.g., `data/`).

---

## **Usage**

Run the toolkit in the terminal:

```bash
python image_toolkit.py
```

The program will prompt the user to:

1. **Enter the input image path**
2. **Enter the output image path**
3. **Choose an operation to execute**

Example menu:

```
Choose operation to execute:
1. Gaussian Blur
2. Edge Detection
3. Color Detection
4. Binary Image
5. Grayscale Tool
```

### **Operation-specific Inputs**

* **Gaussian Blur**: kernel size (int), sigma (float)
* **Edge Detection**: no extra input
* **Color Detection**:

  * Target colors: `r,g,b;r,g,b;...`
  * Highlight color: `r,g,b`
* **Binary Image**: pivot value (0–1)
* **Grayscale Tool**: method (`simple`)

---

## **Examples**

**Color Detection Input Example:**

```
Enter target colors (r,g,b) separated by semicolon: 10,40,45;100,150,200
Enter highlight color (r,g,b): 255,0,0
```

* Pixels with `(10,40,45)` or `(100,150,200)` will be replaced with `(255,0,0)`.

**Binary Image Input Example:**

```
Enter pivot value (0-1) for binary image: 0.5
```

* All pixels above 127 (0.5 * 255) become 255, below become 0.

---

## **Dependencies**

* [Pillow](https://pillow.readthedocs.io/) – For image I/O
* [NumPy](https://numpy.org/) – For array operations
* [SciPy](https://www.scipy.org/) – For convolution operations

Install via pip:

```bash
pip install pillow numpy scipy
```

---

## **Project Structure**

```
image_toolkit.py      # Main Python script
data/                 # Folder for input and output images
README.md             # Project documentation
```

---

## **License**

This project is open-source and available under the MIT License.
