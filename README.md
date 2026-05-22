# medical-llm-tools

## Evidence RAG

This set of notebooks was created in [Google Colab](https://colab.research.google.com) and shows the development of a basic medical chatbot that can be used by clinicians to answer clinical questions. Each question stands alone, and the chatbot (so far) does not retain a memory of earlier questions and answers. Note that this tool is only for demonstration purposes and is **not intended for clinical use**.

[Evidence_RAG_v1.ipynb](https://github.com/timk11/medical-llm-tools/blob/main/Evidence_RAG_v1.ipynb) demonstrates the use of Retrieval-Augmented Generation (RAG) to answer medical questions drawing from a specified selection of freely-available clinical guidelines and review journals as well as [Cochrane](https://www.cochrane.org/) reviews. Three different free LLM models from [Hugging Face](https://huggingface.co/) are compared for producing the final output.

[Evidence_RAG_v1_testing_and_tuning.ipynb](https://github.com/timk11/medical-llm-tools/blob/main/Evidence_RAG_v1_testing_and_tuning.ipynb) shows strategies for testing the chatbot using [RAGAS](https://docs.ragas.io/en/stable/) and for fine-tuning both the embedding model and the generator (inference) model.

[Evidence_RAG_v2.ipynb](https://github.com/timk11/medical-llm-tools/blob/main/Evidence_RAG_v2.ipynb) uses Gemini 3.1 Flash Lite as the inference model. This model is available through the [Gemini API](https://ai.google.dev/gemini-api/docs/models) and allows for a limited amount of use in the free tier. At this stage of development a substantial improvement is seen in the quality of answers.

[Evidence_RAG_v3.ipynb](https://github.com/timk11/medical-llm-tools/blob/main/Evidence_RAG_v3.ipynb) uses the same models as v2 for embedding and inference, but includes the use of [LangChain](https://www.langchain.com/) for building the embeddings and running the inference, and [Chroma](https://www.langchain.com/blog/langchain-chroma) as a retrievable vector database. It also uses paragraph-aware chunking to improve the quality of retrieved chunks.
