---
layout: post
title: '单纯形法'
date: 2016-12-30
author: Christina
tags: 算法
---

---

我们知道，如果线性规划有有限的最优解，那么该最优解一定可以在可行域的顶点上取到。  

单纯形法便是从初始顶点开始，通过最优性判别准则判断，若不是最优，则转移到新顶点迭代，新顶点的目标值必然优于上一个，直到找到最优值停止迭代。    

可行域的顶点称作基本可行解，下面开始介绍单纯形法的迭代步骤。

---

### 1.化标准型   

* **把不等式约束改成等式约束**    

![](/assets/img/1.png)

**基变量：** x<sub>3</sub> , x<sub>4</sub> , x<sub>5</sub>  <small>→只出现在其中一个方程且系数为1 </small>     
**非基变量：** x<sub>1</sub> , x<sub>2</sub>   
**基本可行解：** X=(x<sub>1</sub>,x<sub>2</sub>,x<sub>3</sub>,x<sub>4</sub>,x<sub>5</sub>)<sup>T</sup><small>→非基变量取值全为0的可行解 </small>            
**初始基本可行解：** X<sup>0</sup>=(0,0,6,12,2)<sup>T</sup> 

---

**非退化**基本可行解：基变量都大于0的基本可行解  
**退化**基本可行解：至少有一个基变量等于0的基本可行解

---

### 2.单纯形表 


![](/assets/img/2.png)


介绍一下该表的各值：    
**c<sub>j</sub>：** x<sub>j</sub> 对应在目标函数中的系数   
**C<sub>B</sub>：** X<sub>B</sub> 对应在目标函数中的系数  
**p<sub>j</sub>：** 为 x<sub>j</sub><sup>T</sup>  
**b：** 为约束方程右边的值


**检验数(λ<sub>j</sub>=c<sub>j</sub>-C<sub>B</sub>p<sub>j</sub>) ：** 对于某个基本可行解，若它的检验数都≤0，它便是最优解  

![](/assets/img/3.png)

**目标值(Z<sub>j</sub>=C<sub>B</sub>b) ：** 单纯形表中填的是目标值的相反数，即加上负号    
     
![](/assets/img/4.png)


**由最优性判别准则（<small>对于某个基本可行解，若它的检验数都≤0，它便是最优解</small>）知道该表不是最优表，于是需要通过变换基本可行解来优化目标值**  


### 3.迭代方法

![](/assets/img/5.png)

* **确定进基变量**   
  
  

 X=(x<sub>1</sub>,x<sub>2</sub>,x<sub>3</sub>,x<sub>4</sub>,x<sub>5</sub>)<sup>T</sup>  
 X<sup>0</sup>=(0,0,6,12,2)<sup>T</sup>→Z<sup>0</sup>=0  
 X<sup>1</sup>=(0,θ,x<sub>3</sub>',x<sub>4</sub>',x<sub>5</sub>')<sup>T</sup>→Z<sup>1</sup>=4θ↑    
<strong>maxZ=3x<sub>1</sub>+4x<sub>2</sub>=3×0+4×θ=4θ </strong> <br>
 X<sup>1</sup>=(θ,0,x<sub>3</sub>'',x<sub>4</sub>'',x<sub>5</sub>'')<sup>T</sup>→Z<sup>1</sup>=3θ↑  
<strong>maxZ=3x<sub>1</sub>+4x<sub>2</sub>=3×θ+4×0=3θ </strong>

 选增大倍数大的，即  
λ<sub>k</sub>=max{λ<sub>j</sub>|λ<sub>j</sub>>0}→x<sub>k</sub>为进基变量  
λ<sub>2</sub>=max{λ<sub>1</sub>,λ<sub>2</sub>>0}→x<sub>2</sub>为进基变量 

* **确定离基变量** 
  

![](/assets/img/6.png)

θ=min{6/2,12/2,2/1}=2→x<sub>5</sub>为离基变量  
    
 x<sub>3</sub>'=6-2θ=2  
 x<sub>4</sub>'=12-2θ=8  
 x<sub>5</sub>'=2-θ=0  
 X<sup>1</sup>=(0,2,2,8,0)<sup>T</sup>→Z<sup>1</sup>=8↑  

 离基变量的确定遵循**最小非负比准则**

 该处p<sub>2</sub>为(2,2,1)<sup>T</sup>均>0，若存在≤0的则考虑非负部分即可  

* **换基运算**  

![](/assets/img/7.png)

![](/assets/img/8.png)

![](/assets/img/9.png)

![](/assets/img/10.png)


**X<sup>1</sup>=(0,2,2,8,0)<sup>T</sup>→Z<sup>1</sup>=8↑**

由最优性判别准则知该表不是最优表，继续迭代，方法如上，以下列出相应迭代后的表格  

![](/assets/img/11.png)

**X<sup>2</sup>=(2,2,0,2,0)<sup>T</sup>→Z<sup>2</sup>=14↑**  

![](/assets/img/12.png)

**X<sup>&lowast;</sup>=(3,3/2,0,0,1/2)<sup>T</sup>→Z<sup>&lowast;</sup>=15↑**

---

* X<sup>0</sup>=(0,0,~~6,12,2~~)<sup>T</sup>→Z<sup>0</sup>=0  
* X<sup>1</sup>=(0,2,~~2,8,0~~)<sup>T</sup>→Z<sup>1</sup>=8↑   
* X<sup>2</sup>=(2,2,~~0,2,0~~)<sup>T</sup>→Z<sup>2</sup>=14↑    
* X<sup>&lowast;</sup>=(3,3/2,~~0,0,1/2~~)<sup>T</sup>→Z<sup>&lowast;</sup>=15↑  
  

 **迭代结束，找到最优解**

