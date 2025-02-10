# Debtor Chatbot - n8n Workflow

 Overview

The Debtor Chatbot is an automated workflow in n8n designed to interact with debtors, retrieve payment details from a Google Sheet, and engage with users via WhatsApp. It uses AI-powered chat capabilities to answer debtor queries and request payments efficiently.

 Features

- Google Sheets Integration: Fetches debtor details including due amounts and deadlines.
- WhatsApp Automation: Sends messages and responses to debtors.
- AI-Powered Conversations: Uses Groq AI and Mistral embeddings for natural language interactions.
- Vector Store for Data Retrieval: Stores debtor records in Supabase for quick access.
- Call to Action: Asks debtors for a repayment date and explains consequences of non-payment.
- Logging & Error Handling: Ensures smooth workflow execution.

 Workflow Components

# 1. Google Drive Trigger

- Monitors changes in the Google Sheet containing debtor records.
- Triggers the workflow when new data is added or updated.

# 2. Download File

- Retrieves the latest debtor records from Google Drive.

# 3. Insert into Supabase Vectorstore

- Converts debtor records into vector embeddings using Mistral AI.
- Stores processed data in Supabase for efficient retrieval.

# 4. WhatsApp Message Handling

- Listens for incoming WhatsApp messages from debtors.
- Uses an AI agent to process responses dynamically.

# 5. AI-Powered Query System

- Extracts debtor details from Supabase based on provided ID.
- Responds with due amounts, status, and deadlines.

# 6. AI Chat Agent

- Powered by Groq AI.
- Ensures polite and structured communication.
- Requests repayment dates and explains consequences of delays.

# 7. WhatsApp Reply

- Sends AI-generated responses back to debtors via WhatsApp.

 Installation & Setup

1. Clone the Repository

   ```sh
   git clone <repository-url>
   cd debtor-chatbot-n8n
   ```

2. Import Workflow into n8n

   - Open n8n and navigate to "Import Workflow."
   - Upload the provided JSON workflow file.

3. Configure Credentials

   - Set up Google Drive, Supabase, WhatsApp API, and AI provider credentials in n8n.

4. Activate the Workflow

   - Enable the workflow to start monitoring debtor records and responding to messages.

 Future Enhancements

- Call Transcription & Storage: Log voice interactions.
- Multi-Language Support: Expand chatbot capabilities for global users.
- Payment Gateway Integration: Allow direct payments through chatbot links.

 Support

For any issues, contact [[support@example.com](mailto\:shyampethakamsetty@gmail.com)] or create a GitHub issue.
