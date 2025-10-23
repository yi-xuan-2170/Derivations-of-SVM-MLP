# SVM & MLP分類法 (Homework_1)

> 作者：YiXuan (ChatGPT協助完成.md)
> 日期：2025-10-21  
> 主題：SVM & MLP分類法筆記 (Homework_1)

---

## 一、SVM 的基本概念

SVM（Support Vector Machine）是一種 監督式學習（Supervised Learning） 演算法，主要用於 分類問題（Classification）。
>> SVM 的目標是找到一條分隔線（或超平面）能將資料分成兩類，並且讓兩邊的距離（margin）最大化。



### （1）幾何意義→ 用分隔線區分兩類

嘗試在資料中找出一條能清楚分隔兩個類別的邊界，這樣的邊界稱為「最佳化超平面」

![image](https://charlesliuyx.github.io/2017/09/19/%E6%94%AF%E6%8C%81%E5%90%91%E9%87%8F%E6%9C%BASVM%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0/SVM-margin.jpg)



### （2）最佳化問題→ 讓兩邊的距離（margin）最大化
正樣本決策規則：
存在一個法向量為向量 w，它垂直於分隔線。
任意資料為向量 x 
必滿足 (𝑤 ⋅ 𝑥) + 𝑏 >= 0

![image](https://github.com/yi-xuan-2170/Derivations-of-SVM-MLP/blob/main/%E6%B1%BA%E7%AD%96%E8%A6%8F%E5%89%87.jpg)

圖片截於 https://www.youtube.com/watch?v=_PwhiWxHK8o

- sign函數，f(x)=sign(w ⋅ x + b)

![image](https://upload.wikimedia.org/wikipedia/commons/c/c0/Signum_function.png)

- **正樣本（Positive Sample）**  
  若代入模型後 w ⋅ x + b > 1 ，  
  代表資料點位於「正邊界線」之外。

- **負樣本（Negative Sample）**  
  若代入模型後 w ⋅ x + b < -1 ，  
  代表資料點位於「負邊界線」之外。

- **支撐向量（Support Vectors）**  
而在兩條邊界上的點，決定了**正負邊界的位置，也就是 Support Vectors（支撐向量）**整個分隔面的形狀。
![image](https://github.com/yi-xuan-2170/Derivations-of-SVM-MLP/blob/main/%E6%AD%A3%E8%B2%A0%E9%82%8A%E7%95%8C.jpg)

單位向量的公式是將一個非零向量除以其自身長度，如下所示

![image](https://github.com/yi-xuan-2170/Derivations-of-SVM-MLP/blob/main/%E5%96%AE%E4%BD%8D%E5%90%91%E9%87%8F2.jpg)

圖片截於 https://www.youtube.com/watch?v=_PwhiWxHK8o

我們知道
- 若是 **正類**，則 𝑤 ⋅ 𝑥𝑖 + 𝑏 ≥ 1
- 若是 **負類**，則 𝑤 ⋅ 𝑥𝑖 + 𝑏 ≤ 1
- 所以這兩條不等式可以合併成一條統一的式子：**yi​(w ⋅ xi ​+ b) ≥ 1**

  
### （3）拉格朗日乘數法→ 提煉w→ 帶回最佳化問題
利用拉格朗日乘數法（Lagrange Multiplier）將限制條件帶入，求出最優解，使 margin 最大化。

---

## 二、MLP 基本概念

MLP（Multi-Layer Perceptron）是一種**前饋神經網路**（Feedforward Neural Network），屬於**監督式學習模型**，常用於分類與回歸問題。

特點：
- 含有 **輸入層（Input Layer）**、**隱藏層（Hidden Layer）**、**輸出層（Output Layer）**
- 每層由多個 **神經元（Neuron）** 組成
- 神經元之間透過 **權重（Weight）** 與 **偏差（Bias）** 相連
- 使用 **非線性啟動函數（Activation Function）** 增加模型表現能力

---
