# SaaS Terms and Conditions Analyzer

## Project Overview

This project is an AI-powered tool designed to analyze Terms and Conditions (T&C) documents from various SaaS providers. The tool scrapes T&C from specified URLs, identifies key clauses, and flags potential risks based on predefined categories such as Confidentiality, Liability, Data Privacy, and more.

The primary objective is to assist buyers, legal teams, or marketplaces in understanding potential risks in vendor agreements, helping them make informed decisions before engaging with the SaaS provider.

## Features

- **Web Scraping**: Extracting T&C documents from multiple SaaS provider URLs.
  
- **Risk Identification**: Analyzing and categorizing clauses based on predefined risk categories such as Confidentiality, Liability, Data Privacy, Payment, and others.
  
- **Data Categorization**: Storing identified clauses and risk indicators in a structured format using a Pandas DataFrame.
  
- **Customization**: Easily extendable to include additional risk labels or categories based on specific requirements.

## Project Structure

- **`Jaazee.ipynb`**: Jupyter notebook containing the code for scraping and analyzing T&C documents.
  
- **`requirements.txt`**: List of dependencies required for the project.
  
- **`README.md`**: Project overview and setup instructions.

## Assumptions

The following assumptions i made in this project:

1. **Predefined Risk Labels and Categories**:
   
   - The risk labels and corresponding keywords used for classification are assumed to be comprehensive and cover all relevant clauses typically found in SaaS Terms and Conditions.

2. **Keyword-Based Classification**:
   
   - Clause classification is based on keyword matching. It is assumed that the presence of certain keywords determines the risk category and red flag status accurately.

3. **English Language Only**:
   
   - The analysis assumes all T&C documents are written in English. The keyword-based approach might not perform well with documents in other languages.

4. **Complete Extraction**:
   
   - It is assumed that the entire T&C document is extracted successfully during scraping. Partial scraping results might lead to misclassification or missing risks.

5. **Single Document Type**:
    
   - It is assumed that all T&C documents follow a similar format and structure. The project does not account for variations in legal terminology, document structure, or length.

6. **Binary Classification of Red Flags**:
    
    - Classification into red flag or not is binary. It is assumed that each clause can be definitively categorized as a risk or not without considering varying degrees of severity.
      

## Dependencies

To run this project, the following Python libraries are required:

- `requests`
- `beautifulsoup4`
- `pandas`
- `scikit-learn`
- `tensorflow`
- `re`

### To Install the Dependencies

Installing the dependencies using:
```bash

pip install -r requirements.txt
