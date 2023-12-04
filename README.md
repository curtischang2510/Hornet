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

### Future additions 
1. Create a default dictionary of HSV values for common and primary colours so users can quickly accesss
