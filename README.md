# BrainWave Chrome Extension

**Version:** 1.0.0  
**Author:** Sai Saketh Gooty Kase  
**Project Advisor:** Prof. Michael Jonas  

---

## **Introduction**

BrainWave is an advanced Chrome extension designed to simplify interactions with online educational content. The extension leverages state-of-the-art Natural Language Processing (NLP) models to extract insights, answer user queries, and manage bookmarks, enabling a seamless, interactive, and efficient browsing experience. 

---

## **Features**

### 1. **Explore Insights**
- Extracts keywords and interconnected topics from webpage content.
- Powered by a fine-tuned Named Entity Recognition (NER) model.
- Displays keywords in a user-friendly interface for quick exploration.

### 2. **Query Article**
- Provides precise, context-aware answers to user queries based on webpage content.
- Utilizes a fine-tuned Question Answering (QA) model for enhanced accuracy.

### 3. **Bookmark Management**
- Save, view, and delete bookmarks for efficient resource organization.
- Bookmarks are stored locally using Chrome Storage for privacy and accessibility.

---

## **Technology Stack**

### **Frontend**
- **React** with **TypeScript**
- **Material-UI** for responsive design and UI components

### **Backend**
- Chrome APIs for runtime and storage management
- Integration with:
  - **APYHub API** for text extraction
  - **OpenAI API** for NER and QA models

### **Authentication**
- **Microsoft OAuth2.0** for secure user authentication and session management

---

## **System Architecture**

The system consists of the following components:
- **Popup UI:** User interface built with React, allowing interaction with features.
- **Background Scripts:** Core logic for API communication, authentication, and data processing.
- **Content Scripts:** Extracts text content from webpages and interacts with the DOM.
- **External APIs:** APYHub for content preprocessing, OpenAI for fine-tuned model interactions.
- **Storage:** Chrome Storage API for managing bookmarks and user preferences.

---

## **Installation**

### Prerequisites
- Google Chrome browser
- Node.js and npm installed locally

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/SaiSakethGK/BrainWave-Chrome-Extension.git
   cd BrainWave-Chrome-Extension
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Build the extension:
   ```bash
   npm run build
   ```
4. Load the extension:
   - Open Chrome and navigate to `chrome://extensions`.
   - Enable "Developer mode."
   - Click "Load unpacked" and select the `build` directory.

---

## **Usage**

### **Explore Insights**
1. Open the extension popup while browsing a webpage.
2. Click on "Explore Insights."
3. View extracted keywords and interconnected topics displayed as clickable chips.

### **Query Article**
1. Open the extension popup on an article or blog.
2. Enter a question in the query input field and click "Submit."
3. The answer is displayed in the extension interface.

### **Bookmark Management**
1. Save the current tab’s URL by clicking "Save Bookmark."
2. View saved bookmarks from the "View Bookmarks" section.
3. Delete bookmarks as needed.

---

## **API Details**

### 1. **APYHub API**
- Endpoint: `https://api.apyhub.com/extract/text/webpage`
- Method: `GET`
- Headers: `Authorization: Bearer <apy-token>`
- Response: Extracted webpage text

### 2. **OpenAI API**
- Endpoint: `https://api.openai.com/v1/chat/completions`
- Headers: `Authorization: Bearer <api-key>`
- Payload:
  - **NER Model:** `ft:gpt-4o-mini-2024-07-18:personal::AXIEg8pJ`
  - **QA Model:** `ft:gpt-4o-mini-2024-07-18:personal::AazS6FTz`

---

## **Known Issues and Limitations**
- Limited to Google Chrome; not yet compatible with Firefox or Edge.
- Fine-tuned models may struggle with highly domain-specific or ambiguous content.
- Lack of bookmark categorization impacts organizational efficiency.

---

## **Future Enhancements**
- Adding bookmark categorization for better resource management.
- Expanding compatibility to other browsers like Firefox and Edge.
- Enhancing fine-tuned models to handle more complex and domain-specific content.
- Implementing a recommendation system powered by LLMs.

---

## **References**
1. OpenAI API Documentation: [https://platform.openai.com/docs](https://platform.openai.com/docs)  
2. APYHub API Documentation: [https://apyhub.com/docs](https://apyhub.com/docs)  
3. React Documentation: [https://reactjs.org](https://reactjs.org)  
4. Material-UI Documentation: [https://mui.com](https://mui.com)  
5. Microsoft OAuth2.0 Documentation: [https://learn.microsoft.com/en-us/azure/active-directory/develop/](https://learn.microsoft.com/en-us/azure/active-directory/develop/)
