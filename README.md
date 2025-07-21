Google Drive to Pinecone Embedding Pipeline (n8n Workflow)
This workflow automates the process of retrieving files from Google Drive, extracting their content, splitting the text into chunks, generating embeddings using OpenAI, and storing them in Pinecone for semantic search.

⚙️ Workflow Overview
Trigger – Manually triggered by user (Test workflow).

Search Files and Folders – Searches for specific files in Google Drive.

Get Content – Downloads the contents of each file.

Loop Over Items – Iterates through all the found files.

Text Splitting – Uses Recursive Character Text Splitter to chunk the content.

Generate Embeddings – Calls OpenAI API to create embeddings.

Store in Pinecone – Uploads the embeddings to Pinecone Vector Store.

Data Loader – (Optional) Loads pre-defined documents for processing alongside uploaded content.

📥 Input
Google Drive Access: Ensure valid authentication with access to the target folder/files.

Files Supported: Text-based formats (PDF, DOCX, TXT, etc.).

📤 Output
Embeddings stored in Pinecone: Indexed and ready for similarity search or retrieval-augmented generation (RAG) tasks.

🧠 Requirements
n8n instance running

Google Drive credentials

OpenAI API key

Pinecone API key and environment

Proper setup of Default Data Loader and Recursive Text Splitter nodes

📝 Notes
Make sure file contents are readable text.

Chunk size and overlap in the splitter can be adjusted for better context retention.

Ideal for use cases like document search, FAQ systems, or knowledge bases.
