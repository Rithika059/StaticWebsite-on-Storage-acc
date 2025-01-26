
# Project title
 Hosting a Static Website on Azure Storage Account
 # Project Overview

Hosting a static website on Azure Storage is a straightforward, cost-effective solution for lightweight web applications like personal blogs, portfolios, or documentation. This guide walks you through the process of creating and deploying a static website using Azure's Storage Account service.
Step1
1. Create a Storage Account
A Storage Account serves as the foundation for hosting static websites.

 Steps to create a Storage Account: 
1.Open the Azure Portal and navigate to Storage Accounts.

2.Click Create to start the creation process.


3.Fill in the required details: 
Subscription: Select the subscription under which the resource will be billed.

Resource Group: Choose an existing resource group or create a new one for better organization.

Storage Account Name: Enter a unique name that meets Azure's naming requirements.

Region: Select the nearest region to your target audience for reduced latency.
Performance: Opt for Standard performance, which is sufficient for hosting static websites.
Redundancy: Choose the appropriate redundancy option (e.g., LRS for local redundancy or GRS for geo-redundancy, ensuring data availability in case of regional failures).
4.Review your selections, then click Create and wait for the deployment to complete.

Once the Storage Account is created, it can be used to store and serve your static website.

2. Create a Web Page
To host a static website, you need at least one HTML file (commonly named index.html).

3. Enable the Static Website Feature
Azure Storage Accounts offer a dedicated Static Website feature to serve web content directly.
Steps to enable the Static Website feature:

1.Open the created Storage Account in the Azure Portal.

2.Scroll down to the Data Management section in the left-hand panel and select Static Website.

3.Click Enable to turn on the static website hosting.

4.In the Index document name field, type index.html (or the main file name of your website). 
This file will be displayed when users visit the root of your website.

5.Save the settings.
Enabling this feature creates a special container called $web, which is reserved for storing website files.

4. Access the $web Container
The $web container acts as the directory where your website files are stored.

Steps to locate and open the $web container: 

1.In the Storage Account, go to the Containers section under the Data Storage menu.

2.You will see a container named $web. Click on it to open.
![Screenshot 2025-01-17 095033](https://github.com/user-attachments/assets/60ebb0d7-fc4e-4b55-8d6f-e340f334d948)

5. Upload Website Files
Once the $web container is open, upload your website files.

Steps to upload files:

1.Click on the Upload button within the $web container.

2.Use one of the following methods to upload files: 

Drag and Drop: Drag your index.html (and other files, if any) into the upload area.

Browse: Click the Browse button to locate and select files manually.

3.Click Upload to confirm and complete the process.

Your website files are now hosted in the $web container and ready to be served.

![Screenshot 2025-01-16 214150](https://github.com/user-attachments/assets/8b291761-8f18-4729-9423-03ec1e29b62a)


6. Test the Static Website
After uploading the files, Azure generates a Primary Endpoint URL to access the hosted site.
Steps to test your website: 

1.Go back to the Static Website section of your Storage Account.

2.Copy the Primary Endpoint URL displayed there.

3.Paste the URL into a browser to access your website. 

If the website displays correctly, your deployment was successful.

If you encounter errors, verify that the file names match the settings (e.g., index.html) and that all dependencies are uploaded.

![Screenshot 2025-01-16 214220](https://github.com/user-attachments/assets/7856a5ef-f389-45f3-a7d6-9b4b7311a02f)

# Key Azure Services Used

1.Azure Storage Account: The core service for storing and serving static website files.

2.Static Website Feature: Enables a container ($web) to host web files and generates a public URL for access.

3.$web Container: A dedicated container where all static website files are uploaded.

4.Azure Portal: The user-friendly interface for managing and configuring Azure resources.


# Benefits of Using Azure Storage for Static Websites:
1.Cost-Effectiveness: Hosting static websites on Azure Storage is significantly cheaper compared to using traditional web hosting solutions.

2.High Availability: Azure ensures data redundancy and availability, making your website resilient to failures.

3.Scalability: The service can handle traffic spikes without additional configuration.

4.Simplicity: No need to manage web servers or complex configurations.

5.Global Reach: Azure's globally distributed data centers ensure low-latency access for users worldwide.

# Conclusion
By following the steps above, you can successfully host a static website on Azure Storage Account. This solution is ideal for lightweight, static content with minimal setup and maintenance. 
