# Extract PDF Images That SPan Across Multiple Pages

This notebook contains a series of cells to process images extracted from PDF files. The notebook performs tasks such as installing dependencies, extracting and combining images, and removing duplicate images both locally and in an Azure storage account.

## Requirements
- Python 3.x
- `requirements.txt` file with necessary dependencies
- Azure Key Vault and Storage account setup

## Setup
1. Clone the repository.
2. Navigate to the project directory.
3. You may run this notebook on Fabric Notebooks or AzureML.
4. Run the notebook cells in order.

## Notes
- Ensure you have the necessary permissions to access Azure Key Vault and Storage account.
- Modify the paths and storage account details as needed.


## Cells Overview

### 1. Install Dependencies
This cell installs all the necessary dependencies using the `requirements.txt` file.

### 2. Extract and Combine Images Locally
This cell contains three Python functions to:
1. Extract images from a PDF.
2. Combine extracted images.
3. Extract and combine images from a PDF.

The cell is executed with the following code:

pdf_path = "input_folder/sample_pdf_with_continued_images_10_pages.pdf"
output_folder = "output_folder"
extract_and_combine_images(pdf_path, output_folder)

### 3. Remove Duplicate Images Locally
This cell removes duplicate images from the local output folder.

### 4. Extract and Combine Images from Azure Storage
This cell performs the same tasks as Cell 2 but reads and writes files to an Azure storage account container. The storage account name is `aoaisplit98bd0002`, and the code connects to this storage account using a connection string stored as a secret in Azure Key Vault. Ensure the Azure resource running the notebook has Key Vault Contributor access.

### 5. Remove Duplicate Images in Azure Storage
This cell removes duplicate images from the `input_folder` stored in the Azure storage account.



