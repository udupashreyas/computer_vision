import numpy as np
import cv2

img = cv2.imread('C:\Users\udupa\Desktop\Image Processing\sample.jpg')
gray = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)

#cv2.imshow('letters',gray)

cells = [np.hsplit(row,136) for row in np.vsplit(gray,291)]

x = np.array(cells)

r = []
c = []

for i in range(136):
    for j in range(291):
        for k in range(3):
            if 0 in x[j,i,k] and 255 in x[j,i,k]:
                r.append(i)
                c.append(j)

a1 = max(r) * 10
b1 = max(c) * 3
a0 = min(r) * 10
b0 = min(c) * 3

#print a0,b0,a1,b1

cv2.rectangle(gray,(a0-5,b0-5),(a1+5,b1+5),(0,0,255),1)
cv2.imshow('border',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
