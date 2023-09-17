# RAG Solution

## Introduction

We've developed a powerful Retrieval Augmented Generation (RAG) solution to address challenges related to product reviews. This innovative approach combines Advanced Information Retrieval and Natural Language Generation to answer questions regarding the characteristics of the product, set by the end user.

All the user has to do is ask anything they are interested in learning about the product, in any supported language. Our solution will first translate the question to English, filter through the reviews, retrieve those that closely align with the context and meaning of users' questions (ensuring relevance and reliability), and output an answer extracted from the information presented in the subset. Finally, the answer will be translated back to the original language.

We made use of the open-source LLM framework **Haystack**. Haystack provides a simple yet powerful way to combine different deep learning models seamlessly.

## Usage

To use our RAG solution, follow these steps:

1. Clone this repository.
2. Install the required dependencies.
3. Set up a vector database (e.g., Pinecone) for the retrieval step.
4. Initialize the pipeline, which includes translation, retrieval, summarization, and gpt 3.5 for answer generation.
5. Ask questions about the product, and the solution will provide answers.

For more detailed instructions, refer to the code in the `retrieval_augmented_generation.ipynb` file.

## Files and Architecture

- **retrieval_augmented_generation.ipynb**: This notebook contains the code related to the RAG solution. It explains the pipeline, including translation, retrieval, summarization, and answer generation.

- **fine_tuning_summarizer.ipynb**: This notebook was used to fine-tune the summarization model based on *facebook/bart-large-cnn*. The fine-tuned model, **ThanosAng/Product_Review_Summary**, is available on Hugging Face. You can extract the weights using the provided code.

- **create_summaries_openai.ipynb**: This notebook was used to create target summaries with the use of gpt 3.5 for fine-tuning the summarization model.

## Additional Resources

- [Haystack Framework](https://github.com/deepset-ai/haystack): Link to the Haystack framework repository.
- [Pinecone](https://pinecone.io/): Link to Pinecone, the vector database used in our solution.
- [Fine-Tuned Model on Hugging Face](https://huggingface.co/ThanosAng/Product_Review_Summary): Link to the fine-tuned summarization model on Hugging Face.

This README.md provides an overview of our RAG solution. For more details and usage instructions, please refer to the associated notebooks and resources.


