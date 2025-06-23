# 访谈提纲 1：非技术背景的业务人员版 | Interview Guide 2: For Non-Technical Business Staff
（研究背景：了解业务层面对模型可解释性的需求与担忧 | Research Background: Understanding the business perspective on model interpretability needs and concerns）

## Part A. 破冰和背景 | Part A. Warm-up and Background
1. 请您简单介绍一下自己目前的业务岗位和职责？  
   Could you briefly introduce your current role and responsibilities?

2. 在日常工作中，您有接触到基于机器学习或数据分析的工具或流程吗？可以简单说说？  
   In your daily work, do you use machine learning or data analysis tools or processes? Could you briefly describe them?

## Part B. 模型在业务中的使用与可解释性 | Part B. Model Usage and Interpretability in Business

### B1. 模型的作用认知 | B1. Understanding the Role of Models
3. 在您的业务中，机器学习模型通常是用来做什么的？能举个例子吗？  
   In your business, what are machine learning models usually used for? Could you give an example?

4. 您觉得一个好的机器学习模型在业务上最重要的是什么？  
   What do you think is the most important aspect of a good machine learning model for your business?

### B2. 可解释性对业务的意义 | B2. The Importance of Interpretability
5. 当模型给出一个预测结果（比如用户是否点击广告），您希望能知道模型是怎么做出这个判断的吗？  
   When a model gives a prediction (e.g., whether a user will click on an ad), do you want to know how the model made that decision?

6. 您觉得模型的可解释性（就是“能说得清楚为什么给出这个结果”）对您的工作重要吗？为什么？  
   Do you think model interpretability (being able to explain the decision) is important for your work? Why?  
   - 您是否曾经因为模型太复杂而对它的结果感到疑惑或不信任？  
     Have you ever felt uncertain or mistrustful of model results because they were too complex?  
   - 如果模型结果可解释，您觉得能更好地支持哪些业务上的决策？  
     If the model results were explainable, what business decisions do you think it would better support?

### B3. 业务风险和透明性需求 | B3. Business Risks and Transparency Needs
7. 在您看来，模型预测结果可能会对哪些决策产生直接影响？  
   In your view, what decisions might be directly impacted by model predictions?

8. 您觉得在一些敏感领域（比如招聘、贷款、健康等），模型可解释性是否更加重要？  
   Do you think interpretability is even more important in sensitive areas (e.g., hiring, loans, healthcare)?  
   - 如果一个模型是“黑箱”的，您觉得对客户或内部沟通有影响吗？  
     If a model is a “black box,” do you think it impacts customer or internal communication?  
   - 您在工作中是否有遇到需要对客户或同事解释模型结果的情况？  
     Have you ever needed to explain model results to customers or colleagues in your work?

### B4. 可解释模型 vs. 性能模型 | B4. Interpretability vs. Performance
9. 在很多时候，模型的可解释性和预测的准确性可能会有权衡。比如可解释的模型（LR） vs. 性能好的复杂模型（DNN）。您倾向于更信任哪种？  
   Sometimes there’s a trade-off between interpretability and accuracy. For example, interpretable models (like LR) vs. high-performing complex models (like DNN). Which do you tend to trust more?

10. 如果让您在可解释性和性能之间平衡，您觉得哪个在您的业务里更优先？  
    If you had to balance interpretability and performance, which do you think should be prioritized in your business?

## Part C. 期待与建议 | Part C. Expectations and Suggestions
11. 如果您可以自定义一个用于业务的数据分析/预测工具，您最希望它在“可解释性”上做得如何？  
    If you could design a data analysis/prediction tool for your business, what would you want it to offer in terms of interpretability?

12. 您觉得让模型更容易被业务理解，还有什么能帮到您？  
    What else do you think could help make models easier to understand for the business side?



# 访谈提纲 2：数据科学家版 | Interview Guide 1: For Data Scientists
（研究背景：针对TFD（特征离散化）过程中可解释性、非线性识别与工作流复杂度问题 | Research Background: Focusing on interpretability, nonlinearity detection, and workflow complexity in the TFD process）

## Part A. 建立关系与背景了解 | Part A. Rapport Building and Background
1. 请简单介绍你目前在数据科学项目中的角色和工作内容？  
   Could you briefly introduce your current role and tasks in data science projects?

2. 你在日常工作中涉及特征离散化的频率大概是多少？  
   How frequently do you work on feature discretization in your daily tasks?

## Part B. 聚焦三大任务（引导性问题 + 深入追问） | Part B. Focus on Three Main Tasks (Guiding + Probing Questions)

### T1. Interpretability-Aware Feature Selection
3. 你是如何选择离散化特征的？在这个过程中你通常依赖哪些信息或经验？  
   How do you typically select features for discretization? What information or experience do you rely on?

4. 在实际操作中，你是否曾遇到过“无法解释为什么选择某个特征”的情况？  
   Have you ever experienced situations where you couldn’t explain why you selected a certain feature?  
   - 对于刚入门的同事或新人，你觉得这个流程是否清晰？  
     Do you think this process is clear for newcomers or junior data scientists?  
   - 在选择特征时，有没有什么信息是你希望系统能自动辅助展示的？  
     Is there any information you wish the system could help visualize automatically during feature selection?

### T2. Identifying Nonlinearity & Interactive Discretization
5. 你在判断特征与目标变量的关系时，如何识别潜在的非线性？  
   How do you identify potential nonlinear relationships between features and target variables?

6. 你是否曾在样本量不足时遇到“正负率紊乱”的情况？那是怎么判断出来的？  
   Have you encountered “positive/negative rate disorder” due to insufficient samples? How did you identify it?  
   - 你期望通过怎样的可视化来判断这种情况是否是由样本不足引起的？  
     What kind of visualization would help you determine whether this is caused by small sample sizes?  
   - 当你需要根据领域知识手动调整离散区间时，你希望系统提供什么样的交互能力？  
     When you need to manually adjust discretization bins based on domain knowledge, what kind of interactive capability do you expect?

### T3. Building, Comparing and Managing LR Instances
7. 你通常会尝试多少种不同的离散化方案？你是如何管理和比较这些模型的？  
   How many different discretization schemes do you usually try? How do you manage and compare these models?

8. 在多个版本之间进行回退或比较时，有遇到过混乱或低效的体验吗？  
   Have you experienced confusion or inefficiency when switching or comparing multiple versions?  
   - 你希望看到什么样的对比视图或结构来帮助你梳理多个模型之间的关系？  
     What kind of comparative views or structures would help you clarify the relationships between models?  
   - 如果能让你快速切换不同模型结果并追溯来源，你认为最重要的功能是什么？  
     If you could quickly switch between model results and trace their origins, what would be the most important features for you?

## Part C. 收尾与扩展 | Part C. Wrap-up and Reflection
9. 如果你能自定义一个用于处理特征离散化的系统，你最希望它具备哪些功能？  
   If you could design a system for feature discretization, what features would you most want it to have?

10. 你觉得目前最大的工作痛点是哪些部分？希望通过工具得到什么改善？  
    What are the biggest pain points in your current work? What improvements would you like to see in tools?

