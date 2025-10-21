# 🧩 支持向量機（SVM）學習筆記

> 作者：YiXuan  
> 日期：2025-10-21  
> 主題：SVM 原理與數學推導概要

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

- 可用 **核函數 (Kernel Function)** 將資料映射至高維空間
- 常見核函數：
  - 線性核 (Linear)
  - RBF核 (Gaussian)
  - Polynomial核

---

## 五、心得

我認為 SVM 的關鍵在於理解：
1. **幾何意義**：找最寬的分隔線  
2. **數學推導**：了解拉格朗日乘數法如何導出最優解  
3. **核函數的威力**：可以讓非線性資料變得可分  

SVM 是數學與幾何的完美結合 ❤️

---

_（以上內容由 YiXuan 撰寫，僅作為學習筆記使用）_
