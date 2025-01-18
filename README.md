# Armor_recognition
 QDU未来战队大一上学期视觉组作业，完成于24.11，整理于25.1。

整体思路为：将图像通道相减，寻找其中面积较大的轮廓作为灯条，若寻找到的灯条为偶数，则视为存在能识别的装甲板，将灯条中的装甲板裁切后传入已训练好的模型进行预测。

后期可能会加入通过灯条角度对齐判断装甲板、更多的可识别编号、装甲板的角度拟合等。

Armor文件包含：

​	CMakeLists.txt：cmake文件

​	dataset：装甲板编号数据集，内含test(测试集)、train(训练集)、valid(预测集)

​	digit.onnx：用于识别编号的onnx模型

​	digit.pth：用于识别编号的pth模型

​	recognize.cpp：代码主体，用于定位并识别装甲板

​	train.py：训练模型

​	output.py：导出模型为onnx

