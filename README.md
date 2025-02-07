# Pipeline Analysis for Developing Instruct LLMs in Low-Resource Languages: A Case Study on Basque
Large language models (LLMs) are typically optimized for resource-rich languages like English, exacerbating the gap between high-resource and underrepresented languages. This work presents a detailed analysis of strategies for developing a model capable of following instructions in a low-resource language, specifically Basque, by focusing on three key stages: pre-training, instruction tuning, and alignment with human preferences. Our findings demonstrate that continual pre-training with a high-quality Basque corpus of around 600 million words improves natural language understanding (NLU) of the foundational model by over 12 points. Moreover, instruction tuning and human preference alignment using automatically translated datasets proved highly effective, resulting in a 24-point improvement in instruction-following performance. The resulting models, Llama-eus-8B and Llama-eus-8B-instruct, establish a new state-of-the-art for Basque in the sub-10B parameter category.

- 📄 Paper [Pipeline Analysis for Developing Instruct LLMs in Low-Resource Languages: A Case Study on Basque](https://arxiv.org/abs/2412.13922)
- **Llama-eus-8B** model available in the 🤗HuggingFace Hub [orai-nlp/Llama-eus](https://huggingface.co/collections/orai-nlp/llama-eus-66e2a8cc26ea157c05cfa216)

# New Benchmarks for Basque

To evaluate our model, we created Basque versions of well-established English benchmarks by manually translating a selected subset of these datasets. This approach enabled us to rigorously assess Llama-eus-8B's performance in Basque and directly compare it with its performance in English, providing a comprehensive evaluation of the model's multilingual capabilities.

- [**ARC_HT_eu_sample**](https://huggingface.co/datasets/orai-nlp/ARC_HT_eu_sample) [25-shot]: A subset of 250 samples manually translated to Basque from the ARC dataset (Clark et al., 2018). The corresponding 250 English samples are also provided. The ARC dataset consists of genuine grade-school level, multiple-choice science questions, assembled to encourage research in advanced question-answering.

- [**Winogrande_HT_eu_sample**](https://huggingface.co/datasets/orai-nlp/Winogrande_HT_eu_sample) [5-shot]: A subset of 250 samples manually translated to Basque from the WinoGrande dataset (Sakaguchi et al., 2019). The corresponding 250 English samples are also provided. The Winogrande dataset is a collection of 44k problems, inspired by Winograd Schema Challenge, but adjusted to improve the scale and robustness against the dataset-specific bias. Formulated as a fill-in-a-blank task with binary options, the goal is to choose the right option for a given sentence which requires commonsense reasoning.

- [**MMLU_HT_eu_sample**](https://huggingface.co/datasets/orai-nlp/MMLU_HT_eu_sample) [5-shot]: A subset of 270 samples manually translated to Basque from the MMLU dataset (Hendrycks et al., 2020). The corresponding 250 English samples are also provided. The MMLU dataset is a massive multitask test consisting of multiple-choice questions from various branches of knowledge. The test spans subjects in the humanities, social sciences, hard sciences, and other areas that are important for some people to learn.

- [**HellaSwag_HT_eu_sample**](https://huggingface.co/datasets/orai-nlp/HellaSwag_HT_eu_sample) [10-shot]: A subset of 250 samples manually translated to Basque from the HellaSwag dataset (Zellers et al., 2019). The corresponding 250 English samples are also provided. The HellaSwag dataset is a dataset for commonsense NLI.


# Acknowledgements

This work is part of the BasqueLLM project, titled "First steps towards an artificial intelligence in Basque based on LLMs" (EXP: 2023-CIEN-000081-01), partially funded by the Guipuzcoa Science, Technology and Innovation Network Pro-
gram of the Provincial Council of Gipuzkoa. Model training and development were conducted using the Hyperion system at the Donostia International Physics Center (DIPC).

# Citation

If you use Llama-eus-8B please cite the following reference:

```bibtex
@misc{corral2024pipeline,
      title={Pipeline Analysis for Developing Instruct LLMs in Low-Resource Languages: A Case Study on Basque}, 
      author={Ander Corral and Ixak Sarasua and Xabier Saralegi},
      year={2024},
      eprint={2412.13922},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2412.13922}, 
}
```
