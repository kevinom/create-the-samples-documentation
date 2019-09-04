# API Connect Samples on IBM Cloud
Date: 12 July 2019

This document details how to install the sample applications that are used in the API Connect Education course **WD514** *Create, Secure, and Publish APIs with API Connect V2018*.
  
The IBM Cloud account where the samples are run must be owned by an IBM employee and the account must be upgraded to a *Pay As You Go* type of account. The person's department is (supposedly) billed for the sample usage. To date, no actually billing of the charges have been made to the IBM department, to my knowledge.
## Getting started
Sign on to IBM Cloud at <https://cloud.ibm.com/login>
You are prompted to enter your IBM Id.  
When you are signed on to the IBM Cloud, you can verify your account type from the menu option **Manage > Account**.   
Then, select **Account Settings** from the navigation list.  
The type of account is displayed.  
Cloud account type:
<img src="images/Screen Shot 2019-07-12 at 1.50.56 PM.png">
Your account type must be **Pay-As-You-Go**.  
## Navigation
Click the Navigation icon in the menu.  
<img src="images/Screen Shot 2019-07-12 at 2.13.50 PM.png">  
The list of options is displayed.  
<img src="images/Screen Shot 2019-07-12 at 2.19.15 PM.png" style="border:1px solid black">    
This menu is referred to as the *side navigation menu* in this document.
## Add an organization and space
In this part, you add a Cloud Foundry organization and space to the account. The organization and space is required later when you create a Toolkit.  

From the main menu, select **Manage > Account**.   
Expand **Account resources** then select **Cloud Foundry orgs** from the list.   
Click the icon to **Create** a Cloud Foundry organization.   

Add an organization named **api-org**.    
The organization is added to your list of organizations.  
<img src="images/Screen Shot 2019-07-12 at 11.10.24 AM.png">   

After adding the organization, add a space by selecting the **Spaces** from the options list for the api-org.   

Click the icon **Add a space** to add a space to the organization.  
<img src="images/Screen Shot 2019-07-12 at 11.10.39 AM.png"> 

Select the **US South** region and give the name **api-space** to the space. Then, click **Save**.  
<img src="images/Screen Shot 2019-07-15 at 4.14.09 PM.png">    
The space is added to the organization.
<img src="images/Screen Shot 2019-07-15 at 4.16.46 PM.png">  
## The applications that you are going to build
The part describes the applications that you are about to build with the IBM Cloud Toolchains.  

| Application name    | IBM Cloud URL   | Where used in course   |
|:------------- |:----------------| :-------------|
| savingsample  | savingsample.mybluemix.net | Exercise 2    |
| soapsample    | soapsample.mybluemix.net       | Exercise 3    |
| pricesample   | pricesample.mybluemix.net        | Unit 5        |   
| lookup-price   | lookup-price.mybluemix.net        | Unit 5        |   
## Create the toolchain for the first sample (savingsample)
Click the **DevOps** option from the *side navigation menu*.  
The toolchains page is displayed.  
Set **Location** to *Dallas*.  
Set **Cloud Foundry Org** to *api-org*  
Set **Resource Group** to *None*  

<img src="images/Screen Shot 2019-07-15 at 4.24.45 PM.png">  
Click **Create a Toolchain**.  
Select the template option to **Develop a Cloud Foundry app**.
<img src="images/Screen Shot 2019-07-15 at 10.44.18 AM.png">  
On the Develop a Cloud Foundry app page, change the name of the toolkit to *api-samples-savings-toolchain*.  

