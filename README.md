# FARA text extraction using Gemini - Public Repo

### Project description

This is the public-facing of a repository for the Howard Center for Investigative Journalism. At present, this repo contains the code needed to extract key information from Foreign Agent Registration Act short-form disclosures. That information includes:

* The foreign principal that services are being provided for
* Details regarding the services being provided by the foreign agent
* Details regarding any political activity being carried out by the foreign agent

This work is continuing at the Howard Center for Investigative Journalism in 2025, and the scope of the work is expanding to extract additional information from short-forms and other disclosure types/filings.

### Running the code

BEFORE YOU BEGIN, you'll need to create your own project key for the Google Gemini API. A quickstart guide for the Gemini API can be found here: https://ai.google.dev/gemini-api/docs/quickstart?lang=python

Once you have an API key, update secret_api_key_file.py with your key. Note that without a paid plan, you'll hit rate limits after trying to process less than 1000 documents.

With a billable account, initial testing shows that processing 100 documents costs roughly 10 cents per batch. That can vary, though, depending on the documents being processed.

Run gemini_pipeline to process a batch of documents. The notebook is currently set to process the 100 most-recent filings. If you want to change or expand the selection of documents being processed, update the number(s) in the for loop for both steps.

short_form_14_to_24.csv contains the urls of short-form disclosures from 2014 through mid-November 2024. That csv was derived from a list of all short-forms maintained by the DoJ, which you can access here: https://efile.fara.gov/ords/fara/f?p=107:21