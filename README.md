# Automated Data Flow and AI-Enhanced Record Enrichment with n8n and Airtable

## Overview
This project leverages **n8n** to automate the process of capturing form submissions, updating records in **Airtable**, and enriching those records dynamically with AI-generated content. The workflow is designed to streamline data management and add creative elements such as poetry generation to the records.

### Key Features:
- **Seamless Integration**: Automatically connects form submissions to Airtable, ensuring efficient data capture.
- **Conditional Routing**: Uses a Switch Node to dynamically route data based on specific user inputs, such as the profession selected in the form.
- **AI-Driven Content Creation**: Integrates with the Google Gemini Chat model to generate personalized poetry based on the submitted data.
- **Real-time Updates**: Airtable records are enriched with creative content, ensuring the data is continuously updated and aligned with user submissions.

---

## Workflow Breakdown

### 1. **Trigger Node: Form Submission** 📝
- The workflow begins when a user submits a form via a user-friendly URL.
- The form captures the following data:
  - **Name**
  - **Looks**
  - **Profession** (e.g., Video Editor, Graphic Designer, AI Manager)

### 2. **Create Record in Airtable** 📊
- The form data is mapped and automatically inserted into an Airtable base.
- Each submission creates a new record in a specified table, where the user’s data is stored for future processing.

### 3. **Routing with Switch Node** 🔀
- Depending on the **Profession** selected in the form, the workflow routes the data into different branches:
  - **Video Editor**
  - **Graphic Designer**
  - **AI Manager**
  
Each branch allows for tailored processing, ensuring that data is handled according to specific business rules or needs.

### 4. **Poetry Generation with Google Gemini Chat model** 🤖✍️
- Once the form data is captured and categorized, an AI-driven poetry generation node is invoked.
- The Google Gemini Chat model is used to craft unique, simple poems based on the data submitted, such as the user's name, looks, and profession.

### 5. **Updating Airtable Record** 🔄
- The newly generated poem is added back into the corresponding Airtable record.
- This ensures that the record is updated with both the original form data and the creative AI-generated content, providing a richer dataset for any further analysis or use.

---


## Demo
![Alt text](https://github.com/Sarfrazali-123/Form-Submission-Automation/blob/6f71438fb19953994e837e90b50a89773c1e9b09/Capture-jfdhfjd.PNG)


## Requirements
- **n8n**: Workflow automation tool used to orchestrate the process.
- **Airtable**: Cloud-based database for storing and managing form submissions.
- **Google Gemini Chat**: AI model for generating creative poetry.
- **Airtable API Key**: Required to interact with your Airtable base programmatically.
- **n8n Access**: Required for setting up and managing workflows.

---

## Installation & Setup

1. **Set Up n8n**:  
   Follow the official documentation to install and set up n8n on your system:  
   [n8n Installation Guide](https://n8n.io/docs/getting-started/)

2. **Create an Airtable Account**:  
   Sign up for an Airtable account if you haven't already:  
   [Airtable Sign Up](https://airtable.com/signup)

3. **Create an Airtable Base**:  
   Create a new base in Airtable where your form submissions will be stored.

4. **Configure n8n**:
   - Create a new workflow in n8n.
   - Set up the **Form Submission** trigger (e.g., Google Forms, Typeform, or custom form).
   - Configure Airtable's **Create Record** node to map submitted form data.
   - Add the **Switch Node** to route the data based on the profession selected.
   - Integrate the **Google Gemini Chat** node for poetry generation.
   - Set up the **Update Record** node to update the Airtable record with the generated poem.

5. **Run the Workflow**:  
   After configuring the workflow, execute it and ensure the automation is functioning as expected.

---

## Contributions
Feel free to fork this project and contribute by:
- Adding more creative AI models for content generation.
- Extending the workflow with additional processing or integrations.
- Enhancing the error-handling and logging mechanisms.

---

## License
This project is licensed under the MIT License.

---

By automating these processes with n8n and enriching the data with AI-generated poetry, this workflow brings efficiency and creativity into the data management process!
