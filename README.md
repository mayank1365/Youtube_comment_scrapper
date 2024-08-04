# YouTube Comment Scraper
This project allows you to scrape comments from a YouTube video, convert them into vector embeddings using a pre-trained Sentence Transformer model, and store these embeddings in a FAISS index for efficient similarity search. The resulting files include all comments in text format and a FAISS index for vector-based search.

## Files Created
- comments.txt: Contains all the comments of the video in text format.
- comments_vector_db.index: Contains all the comments of the video in vector database format.
  
## How to Run the Code
- Open Google Colab: Go to Google Colab.
- Upload the Notebook: Upload the provided notebook file to Colab.
- Run All Cells: Execute all cells in order.
  
## Detailed Steps:
- Install Dependencies: Ensure all required packages are installed. The necessary packages include youtube_comment_downloader, faiss, numpy, and sentence_transformers.
- Setup YouTube Comment Downloader: Initialize the downloader to fetch comments from the specified YouTube video URL.

- Load the Sentence Transformer Model: Use the all-MiniLM-L6-v2 model from the sentence_transformers library to convert comments into embeddings.

 - Fetch Comments: Download comments from the YouTube video.

 - Process Comments in Batches: To handle large datasets efficiently, process comments in batches using multi-threading. This speeds up the embedding generation and index building process.

- Save Comments and Index: Save the comments in text format (comments.txt) and the FAISS index (comments_vector_db.index).