Ensure that the region is set to *Dallas*  
Under the Select a resource group area, click the link **Select a CF Organization (deprecated)**. Then, choose *api-org*.  
<img src="images/Screen Shot 2019-07-16 at 9.45.38 AM.png">  
Scroll down on the page, then select or type these values:  
**Server:** *default value*  
**Repository type:** *Clone*  
**Source repository URL:** *https://github.com/kevinom/api-samples-savings*  
**Owner:** *default value (your name)*  
**Repository Name:** *api-samples-savings-toolchain*  
**Make this repository private** *selected*  
**Enable Issues** *cleared*  
**Track deployment of code changes** *selected*   
<img src="images/Screen Shot 2019-07-15 at 4.33.49 PM.png">     
Click **Create**.   
On the subsequent tools integration page, click **Create** to create an IBM Cloud API key for the sample.  
<img src="images/Screen Shot 2019-07-12 at 11.03.32 AM.png">    
On the Create API key page, ensure that the name is set to *API Key for api-samples-savings-toolchain*.  
<img src="images/Screen Shot 2019-07-12 at 11.04.56 AM.png">
Then, click **Create**.  
The key is accepted and filled in on the page.  
You must supply the organization and space values on the page.   
**Organization:** *api-org*  
**Space:** *api-space* 
<img src="images/Screen Shot 2019-07-15 at 4.39.32 PM.png">  
Then, click **Create**.  
The toolchain is created and displayed on the page.
<img src="images/Screen Shot 2019-07-15 at 4.45.01 PM.png">   
### Review the generated toolkit deployment 
The *api-samples-savings-toolchain* includes artifacts under the CODE and DELIVER options.  
Click the **Delivery Pipeline** icon.   
*** 
**NOTE:** A warning might be displayed on the page indicating that a service instance was not found in this resource group and region.
<img src="images/Screen Shot 2019-07-16 at 10.17.49 AM.png">     
If you see this warning, contact IBM Support to request the creation of a Continuous Delivery service instance in this toolchain's organization.   
***   

The Build Stage ran successfully but the Deploy stage failed.
<img src="images/Screen Shot 2019-07-15 at 2.51.22 PM.png">  
Click the **View logs and history** links in the Deploy stage. 
<img src="images/Screen Shot 2019-07-15 at 4.58.18 PM.png">     
The application deployed, but did not start successfully.   
***
**NOTE:** This error will get resolved when you change the application name to **savingsample** later.  
You will need to coordinate the removal of the existing URL for the sample and the application name change.
***  

## Create the toolchain for the second sample (soapample)
Click the navigation icon on the page. Then, click the **DevOps** option from the *side navigation menu*.  
The toolchains page is displayed.  
Set **Location** to *Dallas*.  
Set **Cloud Foundry Org** to *api-org*  
Set **Resource Group** to *None*  

<img src="images/Screen Shot 2019-07-16 at 9.57.12 AM.png">  
Click **Create a Toolchain**.  
Select the template option to **Develop a Cloud Foundry app**.
<img src="images/Screen Shot 2019-07-15 at 10.44.18 AM.png">  
On the Develop a Cloud Foundry app page, change the name of the toolkit to *api-samples-soap-toolchain*.  

