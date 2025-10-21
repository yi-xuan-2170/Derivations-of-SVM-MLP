# ReadME_SVM

> 作者：YiXuan _generateBY GPT 
> 日期：2025-10-21  
> 主題：SVM 原理_基礎 

---

## 一、SVM 的基本概念

SVM（Support Vector Machine）是一種**監督式學習**演算法，主要用於**分類問題**。

它的核心思想是：
> 找出一條能夠最大化類別間距（margin）的超平面。

![](https://upload.wikimedia.org/wikipedia/commons/2/2a/SVM_2D.svg)

---

## 二、數學形式

假設輸入資料為 $x_i$，對應的標籤為 $y_i \in \{-1, +1\}$。

SVM 嘗試找出一個超平面：
$$
w \cdot x + b = 0
$$

使得資料能被正確分類，並同時最大化邊界距離：
$$
\text{maximize } \frac{2}{||w||}
$$

---

## 三、最終目標函數

轉換為一個最佳化問題：
$$
\min_{w,b} \frac{1}{2}||w||^2
$$
subject to:
$$
y_i(w \cdot x_i + b) \geq 1, \forall i
$$

---

## 四、延伸與應用
- 如果資料無法被直線或平面分開，SVM 會使用 Kernel（核函數），把資料投影到更高維空間，使其可以被線性分開。
- 可用 **核函數 (Kernel Function)** 將資料映射至高維空間
- 常見核函數：
  - 線性核 (Linear)
  - RBF核 (Gaussian)
  - Polynomial核

---

_（以上內容由ChatGPT生成， YiXuan 修改，並僅作為學習筆記使用）_
