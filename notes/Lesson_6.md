# Multimodal Recommender System

## Search vs Recommendation

- Search is objective
  - No personalization required
- Recommendation is subjective
  - Personalization is required

## Multimodal Recommendation

- The various modalities are
  - Text description of the product
  - Product image
  - Nutritional info of the food product

## Notebook

- [Jupyter Notebook](../code/L6_Multimodal_Recommender.ipynb)
- Steps
  - #1: Load and embed multi-modal movie data with two separate ML models.
  - #2: Run text and multi-modal queries, in different vector spaces.
- KA: Executed the following command to zip the posters on the course notebook to avoid downloading each posters individually
  
  ```Python
  from zipfile import ZipFile
  import os

  files = os.listdir("./posters")

  with ZipFile('posters.zip', 'w') as myzip:
      for file in files:
          myzip.write(os.path.join("./posters", file))
  ```
  
- Weaviate documentation
  - [OpenAI Embeddings with Weaviate](https://weaviate.io/developers/weaviate/model-providers/openai/embeddings)
