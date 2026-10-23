# Image-Handling-and-Pixel-Transformations-Using-OpenCV

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** Chidroop M J  
- **Register Number:** 212225240029

---

### Ex. No. 01

#### 1. Read the image ('Eagle_in_Flight.jpg') using OpenCV imread() as a grayscale image.
```python
image = cv2.imread('test_image_exer001.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

#### 2. Print the image width, height & Channel.
```python
img_rgb.shape
```

#### 3. Display the image using matplotlib imshow().
```python
plt.imshow(img_rgb, cmap='viridis')  
plt.title("Original Image")
plt.axis('off')  
plt.show()
```

#### 4. Save the image as a PNG file using OpenCV imwrite().
```python
cv2.imwrite('test_image_exer001.png', image)
```

#### 5. Read the saved image above as a color image using cv2.cvtColor().
```python
image = cv2.imread('test_image_exer001.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

#### 6. Display the Colour image using matplotlib imshow() & Print the image width, height & channel.
```python
img_rgb.shape
plt.imshow(img_rgb, cmap='viridis')  
plt.title("Original Image")
plt.axis('off')  
plt.show()
```

#### 7. Crop the image to extract any specific (Eagle alone) object from the image.
```python
rectangle_img = cv2.rectangle(img_rgb, (90, 30), (420, 350), (0, 0, 255), 10)  
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

#### 8. Resize the image up by a factor of 2x.
```python
image = cv2.imread('test_image_exer001.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```

#### 9. Flip the cropped/resized image horizontally.
```python
line_img1 = cv2.line(img_rgb, (0, 0), (530, 567), (255, 0, 0), 10) 
line_img2 = cv2.line(line_img1, (0, 567), (530, 0), (255, 0, 0), 10) 

plt.imshow(line_img2, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

#### 10. Read in the image ('Apollo-11-launch.jpg').
```python
image = cv2.imread('test_image_exer001.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

#### 11. Add the following text to the dark area at the bottom of the image (centered on the image):
```python
text = 'Apollo 11 Saturn V Launch, July 16, 1969'
font_face = cv2.FONT_HERSHEY_PLAIN
text_img = cv2.putText(img_rgb, "Chidroop M J", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 0, 0), 10) 

plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

#### 12. Draw a magenta rectangle that encompasses the launch tower and the rocket.
```python
rect_color = magenta
circle_img = cv2.circle(img_rgb,(255,190),150,(255,0,0),10) 

plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

#### 13. Display the final annotated image.
```python
image = cv2.imread('test_image_exer001.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```

#### 14. Read the image ('Boy.jpg').
```python
image = cv2.imread('test_image_exer001.png') 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```

#### 15. Adjust the brightness of the image.
```python
# Create a matrix of ones (with data type float64)
# matrix_ones = 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```

#### 16. Create brighter and darker images.
```python
img_brighter = cv2.add(img, matrix)
img_darker = cv2.subtract(img, matrix)

image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
```

#### 17. Display the images (Original Image, Darker Image, Brighter Image).
```python
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```

#### 18. Modify the image contrast.
```python
# Create two higher contrast images using the 'scale' option with factors of 1.1 and 1.2 (without overflow fix)
matrix1 = 
matrix2 = 
# img_higher1 = 
# img_higher2 = 
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
```

#### 19. Display the images (Original, Lower Contrast, Higher Contrast).
```python
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```

#### 20. Split the image (boy.jpg) into the B,G,R components & Display the channels.
```python
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

img_rgb.shape
plt.imshow(img_rgb, cmap='viridis')  
plt.title("Original Image")
plt.axis('off')  
plt.show()
```

#### 21. Merged the R, G, B , displays along with the original image
```python
image = cv2.imread('test_image_exer001.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

#### 22. Split the image into the H, S, V components & Display the channels.
```python
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
```

#### 23. Merged the H, S, V, displays along with original image.
```python
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```

## Output:
- **i)** Read and Display an Image.  
- **ii)** Adjust Image Brightness.  
- **iii)** Modify Image Contrast.  
- **iv)** Generate Third Image Using Bitwise Operations.

## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.
