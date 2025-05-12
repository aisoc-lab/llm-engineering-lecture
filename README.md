# LLM Engineering Lecture (Summer Semester 2025)

<p align="center">
<img src="img/header.png" alt="" width="600"/>
</p>

This repository contains the slides and exercises for the [RUB LLM Engineering course](https://vvz.ruhr-uni-bochum.de/campus/all/event.asp?objgguid=0x5740DDED5FAA4912B946261B9D7330DB&from=vvz&gguid=0x2741E524E0074AFEAAA1211DFC92820A&mode=own&lang=en&tguid=0x465D15D340584F31963F02CDAA33142A).

## Course description
Modern LLMs like ChatGPT and LLaMA show impressive performance in a range of real-world applications. Much of this performance is enabled by scaling up the model sizes. State-of-the-art models consist of hundreds of billions of parameters. This massive scale makes training, finetuning and inference with LLMs much more challenging as compared to traditional deep learning models like CNNs and LSTMs. In this course, you will learn about technical advances that power modern LLMs. You will learn how to operate massive LLMs that do not fit on a single GPU. You will also learn about techniques like caching, quantization, pruning and parameter efficient finetuning that enable efficient fine-tuning and inference. You will also learn how to interact with API-based models like GPT-4 and Claude.

The course will be split into **two blocks**. 
1. The first block will consist of **lectures** where we will introduce you to the content in a classroom setting. 
2. The second block will entirely consist of a **project**.

## Lectures
Every Monday between 08:30 - 12:00 in GD 04/620. Each lecture will be split as follows:
1. 45 min lecture
2. 45 min programming exercise
3. break
4. 45 min lecture
5. 45 min programming exercise

|    Date    |         Title         | 
| ---------- | --------------------- |
| 2025-04-14 | [Introduction](01_intro)      |
| 2025-04-28 | [The Transformer Architecture](02_transformer_architecture) |
| 2025-05-05 | [Efficient Inference: Intro to Quantization](03_efficient_inference_part_1) |
| 2025-05-12 | [Efficient Inference: Deeper Look into Quantization](04_efficient_inference_part_2) |

## Contact
The course is taught by [Zahra Dehghanighobadi](https://informatik.rub.de/aisoc/people/dehghanighobadi/), [Elisabeth Kirsten](https://informatik.rub.de/en/aisoc/people/kirsten/), [Bilal Zafar](https://informatik.rub.de/zafar/) with guest lectures from [Vedant Nanda](https://nvedant07.github.io) and [Felipe Vecchietti](https://lfelipesv.github.io).

In case of questions, please contact bilal.zafar@rub.de.

## Learning Outcomes
1. Ability to finetune and perform inference with SoTA LLMs even with limited resources.
2. Working with LLMs in a local (laptop or PC), compute cloud, and API setting.

## Recommended Prior Knowledge
This advanced course assumes deep familiarity with fundamental concepts of Machine Learning. The participants should have taken one of the following courses at RUB (or another similar course): (i) Machine Learning, (ii) Deep Learning, (iii) Natural Language Processing with Deep Learning, (iv) Machine Learning: Supervised Methods.
Participants should also have prior experience with PyTorch.
