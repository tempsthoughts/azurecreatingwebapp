# azurecreatingwebapp

As I am studying for my Azure Fundamentals Certification (AZ-900) I am doing labs that will assist me in becoming familiar with Azure as well as making the fundamentals make sense, not just studying to pass a certification exam.

This lab comes from https://github.com/MicrosoftLearning/AZ-900T0x-MicrosoftAzureFundamentals

<h2>Create A Web App Walkthrough</h2>

In this walkthrough, we will create a web app that runs a Docker container. The Docker container contains a Welcome message.

Azure App Service are actually a collection of four services, all of which are built to help you host and run web applications. The four services (Web Apps, Mobile Apps, API Apps, and Logic Apps) look different, but in the end they all operate in very similar ways. Web Apps are the most commonly used of the four services, and this is the service that we will be using in this lab.

<strong>Task 1: Create a Web App</strong>

In this task, you will create an Azure App Service Web App.

Sign-in to the Azure portal.

From the All services blade, search for and select App Services, and click + Add, + Create, + New

On the Basics tab of the Web App blade, specify the following settings (replace xxxx in the name of the web app with letters and digits such that the name is globally unique). Leave the defaults for everything else, including the App Service Plan.

<table style="width:50%">
  <tr>
    <th>Setting</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>Subscription</td>
    <td>Use default supplied</td>                        
  </tr>
  <tr>
    <td>Resource Group</td>
    <td>Create new resource group</td>
  </tr>
  <tr>
    <td>Name</td>
    <td>myDockerWebAppxxxx</td>
  </tr>
  <tr>
    <td>Publish	Docker</td>
    <td>Container</td>
  </tr>
  <tr>
    <td>Operating System</td>
    <td>Linux</td>
  </tr>
  <tr>
    <td>Region</td>
    <td>East US</td>
  </tr>

</table>
Note: Remember to change the xxxx so that your Web App name is unique.


Click Next > Docker and configure the container information.

<table style="width:60%">
  <tr>
    <th>Setting</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>Options</td>
    <td>Single container</td>                        
  </tr>
  <tr>
    <td>Image Source</td>
    <td>Docker Hub</td>
  </tr>
  <tr>
    <td>Access Type</td>
    <td>Public</td>
  </tr>
  <tr>
    <td>Image and tag</td>
    <td>mcr.microsoft.com/azuredocs/aci-helloworld</td>
  </tr>
 
</table>

Note: The startup command is optional and not needed in this exercise.

Click Review + create, and then click Create.

nbsp;
<h2>Task 2: Test the Web App</h2>

In this task, we will test the web app.

Wait for the Web App to deploy.

From Notifications click Go to resource.

On the Overview blade, locate the URL. Copy the URL to the clipboard.

![image](https://user-images.githubusercontent.com/66889976/151457728-2738d4af-2166-4d99-abc7-4c9b670529c2.png)


In a new browser window, paste the URl and press enter. The Welcome to Azure Container Instances! welcome message will be displayed.

![image](https://user-images.githubusercontent.com/66889976/151457896-f2e1d85f-d96d-40fd-8c68-09ab582aa542.png)

Switch back to the Overview blade of your web app and scroll down. You will notice several charts tracking Data In/Out and Requests. If you repeat step 4 a few times, you should be able to see corresponding telemetry being displayed in these charts. This includes number of requests and average response time.

Note: To avoid additional costs, you can optionally remove this resource group. Search for resource groups, click your resource group, and then click Delete resource group. Verify the name of the resource group and then click Delete. Monitor the Notifications to see how the delete is proceeding.

Congratulations you successfully created an Azure App Service.


