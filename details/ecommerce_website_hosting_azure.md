# **E-Commerce Website Hosting on Azure**

## **Introduction**

This project was undertaken during an internship as a **Project Intern on Microsoft Azure at Verzeo** in **August 2019**. It demonstrates the deployment of a robust and scalable **WordPress website** hosted on **Microsoft Azure**. By leveraging Azure's Virtual Machines (VMs), DNS Zones, and third-party domain registration, the project highlights the integration of cloud infrastructure with a fully functional **eCommerce platform** for gifting, named **TheGiftMasters.ml**.

The presentation for this project is publicly available at [Hosting a WordPress Website on Microsoft Azure](https://www.slideshare.net/slideshow/word-press-website-on-azure-232241506/232241506).

---

## **Objectives**

1. **Cloud-Based Website Hosting:**
   - Deploy a WordPress website on Azure for a high-performance hosting solution.
2. **Custom Domain Integration:**
   - Configure a custom `.ml` domain for seamless user access.
3. **Enhanced Website Features:**
   - Customise WordPress with themes and plugins for a rich user experience.
4. **Scalability and Reliability:**
   - Ensure the hosted website can scale and maintain uptime under varying loads.

---

## **System Architecture**

### **1. Components**
- **Azure Virtual Machine:**  
  Hosts the WordPress application using the **Bitnami WordPress image**.
- **Azure DNS Zones:**  
  Manages DNS records to route custom domain traffic to the website.
- **Freenom:**  
  Provides free `.ml` domain registration for branding.
- **WordPress CMS:**  
  Powers the website’s backend and facilitates customisation.

### **2. Workflow**
1. **Azure VM Deployment:**
   - Host WordPress on Azure Virtual Machines using a pre-configured image.
2. **Domain Registration:**
   - Acquire a `.ml` domain from Freenom and configure DNS settings.
3. **DNS Resolution:**
   - Configure A and CNAME records in Azure DNS Zones for domain linking.
4. **Website Customisation:**
   - Customise the WordPress website with eCommerce themes and plugins.
5. **Validation:**
   - Test DNS propagation and website functionality across browsers.

---

## **Implementation Details**

### **1. Deploying WordPress on Azure**
1. **Azure Marketplace:**  
   - Navigate to the **Azure Marketplace** and search for the **Bitnami WordPress Certified Image**.
2. **VM Configuration:**
   - Configure VM specifications:
     - **Region:** Based on the nearest location.
     - **Authentication:** SSH key or password-based.
     - **Pricing Tier:** Standard B1ms (1 vCPU, 2 GB RAM) for cost-efficiency.
   - Deploy the VM and note the public IP address.
3. **Initial WordPress Setup:**
   - Access WordPress via `<Public_IP>/wp-admin`.
   - Retrieve credentials from the Boot Diagnostics logs in the Azure portal.
   - Configure basic WordPress settings.

### **2. Domain Registration and Integration**
1. **Domain Registration:**
   - Visit [Freenom](http://www.freenom.com/) to register a free `.ml` domain.
   - Chosen Domain: **www.thegiftmasters.ml**.
2. **DNS Configuration on Freenom:**
   - Add DNS records:
     - **A Record:** Points the domain to the public IP address of the Azure VM.
     - **CNAME Record:** Configures subdomain redirection (e.g., `www` to root domain).
3. **Azure DNS Zones:**
   - Create a DNS Zone in Azure and configure records:
     - **A Record:** Public IP of the VM.
     - **TTL:** Set to 300 seconds for quick propagation.

### **3. Customising the Website**
1. **Theme Installation:**
   - Install and activate the **Astra Theme** for responsiveness.
2. **Plugins Setup:**
   - Add plugins such as:
     - **WooCommerce:** Enables eCommerce functionalities like product listings and shopping cart.
     - **Yoast SEO:** Optimises website for search engines.
     - **Contact Form 7:** Provides a dynamic contact form.
3. **Website Pages:**
   - Develop core pages:
     - **Home Page:** Features promotions and highlights.
     - **Shop Page:** Displays product listings with pricing and descriptions.
     - **About Us:** Shares the brand's mission.
     - **Contact Us:** Includes a form integrated with Contact Form 7.

---

## **Testing and Results**

### **1. Functional Testing**
- **DNS Propagation:**  
  Verified the domain `www.thegiftmasters.ml` resolved to the WordPress-hosted VM.
- **Website Accessibility:**  
  Tested across multiple devices (desktop, mobile) and browsers (Chrome, Edge, Firefox).

### **2. Website Performance**
- **Response Time:**  
  Measured average response time of 1.4 seconds using **GTmetrix**.
- **Load Testing:**  
  Simulated concurrent users with **Apache JMeter**:
  - Handled 100 simultaneous requests with no downtime.

---

## **Key Features**

1. **Cloud-Hosted WordPress Site:**  
   Utilised Azure Virtual Machines for scalable and reliable hosting.
2. **Custom Domain Integration:**  
   Successfully configured `www.thegiftmasters.ml` using Azure DNS and Freenom.
3. **eCommerce Capabilities:**  
   Enabled product listings, shopping cart, and payment processing via WooCommerce.
4. **SEO-Optimised Design:**  
   Integrated Yoast SEO for improved visibility.

---

## **Learning Outcomes**

1. **Cloud Infrastructure Deployment:**  
   - Learned to configure and manage Azure Virtual Machines.
2. **Domain and DNS Management:**  
   - Gained expertise in linking domains using Azure DNS Zones and third-party registrars.
3. **Website Customisation:**  
   - Developed advanced skills in customising WordPress with themes and plugins.
4. **Performance Testing:**  
   - Enhanced knowledge of load testing tools like JMeter for hosted applications.

---

## **Conclusion**

This project demonstrates the deployment of a WordPress website on Microsoft Azure, showcasing cloud infrastructure integration with domain services and CMS customisation. The hosted eCommerce platform, **TheGiftMasters.ml**, highlights the effectiveness of Azure for scalable and high-performing web hosting solutions.

---

**Author:** Yashas Javali  
**Duration:** August 2019  
**Specialisation:** Cloud Computing and Web Hosting  
**Statement:** This project highlights expertise in cloud-based WordPress hosting, custom domain configuration, and scalable eCommerce platform deployment on Azure.

---

