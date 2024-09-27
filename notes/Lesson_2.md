# Multimodal Search

## Chapter Objectives

- Learn how a concept is understood across multiple modalities.
- Then implement a multimodal retrieval using Weaviate, an open source vector database.
- Build a text-to-any search as well as any-to-any search.

## Multimodal Embedding Models

- Shared multimodal vector space

## Performing Multimodal Search

## Notebook

- **Local execution pre-requisites**:
  - [Google Cloud account](https://cloud.google.com/vertex-ai/generative-ai/docs/embeddings/get-multimodal-embeddings#prereqs)
    - Create Google Cloud account
    - Enable Vertex AI API
    - Authentication set up for your environment
    - I followed steps 1 to 5.
    - Screenshots of the steps are available on [this webpage](https://docs.mindmac.app/how-to.../add-api-key/create-google-cloud-vertex-ai-api-key)
  - Access Token creation
    - I followed [Manual token retrieval](https://weaviate.io/developers/weaviate/model-providers/google/embeddings-multimodal#manual-token-retrieval) option
      - >gcloud auth print-access-token
      - Token lifetime = 1 hour
      - Save this token as environment variable `EMBEDDING_API_KEY` in [.env file](../code/.env).
  - Ensure that `project_id` parameter of `multi2vec_palm`is changed to the one mentioned in your Google Cloud account. Otherwise it will raise authentication failure error.
- [Jupyter Notebook](../code/L2_Multimodal_Search.ipynb)
- Steps
  - Step #1: Add multimodal data to a vector database.
  - Step #2: Perform any-to-any search.
- Weaviate documentation
  - [Embedded version of Weaviate](https://weaviate.io/developers/weaviate/installation/embedded): Allows to run the database in memory.
    - Embedded Weaviate is a deployment model.
    - It runs a Weaviate instance from your application code rather than from a standalone Weaviate server installation.
  - [connect_to_embedded](https://weaviate.io/developers/weaviate/client-libraries/python#connection-helper-functions)
  - [v4.5.4 connect_to_embedded](https://weaviate-python-client.readthedocs.io/en/v4.5.4/weaviate.html#weaviate.connect_to_embedded)
  - [weaviate.backup package](https://weaviate-python-client.readthedocs.io/en/v4.5.4/weaviate.backup.html)
    - APIs to create and restore available.
    - Though in this notebook, we restore the backup provided as part of the notebook.
