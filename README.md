# end2endOCR


```python
# get image
import cv2
cap=cv2.VideoCapture(0)
i=0
while(1):
    ret ,frame = cap.read()
    k=cv2.waitKey(1)
    if k != -1:
        print(k)
    if k==27:
        break
    elif k==115:
        cv2.imwrite('/home/doujian/Desktop/'+str(i)+'.jpg',frame)
        i+=1
    cv2.imshow("capture", frame)
cap.release()
cv2.destroyAllWindows()
```
