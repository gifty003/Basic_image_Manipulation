### Basic_image_Manipulation

## 1
### Read the image ('Rocke.jpg')using OpenCV imread() as a grayscale image.
### Print the image width and height.
### Display the image using matplotlib imshow().
### Save the image as a PNG file using OpenCV imwrite().

## Code:
```
import cv2
import matplotlib.pyplot as plt

# Read the image ('Apollo-11-launch.jpg') using OpenCV imread() as a grayscale image.
image = cv2.imread('Apollo-11-launch.jpg', cv2.IMREAD_GRAYSCALE)

# Print the image width and height.
height, width = image.shape
print("Width:", width)
print("Height:", height)

# Display the image using matplotlib imshow().
plt.figure(figsize=[10, 10])
plt.imshow(image, cmap='gray')
plt.axis('off')
plt.show()

# Save the image as a PNG file using OpenCV imwrite().
cv2.imwrite('Apollo-11-launch.png', image)
```

### Output:
![Screenshot 2024-10-29 115314](https://github.com/user-attachments/assets/7d5a3448-8788-40c1-ae56-f6f7f1837f8b)

## 2

### Load and Display the Image
### Crop the Image
### Resize the Cropped Image
### Flip and Display the Final Image

## Code:
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('New_Zealand_Boat.jpeg', cv2.IMREAD_COLOR)
plt.figure(figsize=[3, 3])
plt.imshow(img[:, :, ::-1])  
plt.show()

cropped_img = img[200:300, 300:450]

resized_img = cv2.resize(cropped_img, (0, 0), fx=2, fy=2)

flipped_img = cv2.flip(resized_img, 1)


plt.figure(figsize=[5, 5])
plt.imshow(flipped_img[:, :, ::-1])  
plt.show()
```

## Output:
![Screenshot 2024-10-29 115951](https://github.com/user-attachments/assets/ee95baed-e8eb-4b1c-accb-b05d50be9aba)
![Screenshot 2024-10-29 120023](https://github.com/user-attachments/assets/f0234a0c-5cc7-4ad4-9790-1f9653e28d28)

## 3

### Load and Display the Original Image
### Define Rectangle Parameters
### Draw the Rectangle
### Display the Modified Image

## Code:
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("Rocke.jpg")
fig, ax = plt.subplots()
ax.imshow(image)
ax.set_xticks(range(0, image.shape[1], 100))
ax.set_yticks(range(0, image.shape[0], 100))
plt.show()
image = cv2.imread("Rocke.jpg")
x, y = 500, 50
width = 200
height = 600
cv2.rectangle(image, (x, y), (x + width, y + height), (0, 0, 255), 3)
fig, ax = plt.subplots()
ax.imshow(image)
ax.set_xticks(range(0, image.shape[1], 100))
ax.set_yticks(range(0, image.shape[0], 100))
plt.show()
```

## Output:
![Screenshot 2024-10-29 120355](https://github.com/user-attachments/assets/9f65c481-2065-41cf-92e3-ea0e83dacef4)

## 4

### Load the Color Image
### Convert to Grayscale
### Set Up the Display
### Show the Image

## Code:
```
import cv2
import matplotlib.pyplot as plt

image = cv2.imread('lake.jpg', cv2.IMREAD_COLOR)

print("Color image shape:", image.shape)

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

print("Grayscale image shape:", gray_image.shape)

plt.figure(figsize=[10, 10])
plt.imshow(gray_image, cmap='gray')  
plt.show()
```

## Output:
![Screenshot 2024-10-29 120633](https://github.com/user-attachments/assets/df12db35-7ce2-44b1-bd01-163ee78c143d)
