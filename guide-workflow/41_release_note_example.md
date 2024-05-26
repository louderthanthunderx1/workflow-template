# Release Notes Example

## Demo Project Sprint #3 — Release Notes

  

### Introduction

This release brings new enhancements to the Demo Project, incorporating new features and updates that streamline its functionality and user experience. Key highlights include the integration of a new data pipeline, updates on data uploading, and the introduction of GPT-4 Turbo.

  

### New Features

1. New data pipeline integrated with Azure and the production version of the bot.
2. Updated instructions on how to upload new data.
3. Integration of the new GPT-4 Turbo model.
4. User option to select different models (GPT-3.5 / GPT-4 / GPT-4 Turbo).
5. Assistance and validation on the new product data.
6. Running unit tests for new data in LangSmith for the different models.
7. Research and plan to integrate customer data into the bot.

  

### 1\. Data Pipeline Integration with Azure

We have successfully integrated a new data pipeline using Azure and pgvector, enhancing the production version of the bot. This update improves data processing efficiency and simplifies the CRUD operations for FAQ data.

  

### 2\. Updated Data Upload Instructions

The CSV file can now be uploaded directly to the Azure Storage account. Here's a quick video of how that works. You can easily upload new data, overwrite existing files, and delete old ones.

  

Data requirements

*   Must be a `.csv` file
*   Must be `comma` separated
*   Check that there are no empty rows, or rows without answers.

  

### 3\. GPT-4 Turbo Integration

The bot now includes integration with the new GPT-4 Turbo model, offering enhanced performance and expanded knowledge.

*   **Release Overview**: GPT-4 Turbo, an advanced version of GPT-4, is now in preview. This model offers enhanced capabilities and a 128k context window, equivalent to over 300 pages of text.
*   **Pricing and Availability**: GPT-4 Turbo is more cost-effective, with a 3x cheaper price for input tokens and 2x cheaper for output tokens compared to GPT-4. Available for all paying developers using the `gpt-4-1106-preview` API.
*   **Production Readiness**: The preview model is not yet suited for production traffic. The stable, production-ready model is expected in the coming weeks. [Learn more](https://openai.com/blog/new-models-and-developer-products-announced-at-devday).

  

### 4\. Model Selection Option

Users can now choose between different models (GPT-3.5, GPT-4, GPT-4 Turbo) for varied response capabilities and levels of context understanding. This is done by adding `--model` followed by the model. The following models are available:

  

*   `--model gpt-3.5-turbo`
*   `--model gpt-4`
*   `--model gpt-4-turbo`

  

Example:

```plain
@Bot Question for the bot here --model gpt-4
```

  

The default model `gpt-3.5-turbo`

  

### 5\. Product Data Assistance and Validation

Here are some best practices to improve the quality of the data:

  

**Descriptive File Naming:**

*   Use clear, descriptive names for each CSV file.
*   Names should reflect the content, such as the product category, name, or issue type.

**Data Validation and Integrity:**

*   Ensure each record in the CSV is complete and valid.
*   Avoid empty fields; ensure every question has a corresponding answer.
*   Remove extraneous spaces or characters that could corrupt data.

**Consistent Formatting:**

*   Standardize the format for all CSV files.
*   Define a uniform structure for questions and answers (e.g., first column for questions, second for answers), and potentially third column for metadata.

**Use of Folders for Organization:**

*   Utilize folders to organize CSV files logically.
*   Structure folders by product lines, categories, or other relevant categories.

**Regular Data Audits:**

*   Conduct periodic reviews to ensure data quality and relevance.
*   Update or remove outdated information to maintain the dataset's accuracy.

  

### 6\. LangSmith Unit Tests for Different Models

We've updated the evaluation pipeline to consider all data and ran tests using different models to assess the performance. The results can be viewed here.

  

### 7\. Integration Plan for Customer Data

We have successfully established a connection with the CRM and are now able to retrieve data from it. Here's a video outlining what we got so far and what's possible.

  

### Bug Fixes and Updates

*   **Removed Similarity Score**: The similarity score feature has been removed to simplify the retrieval process and reduce confusion.
*   **CSV File Structure**: We have standardized the code to only work with comma (",") as the separator in CSV files, ensuring uniformity in data processing.
*   **Factory Pattern**: Refactored the application to follow the Flask factory pattern for a more modular approach