# QueryMaster

QueryMaster is an AI-powered project management and query interface that allows users to upload files, convert them into vector embeddings using OpenAI, store these embeddings in a Pinecone database, and query the files using a chatbot interface.

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)

## Features

- Create and manage projects
- Upload files to projects
- Generate vector embeddings using OpenAI API
- Store vector embeddings in Pinecone database
- Query files through a chatbot interface

## Tech Stack

- Node.js
- Express.js
- React.js
- Tailwind CSS
- Pinecone
- OpenAI

## Prerequisites

- Node.js installed
- Pinecone account
- OpenAI API key

## Setup Instructions

1. **Clone the repository:**
    ```sh
    git clone https://github.com/yourusername/querymaster.git
    cd querymaster
    ```

2. **Install dependencies:**
    ```sh
    npm install
    ```

3. **Configure environment variables:**
   Create a `.env` file in the root directory and add your configuration details:
    ```env
    OPENAI_API_KEY=your_openai_api_key
    PINECONE_API_KEY=your_pinecone_api_key
    PINECONE_INDEX_NAME=your_pinecone_index_name
    ```

4. **Run the application:**
    ```sh
    npm run dev
    ```

## Usage

1. **Create a Project:**
   Navigate to the create project page, enter the project name, and upload files. The files will be processed and vector embeddings will be stored.

2. **Query Files:**
   Use the chatbot interface to query files within a project. Select a project and enter your query to get relevant file content.

## API Endpoints

1. **Create Project and Upload Files:**
    ```http
    POST /api/createproject
    Body: {
      "projectName": "Your Project Name",
      "files": [File]
    }
    ```

2. **List Projects:**
    ```http
    GET /api/listprojects
    ```

3. **Query Files:**
    ```http
    POST /api/queryfiles
    Body: {
      "projectId": "Project ID",
      "query": "Your query text"
    }
    ```

4. **Delete Project:**
    ```http
    DELETE /api/deleteproject
    Body: {
      "projectId": "Project ID"
    }
    ```

    
## Conclusion

QueryMaster is designed to provide a seamless project management and query experience using state-of-the-art AI and database technologies. The combination of Zoho Catalyst, Pinecone, and OpenAI makes it a robust solution for managing and querying project files efficiently.

