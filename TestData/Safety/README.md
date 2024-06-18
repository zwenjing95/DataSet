# China Unicom Large Language Model safety Dataset



## Introduction

- China Unicom AI Innovation Center releases a large-scale model safety dataset, which is designed based on the standard "Basic security requirements for generative artificial intelligence service" issued by the Chinese government on February 29, 2024. It covers 5 major areas and 31 categories of risk types, as illustrated in the diagram below.
- The safety dataset comprises two types of data: risk content identification and refusal to answer.
- Risk content identification data contains 1,861 multiple-choice questions (the data will continue to increase dynamically). The accuracy of the large model's selection is used to evaluate its ability to perceive and detect risky content.
  - Refusal to answer data includes 462 questions that require a refusal to answer (the data will continue to increase dynamically). The large model's ability to identify risky questions and refuse to answer is assessed based on whether it refuses to respond.
- This dataset is evaluated on 12 mainstream SOTA Chinese large models, assessing their risk identification and refusal to answer capabilities.

![屏幕快照 2024-06-13 下午4.33.35](/Users/zwj/Desktop/屏幕快照 2024-06-13 下午4.33.35.png)

## Evaluation

- **Risk Content Identification**

  The evaluation is conducted directly based on the correctness of the large model's selections. The evaluation metric is ACC (Accuracy).

- **Refusal to Answer**

  The questions and their corresponding large model's response are fed into the Qwen-72B model for automatic assessment. The evaluation metrics are:

  - Rejection Rate (RR-1): Measures the percentage of questions where the model refuses to answer.
  - Responsible Response Rate (RR-2): Evaluates the percentage of answers that are deemed responsible and appropriate.
  - Harm Rate (HR): Calculates the percentage of responses that are considered harmful or inappropriate.

- 

  ![屏幕快照 2024-06-13 下午4.29.40](/Users/zwj/Desktop/屏幕快照 2024-06-13 下午4.29.40.png)



## Results

- Risk Content Identification

  ![屏幕快照 2024-06-13 下午4.34.21](/Users/zwj/Desktop/屏幕快照 2024-06-13 下午4.34.21.png)

- Refuse to Answer

  ![屏幕快照 2024-06-13 下午4.37.39](/Users/zwj/Desktop/屏幕快照 2024-06-13 下午4.37.39.png)

## Citation



```
@misc{zhang2024chisafetybench,
      title={CHiSafetyBench: A Chinese Hierarchical Safety Benchmark for Large Language Models}, 
      author={Wenjing Zhang and Xuejiao Lei and Zhaoxiang Liu and Meijuan An and Bikun Yang and KaiKai Zhao and Kai Wang and Shiguo Lian},
      year={2024},
      eprint={2406.10311},
      archivePrefix={arXiv}
}
```

