# IPCV_Lab1.
OpenCV documentation 

#IPCV Lab2.
1. Image Negative
Theory
Image negative transformation enhances white or gray details in dark regions. For an
8-bit grayscale image, the transformation is given by:
s = 255 − r

where r is the input pixel value and s is the output pixel value.

2. Contrast Stretching
Theory
Contrast stretching improves image visibility by expanding the range of intensity values.

s =((r − rmin)/(rmax − rmin))× 255
           

3. Bit Plane Slicing
Theory

Bit plane slicing decomposes an image into its binary components, highlighting the im-
portance of each bit in image formation.

4. Gray Level Slicing
Theory
Gray level slicing highlights a specific range of gray levels in an image. It can be performed
with or without suppressing the background.


##IPCV_Lab3

Theory
Histogram equalization is an image enhancement technique that improves image contrast

by redistributing gray level intensities over the entire available range. It uses the cumu-
lative distribution function (CDF) of the image histogram to map old intensity values to

new ones.
The transformation function is given by:
s = (L − 1)Xr
j=0
pr(j)

where L is the number of gray levels and pr(j) is the probability of occurrence of gray
level j.

### Pseudo Code (Python Style)
1. Read the grayscale image into a variable img
2. Initialize an array hist with zeros of size 256
3. for each pixel value p in img:
• Increment hist[p] by 1
4. Normalize hist by dividing each value by total number of pixels
5. Compute cumulative sum of hist to obtain cdf
6. for each gray level i from 0 to 255:
• new value[i] = round(255 * cdf[i])
7. for each pixel p in img:
• Replace p with new value[p]
8. Display the histogram equalized image
