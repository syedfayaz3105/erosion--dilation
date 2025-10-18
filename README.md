## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step-1:
Create a black image of size 100x600 pixels.

## Step-2:
Use a specified font to write the word "Lifestyle" on the image at a defined position.

## Step-3:
Show the image containing the text without axis labels.

## Step-4:
Define a structuring element for morphological operations (e.g., a cross-shaped kernel).

## Step-5:
Apply erosion to the image using the defined structuring element to reduce the size of white regions.

## Step-6:
Apply dilation to the original image using the same structuring element to increase the size of white regions.

 
## Program:
### DEVELOPED BY : JANARTHANAN K
### REG NO : 212223040072

# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100, 600, 3), dtype='uint8')  # Black background (RGB: 0, 0, 0)
font = cv2.FONT_HERSHEY_COMPLEX
text_color = (255, 255, 255)  # White text (RGB: 255, 255, 255)
cv2.putText(img, 'Farhana_syed', (60, 70), font, 2, text_color, 5, cv2.LINE_AA)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```


# Create the structuring element

```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```

# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```



# Dilate the image

```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
## Output:

### Display the input Image
<br>
<br>

<img width="648" height="141" alt="Screenshot 2025-10-18 110037" src="https://github.com/user-attachments/assets/5c9eae79-edf2-4b57-8038-6c63f20d5bb8" />

<br>
<br>
<br>

### Display the structured elements
<br>
<br>
<img width="336" height="567" alt="Screenshot 2025-10-18 110110" src="https://github.com/user-attachments/assets/0874cbfb-13b5-415f-a806-bfaa9f3eae4f" />


<br>
<br>
<br>


### Display the Eroded Image
<br>
<br>
<img width="806" height="184" alt="Screenshot 2025-10-18 110116" src="https://github.com/user-attachments/assets/7f9aeaa6-f2fb-4cf9-932a-8da54216e746" />


<br>
<br>
<br>

### Display the Dilated Image
<br>
<br>
<img width="733" height="190" alt="Screenshot 2025-10-18 110121" src="https://github.com/user-attachments/assets/15d57f0a-2f25-45f2-b9f4-65233dc437e9" />




<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
