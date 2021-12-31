## Image To Pencil Art
![Open in Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)
![python](https://img.shields.io/badge/Python-0078D4?style=flat-square&logo=python&logoColor=white)
![streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![opencv](https://img.shields.io/badge/OpenCV-27338e?style=flat-square&logo=OpenCV&logoColor=white)
![sublime text](https://img.shields.io/badge/sublime_text-%23575757.svg?style=flat-square&logo=sublime-text&logoColor=important)
![terminal](https://img.shields.io/badge/Windows%20Terminal-4D4D4D?style=flat-square&logo=Windows%20terminal&logoColor=white)

- We need to read the image in RBG format `np.array(our_image.convert("RGB"))` 
- Then convert it to a grayscale image using `cv2.cvtColor(image, cv2.COLOR_RGB2GRAY)`. 
- Then invert the grayscale image using `cv2.bitwise_not()` method. 
- Then blur the inverted image using `cv2.GaussianBlur()` method and invert the blurred image using `cv2.bitwise_not()` method.
- To Pencil drawing image can be done by dividing the grayscale image by the inverted blurry image. 
- Since images are just arrays, we can easily do this programmatically using the `cv2.divide()` function from the `cv2` library in Python.

### Installation
To install all necessary requirement packages for the app 👇
```
pip install -r requirements.txt
```

### Image To Pencil Art Function
```python
def sketch(our_image):
    image = np.array(our_image.convert("RGB"))
    grey_img = cv2.cvtColor(image, cv2.COLOR_RGB2GRAY) 
    invert = cv2.bitwise_not(grey_img)
    blur = cv2.GaussianBlur(invert, (21, 21), 0)
    invertedblur = cv2.bitwise_not(blur)
    return cv2.divide(grey_img, invertedblur, scale=256.0)
```

#### Original Image:
![original image](https://github.com/PrakashAnalyst/LGMVIP-DataScience/blob/main/Task%202/images/Vijay.jpg)

#### Pencil Drawing Image: 
![output image](https://github.com/PrakashAnalyst/LGMVIP-DataScience/blob/main/Task%202/images/Vijay-Pencil-Drawing.jpeg)

#### App Demo: 
![app demo gif](https://github.com/PrakashAnalyst/LGMVIP-DataScience/blob/main/Task%202/images/demo.gif)