Ensure that the region is set to *Dallas*  
Under the Select a resource group area, click the link **Select a CF Organization (deprecated)**. Then, choose *api-org*.  
<img src="images/Screen Shot 2019-07-16 at 10.02.29 AM.png">    
Scroll down on the page, then select or type these values:  
**Server:** *default value*  
**Repository type:** *Clone*  
**Source repository URL:** *https://github.com/kevinom/api-samples-soap*  
**Owner:** *default value (your name)*  
**Repository Name:** *api-samples-soap-toolchain*  
**Make this repository private** *selected*  
**Enable Issues** *cleared*  
**Track deployment of code changes** *selected*   
<img src="images/Screen Shot 2019-07-16 at 10.06.54 AM.png">     
Click **Create**.   
On the subsequent tools integration page, click **Create** to create an IBM Cloud API key for the sample.  
<img src="images/Screen Shot 2019-07-16 at 10.08.46 AM.png">    
On the Create API key page, ensure that the name is set to *API Key for api-samples-soap-toolchain*.  
<img src="images/Screen Shot 2019-07-16 at 10.10.26 AM.png">
Then, click **Create**.  
The key is accepted and filled in on the page.  
You must supply the organization and space values on the page.   
**Organization:** *api-org*  
**Space:** *api-space* 
<img src="images/Screen Shot 2019-07-16 at 10.12.33 AM.png">  
Then, click **Create**.  
The toolchain is created and displayed on the page.
<img src="images/Screen Shot 2019-07-16 at 10.14.19 AM.png">   
### Review the generated toolkit deployment 
The *api-samples-soap-toolchain* includes artifacts under the CODE and DELIVER options.  
Click the **Delivery Pipeline** icon.   
*** 
**NOTE:** A warning might be displayed on the page indicating that a service instance was not found in this resource group and region.
<img src="images/Screen Shot 2019-07-15 at 2.30.27 PM.png">   
If you see this warning, click the **Add a service** link in the warning dialog.  
Accept the default service name, region, and resource group on the Continuous Delivery page.
Then, scroll down the page and select the **Professional** plan. 
<img src="images/Screen Shot 2019-07-15 at 2.44.20 PM.png">  
Click **Create**.
The Continuous Delivery Service is added to your resource group and location.   
Navigate to the other tab in the browser refresh the page.    
***   

The Build Stage and Deploy stages run successfully.
<img src="images/Screen Shot 2019-07-16 at 10.26.36 AM.png">   
***
**NOTE:** You change the application name to **soapsample** later.  
You will need to coordinate the removal of the existing URL for the sample and the application name change.
***   
## Create the toolchain for the third sample (pricesample)
Click the navigation icon on the page. Then, click the **DevOps** option from the *side navigation menu*.  
The toolchains page is displayed.  
Set **Location** to *Dallas*.  
Set **Cloud Foundry Org** to *api-org*  
Set **Resource Group** to *None*  

<img src="images/Screen Shot 2019-07-16 at 2.02.43 PM.png">  
Click **Create a Toolchain**.  
Select the template option to **Develop a Cloud Foundry app**.
<img src="images/Screen Shot 2019-07-15 at 10.44.18 AM.png">  
On the Develop a Cloud Foundry app page, change the name of the toolkit to *api-samples-pricing-setup-toolchain*.  

Ensure that the region is set to *Dallas*  
Under the Select a resource group area, click the link **Select a CF Organization (deprecated)**. Then, choose *api-org*.  
<img src="images/Screen Shot 2019-07-16 at 2.06.56 PM.png">    
Scroll down on the page, then select or type these values:  
**Server:** *default value*  
**Repository type:** *Clone*  
**Source repository URL:** *https://github.com/kevinom/api-samples-pricing-setup*  
**Owner:** *default value (your name)*  
**Repository Name:** *api-samples-pricing-setup-toolchain*  
**Make this repository private** *selected*  
**Enable Issues** *cleared*  
**Track deployment of code changes** *selected*   
<img src="images/Screen Shot 2019-07-16 at 2.09.37 PM.png">     
Click **Create**.   
On the subsequent tools integration page, click **Create** to create an IBM Cloud API key for the sample.  
<img src="images/Screen Shot 2019-07-16 at 2.12.01 PM.png">    
On the Create API key page, ensure that the name is set to *API Key for api-samples-pricing-setup-toolchain*.  
<img src="images/Screen Shot 2019-07-16 at 2.14.26 PM.png">
Then, click **Create**.  
The key is accepted and filled in on the page.  
You must supply the organization and space values on the page.   
**Organization:** *api-org*  
**Space:** *api-space* 
<img src="images/Screen Shot 2019-07-16 at 10.12.33 AM.png">  
Then, click **Create**.  
The toolchain is created and displayed on the page.
<img src="images/Screen Shot 2019-07-16 at 2.16.16 PM.png">   
### Review the generated toolkit deployment 
The *api-samples-pricing-setup-toolchain* includes artifacts under the CODE and DELIVER options.  
Click the **Delivery Pipeline** icon.   

