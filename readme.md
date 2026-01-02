# Kings Dominion NLP Project

## Project Intention Disclaimer
This project was developed as a collaboration amongst students of the VCU Masters of Decision Analytics (MDA) program to learn how to develop NLP solutions.
There is no intention for paid and/or commercial use of any data contained within the project, and no claims are made regarding the ownership and usage of source materials.


## Project Description
As a coursework assignment, the team was challenged to develop a functional NLP chatbot using source material of their choosing. 
The White Water Canyon ride manual from Kings Dominion, located in Doswell, Virginia, appeared to be a promising source as it contains 
detailed descriptions of ride equipment, staffing positions, standard operating procedures, and emergency protocols. 
The team found this material to be of a high enough quality to use for the proposed NLP chatbot.

This repo contains the core materials for the project to preserve the original functionality as well as to extend as possible in an effort to continue learning.

## Orginal Contents
The chatbot is currently built within a singular Python notebook file that was originally hosted on Google Colab for use of its GPU clusters. 

### Notebook Steps of Operation
- Step 1: Install Dependencies
- Step 2: Mount Google Drive & Import Libraries
- Step 3: Load & Process PDF Documents
    - This section chunks the pdf, sanitizes them of keywords that cause issues with the LLM output, and screates hybrid embeddings
- Step 4: Initialize ChromaDB Vectore Database
- Step 5: Clear GPU Memory 
    - On initial run this step can be skipped, but during subsequent runs after changes made in prior steps, clearing the GPU memory 
    removes the older model to force creation of a new model to avoid cross-contamination. 
- Step 6: Initialize Language Model
    - The model currently uses Qwen2.5-3B-Instruct
- Step 7: Define RAG Pipeline Function
    - The pieline function contains the basis for user input/model output including prompts for the LLM to assist processing the input
- Step 8: Create Chatbot Interface
    - The interface is developed using Gradio
- Step 9: Launch the Gradio Chatbot
    - Gradio provides a user-friendly interface for asking questions of the data and receiving responses from the model

## Modifications
Code in this repo was modified to allow for running the notebook on a local machine while still using the Google Colab runtime, in addition to 
making some adjustments to allow for publishing on a GitHub repo without sharing secret token values. 