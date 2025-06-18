# Survey Analysis

## Research Topics

### T1. Interpretability-Aware Feature Selection  
### T1. 注重可解释性的特征选择

Although we must acknowledge that business-experienced data scientists can accurately identify important features in an intuitive way, this subjective selection method lacks **decomposability**, meaning it does not admit intuitive simulation here, which directly threatens the **interpretability** of the ML system [1].  
尽管我们必须承认，具有业务经验的数据科学家能够以直觉的方式准确识别重要特征，但这种主观的特征选择方法缺乏**可分解性**，即无法进行直观的模拟，这直接威胁了机器学习系统的**可解释性** [1]。

On the other hand, this experience-based behavior is not friendly enough for **novice data scientists** who are not yet familiar with the business.  
另一方面，这种基于经验的做法对尚不熟悉业务的**初级数据科学家**并不友好。

Therefore, making **FD reasonably interpretable** is one of the main tasks.  
因此，使**特征离散化（FD）具有合理的可解释性**是主要任务之一。

---

### T2. Identifying Nonlinearity and Adjusting Discretization Scheme Interactively  
### T2. 识别非线性并交互式调整离散化方案

The reason why **RDS** and **LTD** will cause disorders is that the **randomness of sample labels** will override the intrinsic pattern when the sample size is insufficient.  
**RDS** 和 **LTD** 导致紊乱的原因在于，当样本数量不足时，**样本标签的随机性**会掩盖其内在模式。

This randomness not only directly affects our observation but also the effect of **supervised discretization methods** [2].  
这种随机性不仅会直接影响我们的观察结果，还会影响**有监督的离散化方法**的效果 [2]。

Data scientists need an **efficient view** that reflects the intrinsic **nonlinear patterns** in the data while suggesting that disorders are due to **insufficient sample size**.  
数据科学家需要一种**高效的视图**，既能反映数据中的**非线性内在模式**，又能提示紊乱是由**样本数量不足**引起的。

At the same time, data scientists need to be able to **interfere directly** with the discretization scheme, because sometimes **prior knowledge from experts** is vital for the ML system.  
同时，数据科学家需要能够**直接干预**离散化方案，因为有时候**专家的先验知识**对于机器学习系统至关重要。

---

### T3. Building, Comparing, and Managing LR Instances Agilely  
### T3. 灵活地构建、比较和管理逻辑回归（LR）实例

The complexity of **TFD** leads directly to the fact that data scientists must try several times before they find the **optimal discretization scheme**.  
**特征离散化（TFD）**的复杂性意味着，数据科学家必须尝试多次才能找到**最优的离散化方案**。

This means data scientists inevitably **iterate** the process of instance building, comparison, and callback.  
这意味着数据科学家不可避免地要**反复构建、比较和回调**多个模型实例。

Such workload is almost **unbearable** when adjustments are timed by tens.  
当调整次数达到几十次时，这种工作量几乎是**无法承受的**。

Therefore, data scientists are in dire need of a system that can:  
因此，数据科学家迫切需要一个系统，能够：

- Empower them to **build LR instances agilely**  
  支持他们**灵活地构建LR实例**
- **Clearly demonstrate** the variation in performance of instances based on different discretization schemes  
  **清晰地展示**基于不同离散化方案的性能变化
- **Structurally express** the lineage between them  
  **结构化地表达**这些实例之间的演化关系

## Appendix 

### Literatures 

[1] Zachary C. Lipton, *The Mythos of Model Interpretability: In machine learning, the concept of interpretability is both important and slippery*, Queue, vol. 16, no. 3, pp. 31–57, May–June, 2018.

[2] James Dougherty, Ron Kohavi, and Mehran Sahami, *Supervised and Unsupervised Discretization of Continuous Features*, in *Proceedings of the Twelfth International Conference on Machine Learning*, 1995, pp. 194–202.
