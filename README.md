# conspiratory-cn


## 介绍
这个简单的Python package旨在帮助识别中文文本中的阴谋论言论。它使用logistics回归模型进行训练，并提供了一个简单的接口，可以用于检测文本中是否包含可能的阴谋论言论。下面是如何使用这个package的详细说明。

## 安装
首先，你需要安装这个Python package。你可以使用pip来安装它：

```
pip install conspira
# 或者
pip install -i https://pypi.org/simple/ conspira
```

## 使用方法

```
# 导入包
from conspira.detector import ConspiracyDetector

# 创建识别器对象
detector = ConspiracyDetector()

# 分析文本，判断是否包含阴谋论言论。例如：
text = "地球是平的，NASA在隐瞒真相！"
detector.predict(text)
# Output: {'label': array([1]), 'proba': array([[0.27879017, 0.72120983]])}
