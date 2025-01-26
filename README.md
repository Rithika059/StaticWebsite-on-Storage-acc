
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
Steps to create a basic web page: 
1.Use any text editor (e.g., Notepad, Visual Studio Code, or Sublime Text) to create an HTML file.
2.Write simple HTML code with custom text or styling.
 For example: 
3.<!DOCTYPE html>
4.<!doctype html>
5.<html lang="en">
6.<head>
7.    <meta charset="utf-8" />
8.    <title>Home page</title>
9.    <meta name="viewport" content="width=device-width, initial-scale=1">
10.    <link rel="preconnect" href="https://fonts.gstatic.com">
11.    <link href="https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@300;400&display=swap" rel="stylesheet">
12.    <link rel="stylesheet" href="css/bootstrap.min.css" type="text/css" />
13.    <link rel="stylesheet" href="fontawesome/css/all.min.css" type="text/css" /> 
14.    <link rel="stylesheet" href="css/slick.css" type="text/css" />   
15.    <link rel="stylesheet" href="css/tooplate-simply-amazed.css" type="text/css" />
16.<!--
17.
18.Tooplate 2123 Simply Amazed
19.
20.https://www.tooplate.com/view/2123-simply-amazed
21.
22.-->
23.</head>
24.
25.<body>
26.    <div id="outer">
27.        <header class="header order-last" id="tm-header">
28.            <nav class="navbar">
29.                <div class="collapse navbar-collapse single-page-nav">
30.                    <ul class="navbar-nav">
31.                        <li class="nav-item">
32.                            <a class="nav-link" href="#section-1"><span class="icn"><i class="fas fa-2x fa-air-freshener"></i></span> Our Company</a>
33.                        </li>
34.                        <li class="nav-item">
35.                            <a class="nav-link" href="#section-2"><span class="icn"><i class="fab fa-2x fa-battle-net"></i></span> Our Work</a>
36.                        </li>
37.                        <li class="nav-item">
38.                            <a class="nav-link" href="#section-3"><span class="icn"><i class="far fa-2x fa-images"></i></span> Gallery</a>
39.                        </li>
40.                        <li class="nav-item">
41.                            <a class="nav-link" href="#section-4"><span class="icn"><i class="far fa-2x fa-comments"></i></span> Contact</a>
42.                        </li>
43.                    </ul>
44.                </div>
45.            </nav>
46.        </header>
47.        
48.        <button class="navbar-button collapsed" type="button">
49.            <span class="menu_icon">
50.                <span class="icon-bar"></span>
51.                <span class="icon-bar"></span>
52.                <span class="icon-bar"></span>
53.            </span>
54.        </button>
55.        
56.        <main id="content-box" class="order-first">
57.            <div class="banner-section section parallax-window" data-parallax="scroll" data-image-src="img/section-1-bg.jpg" id="section-1">
58.                <div class="container">
59.                    <div class="item">
60.                        <div class="bg-blue-transparent logo-fa"><span><i class="fas fa-2x fa-atom"></i></span> ARC architectures</div>
61.                        <div class="bg-blue-transparent simple"><p>We create Beautiful architecture and Interiors</p></div>
62.                    </div>
63.                </div>
64.            </div>
65.            <section class="gallery-section section parallax-window" data-parallax="scroll" data-image-src="img/section-3-bg.jpg" id="section-3">
66.                <div class="container">
67.                    <div class="title text-right">
68.                        <h2>Our Gallery</h2>
69.                    </div>
70.                        <script src="js/jquery-3.3.1.min.js"></script>
71.    <script src="js/bootstrap.bundle.min.js"></script>
72.    <script src="js/jquery.singlePageNav.min.js"></script>
73.    <script src="js/slick.js"></script>
74.    <script src="js/parallax.min.js"></script>
75.    <script src="js/templatemo-script.js"></script>
76.</body>
77.</html>
78.Save the file as index.html on your local machine.
Feel free to add additional files like CSS, images, or JavaScript if your site requires them.

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

5. Upload Website Files
Once the $web container is open, upload your website files.

Steps to upload files:

1.Click on the Upload button within the $web container.

2.Use one of the following methods to upload files: 

Drag and Drop: Drag your index.html (and other files, if any) into the upload area.

Browse: Click the Browse button to locate and select files manually.

3.Click Upload to confirm and complete the process.

Your website files are now hosted in the $web container and ready to be served.



6. Test the Static Website
After uploading the files, Azure generates a Primary Endpoint URL to access the hosted site.
Steps to test your website: 

1.Go back to the Static Website section of your Storage Account.

2.Copy the Primary Endpoint URL displayed there.

3.Paste the URL into a browser to access your website. 

If the website displays correctly, your deployment was successful.

If you encounter errors, verify that the file names match the settings (e.g., index.html) and that all dependencies are uploaded.


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
