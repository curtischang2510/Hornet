# Hornet

## Getting Started 
Goal: The basic premise of the programme is to take in an image and draw bounding box and identify shapes of a certain colour within that image

### Disclaimer
As of 2/11/23 HSV values need to be changed whenever user wants to detect a certain colour. The HSV values in the pushed code are used to detect the orange ball in the photo "soccerballs.png" 

### ULAP.py
Most of the code was taken from https://github.com/wangyanckxx/Single-Underwater-Image-Enhancement-and-Color-Restoration/blob/master/README.md 

Just added some code to make using the processing techniques more straightforward 

To use this for image pre-processing just use the following steps: 
1. Clone/Copy the file
2. Import the `ULAP_enhance` function
3. This function takes in an image and returns its enhance version
`
img = cv2.imread("image path")
result = ULAP_Enhance(img)
`

### gate_detection.py
The gate in SAUVC alternates between black and green/blue. When using normal color detection your mask will (should) have distinct portions highlighting the green parts. The loop draws a bounding box over each portion and takes the top right corner and bottom by considering all the bounding boxes. Finally it draws a bounding box using the 2 points. 

This means that the effectiveness of this script depends on how accurate aret he HSV values are so some tweaking will need to be done after pool test.

### Future additions 
1. Create a default dictionary of HSV values for common and primary colours so users can quickly accesss