The Build Stage ran successfully. In this example, the Deply stage failed.
<img src="images/Screen Shot 2019-07-16 at 2.25.49 PM.png">    
Click the **View logs and history** links in the Deploy stage.   
Use the log to find out why the Deploy stage failed.
<img src="images/Screen Shot 2019-07-16 at 2.29.45 PM.png">       
The application deployed, but did not start successfully because the route is already in use. 
***
**NOTE:** You change the application name to **pricesample** later.  
You will need to coordinate the removal of the existing URL route for the sample and the application name change.
***   
## Create the toolchain for the fourth sample (lookup-price)
Click the navigation icon on the page. Then, click the **DevOps** option from the *side navigation menu*.  
The toolchains page is displayed.  
Set **Location** to *Dallas*.  
Set **Cloud Foundry Org** to *api-org*  
Set **Resource Group** to *None*  

<img src="images/Screen Shot 2019-07-17 at 12.28.37 PM.png">  
Click **Create a Toolchain**.  
Select the template option to **Develop a Cloud Foundry app**.
<img src="images/Screen Shot 2019-07-15 at 10.44.18 AM.png">  
On the Develop a Cloud Foundry app page, change the name of the toolkit to *api-samples-lookup-price-toolchain*.  

Ensure that the region is set to *Dallas*  
Under the Select a resource group area, click the link **Select a CF Organization (deprecated)**. Then, choose *api-org*.  
<img src="images/Screen Shot 2019-07-16 at 2.06.56 PM.png">    
Scroll down on the page, then select or type these values:  
**Server:** *default value*  
**Repository type:** *Clone*  
**Source repository URL:** *https://github.com/kevinom/api-samples-lookup-price*  
**Owner:** *default value (your name)*  
**Repository Name:** *api-samples-lookup-price-toolchain*  
**Make this repository private** *selected*  
**Enable Issues** *cleared*  
**Track deployment of code changes** *selected*   
<img src="images/Screen Shot 2019-07-16 at 2.09.37 PM.png">     
Click **Create**.   
On the subsequent tools integration page, click **Create** to create an IBM Cloud API key for the sample.  
<img src="images/Screen Shot 2019-07-16 at 2.12.01 PM.png">    
On the Create API key page, ensure that the name is set to *API Key for api-samples-lookup-price-toolchain*.  
<img src="images/Screen Shot 2019-07-16 at 2.14.26 PM.png">
Then, click **Create**.  
The key is accepted and filled in on the page.  
You must supply the organization and space values on the page.   
**Organization:** *api-org*  
**Space:** *api-space* 
<img src="images/Screen Shot 2019-07-16 at 10.12.33 AM.png">  
Then, click **Create**.  
The toolchain is created and displayed on the page.
<img src="images/Screen Shot 2019-07-16 at 2.16.16 PM.png">   
### Review the generated toolkit deployment 
The *api-samples-lookup-price-toolchain* includes artifacts under the CODE and DELIVER options.  
Click the **Delivery Pipeline** icon.   

The Build Stage ran successfully. In this example, the Deply stage failed.
<img src="images/Screen Shot 2019-07-16 at 2.25.49 PM.png">    
Click the **View logs and history** links in the Deploy stage.   
Use the log to find out why the Deploy stage failed.
<img src="images/Screen Shot 2019-07-16 at 2.29.45 PM.png">       
The application deployed, but did not start successfully because the route is already in use. 
***
**NOTE:** You change the application name to **lookup-price** later.  
You will need to coordinate the removal of the existing URL route for the sample and the application name change.
***    
## Change the application routes of the tookits that you have built
The part describes how you change the application routes for the IBM Cloud Toolchains that you have just built.   
The application route defaults to a route that includes the toolchain name. You must change the of the route to the route that is used by the API Connect application samples.  

