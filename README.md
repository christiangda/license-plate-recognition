# license-plate-recognition
The license-plate-recognition call the OpenVINO pre-trained models with python and the DNN in OpenCV. It comes from the [Security Barrier Camera Demo](https://docs.openvinotoolkit.org/2018_R5/_samples_security_barrier_camera_demo_README.html).This demo showcases Vehicle and License Plate Detection network followed by the Vehicle Attributes Recognition and License Plate Recognition networks applied on top of the detection results
* vehicle-license-plate-detection-barrier-0106, which is a primary detection network to find the vehicles and license plates
* vehicle-attributes-recognition-barrier-0039, which is executed on top of the results from the first network and reports general vehicle attributes, for example, vehicle type (car/van/bus/track) and color
* license-plate-recognition-barrier-0001, which is executed on top of the results from the first network and reports a string per recognized license plate

The license-plate-recognition test in win10 + python3.6 + openvino_2021.1.110 + opencv-contrib-python 4.4.0.44.

# How to run the license-plate-recognition
1. instal OpenVINO.
2. Run the setupvars.bat in C:\Program Files (x86)\Intel\openvino_2021.1.110\bin
3. Run the testOpenVINO.py. The license-plate-recognition will process the images in testImgs one-by-one.
```
C:\Users\username>cd C:\Program Files (x86)\Intel\openvino_2021.1.110\bin
 
C:\Program Files (x86)\Intel\openvino_2021.1.110\bin>setupvars.bat
Python 3.6.5
[setupvars.bat] OpenVINO environment initialized
 
C:\Program Files (x86)\Intel\openvino_2021.1.110\bin>D:
 
D:\>cd D:\Python\OpenVINOMODEL
 
D:\Python\OpenVINOMODEL>python testOpenVINO.py
[E:] [BSL] found 0 ioexpander device
```
![image](https://github.com/livezingy/license-plate-recognition/blob/master/license1.png)

![image](https://github.com/livezingy/license-plate-recognition/blob/master/license2.png)

# About vehicle-attributes-recognition-barrier-0039
The test result of vehicle-attributes-recognition-barrier-0039 is not very accurate, so the result is not displayed in the picture by default. If you want to observe the test results of the model, you could set the bShowColor = True in testOpenVINO.py.

