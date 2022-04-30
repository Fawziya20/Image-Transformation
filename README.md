# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
###
Step1:
Import the necessary libraries and read the original image and save it a image variable.

Step2:
Translate the image using Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))

Step3:
Scale the image using Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]]) Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))

Step4:
Shear the image using Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))

Step5:
Reflection of image can be achieved through the code Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))

Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))

Step7:
Crop the image using cropped_image=org_img[10:350,320:560]

Step8:
Display all the Transformed images.

## Program:
```python
Developed By:A.FAWZIYA
Register Number:212220230017
i)Image Translation
```python
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(original_img,Translation_matrix,(col,row))
plt.axis("off")
plt.imshow(Translated_image)
```


ii) Image Scaling
```python
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(original_img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)
```



iii)Image shearing
```python
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(original_img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image)
```


iv)Image Reflection
```python
Reflection_matrix_col=np.float32([[-1,0,col],[0,1,0],[0,0,1]])
Reflected_image_col=cv2.warpPerspective(original_img,Reflection_matrix_col,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_col)

Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]])
Reflected_image_row=cv2.warpPerspective(original_img,Reflection_matrix_row,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_row)
```



v)Image Rotation
```python
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(original_img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)
```



vi)Image Cropping
cropped_image=original_img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)

```





## Output:
### i)Image Translation

![Untitled8 - Jupyter Notebook - Google Chrome 30-04-2022 23_44_43](https://user-images.githubusercontent.com/75235022/166117531-caee8f61-1ba4-479f-9222-05ce049545b0.png)



### ii) Image Scaling

![Untitled8 - Jupyter Notebook - Google Chrome 30-04-2022 23_45_15](https://user-images.githubusercontent.com/75235022/166117543-d71f5d4f-be42-4d1f-b1da-71d0750fe7ea.png)


### iii)Image shearing
![shearing](https://user-images.githubusercontent.com/75235022/166117576-4c2db390-dd62-466d-b7fd-e44438313275.png)


### iv)Image Reflection

![Untitled8 - Jupyter Notebook - Google Chrome 30-04-2022 23_46_26](https://user-images.githubusercontent.com/75235022/166117591-21992912-07ce-4577-bba2-913784a8804d.png)



### v)Image Rotation
![Untitled8 - Jupyter Notebook - Google Chrome 30-04-2022 23_46_47](https://user-images.githubusercontent.com/75235022/166117608-dd6a4cb0-aca9-443a-9766-8a8688860961.png)



### vi)Image Cropping

![Untitled8 - Jupyter Notebook - Google Chrome 30-04-2022 23_47_12](https://user-images.githubusercontent.com/75235022/166117621-8d55563d-563b-49d2-a658-6e79ea2c11c4.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
