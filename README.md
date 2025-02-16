## Mistral-ai-agent (n8n)

![image](https://github.com/user-attachments/assets/79012f96-ad62-4824-80a4-2b8fd1261202)

## Workflow Steps  

### 1. Google Sheets Trigger  
- **Source:** A Google Sheet containing lead data.  
- **Columns:** `Name, Age, Email, Budget ($), Processed (Yes/No), Notes`  
- **Trigger:** The workflow activates when a new row is added.  

### 2. Filtering Unprocessed Leads  
- A **Filter** node ensures that only leads marked as **"No"** under the "Processed" column are forwarded for further analysis.  

### 3. Mistral AI Processing  
- The filtered data is sent to the **Mistral-Agent** node.  
- **Configuration:**  
  - **Model:** `mistral-large-latest`  
  - **Max Tokens:** `131k`  
  - **Version:** `24.11`  
  - **API Key:** Configured for authentication.  
  - **Prompt:** Designed to extract candidates with **relevant AI experience**.  

## Expected Outcome  
- The workflow ensures that only **unprocessed** leads with relevant AI experience are shortlisted.
