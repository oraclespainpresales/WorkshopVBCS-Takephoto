# Visual Builder workshop.
This workshop will teach you how to create a new Oracle Visual Builder mobile application, that will allow you to take a photo with the mobile camera and upload it to Oracle Cloud (OCI) Object Storage.

<details>
  <summary>1.- Creating the API Key.</summary>

---
You will have to connecto the Visual Builder app to OCI Object Storage Bucket to Store the mobile photo or image files. You must create an API key OCI element to access to the OCI Services via API REST. Let's create the API Key.
  
---
  
## Creating the API Key
First Sign in [OCI web console](https://cloud.oracle.com) with your credentials 
> Note: this credentials will be provided to you in the workshop by the trainers, or you can use youw own credentials if you have a trial or paid tenancy.

Write your tenancy name and click **Next** Button.

![](./images/oci-signin-01.png)

Then click Continue leaving the Identity Providers as *oracleidentitycloudservice*

![](./images/oci-signin-02.png)

Next write you *User Name* and *Password* and click in **Connect** Button to access to OCI web console.

![](./images/oci-signin-03.png)

![](./images/oci-signin-04.png)

Then click in the **Profile icon** at the top right of the console to access to the user **Settings**.

![](./images/oci-apikey-01.png)

Scroll down and click **API Keys** in the *Resources menu*

![](./images/oci-apikey-02.png)

Next click **Add API Key** button to add a new API Key.

![](./images/oci-apikey-03.png)

Select **Generate API Key Pair**. 
> Note: you could use your own public and private keys in pem format, but in this workshop and for academical purposes we'll use the auto generathed keys.

![](./images/oci-apikey-04.png)

Next you must to download the *Private* and *Public* Keys to your laptop/desktop.

![](./images/oci-apikey-05.png)

After that, you might have two **.pem** files one mark as public.

![](./images/oci-apikey-06.png)

Then click in **Add** button.

![](./images/oci-apikey-07.png)

Next window is the summary or **Configuration File Preview**. Click in the **copy** link to copy your OCI API credentials to a text file in you local computer as you will need them in future steps in the workshop. Then click **Close** Button to finish the process.

![](./images/oci-apikey-08.png)

You might have a new API key created and you should see the Fingerprint key in the OCI web console. 

![](./images/oci-apikey-09.png)

You can get the Config file that you copied before clicking in the *tree vertical* dots in the Fingerprint row and select **View Config File**.

![](./images/oci-apikey-10.png)
</details>
<details>
  <summary>2.- Acessing Visual Builder Studio and WorkSpace using Visual Builder Cloud Service</summary>
  
---
  To develop your Visual Builder Application you must access to the workshop Visual Builder Studio instance. Visual Builder is not only used to develop Visual Builder applications, but it allows the development of any kind of modern application thanks to its multitude of integrated development tools, such as a GIT repository, CI/CD pipelines engine, artifact generation, container repository, agile tools, team building tools like wiki and snipples and more. If you want to know more please click [here](https://www.oracle.com/application-development/visual-builder-studio/)
 
---
  
## Acessing Visual Builder Studio and WorkSpace using Visual Builder Cloud Service
To get access to Visual Builder Studio (VBS) you have to Sign-in Oracle Cloud web console with your tenancy user credentials. Then Click in the *hamburguer icon* in the top left part of the web console and select **OCI Classic Services** then click in **Developer** to access to Visual Builder Studio instance.

![](./images/oci-vbs-01.png)
  
Next you have to click in the VBS instance **menu icon** and click in the **Access Service Instance**
  
![](./images/oci-vbs-02.png)  
 
Then in **Organization**, select the *Project* -> **Workshop-VBCS-Takephoto** that you will use for this workshop. 
  
![](./images/oci-vbs-03.png)
  
Select *Workspaces* in the left menu to get all the workspaces in the project. Then select the appropiate workspace asigned to you by the trainer. In this tutorial, you will see that the screenshots show *userXX*, but you will have to change XX with your user number.
> Note: if the trainer asign you the numbre 01 or user01, your workspace will be something like **workspace-user01**.
  
All trainees will use their own git repository tied to their own workspace.
  
![](./images/oci-vbs-04.png)
  
Wait a couple of second to access to your workspace. You should see the *Welcome to your Workspace* page.
  
![](./images/oci-vbs-05.png)
    
</details>
