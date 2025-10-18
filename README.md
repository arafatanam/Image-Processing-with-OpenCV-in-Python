# Image Processing with OpenCV in Python

## Project Overview

This project demonstrates fundamental image processing techniques using Python and OpenCV. It covers reading, displaying, manipulating, and saving images. These operations are essential for pre-processing in **Machine Learning (ML)** and **Deep Learning (DL)** tasks, especially for computer vision applications.

---

## Features Implemented

1. **Reading and Displaying Images**

   * Load images in BGR format.
   * Display images in Google Colab using `cv2_imshow()`.
   * Print image type and shape.

2. **Grayscale Conversion**

   * Convert a colored image to grayscale using OpenCV.

3. **RGB Channel Manipulation**

   * Remove individual color channels (Blue, Green, Red) to analyze color contribution.
   * Display all channel-modified images side by side.

4. **Image Resizing**

   * Resize image to a fixed dimension (e.g., 256x256 pixels).
   * Resize image by a percentage of original dimensions (e.g., 50%).

5. **Image Flipping**

   * Flip image vertically, horizontally, or both.

6. **Image Cropping**

   * Crop a specific region from the image.

7. **Saving Images**

   * Save images locally after processing.

8. **Drawing Shapes and Adding Text**

   * Draw rectangles, circles, and lines.
   * Add text annotations with customizable font, color, and thickness.

---

## Code Example

```python
# Read an image
img = cv2.imread('/content/fruits.jpg')
cv2_imshow(img)

# Convert to grayscale
img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
cv2_imshow(img_gray)

# Remove blue channel
img_no_blue = img.copy()
img_no_blue[:, :, 0] = 0
cv2_imshow(img_no_blue)

# Resize image
img_resize = cv2.resize(img, (256, 256))
cv2_imshow(img_resize)

# Draw shapes
cv2.rectangle(img, (100, 100), (300, 300), (255, 0, 0), 2)
cv2.circle(img, (400, 400), 100, (0, 255, 0), 3)
cv2.line(img, (0, 0), (512, 512), (0, 0, 255), 2)
cv2.putText(img, "Hello World", (50, 250), cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 255, 255), 2)
cv2_imshow(img)
```

---

## Prerequisites

* Python 3.x
* OpenCV (`cv2`)
* NumPy
* Pandas (optional, for array manipulations)
* Google Colab (optional, for `cv2_imshow`)

**Install packages using:**

```bash
!pip install opencv-python numpy pandas
```