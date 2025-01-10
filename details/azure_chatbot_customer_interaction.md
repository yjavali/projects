# **Azure Chatbot for Automated Customer Interaction**

## **Introduction**

This project, carried out during my internship as a Project Intern on Microsoft Azure at **Verzeo** in **July 2019**, focuses on developing and deploying a chatbot using **Microsoft Azure Bot Service**. The chatbot, powered by **QnA Maker**, serves as an intelligent conversational agent capable of answering predefined questions and integrating with web pages and platforms like Facebook Messenger. The solution demonstrates the creation of a scalable, interactive, and AI-driven bot using Azure's **AI + Machine Learning** services.

The presentation for this project is publicly available at [Deploying a Chatbot Service Using Microsoft Azure](https://www.slideshare.net/slideshow/deploying-a-chatbot-service-using-microsoft-azure/232241596).

---

## **Objectives**

1. **Design and Deploy a Chatbot:**
   - Create a web-based chatbot using Azure's Bot Service and QnA Maker.
2. **Knowledge Base Creation:**
   - Automate responses by linking the bot to a curated knowledge base (FAQs).
3. **Integration with External Platforms:**
   - Enable chatbot deployment on websites and messaging platforms.
4. **Real-Time Testing and Optimization:**
   - Evaluate the chatbot's functionality through web-based simulations.

---

## **System Architecture**

### **1. Components**
- **QnA Maker:** Service to create, train, and deploy a knowledge base for FAQs.
- **Azure Bot Service:** Framework to host and deploy the chatbot.
- **Web App Bot:** Azure-hosted web application to manage and test the bot.
- **Direct Line API:** Facilitates communication between the bot and client applications.
- **LUIS Integration (Optional):** Supports natural language processing for advanced conversational capabilities.

### **2. Workflow**
1. **Knowledge Base Creation:**
   - Curate FAQs from a URL or upload files (e.g., PDFs, Excel sheets).
   - Use QnA Maker to structure the question-answer pairs.
2. **Bot Deployment:**
   - Host the bot on Azure as a Web App Bot under the **AI + Machine Learning** domain.
3. **Integration and Testing:**
   - Integrate the chatbot into platforms like web pages or Facebook Messenger.
   - Test the chatbot in the Azure Web Chat interface.

---

## **Implementation Steps**

### **1. Knowledge Base Creation**
1. **Visit QnA Maker Portal:**  
   Navigate to [QnA Maker](https://www.qnamaker.ai) and select "Create a Knowledge Base."
2. **Create QnA Service:**  
   Link the service to an Azure resource by selecting "Create a QnA Service."  
   Fill in required details like resource group, pricing tier, and region.
3. **Upload Data Source:**  
   - Use a URL (e.g., Microsoft Azure FAQs) or upload local files (PDF, Excel) as a data source.
4. **Save and Train:**  
   - Curate or add custom QnA pairs to the knowledge base.
   - Save changes and train the model for accuracy.
5. **Pre-Test Knowledge Base:**  
   - Test the curated QnA pairs to verify functionality.

### **2. Deploying the Bot**
1. **Visit Azure Marketplace:**  
   Navigate to the **AI + Machine Learning** domain in the Azure portal.
2. **Create a Web App Bot:**  
   - Select "Web App Bot" and provide the required inputs:
     - Bot Name: e.g., `MinorChatBot`.
     - Region: Based on user location.
     - App Service Plan: Choose a scalable pricing tier.
   - Click "Create" to deploy the bot.
3. **Test in Web Chat:**  
   - After deployment, test the bot using the "Test in Web Chat" feature to validate its functionality with the connected QnA knowledge base.

### **3. Integration and Testing**
1. **Integrate Platforms:**
   - Deploy the chatbot on web pages, Facebook Messenger, or other platforms using Direct Line API.
2. **Testing:**  
   - Use the Azure Web Chat interface and integrated platforms to validate the bot's responses.

---

## **Key Features**

1. **Dynamic Knowledge Base:**
   - Supports custom and curated QnA pairs for varied use cases.
2. **Platform Integration:**
   - Compatible with web and social media platforms via APIs.
3. **Scalability:**
   - Hosted on Azure with automatic scaling for handling high traffic.
4. **Advanced Features (Optional):**
   - Integration with LUIS for context-aware and natural language processing capabilities.

---

## **Learning Outcomes**

1. **Cloud-Based Chatbot Development:**
   - Gained expertise in using Azure services for chatbot creation.
2. **QnA Maker Integration:**
   - Learned to structure and train a knowledge base for automated responses.
3. **Web App Deployment:**
   - Acquired skills in deploying and managing Azure-hosted applications.
4. **Direct Line API Implementation:**
   - Developed an understanding of API integration for external platform connectivity.
5. **Real-Time Testing:**
   - Enhanced skills in testing and optimizing chatbot performance for diverse use cases.

---

## **Conclusion**

This project showcases the design and deployment of a chatbot using **Microsoft Azure Bot Service** and **QnA Maker**. The chatbot automates responses, improving user engagement and operational efficiency. By integrating with web platforms, the system demonstrates versatility and scalability, making it suitable for a wide range of applications.

---

**Author:** Yashas Javali  
**Duration:** July 2019  
**Specialisation:** Cloud Computing and AI Integration  
**Statement:** This project reflects the practical application of Azure Bot Service and QnA Maker, showcasing their capabilities in creating intelligent conversational agents for real-world use cases.

---

