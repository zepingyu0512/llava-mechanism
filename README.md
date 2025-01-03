# Understanding Multimodal LLMs: the Mechanistic Interpretability of Llava in Visual Question Answering 

## Introduction

This repo is for the arxiv preprint: [Understanding Multimodal LLMs: the Mechanistic Interpretability of Llava in Visual Question Answering](https://arxiv.org/pdf/2411.10950) 

This work explores the mechanism of Llava in visual question answering. The overall mechanism is an ICL mechanism similar to TextualQA. 

This work uses the techniques and insights in:

[EMNLP 2024: Neuron-Level Knowledge Attribution in Large Language Models](https://zepingyu0512.github.io/neuron-attribution.github.io/)

[EMNLP 2024: How do Large Language Models Learn In-Context? Query and Key Matrices of In-Context Heads are Two Towers for Metric Learning](https://zepingyu0512.github.io/in-context-mechanism.github.io/)

[EMNLP 2024: Interpreting Arithmetic Mechanism in Large Language Models through Comparative Neuron Analysis](https://zepingyu0512.github.io/arithmetic-mechanism.github.io/)

## Running code

You can have a look at the example in Llava_visualize_code.ipynb without running the code.

Environment versions: please see **environment.yml**. The llava model is downloaded at: https://huggingface.co/llava-hf/llava-1.5-7b-hf

First, please use modeling_llava.py and modeling_llama.py to replace the original file in the transformers path, which is usually in anaconda3/envs/YOUR_ENV_NAME/lib/python3.8/site-packages/transformers/models/llava and anaconda3/envs/YOUR_ENV_NAME/lib/python3.8/site-packages/transformers/models/llama. These modified files are useful for extracting the internal vectors during inference time. **Please remember to save the original file.** 

Then run Llava_visualize_code.ipynb to visualize the important image patches for the generations in Llava. Please use similar patterns to fit Llava: USER: <image>\nWhat is the color of the dog?\nASSISTANT: The color of the dog is

And you can also try using other images and questions; this work is not limited to animals and colors.

## cite us: 

```
@article{yu2024understanding,
  title={Understanding Multimodal LLMs: the Mechanistic Interpretability of Llava in Visual Question Answering},
  author={Yu, Zeping and Ananiadou, Sophia},
  journal={arXiv preprint arXiv:2411.10950},
  year={2024}
}
```
