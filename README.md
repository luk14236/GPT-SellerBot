# Seller bot with chat GPT.ipynb

This notebook contains a seller bot implemented using OpenAI's GPT model for chat interactions.

## Requirements

- Python 3.x
- OpenAI Python library (version 0.28)

To install the required library, run:
!pip install openai==0.28

## Usage

1. **Setup API Key:** Replace `"api-key"` with your OpenAI API key.
2. **Data Loading:** Ensure the `houses.json` file is present in the same directory as the notebook.
3. **Run the Notebook:** Execute the notebook cell by cell.

## Overview

The seller bot is designed to negotiate prices with customers and answer questions about products using the GPT-3.5 model. It utilizes the `openai.ChatCompletion` API to generate responses based on user messages.

## How it Works

- The bot maintains a list of messages exchanged between the user and itself.
- Each user message is appended to this list and passed to the GPT model to generate a response.
- The generated response is appended to the list and returned to the user.

## Important Notes

- When a customer asks for the price, the bot increases it by 10%.
- During negotiation, the minimal price is set to at least 2% more than the original cost.
