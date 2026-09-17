# Tool Use in Large Language Model Agents — Curated Reading List

Topic: **Tool use in LLM agents** — function calling, tool selection, and tool learning. A short, curated set of core papers to align the team before our next sync.

---

## 1. Toolformer: Language Models Can Teach Themselves to Use Tools

- **arXiv ID:** 2302.04761
- **Authors:** Timo Schick, Jane Dwivedi-Yu, Roberto Dessì, Roberta Raileanu, Maria Lomeli, Luke Zettlemoyer, Nicola Cancedda, Thomas Scialom (Meta AI Research; Universitat Pompeu Fabra)
- **Takeaway:** Toolformer shows that a language model can teach itself when and how to call external APIs in a self-supervised way — sampling candidate API calls and keeping only those that actually help predict future tokens. A 6.7B GPT-J-based model fine-tuned this way gains large zero-shot improvements on arithmetic, QA, and translation tasks while keeping its core language abilities, rivaling much larger models.
- **Code / Project Page:** Project page (Meta AI Research): https://ai.meta.com/research/publications/toolformer-language-models-can-teach-themselves-to-use-tools/ — note: Meta did not release official code; a widely used third-party open-source implementation exists at https://github.com/conceptofmind/toolformer

---

## 2. Gorilla: Large Language Model Connected with Massive APIs

- **arXiv ID:** 2305.15334
- **Authors:** Shishir G. Patil, Tianjun Zhang, Xin Wang, Joseph E. Gonzalez (UC Berkeley)
- **Takeaway:** Gorilla is a fine-tuned LLaMA model that outperforms GPT-4 at writing API calls, addressing two key failure modes of LLM tool use: generating wrong input arguments and hallucinating API usage. Pairing the model with a document retriever lets it adapt to changed or versioned API documentation at test time and substantially reduces hallucination; the paper also introduces the APIBench evaluation set covering HuggingFace, TorchHub, and TensorHub APIs.
- **Code / Project Page:** Project page: https://gorilla.cs.berkeley.edu/ | GitHub: https://github.com/ShishirPatil/gorilla

---

## 3. ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs

- **arXiv ID:** 2307.16789
- **Authors:** Yujia Qin, Shihao Liang, Yining Ye, Kunlun Zhu, Lan Yan, Yaxi Lu, Yankai Lin, Xin Cong, Xiangru Tang, Bill Qian, Sihan Zhao, Lauren Hong, Runchu Tian, Ruobing Xie, Jie Zhou, Mark Gerstein, Dahai Li, Zhiyuan Liu, Maosong Sun
- **Takeaway:** ToolLLM is an end-to-end tool-use framework spanning data construction, model training, and evaluation, built on ToolBench — an instruction-tuning dataset of 16,464 real-world RESTful APIs with automatically generated single- and multi-tool instructions. Using a depth-first search-based decision tree for solution-path annotation plus a neural API retriever, the fine-tuned ToolLLaMA executes complex multi-step instructions and generalizes to unseen APIs, approaching ChatGPT-level tool-use performance.
- **Code / Project Page:** GitHub: https://github.com/OpenBMB/ToolBench | Project page: https://openbmb.github.io/ToolBench/

---

*Reading list compiled for team sharing. All takeaways are based on the papers' abstracts.*
