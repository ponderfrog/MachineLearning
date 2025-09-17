# 机器学习
## 概念
Machine Learning≈Looking for Function  

Regression: The function outputs a **scalar**.  
Classification: Given options, outpus the **correct one**.

## 步骤
1. 猜测可能的函数形式，设置未知参数
2. 定义损失
3. 最佳化Optimization——Gradient Descent

## 函数形式
$$
y=b+\sum_{i} c_i sigmoid(b_i+\sum_{j} w_{ij} x_j)
$$

### Activation function
- Sigmoid
- Rectified Linear Unit (ReLU)

## General guide
- 检查training data的loss
    - large
        - Model bias
            1. 模型过于简单
            2. 重新设计模型，使之更有弹性
        - Optimization Issue
            1. local minima
        - 如何判断出现了上述的哪种问题?
            1. 通过比较不同模型来确定是上述的哪种问题
            2. 用简单的模型来检查是否可以达到更好的效果
    - small
        - loss on testing data
        - large
            - overfitting
                1. 增加训练资料
                2. 限制模型弹性
            - mismatch
        - small
            - OK

## N-fold cross validation
1. 将训练集分成N份
2. 轮流将其中一份作为测试集
3. 重复N次


## 梯度消失
critical point
gradient is close to **zero**
- local minima
- local maxima
- saddle point

which one?
1. 泰勒公式展开
2. 观察Hessian矩阵（二阶偏微分）的eigen value
3. Hessian矩阵指出了saddle point继续下降的方向
4. 多数时候卡在saddle point