| Toolchain name    | Application Route URL   |
|:------------- |:----------------| 
| api-samples-saving-toolchain  | savingsample.mybluemix.net | 
| api-samples-soap-toolchain    | soapsample.mybluemix.net       | 
| api-samples-pricing-setup-toolchain   | pricesample.mybluemix.net        |   
| api-samples-lookup-price-toolchain   | lookup-price.mybluemix.net |   
You change the application route for a toolchain in the DEPLOY DevOps process.   
You must be signed on to you Cloud account.   
Then, select *DevOps* from the navigation menu. You see the toolchain landing page.   
Select **Dallas** under Location.   
Select **api-org** for the Cloud Foundry Org. You see the toolchains that you have built.   
<img src="images/Screen Shot 2019-07-31 at 9.51.22 AM.png">       
Click the **Delivering Pipeline** icon for the toolkit that you want to change the application route. The Delivery Pipeline opens for that toolkit.   
You see a BUILD and a DEPLOY stage.
<img src="images/Screen Shot 2019-07-31 at 9.57.00 AM.png">    
Click the *Stage Configuration* icon for the **DEPLOY** stage. This is a cog icon at the upper left of the DEPLOY stage. Then, click **Configure Stage**.  
<img src="images/Screen Shot 2019-07-31 at 9.59.48 AM.png">       
In the configuration, navigate to the *Application Name*. Then, change the name from the toolchain name to the corresponding API Connect sample name that is shown in the previous table. 
<img src="images/Screen Shot 2019-07-31 at 10.02.59 AM.png">      
Save the change.    

## What the samples look like when running on the IBM Cloud  

### SOAP Sample
Run the soap sample application from <http://soapsample.mybluemix.net>  
When you click getInventory, the correct response is shown:
<img src="images/Screen Shot 2019-07-16 at 3.30.47 PM.png">   
You must use the http header rather than the https header when you run this sample. An HTTP status code 200 is returned and the results show a SOAP envelope that includes a number of products that are returned from calling the Liberty back-end application.  
If you get a 200 response code with only the SOAP XML returned, you are not accessing the Liberty back-end properly.   

### Saving Sample   
Run the savings sample application from <https://savingsample.mybluemix.net>   
The page is displayed:   
<img src="images/Screen Shot 2019-07-31 at 8.47.09 AM.png">   
When you click the OpenAPI definition file link, the page prompts you to download the file.
Ths savings sample calculation takes values of integer, decimal, and integer in  the fields. An example is shown on the page.   
When you type in these value and click **Calculate** the response is displayed at the bottom of the page.   
<img src="images/Screen Shot 2019-07-31 at 8.53.38 AM.png">   
Clicking this link displays the result in another browser tab.   
<img src="images/Screen Shot 2019-07-31 at 8.55.54 AM.png">   
### Price Sample
Run the price sample application by typing <https://pricesample.mybluemix.net/price/>    
This output is the result of running the  Cloud Foundry Price Setup application.   
<img src="images/Screen Shot 2019-07-31 at 9.10.41 AM.png">        
There are 6 products with product-id values of 1 - 6.   
You can call individual product-ids, for example, by typing <https://pricesample.mybluemix.net/price/1>    
<img src="images/Screen Shot 2019-07-31 at 9.20.42 AM.png">         
### Product Lookup    
Run the price sample application by typing <https://lookup-price.mybluemix.net/api/products/lookupPrice?productId=1>   
This application uses the price sample backend that returns an individual product-id shown earlier.   
<img src="images/Screen Shot 2019-07-31 at 9.27.58 AM.png">   
### Summary
This document describes how to manually create the sample applications on the IBM Cloud by cloning them from Github.   
Kevin has been working with IBM Cloud Support who have offered an alternative way to migrate these applications to another Cloud user account.   
The solution involves adding a sub user to the original account. Then, IBM Support will make the sub-user the new owner of the Cloud Foundry applications.
This process will greatly simplify the process of migrating the sample applications from one owner to another.   
This documentation can be used as a reference if you ever need to clone the applications from <https://github.com/kevinom/>   
***
     
